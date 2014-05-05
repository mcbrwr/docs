# Kirby 2

## Toolkit

### New features

- Massive update with lots of new classes
- Autoloaded classes for improved memory usage and performance

### Helpers

- `r()`
- `e()`
- `attr()`
- `html()`
- `h()`
- `xml()`
- `widont()`
- `memory()`
- `size()`
- `gravatar()`
- `csfr()`
- `call()`
- `yaml()`
- `thumb()`
- `email()`
- `upload()`
- `invalid()`
- `l()`
- `load()`

### New Classes

- bitmask
- cache
- collection
- crypt
- data
- database
- detect
- dimensions
- email
- embed
- error
- errorreporting
- exif
- folder
- header
- html
- i
- media
- obj
- pagination
- password
- redirect
- remote
- response
- router
- silo
- sql
- system
- thumb
- upload
- url
- visitor

### Removed Classes

- browser
- content
- g
- size

### Renamed Classe

- x = xml

***

## Kirby

### New features

- Built-in Thumb generation class and helper (see toolkit)
- Built-in Email sender class and helper (see toolkit)
- Site-wide user registration, authentication and handling
- Omittable language code in URLs for the default language
- New Kirbytags extension system. It's now way easier to add your own kirbytags and share them with others.
- New Markdown parser class, which massively improves performance of markdown rendering
- Better overall performance.
- Template controllers, which make it possible to assign your own variables for templates and also outsource more complex PHP code to separate logic and view.
- Option to switch file-based caching to APC or Memcached (see toolkit cache)

### Easy access to Kirby's internal system

This makes it possible to use Kirby's data engine in any external file to use
it for all kinds of nice little use cases: your own Kirby API, using Kirby to batch-edit files,
create your own app on top of Kirby's data engine, etc.

```

require('kirby/bootstrap.php');

$site = kirby::setup();
$page = $site->find('some/subpage');

```

### New site methods

- $site->page()
- $site->children()
- $site->users()
- $site->user()

For multi-language sites:

- $site->languages()
- $site->language()
- $site->defaultLanguage()

Site now inherits all methods from the page class.
This makes it possible to store images, docs and other files directly within the
content folder and access it from the $site object with $site->files() etc.

### New page methods

- $page->find()
- $page->file()
- $page->image()
- $page->parents()
- $page->inventory()
- $page->is()
- $page->textfile()
- $page->blueprint()
- $page->update()
- $page->move()
- $page->sort()
- $page->hide()
- $page->delete()
- $page->date($format, $field) 

### New file methods

- $file->dimensions()
- $file->read()
- $file->mime()
- $file->is()
- $file->base64()
- $file->uri()
- $file->header()
- $file->download()
- $file->exif()
- $file->ratio()
- $file->isPortrait()
- $file->isLandscape()
- $file->isSquare()
- $file->textfile()
- $file->meta()
- $file->rename()
- $file->update()
- $file->delete()

### Helpers

- better `css()` and `js()`
- `site()`
- `page()`
- `kirbytag()`

***

## Panel

- Completely redesigned. No Kirby branding left. It's all yours
- AngularJS-based interface. Crazy fast loading of views + many little dynamic magic tricks
- New form field framework with a built-in grid system to layout multi-column form fields.
- More blueprint options, better field options, more file fields
- New subpage manager
- New file manager
- Drag & Drop multi-upload
- New user manager
- A new text editor for longer textfields, based on CodeMirror
- Easy installation without copying or moving files

![Kirby Panel](http://f.cl.ly/items/330p313K2H231Q280v2B/panel.png)

![Kirby Panel](http://f.cl.ly/items/1h1E1a090q2V2a3d1q19/panel-files.png)

![Kirby Panel](http://f.cl.ly/items/0x0G0R1J1f0O0c231g1I/panel-file-editor.png)

![Kirby Panel](http://f.cl.ly/items/1E0A0t101C1P0z2g3O1Z/panel-users.png)

![Kirby Panel](http://f.cl.ly/items/0910062v3I2J3Y0v1y0y/panel-subpages.png)
