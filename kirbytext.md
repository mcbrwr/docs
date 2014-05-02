# Kirbytext Cheat Sheet

## Headings

```
# Heading 1
Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

## Heading 2
Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

### Heading 3
Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

#### Heading 4
Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
```

## Line breaks & paragraphs
```
My first line of lorem ipsum dolor text.
My second line of lorem ipsum dolor text.

Another paragraph…
```

## Bold text
```
**Your bold lorem ipsum dolor text**
```

## Italic text
```
_Your italic lorem ipsum dolor text_
```

## Unordered list
```
- Lorem ipsum dolor sit amet a
- Lorem ipsum dolor sit amet b
- Lorem ipsum dolor sit amet c
```

## Ordered list
```
1. Lorem ipsum dolor sit amet a
2. Lorem ipsum dolor sit amet b
3. Lorem ipsum dolor sit amet c
```

## Quotes
```
> Design is not just what it looks like and feels like.
> Design is how it works.
– Steve Jobs
```

## Horizontal rules
```
Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

****

Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
```

## Links

### Link without link text
```
<http://wikipedia.org>
```
or

```
(link: http://wikipedia.org)
```

### Link with link text
```
(link: http://wikipedia.org text: Wikipedia)
```
### Open link in a new window
```
(link: http://wikipedia.org text: Wikipedia popup: yes)
```

### Link with a title
```
(link: http://wikipedia.org text: Wikipedia title: Go to Wikipedia)
```

### Link with a custom CSS class
```
(link: http://wikipedia.org text: Wikipedia class: mylink)
```


## Code blocks
```
  <?php
  // awesome code example
  ?>
```

## Email Addresses
### Email without link text
```
<bastian@getkirby.com>
```
or

```
(email: bastian@getkirby.com)
```

### Email with link text
```
(email: bastian@getkirby.com text: Send me an email)
```

### Email with a title
```
(email: bastian@getkirby.com text: Send me an email title: Contact me)
```

### Email with a custom CSS class
```
(email: bastian@getkirby.com text: Send me an email class: email)
```

## Images
### Images in your content folder
```
(image: myawesomepicture.jpg)
```

### Set the width and height of an image
```
(image: myawesomepicture.jpg width: 120 height: 200)
```

### Define an alternative text for an image
```
(image: myawesomepicture.jpg alt: On this picture you can see a cat)
```

### Image with custom css class
```
(image: myawesomepicture.jpg class: floated)
```

### A linked image
```
(image: myawesomepicture.jpg link: http://flickr.com)
```

### Link to a different picture in the same content folder
```
(image: myawesomepicture.jpg link: anothergreatpic.jpg)
```

### Images from other websites
```
(image: http://flickr.com/someimage.jpg)
```


## Files
### Provide a download link to a file in your page's content folder
```
(file: companysecrets.pdf)
```
### Download link with link text
```
(file: companysecrets.pdf text: Download our company secrets)
```


## Videos
### YouTube
```
(youtube: http://www.youtube.com/watch?v=lLuc6rtWkrM)
```

### Vimeo
```
(vimeo: http://vimeo.com/3432886)
```

### Set the width and height of the embedded video
```
(vimeo: http://vimeo.com/3432886 width: 400 height: 300)
```

## Twitter Profile Links
### Linking to Twitter profiles
```
(twitter: getkirby)
```

### With link text
```
(twitter: getkirby text: Follow Kirby on Twitter)
```

## Github Gists
### Embed Gists
```
(gist: https://gist.github.com/2556891)
```

### Define, which file you want to embed
(gist: https://gist.github.com/2556891 file: targetblank.js)
