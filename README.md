# s2oauth
第三方网页登陆授权，如微信网页授权
### 实现过程
用户进入客户端（H5页面），进入登录页面，检测到为微信客户端，进行微信网页授权（实现自动登录或获取用户信息），首先跳转到本服务，本服务获取完微信授权信息后，将用户信息返回给客户端的登陆页。

### 使用方法
- 修改yml文件配置，假设该项目访问网址为 http://www.a.com
- 完整的跳转网址例子，http://www.a.com?targetUrl=http://www.mall.com/login?ref=/goods/detail/1
- targetUrl=后面为客户端地址，也就是登录页地址，ref=后面是登录成功后的重定向地址，如果没有可重定向的可以留空
- 首先对ref=后面内容进行urlencode，再对targetUrl=后面内容进行urlencode
