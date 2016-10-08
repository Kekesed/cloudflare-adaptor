# Cloudflare Adaptor
An easy way to normalize your Cloudflare-altered HTTP Information with a single line.

This will help your Framework to understand what is happening with the current connection made from Cloudflare's server.
This will just simply change your `$_SERVER` variables.

## How to use it
Simple do this JUST BEFORE EVERYTHING STARTS!
```php
require_once('cf-adapt.php');
```

Here's an example with [Fat Free Framework](https://github.com/bcosca/fatfree)

```php

$playlist = [
  'app/Adaptor/cf-adapt.php', // see? this is the adaptor
  'app/f3/base.php',
  'app/config.php',
  'app/app.php'
];
for($_p = 0; $_p<count($playlist); $_p++)
  require_once($playlist[$_p]);
\F3::run();

```
