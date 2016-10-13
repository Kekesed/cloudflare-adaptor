# Cloudflare Adaptor
An easy way to normalize your Cloudflare-altered HTTP Information with a single line.

This will help your Framework to understand what is happening with the current connection made from Cloudflare's server.
This will just simply change your `$_SERVER` variables.

## How to use it
Simply do this JUST BEFORE EVERYTHING STARTS!
```php
require_once('cf-adaptor/cf-adaptor.php');
```


Here's an example with [Fat Free Framework](https://github.com/bcosca/fatfree)

```php
array_map(function($_p){ require_once($_p); },[
  'app/Adaptor/cf-adaptor.php', // see? this is the adaptor
  'app/f3/base.php',
  'app/config.php',
  'app/app.php'
]);
\F3::run();
```

## Main Feature
 - Detect HTTPS.
 - Get Real IP.<br/>
   This normalize the `$_SERVER['REMOTE_ADDR']` var.
