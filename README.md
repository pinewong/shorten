## URL IS 定义
**URL IS(专属链接) 是一个短链接开源项目。**<br />
**官网：**[http://urlis.cn/](http://urlis.cn/)<br />
**API地址：**[http://api.urlis.cn/docs/#/shortens](http://api.urlis.cn/docs/#/shortens)<br />
**短链接：**通俗来说，就是将长的URL网址，通过程序计算等方式，转换为简短的网址字符串。<br />
**短链接意义：**让各种带有`?&=`符号的长链接更优雅；防止链接失效（本站允许修改原始链接）。<br />
**小技巧：**如果你新买的服务器，还没有绑定域名，可以直接将你的IP缩短哦！<br />

本地安装测试
==========
环境
---
```shell
Ruby: 2.2.5
Rails: 4.2
```
安装
---
```shell
git clone https://github.com/pinewong/shorten.git;
cd shorten;
# 修改config/database.yml配置，设置本地用户名和密码等
# 完成后接下面操作...

bundle install;
rake db:create;
rake db:migrate;
rake db:seed;
rails s;
# 成功启动后，打开 http://localhost:3000 查看效果
```

项目意义
=======
这几年短链接是真的很火，大公司都有自己的短链服务器。<br />
腾讯的url.cn和百度的dwz.cn都只做到给你生成链接就完了，到时候我们原链接改了，那个短链接就还是失效了。<br />
URL IS(专属链接) 是专门来增强短链服务的。我们不盈利，没有商业利益关系，功能上做到了以下几点：<br />
* 匿名用户可以随机产生链接，得到与其他短链一样的服务。<br />
* 提供API接口，如果你觉得WEB端程序不合用，且有能力编写其他平台客户端，我们提供给你功能API接口和文档。<br />
* 当用户登录授权后，允许用户自定义链接，管理自己创建的链接（下版本添加）。<br />

版本更新
=======
v0.1 2016-06-22
---------------
完成初步短链功能，包含匿名生成短链以及跳转功能。<br />
完成API接口和文档。<br />
*下版本优先增加授权用户对链接的管理功能。*
