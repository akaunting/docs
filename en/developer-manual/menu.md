Menu
====

The left sidebar of Akaunting contains the company switcher and menu. We use our own [akaunting/menu](https://github.com/akaunting/menu) package as builder.

You may want to extend the menu by adding your own pages. You should listen to the `AdminCreated` event for admin and/or `PortalCreated` for client sides.

Here it is a listener example:

```php
<?php

namespace Modules\MyBlog\Listeners;

use App\Events\Menu\AdminCreated as Event;

class AddToAdminMenu
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
        $item = $event->menu->whereTitle(trans_choice('general.sales', 2));
        $item->route('my-blog.posts.index', trans('my-blog::general.posts'), [], 4, ['icon' => '']);

        // Add new menu item
        $event->menu->add([
            'route' => 'my-blog.posts.index',
            'title' => trans('my-blog::general.posts'),
            'icon' => 'fas fa-pen',
            'order' => 5,
        ]);
    }
}
```

[Menu](https://github.com/akaunting/menu/wiki) documentation can help to understand the system, especially about how to find a menu item, add child ones, and create dropdown menus.
