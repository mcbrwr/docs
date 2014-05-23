# Multi-language Support

Kirby 2 has even better multi-language support with some nice additions and updates. 

## Setup

The setup for multi-language sites has changed a bit, so make sure to update your config if you are migrating from a Kirby 1 installation. 

```php

c::set('languages', array(
    'en' => array(
      'name'    => 'English',
      'code'    => 'en',
      'locale'  => 'en_US',
      'default' => true
    ),
    'de' => array(
      'name'    => 'Deutsch',
      'code'    => 'de',
      'locale'  => 'de_DE'
    ),
));

```

The languages config variable takes an array with all active languages. Each language must have the following attributes: 

- name
- code
- locale

You also should assign the default attribute to the default language and set it to true. 

## The languages object

When setup correctly, you get access to all installed languages from the $site->languages() method. This will give you a collection of language objects, which offer a nice API to work with languages. 

Here's an example for a simple language switch:

```php

<select onchange="window.location.href = this.value">
  <?php foreach($site->languages() as $lang): ?>
  <option value="<?php echo $lang->url() ?><?php e($lang == $site->language(), ' selected') ?>">
    <?php echo html($lang->name()) ?>
  </option>
  <?php endforeach ?>
</select>

```







