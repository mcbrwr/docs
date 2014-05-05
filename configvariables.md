# Config Variables

## license 

If you want to keep track of which license key is valid for which installation you can add it to your config. This does not change Kirby's features or send any information to the Kirby server. It's only for your personal info.

```php
c::set('license', 'your license key');
```

## url

By default Kirby will figure out, which is the base url of your site. If you want to take control here or Kirby gets it wrong, you can set the URL in your config like this: 

```php
c::set('url', 'http://yourdomain.com');
```

For relative URLs use the following syntax: 

```php
c::set('url', '/');
```

## home

By default Kirby will recognize the `home` folder with or without a prepended number as the content folder for the home page. You can change this by setting your `home` folder in the config.  

```php
c::set('home', 'blog');
```
    
## error

By default Kirby will use the `error` folder to build the error page for your site. If you want to change the name of the error folder you can adjust this in the config. 

```php
c::set('error', 'fehler');
```

## headers (new)

If you need to send special response headers for a specific template, you can add the header info by template to the config: 
```php
c::set('headers', array(

  // numeric for simple http status headers
  'my-template-a' => 400,
  'my-template-b' => 500,
  
  // with callbacks
  'my-template-c' => function() {
    header('Content-type: application/json');
  },
  
  // with the toolkit header class
  'my-template-d' => function() {
    header::type('application/json')
  }

));
```

## timezone

```php
c::set('timezone', 'UTC');
```

## auto css and js linking (new)

The `css()` and `js()` helpers have a new built-in auto-linking feature, which makes it possible to load a template-specific css or javascript file:

```php

<?php echo css('@auto') ?>
<?php echo js('@auto') ?>

```

This will look for a css or js file in `/assets/css/templates` and `/assets/js/templates` which matches the name of the current template (template: project.php => css: project.css => js: project.js)

To setup the location for auto-loaded css and js files you can change the config like this: 

```php
c::set('auto.css.url', '/your/custom/css/folder');
c::set('auto.css.root', '/your/custom/css/folder');
c::set('auto.js.url', '/your/custom/js/folder');
c::set('auto.js.root', '/your/custom/js/folder');
```















