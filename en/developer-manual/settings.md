Settings
========

Akaunting ships with a centralized settings page where modules can add their own in a few steps.

### Simple Settings

We've tried the best to ease the life of developers. Mostly, developers just want to add just some inputs on the settings page. In such a case, you can add them to the `module.json` file and Akaunting will display your module under the Settings page, nothing else is required.

All you have to do is to fill the `settings` array there.

```json
"settings": [
    {
        "type": "textGroup",
        "name": "title",
        "title": "blog::general.title",
        "icon": "font",
        "attributes": {
            "required": "required"
        },
        "rules": "required|string"
    },
    {
        "type": "textGroup",
        "name": "header",
        "title": "blog::general.header",
        "icon": "user",
        "attributes": {
            "required": "required"
        },
        "rules": "nullable|string"
    },
    {
        "type": "textareaGroup",
        "name": "meta_description",
        "title": "blog::general.meta_description",
        "icon": "key",
        "attributes": {
            "required": "required"
        },
        "rules": "nullable|string"
    }
]
```

### Custom Settings

If your settings page needs a little bit more actions then you can listen to the `SettingShowing` event and create your own route, controller, and view files.

Lets firstly create the listener:

```php
<?php

namespace Modules\Blog\Listeners;

use App\Events\Module\SettingShowing as Event;

class ShowSetting
{
    /**
     * Handle the event.
     *
     * @param  Event $event
     * @return void
     */
    public function handle(Event $event)
    {
        $event->modules->settings['blog'] = [
            'name' => trans('blog::general.name'),
            'description' => trans('blog::general.description'),
            'url' => route('blog.settings.edit'),
            'icon' => 'fas fa-edit',
        ];
    }
}
```

Then add your handler/listener into the `boot` method of your service provider:

```php
$this->app['events']->listen(SettingShowing::class, ShowSetting::class);
```

You can check the built-in Akaunting modules as live examples. **Offline Payments** module ships with a custom settings page and **PayPal Standard** module uses the module.json file.
