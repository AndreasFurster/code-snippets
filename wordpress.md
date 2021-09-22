# Wordpress

## Address bar snippets

Type `j` in address bar and paste snippet after it. Outputs are in the console (if applicable). 

### Get all edit url's on posts page

    avascript:console.log(jQuery('#the-list .edit a').map((i, el) => el.href).get().join(','))

## PHP Snippets

### Disallow direct file access

```php
if (!defined('ABSPATH')) exit;
```
