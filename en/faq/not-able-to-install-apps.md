Not able to install apps
========================

This problem is caused by the PHP CLI and "php" command set lower than 7.2.5 version and/or disabled PHP functions in your server. It generally happens in shared hosting with cPanel, Plesk, etc. panels where they offer Multi-PHP versions and set the lowest one for CLI and/or "php" command, mostly 5.x version.

Please, ask your hosting provider to make sure that **PHP CLI** and **php** command has at least 7.2.5 version and the following PHP functions are not disabled:

- proc_open
- proc_close

You can get Akaunting installed within one-click on [DigitalOcean](https://bit.ly/akaunting-do-start) servers and see the app installation working fine.

### How to change PHP version?

If you have SSH access to your Ubuntu server, you can change the PHP version by running the following commands:

```bash
sudo update-alternatives --set php /usr/bin/php7.4
sudo update-alternatives --set phar /usr/bin/phar7.4
sudo update-alternatives --set phar.phar /usr/bin/phar.phar7.4
sudo update-alternatives --set phpize /usr/bin/phpize7.4
sudo update-alternatives --set php-config /usr/bin/php-config7.4
```

Keep in mind that the `/usr/bin/php7.4` path may differ on your server. [Here](https://tecadmin.net/switch-between-multiple-php-version-on-ubuntu) you can learn more.

If you don't have SSH access then your hosting provider must apply the change.
