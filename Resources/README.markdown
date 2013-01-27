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

karmacracyBundle
=============

This Bundle, gives a wrapper to [karmacracy-php](https://github.com/CayetanoSoriano/karmacracy-php.git) API lib



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
To actually install in your project, download the composer binary and run it:

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

