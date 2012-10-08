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
1.登录:/info/UserLogin/login      77           登录不可访问
2.提交审核:/info/info/registerVerify     80    未登录不可访问
3.完善信息:/info/info/submitInfo         81    未登录不可访问
4.修改密码:/info/UserLogin/profile   82        未登录不可访问
5.登出:/info/authake/user/logout     83        是否登录没有影响
6.注册:/info/UserLogin/register          78        登录不可访问
7.忘记密码:/info/authake/user/lost_password   79   登录不可访问
8.邮箱验证码:/info/authake/user/verify    84       登录不可访问
9.注册后提示看邮件:/info/authake/user/verify1   85 废弃
10.忘记密码后修改密码:/info/authake/user/pass   92 登录不可访问
</pre>

###基金会捐赠数据提交至数据库
<pre>
c 支付单号 姓名	支付时间	支付方式	金额	付款状态	管理操作	团体名称	性别	邮箱	电话	类型	详细地址	邮政编码	学校信息	捐赠用途	捐赠留言

a 数据编号	是否捐赠	协议签订时间	协议签订人	协议参与人	协议金额	用途	执行年度	到款方式	到款时间

b 数据编号	职务	所属部门	姓名	身份证号	是否校友	校友信息	性别	生日	籍贯	学历	履历	工作电话	移动电话	电子邮箱	QQ	个人喜好	是否喝酒	喜欢酒牌	是否抽烟	喜欢烟牌	家庭电话	家属姓名	工作单位	家庭地址

c姓名 b姓名
c支付时间 a到款时间
c支付方式 a到款方式
c金额 a协议金额
c团体名称 b工作单位
c性别 b性别
c邮箱 b电子邮箱
c电话 b移动电话
c类型(个人 企业) ???
c详细地址 b家庭地址
c邮政编码 ???
c学校信息 ???
c捐赠用途 a用途
c捐赠留言 ???
</pre>