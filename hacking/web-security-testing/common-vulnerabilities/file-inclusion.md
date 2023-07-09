# File Inclusion

## Summary

<table><thead><tr><th width="209"></th><th></th></tr></thead><tbody><tr><td>Description</td><td>File Inclusion vulnerabilities often affect web applications that rely on a scripting run time, and occur when a web application allows users to submit input into files or upload files to the server. They are often found in poorly-written applications.</td></tr><tr><td>Impact</td><td><ul><li>An attacker can read local file</li><li>An attacker can execute code </li></ul></td></tr><tr><td>Recommendation</td><td><ul><li>save your file paths in a secure database and give an ID for every single one, this way users only get to see their ID without viewing or altering the path</li><li>use verified and secured whitelist files and ignore everything else</li><li>don’t include files on a web server that can be compromised, use a database instead</li><li>make the server send download headers automatically instead of executing files in a specified directory</li></ul></td></tr><tr><td>References</td><td><ul><li><a href="https://brightsec.com/blog/local-file-inclusion-lfi/">https://brightsec.com/blog/local-file-inclusion-lfi/</a></li><li><a href="https://crashtest-security.com/file-inclusion/">https://crashtest-security.com/file-inclusion/</a></li></ul></td></tr></tbody></table>

##
