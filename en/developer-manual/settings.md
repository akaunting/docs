Settings
========

Akaunting ships with a centralized settings page where modules can add their own in a few steps.

### Simple Settings

We've tried the best to ease the life of developers. Mostly, developers just want to add just some inputs on the settings page. In such a case, you can add them to the `module.json` file and Akaunting will display your module under the Settings page, nothing else is required.

All you have to do is to fill the `settings` array like the following:

```json
"settings": [
    {
        "type": "textGroup",
        "name": "title",
        "title": "my-blog::general.title",
        "icon": "font",
        "attributes": {
            "required": "required"
        },
        "rules": "required|string"
    },
    {
        "type": "textGroup",
        "name": "header",
        "title": "my-blog::general.header",
        "icon": "user",
        "attributes": {},
        "rules": "nullable|string"
    },
    {
        "type": "textareaGroup",
        "name": "meta_description",
        "title": "my-blog::general.meta_description",
        "icon": "key",
        "attributes": {},
        "rules": "nullable|string"
    }
]
```

### Custom Settings

If your settings page needs a little bit more actions then you can listen to the `SettingShowing` event and create your own route, controller, and view files.

Here it is a listener example:

```php
<?php

namespace Modules\MyBlog\Listeners;

use App\Events\Module\SettingShowing as Event;

class ShowInSettingsPage
{
    /**
     * Handle the event.
     *
     * @param  Event $event
     * @return void
     */
    public function handle(Event $event)
    {
        $event->modules->settings['my-blog'] = [
            'name' => trans('my-blog::general.name'),
            'description' => trans('my-blog::general.description'),
            'url' => route('my-blog.settings.edit'),
            'icon' => 'fas fa-edit',
        ];
    }
}
```

You can check the built-in Akaunting modules as live examples. **Offline Payments** module ships with a custom settings page and **PayPal Standard** module uses the module.json file.
