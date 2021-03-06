# 验证授权

授权验证是一个很敏感的话题,在一个大型企业里往往需要一个专门的团队来负责,这里整理一些和授权验证相关的基本内容.

## 基础
不管是采用何种方式,都要首先保证链接安全,即至少是使用 HTTPS,为了简化开发和快速使用可使用 [letsencrypt](https://letsencrypt.org/) 提供的证书来提供安全链接.

出于安全考虑,也可以选择在客户端加密,即用户提交到服务器的的密码已经是加密过的,例如 sha1 用户的密码,这样也能避免用户密码的直接泄露.



## Auth 2.0
[Auth 2](http://oauth.net/2/)

* 是一套认证框架
* 规范复杂且庞大
* 主要用于对外提供用户认证服务

__强项__

* 快速开发
* 只需要少量的代码即可实现
* 减少管理

__限制__

* 授权交由第三方


## JWT
[JWT](http://jwt.io/)

* 是一套认证协议
* 协议简单且易于实现
* 主要用于分布式的无状态接口调用
* 国际标准 [RFC 7519](https://tools.ietf.org/html/rfc7519)

__强项__

* 快速开发
* 不需要 Cookie
* JSON 相对友好
* 不依赖社交登陆
* 概念简单易于理解

__限制__
* Token 有大小限制
* Token 不能被回收
* 需要 Token 有个较短的失效周期


## Resources
* [Auth 2.0 vs JWT](http://www.seedbox.com/en/blog/2015/06/05/oauth-2-vs-json-web-tokens-comment-securiser-un-api/)
* [JWT 验证](https://www.jsonwebtoken.io/)
