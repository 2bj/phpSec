[phpSec](https://phpseclib.com/) - PHP security library
=======================================================
* phpSec is a open-source [PHP](http://php.net) security library that takes care
  of the common security tasks a web developer faces.
  
[Official Website](https://phpseclib.com/) and [Documentation](https://github.com/phpsec/doc/)

Features
--------
* Data encryption
* XSS filter
* Password hashing
* Secure session handler
* CSRF protection
* Yubikey integration
* Random data generator

Installing
---------------
phpSec is now a PSR-0 compatible library. this means that it can easilly be installed and loaded using [Composer](http://getcomposer.org/doc/00-intro.md).
You can also install phpSec manually, or using Git.

### Installing using [Composer](http://getcomposer.org/doc/00-intro.md)
To install using Composer just add phpSec to your composer.json file in your project directory.
```
{
    "require": {
        "phpsec/phpsec":"dev-master"
    },
    "minimum-stability": "dev"
}
```

Then all you need to do is to run `$ php composer.phar install` .
phpSec can then be loaded using the Composer autoloader.

`require 'vendor/autoload.php';`

### Installing manually/Git
Download, checkout or peferrably add phpSec as a Git submodule. Then load the *lib/phpSec/bootstrap.php* file.
This is a really simple autoloader that will load phpSec classes when needed.

`require_once 'lib/phpSec/bootstrap.php';`

If you already have a PSR-0 compatible autoloader for your project there is no need to call the *bootstrap.php* file.
All you have to do is to register the *phpSec* namespace to the *phpSec/lib* folder.

If you want to add an autoloader to your project there is [one example here](http://gist.github.com/221634).
This can be initialized like this:

```php
<?php
require_once 'SplClassLoader.php';
$classLoader = new SplClassLoader('phpSec', '/var/www/vendor/phpSec/lib');
$classLoader->register();
```

For documentation on how to use the various phpSec functionality, take alook at the [phpSec manual](https://phpseclib.com/manual). 
*Note: The manual is currently for the old version of phpSec. Updated ducumentation will be available the [phpsec/doc](https://github.com/phpsec/doc) repository.*

System requirements
-------------------
PHP 5.3.0 or greater with the following extensions is required to use phpSec:

* [Mcrypt](http://no.php.net/manual/en/mcrypt.installation.php)

Getting help / Contact
----------------------
 * [phpSec manual](https://github.com/phpsec/doc/)
 * [phpSec issues] (https://github.com/phpsec/phpSec/issues/)
 * [Twitter (@xqus)](http://twitter.com/xqus/)
 * [Website](https://phpseclib.com/)
 * E-mail: larsen@xqus.com

Wishlist
--------
 * **Updated documentation**
   Currently almost all the documentation needs to be converted from the "old" library to the "new".
 * **Unit testing.**
 * **Anything that fixes a issue.**

License
-------
phpSec is open-sourced software licensed under the MIT License.
