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
    