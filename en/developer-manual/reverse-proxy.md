Reverse Proxy
=============

Some Akaunting installations, especially those within containers, may have problems with proxies and/or HTTPS protocol.

Akaunting ships with [TrustedProxy](https://github.com/fideloper/TrustedProxy) package so you could easily configure your proxies.

### Installation

All you have to do is to publish the configuration file from the command line:

```
php artisan vendor:publish --provider="Fideloper\Proxy\TrustedProxyServiceProvider"
```

### Configuration

Now you can enter your proxy details in the `config/trustedproxy.php` file like the following:

```
'proxies' => '*',
```

[Here](https://github.com/akaunting/akaunting/issues/213) you can find an example with Apache as a reverse proxy and [here](https://github.com/fideloper/TrustedProxy#configure-trusted-proxies) there are more details about configuration.