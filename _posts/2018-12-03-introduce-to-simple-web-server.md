---
layout: post
title: 简单web服务搭建-GraphQL框架-项目介绍
categories: Simplewebserver
description: 对GraphQL框架的服务端开发部分项目的介绍
keywords: GraphQL,SimpleWebServer
---

<!--上面的尽量不要动-->
# 项目信息：
+ 项目名称：简单web服务搭建
+ 项目框架：
  + 后端：GraphQL
  + 前端：vue.js
+ 数据来源：
  [https://swapi.co/](https://swapi.co/)
  
# 项目安装与运行：

+ 前端：

   >mkdir D:\Code\ServiceComputingGroup\SWPI\Client\  
   cd D:\Code\ServiceComputingGroup\SWPI\Client\  
   git clone https://github.com/ServiceComputingGroup/SWPIClient.git  
   npm install  
   npm run dev  
  
+ 后端：

  >go get github.com/ServiceComputingGroup/simpleWebServer  
  cd %GOPATH%/src/github.com/ServiceComputingGroup/simpleWebServer  
  go install  
  simpleWebServer  
  
# 项目使用：

在安装了前端和后端代码之后，打开浏览器，在地址栏输入：
> http://localhost:8080

出现客户端界面.  
![初始界面](https://github.com/ServiceComputingGroup/ServiceComputingGroup.github.io/blob/master/images/posts/SWApi/apiRoot.PNG)
+ api使用如下：
  + 当处于未登录状态时：只能执行用户的注册和登录
  + 当处于登录状态下：
  + 用户信息修改
  + 用户登出
  + swapi数据查询：
     + 查询people：
        + people/index/?page=page#
          + 例如：
          
          >people/3 查询index为3的people  
          >people/?page=3 查询处于第三页的people，一共10个  
          >people/3/?page=3 查询index为3的people  
          >people/ 查询第一页的people  
          
     + 查询film：
        + films/index/?page=page#
          用法如people
     + 查询planets：
        + planet/index/?page=page#
     + 查询species：
        + species/index/?page=page#
     + 查询starship
        + starships/index/?page=page#
     + 查询vehicles：
        + vehicles/index/?page=page#
    
