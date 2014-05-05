# Using Kirby's core engine in your own scripts

Kirby 2 makes it possible to use Kirby's core engine in any external PHP script. This is great to access all your site's data or modifying the content structure or files. 

## Setup

```php

<?php 

// /myownscript.php

require('kirby/bootstrap.php);

$site    = kirby::setup();
$project = $site->find('projects/project-a');
$project->update(array(
  'title' => 'Changed title'
));

```
