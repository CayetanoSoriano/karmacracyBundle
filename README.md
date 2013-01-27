karmacracyBundle
================

#Installation

##Composer

```bash
"cayetanosoriano/karmacracy-bundle": "dev-master"
```

##Add the following to the appkernel.php

```php
new cayetanosoriano\KarmacracyBundle\cayetanosorianoKarmacracyBundle(),
```

LadybugBundle
=============

[![Build Status](https://secure.travis-ci.org/raulfraile/LadybugBundle.png)](http://travis-ci.org/raulfraile/LadybugBundle)

This bundle provides an easy and extensible var_dump/print_r replacement for
Symfony2 projects, both in controllers or Twig templates. For example, with this
bundle, the following is possible:

``` php
<?php
    class UserController extends Controller
    {
        public function userAction($username) {
            ladybug_dump($username); // or just ld($username)
        }
    }
```

``` jinja
{{ user.username|ladybug_dump }}
```

Getting as a result:

<pre><strong><em>string(10)</em></strong> <span style="color:#080">"raulfraile"</span></pre>

## Installation

### Step 1: Install vendors


#### Symfony 2.1.x: Composer

[Composer](http://packagist.org/about-composer) is a project dependency manager for PHP. You have to list
your dependencies in a `composer.json` file:

``` json
{
    "require": {
        "cayetanosoriano/karmacracy-bundle": "dev-master"
    }
}
```
To actually install Ladybug in your project, download the composer binary and run it:

``` bash
wget http://getcomposer.org/composer.phar
# or
curl -O http://getcomposer.org/composer.phar

php composer.phar install
```

### Step 2: Enable the bundle

Finally, enable the bundle in the kernel:

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...

            new cayetanosoriano\KarmacracyBundle\cayetanosorianoKarmacracyBundle(),
    );
}
```

## Configuration

