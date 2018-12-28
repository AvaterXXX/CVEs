# ReloadApplication
--------------------------
Visit to /install
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_Reload-Application_1-1.png)

The source code `\install\index.php` uses the file_exists function to determine if the install.lock file exists.
If there is a problem with the permission settings at this time, file_exists may not be able to read the file, and the function will return false, which can result in reloading.
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_Reload-Application_1-2.png)

# Information Disclosure
-----------------------------
Can be used with the previous vulnerability, enter some special characters on the installation page.
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_Information-Disclosure_1-1.png)

Access any address after installation, such as the home page http://www.a.com:81/
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_Information-Disclosure_1-2.png)

# XSS
-----------------------------
### The following vulnerabilities are all stored XSS, the main reason is that the user's input is not restricted and filtered.
### Here is a unified description of the vulnerability: after the administrator logs in, you can modify and insert the XSS statement. It can be seen in the given code that the addition and modification do not limit the user's input, so the attacker can construct the statement. Inserted into it, causing XSS vulnerabilities  
-----------------------------
## XSS1
Source code `\admin\nav.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_1-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_1-2.png)

## XSS2
Source code `\admin\show.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_2-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_2-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_2-3.png)

## XSS3
Source code `\admin\page.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_3-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_3-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_3-3.png)

## XSS4
Source code `\admin\product_category.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_4-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_4-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_4-3.png)

## XSS5
Source code `\admin\product.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_5-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_5-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_5-3.png)

## XSS6
Source code `\admin\article_category.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_6-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_6-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_6-3.png)

## XSS7
Source code `\admin\article.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_7-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_7-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_7-3.png)

## XSS8
Source code `\admin\system.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_8-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_8-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_8-3.png)

## XSS9
Source code `\admin\mobile.php`
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_9-1.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_9-2.png)
![](https://github.com/AvaterXXX/CVEs/blob/master/images/images/douphp_xss_9-3.png)
