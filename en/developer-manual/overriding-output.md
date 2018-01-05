Overriding Output
=================

Lets say you're developing a module/app that adds/removes functionality to/from Akaunting core and you want to override the output. However, in order to keep Akaunting up-to-date, you don't want to, and shouldn't, change/hack the core files. As an example, lets see how to remove the `Phone` field from the customer creation form without changing the core files.

First of all, create and install a [module](https://akaunting.com/docs/developer-manual/modules).

Then add the folowing code into the `boot` method of your `ServiceProvider`. [Here](https://laravel.com/docs/5.4/views#view-composers) you can learn more about view composers.

```
View::composer(
    ['incomes.customers.create'], 'Modules\FooBar\Http\ViewComposers\Customers'
);
```

Then create the view composer file:

```
<?php

namespace Modules\FooBar\Http\ViewComposers;

use Illuminate\View\View;

class Customers
{
    /**
     * Bind data to the view.
     *
     * @param  View  $view
     * @return mixed
     */
    public function compose(View $view)
    {
        // Override just the 'content' section
        $view->getFactory()->startSection('content', view('foobar::customers.create'));

        // Override the whole file
        $view->setPath(view('foobar::customers.create')->getPath());
    }
}
```

Finally, create a [Blade](https://laravel.com/docs/5.4/blade) template file `modules/FooBar/Resources/views/customers/create.blade.php` with your custom output. The original one is located in `resources/views/incomes/customers/create.blade.php` file.

If you also want to modify the data stored in the database, then you can create an Observer to listen Eloquent's [events](https://laravel.com/docs/5.4/eloquent#events).