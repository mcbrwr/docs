# Kirbytags

Kirby 2 introduces a completely rewritten engine for Kirbytags, which makes it much easier to add your own tags and share them with other Kirby users. 

## Installing your own kirbytag

Custom Kirbytags are located in `/site/tags` Each file must be named like the tag. So if you want to create a new Wikipedia tag, the file should be called `/site/tags/wikipedia.php``

A Kirbytag file is a simple array, which describes the allowed attributes and how to render the tag. 

```php

// wikipedia 
kirbytext::$tags['wikipedia'] = array(
  'attr' => array(
    'text',
    'language'
  ),
  'html' => function($tag) {

    // build the final url
    $url = 'http://' . $tag->attr('language', 'en') . '.wikipedia.org/w/index.php?search=' . urlencode($tag->attr('wikipedia'));
  
    // build the link tag  
    return '<a class="wikipedia" href="' . $url . '">' . html($tag->attr('text')) . '</a>';    
      
  }
);

```

## More…

More docs about the $tag object and how to access the current page and site will follow soon. Check out `/kirby/config/tags.php` for all default tags as inspiration. You can also overwrite them all by naming them exactly as they are named. 
