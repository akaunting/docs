Menu
====

The left sidebar of Akaunting contains the company switcher and menu. We use our own [akaunting/menu](https://github.com/akaunting/menu) package as builder.

You  may want to extend the menu by adding your own pages. You should listen to the `AdminCreated` event for admin and/or `CustomerCreated` for client side.

Lets firstly create the listener:

```php
<?php

namespace Modules\Blog\Listeners;

use App\Events\Menu\AdminCreated as Event;

class AddMenu
{
    /**
     * Handle the event.
     *
     * @param  Event $event
     * @return void
     */
    public function handle(Event $event)
    {
        // Add child to existing menu item
        $item = $event->menu->whereTitle(trans_choice('general.incomes', 2));
        $item->url('modules/blog/posts', 'Posts', 4, ['icon' => '']);

        // Add new menu item
        $event->menu->add([
            'url' => 'modules/blog/posts',
            'title' => 'Posts',
            'icon' => 'fa fa-rocket',
            'order' => 5,
        ]);
    }
}
```

Then add your listener into the `boot` method of your service provider:

```php
$this->app['events']->listen(AdminCreated::class, AddMenu::class);
```

[Menu](https://github.com/akaunting/menu/wiki) documentation can help to understand the system, especially about how to find a menu item, add child ones, and create dropdown menus.
