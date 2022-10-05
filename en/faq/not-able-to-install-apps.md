Not able to install apps
========================

This problem is caused by the PHP CLI and "php" command set lower than 8.0.2 version and/or disabled PHP functions in your server. It generally happens in shared hosting with cPanel, Plesk, etc. panels where they offer Multi-PHP versions and set the lowest one for CLI and/or "php" command, mostly 5.x version.

Please, ask your hosting provider to make sure that **PHP CLI** and **php** command has at least 8.0.2 version and the following PHP functions are not disabled:

- proc_open
- proc_close

You can get Akaunting installed within one-click on [DigitalOcean](https://bit.ly/akaunting-do-start) or [Linode](https://bit.ly/akaunting-linode-start) servers and see the app installation working fine.

### How to set PHP path manually?

If you know the exact path of PHP executable in your server, then you can set it within the `.env` file (located in the root directory of your Akaunting installation) like the following:

```bash
APP_PHP_PATH="/usr/bin/php8.0"
```

### How to change PHP version?

If you have SSH access to your Ubuntu server, you can change the PHP version by running the following commands:

```bash
sudo update-alternatives --set php /usr/bin/php8.0
sudo update-alternatives --set phar /usr/bin/phar8.0
sudo update-alternatives --set phar.phar /usr/bin/phar.phar8.0
sudo update-alternatives --set phpize /usr/bin/phpize8.0
sudo update-alternatives --set php-config /usr/bin/php-config8.0
```

Keep in mind that the `/usr/bin/php8.0` path may differ on your server. [Here](https://tecadmin.net/switch-between-multiple-php-version-on-ubuntu) you can learn more.

If you don't have SSH access then your hosting provider must apply the change.
