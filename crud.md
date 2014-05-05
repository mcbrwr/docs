# Create/Update/Delete

Kirby 2 introduces a CRUD engine for all pages of a site. This is great to write your own modification scripts, i.e. a simple like counter or a simple comment system. 

## Creating pages

```php

// first get the parent page object
$projects = $site->find('projects');
$projects->children()->create('project-d', $template = 'project', array(
  'title' => 'Project D',
  'text'  => 'This is a really nice project'
));

```

## Updating pages

```php
$project = $site->find('projects/project-d');
$project->update(array(
  'title' => 'Some other title for project d',
));
```

## Deleting pages

```php
$project = $site->find('projects/project-d');
$project->delete();
```


