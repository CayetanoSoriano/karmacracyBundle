karmacracyBundle
=============

This Bundle, gives a wrapper to [karmacracy-php](https://github.com/CayetanoSoriano/karmacracy-php.git) API lib



## Installation

#### Symfony 2.0.x: vendors

```
[karmacracyBundle]
    git=http://github.com/CayetanoSoriano/karmacracyBundle.git
    target=/bundles/RaulFraile/Bundle/LadybugBundle

[karmacracy-php]
    git=https://github.com/CayetanoSoriano/karmacracy-php.git
    target=lib/

```

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
###Add the following to your config.yml
```
cayetanosoriano_karmacracy:
    keypass: "your_key_pass"
    appkey: "your_app_key"
```

### Then use the service
```
$kcy = $this->get('kcy');
```
