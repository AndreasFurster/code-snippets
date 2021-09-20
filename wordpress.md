# Wordpress

## Address bar snippets

Type `j` in address bar and paste snippet after it. 

### Get all edit url's on posts page

    avascript:prompt('Result:', jQuery('#the-list .edit a').map((i, el) => el.href).get().join(','))
