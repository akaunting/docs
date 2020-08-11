Not able to install apps
========================

This problem is caused by the PHP CLI set lower than 7.2.5 version and/or disabled PHP functions in your server. It generally happens in shared hosting with cPanel, Plesk, etc. panels where they offer Multi-PHP versions and set the lowest one for CLI, mostly 5.x version.

Please, ask your hosting provider to make sure that **PHP CLI** has at least 7.2.5 version and the following PHP functions are not disabled:

- proc_open
- proc_close

You can get Akaunting installed within one-click on [DigitalOcean](https://bit.ly/akaunting-do-start) servers and see the app installation working fine.
