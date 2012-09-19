###校友会数据库内部简单key value数据库接口
####1.设置
  * url:/alumni/kvdb/setValue
  *  方法:POST或GET
  *  参数:
    *  1.key键
    *  2.value值

####2.获取
  *  url:/alumni/kvdb/getValue
  *  方法:POST或GET
  *  参数:
    *  1.key键
  *  json返回:
    *  value的值

###校友会前台用户登录
####状态信息（ajax）
 * url:/info/UserLogin/loginInfo
 * 方法：GET
 * json返回：
   * 样例：
   <pre>
   {"is_login":false,"user_name":null,"is_alumni":false}}
   </pre>
   * 详细:
   <pre>
     is_login是否登录
     user_name用户名
     is_alumni 是否校友(通过审核)
   </pre>

###校友会网站登录接口
<pre>
1.登录:/info/UserLogin/login
2.提交审核:/info/info/registerVerify
3.完善信息:/info/info/submitInfo
4.修改密码:/info/UserLogin/profile
5.登出:/info/authake/user/logout
6.注册:/info/UserLogin/register
7.忘记密码:/info/authake/user/lost_password
8.邮箱验证码:/info/authake/user/verify
9.注册后提示看邮件:/info/authake/user/verify1
</pre>