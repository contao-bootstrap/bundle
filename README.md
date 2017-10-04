Contao-Bootstrap Bundle
=======================

[![Build Status](http://img.shields.io/travis/contao-bootstrap/bundle/master.svg?style=flat-square)](https://travis-ci.org/contao-bootstrap/bundle)
[![Version](http://img.shields.io/packagist/v/contao-bootstrap/bundle.svg?style=flat-square)](http://packagist.org/packages/contao-bootstrap/bundle)
[![License](http://img.shields.io/packagist/l/contao-bootstrap/bundle.svg?style=flat-square)](http://packagist.org/packages/contao-bootstrap/bundle)
[![Downloads](http://img.shields.io/packagist/dt/contao-bootstrap/bundle.svg?style=flat-square)](http://packagist.org/packages/contao-bootstrap/bundle)
[![Contao Community Alliance coding standard](http://img.shields.io/badge/cca-coding_standard-red.svg?style=flat-square)](https://github.com/contao-community-alliance/coding-standard)


This extension is a metapackages which includes all bootstrap components for Contao CMS.

Features
--------

 - Core
 - Layout
 - Grid 
 - Form
 - Navbar
 
Changelog
---------

See [changelog](CHANGELOG.md)
 
Requirements
------------

 - PHP 7.1
 - Contao ~4.4
 
 
Install
-------

### Managed edition

When using the managed edition it's pretty simple to install the package. Just search for the package in the
Contao Manager and install it. Alternatively you can use the CLI.  

```bash
# Using the contao manager
$ php contao-manager.phar.php composer require contao-bootstrap/bundle~2.0@beta

# Using composer directly
$ php composer.phar require contao-bootstrap/bundle~2.0@beta
```

### Standard edition

Without the contao manager you also have to register the bundle

```php

class AppKernel
{
    public function registerBundles()
    {
        $bundles = [
            // ...
            new Contao\CoreBundle\HttpKernel\Bundle\ContaoModuleBundle('metapalettes', $this->getRootDir()),
            new Contao\CoreBundle\HttpKernel\Bundle\ContaoModuleBundle('multicolumnwizard', $this->getRootDir()),
            new Netzmacht\Html\NetzmachtHtmlBundle(),
            new ContaoBootstrap\Core\ContaoBootstrapCoreBundle(),
            new ContaoBootstrap\Layout\ContaoBootstrapLayoutBundle(),
            new ContaoBootstrap\Grid\ContaoBootstrapGridBundle(),
            new ContaoBootstrap\Form\ContaoBootstrapFormBundle(),
            new ContaoBootstrap\Navbar\ContaoBootstrapNavbarBundle(),
        ];
    }
}

```
