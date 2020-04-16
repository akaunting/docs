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
        Item::observe('Modules\MyBlog\Observers\Common\Item');
    }

...
```

Then create the observer file:

```php
<?php

namespace Modules\MyBlog\Observers\Common;

use App\Abstracts\Observer;
use App\Models\Common\Item;
use Modules\MyBlog\Models\Post;

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
        $post = Post::where('item_id', $item->id)->first();

        $post->opening_stock = $item->quantity;

        $post->update();
    }
}

```

That's all you need to do to hook a model.
