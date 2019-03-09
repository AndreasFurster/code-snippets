<pre>
  if($_SERVER['REMOTE_ADDR'] == 'YOUR_IP_ADDRESS'){
    var_dump($value);
  }
</pre>


<script>
  function onIpRecieved(result) {
    document.body.innerHTML = document.body.innerHTML.replace('YOUR_IP_ADDRESS', result.ip);
  }
</script>
<script src="https://api.ipify.org?format=jsonp&callback=onIpRecieved"></script>
