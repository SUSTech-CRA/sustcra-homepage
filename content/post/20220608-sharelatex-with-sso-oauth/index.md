---
title: "快速同步CAS中的信息至CRA SSO及使用南科大CAS一键登录sharelatex等服务"                         
author: "CRA"  
description : ""    
date: 2022-06-10T18:00:00.00+08:00
slug: "cra-sharelatex-sso-cas"
image: "sign-in-via.jpg"
tags : [                                    
"service",
]
categories : [                              
"service",
]
keywords : [                                
"sso",
]
---

注：这篇文章是[关于CRA-Sharelatex切换域名及启用LDAP的说明](https://blog.sustcra.com/p/cra-sharelatex-sso/)的补充。

# 快速同步CAS中的信息至CRA SSO及使用南科大CAS一键登录sharelatex等服务

计算机研究协会现已实验性提供将CAS账户快速同步至CRA SSO的功能，老师同学们也可以使用此功能使用南科大CAS一键登录sharelatex等服务。

注意：此方式**无法同步CAS的密码**。如需设置密码，用户可在控制面板（[https://sso.cra.ac.cn/realms/cra-service-realm/account/](https://sso.cra.ac.cn/realms/cra-service-realm/account/)）中自行设置。

# 同步教程

## 未注册过CRA SSO的用户，需要先进行账户注册

开始同步前，**请确认您的CAS账户已经绑定了学校的邮箱（已知2021级的部分同学默认是没有绑定邮箱的！）**，请先参考此说明进行检查和绑定：

### 南科大CAS绑定邮箱

1. 使用此链接： [https://cas.sustech.edu.cn/cas/login](https://cas.sustech.edu.cn/cas/login) 登入CAS控制面板。
2. 登入后，点击左侧的菜单选项，选择`Sustech Email`菜单。

![cas-login](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/cas-login.png)

3. 检查自己是否绑定了邮箱，如果没有，请绑定自己的南科大邮箱（学生请绑定数字为用户名的邮箱）。

![check-cas-email](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/check-cas-email.png)

### 登入CRA SSO

打开 [https://sso.cra.ac.cn/realms/cra-service-realm/account/](https://sso.cra.ac.cn/realms/cra-service-realm/account/) 点击右上角的`Sign in`。

![register](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/register.png)

点击右下角的`via SUSTech CAS` :

![sign-in-via](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/sign-in-via.png)

随后用户会被跳转至南科大CAS进行认证。

如果信息不完整，CRA SSO将会返回一个完善信息的页面，请在此页面按照要求完善自己的姓名和邮箱：

![fill-information](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/fill-information.png)

如果信息完整，用户将会直接进入CRA SSO的个人主页，请在此主页内完善自己的姓名等信息并保存：

![user-info](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/user-info.png)

## 已注册过CRA SSO的用户，需要进行账户绑定

使用此链接进入控制面板： [https://sso.cra.ac.cn/realms/cra-service-realm/account/#/security/linked-accounts](https://sso.cra.ac.cn/realms/cra-service-realm/account/#/security/linked-accounts) ， 并点击`Link account` :

![link-account](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/link-account.png)

检查账户是否已经正确连接：

![linked-account](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/linked-account.png)

## 修改密码

如果此前未有注册过CRA SSO，在第一次通过CRA SSO登录时，系统会为您生成一个随机密码，您可以在控制面板的`Account Security`（[https://sso.cra.ac.cn/realms/cra-service-realm/account/#/security/signingin](https://sso.cra.ac.cn/realms/cra-service-realm/account/#/security/signingin)）里更改：

![update-pw](/Users/cyf/Documents/GitHub/cra/sustcra-com/content/post/20220608-sharelatex-with-sso-oauth/update-pw.png)

# 登录教程

点击sharelatex里的 `Log in via SUSTech CRA SSO / CAS` ，选择`via SUSTech CAS`登入即可。

---

如有任何问题，欢迎电邮至 [service@cra.moe](mailto:service@cra.moe) 询问。

有关通过CRA SSO的账户-密码组合（LDAP）登录的教程，请参考[这篇文章](https://blog.sustcra.com/p/cra-sharelatex-sso/)。
