# Laravel HTML Minify

Simple package to minify the HTML in your Laravel application.

# Install
##### Install with composer
```
$ composer require redcenter/laravel-html-minify
```

##### Publish the package
```
$ php artisan vendor:publish --provider="LaravelHtmlMinify\LaravelHtmlMinifyServiceProvider" --force
```
... this will create a config file (laravel-html-minify.php) in your config folder.

##### Register the middleware
Register the middleware in kernel file (`app/Http/kernel.php`) by adding the class to the `$middleware` property...

    protected $middleware = [
        ...
        \LaravelHtmlMinify\LaravelHtmlMinifyMiddleware::class,
    ];


##### Enable and disable
Put a variable in you .env file to enable or disable the package on your different environments. This is optional. By default the package directly works after the `register` step, but maybe you want to diable the package locally for debugging purposes...
```
LARAVEL_HTML_MINIFY=false
```

##### Good bye!

Check out the documentation on Bitbucket for all details!

https://bitbucket.org/redcenter/laravel-html-minify
