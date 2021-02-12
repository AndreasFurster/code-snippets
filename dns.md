<h1>Generate DNS settings for www & non-www for ipv4 & ipv6</h1>
<form>
	<p>
		<label>
			Domain <br>
			<input type="text" oninput="fillDNS()" name="domain" autocomplete="off">
		</label>
	</p>
	<p>
		<label>
			IPv4 <br>
			<input type="text" oninput="fillDNS()" name="ipv4" autocomplete="off">
		</label>
	</p>
	<p>
		<label>
			IPv6 <br>
			<input type="text" oninput="fillDNS()" name="ipv6" autocomplete="off">
		</label>
	</p>
</form>

<code></code>



<script>
	function fillDNS() {
		var domain = document.forms[0].elements.domain.value;
		var ipv4 = document.forms[0].elements.ipv4.value;
		var ipv6 = document.forms[0].elements.ipv6.value;

		if(domain) {
			document.getElementsByTagName('code')[0].innerHTML = "<br>";
			if(ipv4){
				document.getElementsByTagName('code')[0].innerHTML += `${domain}.     A    ${ipv4}<br>`.replaceAll(' ', '&nbsp');
				document.getElementsByTagName('code')[0].innerHTML += `www.${domain}. A    ${ipv4}<br>`.replaceAll(' ', '&nbsp');
			}
			if(ipv6) {
				document.getElementsByTagName('code')[0].innerHTML += `${domain}.     AAAA ${ipv6}<br>`.replaceAll(' ', '&nbsp');
				document.getElementsByTagName('code')[0].innerHTML += `www.${domain}. AAAA ${ipv6}<br>`.replaceAll(' ', '&nbsp');
			}
		}
	}
</script>
