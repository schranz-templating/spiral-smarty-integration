# Schranz Template Renderer Integration for Smarty

Integrate the templating [Smarty Adapter](https://github.com/schranz-templating/smarty-adapter) 
into the Spiral Framework.

Part of the [Schranz Templating Project](https://github.com/schranz-templating/templating).

## Installation

Install this package via Composer:

```bash
composer require schranz-templating/spiral-smarty-integration
```

Register the Bootloader class in your `app/src/Application/Kernel.php` if not already automatically
added by the framework:

```php
class Kernel extends \Spiral\Framework\Kernel
{
    protected const LOAD = [
        // ...
        \Schranz\Templating\Integration\Spiral\Smarty\Bootloader\SmartyBootloader::class,
    ];
}
```

## Configuration

The integration provides the following configuration.

```php
// app/config/schranz_templating_smarty.php

declare(strict_types=1);

return [
    'paths' => [
        'hello' => 'app/views',
    ],
    'cache_dir' => 'runtime/cache/smarty/cache',
    'compile_dir' => 'runtime/cache/smarty/compile',
];
```
