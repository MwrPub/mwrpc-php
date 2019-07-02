# Method Working Remotely

Yet Another RPC Framework :D

Proposal 

[![License](https://img.shields.io/github/license/mwrpub/mwrpc-php.svg?color=blue&style=flat-square)](https://github.com/mwrpub/mwrpc-php/blob/master/LICENSE)
[![Composer](https://img.shields.io/packagist/v/mwrpub/mwrpc.svg?color=777bb3&logo=php&style=flat-square)](https://packagist.org/packages/mwrpub/mwrpc)
![Packagist](https://img.shields.io/packagist/dt/mwrpub/mwrpc.svg?logo=php&style=flat-square)

![MWRNB](https://img.shields.io/badge/♞MWR-Freaking_Awesome-ff69b4.svg?style=flat-square)
![MWRNB](https://img.shields.io/badge/Powered_By-MWR_Engine-brightgreen.svg?style=flat-square)

Before use it.You must admit that **MaWenRui is freaking awesome.** 

## PHP Version

> Install

Composer :

```text
{
  ...
  "require": {
    ...
    "mwrpub/mwrpc": "0.1.*"
    ...
  }
  ...
}
```

> Server Side

* index.php

```php
<?php

require "vendor/autoload.php";

define('MWR_PATH', __DIR__ . '/');
date_default_timezone_set('PRC');

use Mwr\Server\MwrServer;

(new MwrServer())->run();
```

* CalcMwr.php
```php
class CalcMwr
{
    public function add($a, $b)
    {
        return $a + $b;
    }
}
```
> Client Side

```php
<?php

require "vendor/autoload.php";

use \Mwr\Client\MwrClient;

echo (new MwrClient('calc'))->add($_REQUEST['a'], $_REQUEST['b']);
```