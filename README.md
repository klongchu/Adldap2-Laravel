# Adldap2 - Laravel

[![Build Status](https://img.shields.io/travis/Adldap2/Adldap2-laravel.svg?style=flat-square)](https://travis-ci.org/Adldap2/Adldap2-laravel)
[![Scrutinizer Code Quality](https://img.shields.io/scrutinizer/g/Adldap2/Adldap2-laravel/master.svg?style=flat-square)](https://scrutinizer-ci.com/g/Adldap2/Adldap2-laravel/?branch=master)
[![Total Downloads](https://img.shields.io/packagist/dt/adldap2/adldap2-laravel.svg?style=flat-square)](https://packagist.org/packages/adldap2/adldap2-laravel)
[![Latest Stable Version](https://img.shields.io/packagist/v/adldap2/adldap2-laravel.svg?style=flat-square)](https://packagist.org/packages/adldap2/adldap2-laravel)
[![License](https://img.shields.io/packagist/l/adldap2/adldap2-laravel.svg?style=flat-square)](https://packagist.org/packages/adldap2/adldap2-laravel)

## Installation

Insert Adldap2-Laravel into your `composer.json` file:

    "adldap2\adldap2-laravel": "1.1.*",

Then run `composer update`.

Once finished, insert the service provider in your `config/app.php` file:

    Adldap\Laravel\AdldapServiceProvider::class,
    
Then insert the facade:

    'Adldap' => Adldap\Laravel\Facades\Adldap::class

Publish the configuration file by running:

    php artisan vendor:publish

Now you're all set!

## Usage

You can perform all methods on Adldap through its facade like so:

    $user = Adldap::users()->find('john doe');
    
    $search = Adldap::search()->where('cn', '=', 'John Doe')->get();
    
    
    if(Adldap::authenticate($username, $password))
    {
        // Passed!
    }

To see more usage in detail, please visit the [Adldap2 Repository](http://github.com/Adldap2/Adldap2);