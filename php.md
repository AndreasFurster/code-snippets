# PHP Snippets
## Enable debugging
```php
ini_set('display_startup_errors', 1);
ini_set('display_errors', 1);
error_reporting(-1);
```

## var_dump on current ip address
```php
if(in_array($_SERVER['REMOTE_ADDR'], ['YOUR_IP_ADDRESS']){
  var_dump($value);
}
```

## exit if not on current ip address
```php
if(!in_array($_SERVER['REMOTE_ADDR'], ['YOUR_IP_ADDRESS']){
  exit('');
}
```

<script>
  function onIpRecieved(result) {
    document.body.innerHTML = document.body.innerHTML.replace('YOUR_IP_ADDRESS', result.ip);
  }
</script>
<script src="https://api.ipify.org?format=jsonp&callback=onIpRecieved"></script>
