How to see error details?
=========================

As all the software outside, Akaunting is not perfect so you may encounter errors. In such a case, you may want to see the details of the error. To get that, you should enable the debug variable.

By default, the debug is disabled as it designed to be used only in development environment. It can slow the application down (because it has to gather data). To enable it, set `true` the `APP_DEBUG` variable in the `.env` file, located in the root directory of your Akaunting installation.

![debug enable](_images/debug_enable.png)