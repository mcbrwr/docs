# Controllers

Kirby 2 introduces a new feature called template controllers. Template controllers make it possible to out-source complex template code into a separate file and add new template variables. This is very handy to keep your templates nice and clean. 

## Setup 

Add a `/site/controllers` folder. All your template controllers go in here. **Your controllers have to have the exact same name as your templates**. So if your template is called `/site/templates/projects.php` and you want to add a controller for it, it has to be `/site/controllers/projects.php`

## Controller architecture

Controllers are simple PHP callbacks, which return an associative array of data, which should be passed to the template.

```php

// /site/controllers/example.php

return function($site, $pages, $page) {
  
  return array(
    'variableA' => 'some custom variable for the template',
    'variableB' => 'Another custom variable for the template'
  );

}

```

This will make `$variableA` and `$variableB` available in the `example.php` template.

