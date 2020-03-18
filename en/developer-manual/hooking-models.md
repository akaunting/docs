Hooking Models
==============

Lets say you're developing a module/app that adds functionality to Akaunting. However, in order to keep Akaunting up-to-date, you don't want to, and shouldn't, change/hack the core files.

Eloquent fires [several events](https://laravel.com/docs/eloquent#events), allowing you to hook into lots of points in a model's lifecycle. You can listen these events using [Observers](https://laravel.com/docs/eloquent#observers) feature of Eloquent. Lets make an example for modules.

First of all, create and install a [module](https://akaunting.com/docs/developer-manual/modules).

Then add the folowing code into the `boot` method of your `Service Provider`.

```php
use App\Models\Common\Item;

...

    public function boot()
    {
        Item::observe('Modules\FooBar\Observers\Common\Item');
    }

...
```

Then create the observer file:

```php
<?php

namespace Modules\FooBar\Observers\Common;

use App\Abstracts\Observer;
use App\Models\Common\Item;
use Modules\FooBar\Models\Common\Item as FooBarItem;

class Item extends Observer
{
    /**
     * Listen to the updated event.
     *
     * @param  Item $item
     *
     * @return void
     */
    public function updated(Item $item)
    {
        $foobar_item = FooBarItem::where('item_id', $item->id)->first();

        $foobar_item->opening_stock = $item->quantity;

        $foobar_item->update();
    }
}

```
