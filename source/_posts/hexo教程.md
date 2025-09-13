---
abbrlink: 9caf0a8d
categories: []
date: '2023-08-27T10:11:39.062954+08:00'
tags: []
title: hexo教程
updated: '2023-8-27T10:11:39.492+8:0'
cover: https://blog.yizhixiaozhu.top/image/23.webp

---
一、前言
我看b站上有的教程一点都不专业，很繁琐，基本上都说用github pages，没有人教其他的内容，所以，我的全系列hexo教程，来了，本人也不专业，所以大佬轻点喷。

二、hexo搭建
第一步就是hexo搭建了，很多朋友看的这里就想跳过，但是，这个方法可能与你们的不一样，这个不是依赖于github pages，而是使用vercel进行部署

什么是vercel
vercel是一个站点托管平台，可以托管静态网页，后台提供CDN加速，同类的平台有Netlify 和 Github Pages，相比之下，vercel国内的访问速度更快。

我的解释
vercel和github pages不是同类型的东西，vercel的很多东西都是很厉害的，比起GitHub pages，vercel可以算作是半动态

正式开始
vercel的官网是vercel.com，注册一个账号，然后不用管了，把网页关掉。

输入这个网址https://vercel.com/new/clone?repository-url=https://github.com/Can1425/Blog

还是感谢一下Can1425大佬，这是他开发的工具然后直接下一步，部署就可以了

绑定域名
为什么要绑定域名呢，因为vercel的域名被墙了，所以，要绑定一下自己的域名，买一级域名的话建议选择top域名，在阿里云之类的云服务平台都可以买域名。

如果不想花钱可以用免费的二级域名，但我不是很推荐。

在vercel项目的setting，域名那一项就可以绑定了，输入你想分配的域名，比如blog.yizhixiaozhu.top就可以了，但是会报错，你把他的chame验证的信息地址下来，在阿里云的域名解析的地方，输入记录值，就可以了

前言
这篇文章转载于https://lanta.bangumi.cyou/2022/05/29/Qexo/

什么是Qexo？
Qexo 是一个快速、强大、漂亮的在线 Hexo 编辑器。使用 GPL 开源协议。支持包括且不限于在 Vercel 等平台部署

事前准备
按照上篇文章弄好

如果不知道怎么搞可以看看上篇文章



注册MongoDB
首先我们要去注册MongoDB来给Qexo提供数据库





新建成功后会自动跳到”Security”的”Quickstart”



等待几分钟数据库新建完成后

点击Connect



允许所有IP段访问（0.0.0.0）

然后连接方式选择MangoDB Shell





部署到Vercel
点击下面的按钮部署

部署到 Vercel

第一次部署会直接爆炸，问题不大，这是因为我们还没有设置数据库



回到项目首页，点击上面的”Settings”



然后点左侧栏的”Environment Variables”



照着下列表格来添加

名称	意义	示例
DOMAINS	你所允许通信的安全域名，可以添加多个（ 注意双引号而且是英文半角）	[“XXX.vercel.app”, “XXX.com”]
MONGODB_HOST	MongoDB 数据库连接地址	mongodb+srv://cluster0.xxxx.mongodb.net
MONGODB_PORT	MongoDB 数据库通信端口 默认应填写 27017	27017
MONGODB_USER	MongoDB 数据库用户名	chenrui
MONGODB_DB	MongoDB 数据库名	Cluster0
MONGODB_PASS	MongoDB 数据库密码	JWo0xxxxxxxx
添加完之后到顶部的”Deployments”然后”Redeploy”



然后就能顺利部署成功了

初始化Qexo
设置一下用户配置，API密钥看你自己配置



配置Github
你使用了Github Actions部署Hexo的仓库

1
username/repo
仓库的分支

1
master
Github 密钥
注意，请保留好该密钥，密钥生成后出于安全原因不会再出现，也不要泄漏给别人

于** **Github 设置 生成的 Token 需要 Repo 的读取和写入权限

1
wrq_P8sYPlYA9fjMlOPEYSKA84xxxxxxxxxxxxxx


仓库路径
仓库的路径 若为根目录留空

1
path/
图床配置
参照官方文档来设置，如果你要使用别的图床程序（比如PicGO）也可以直接跳过

Qexo文档 - 自定义图床配置

Qexo文档 - S3 图床配置

Qexo文档 - FTP 图床配置

Vercel配置
Vercel密钥
注意，请保留好该密钥，密钥生成后出于安全原因不会再出现，也不要泄漏给别人

首先前往Vercel后台生成密钥





项目ID
前往你的Qexo项目

Settings 里面的 General

往下滑就可以看到Project ID



完成


至此，Qexo的安装就已经完成了
本博客也使用了Qexo进行管理
祝你使用愉快

 
教程
这个工具是Can1425大佬的，所以他的文章可以删除，不要侵犯别人的版权，然后，在你的GitHub的仓库里，有一个叫config的文件，它是hexo主配置文件，打开它，在里面可以编辑网站名称与作者名称，选择主题，在theme的后面，我选择Anzhiyu，就输入就可以了，现在Can1425大佬只移植了三个主题，推荐Anzhiyu。

三、主题更改
因为Anzhiyu有官方文档，所以就不在说了，官方文档地址 docs.anheyu.com

教程
Vercel 部署
注意

Vercel 部署的环境需配合 1.4.0 以上版本的 twikoo.js 使用

默认域名** ***.vercel.app 在中国大陆访问速度较慢甚至无法访问，绑定自己的域名可以提高访问速度

查看视频教程

申请** **MongoDB 账号
创建免费 MongoDB 数据库，区域推荐选择** **AWS / N. Virginia (us-east-1)
在 Clusters 页面点击 CONNECT，按步骤设置允许所有 IP 地址的连接（为什么？），创建数据库用户，并记录数据库连接字符串，请将连接字符串中的** **<password> 修改为数据库密码
申请** **Vercel 账号
点击以下按钮将 Twikoo 一键部署到 Vercel

进入 Settings - Environment Variables，添加环境变量** **MONGODB_URI，值为第 3 步的数据库连接字符串
进入 Deployments , 然后在任意一项后面点击更多（三个点） , 然后点击Redeploy , 最后点击下面的Redeploy
进入 Overview，点击 Domains 下方的链接，如果环境配置正确，可以看到 “Twikoo 云函数运行正常” 的提示
Vercel Domains（包含** https://前缀，例如**https://xxx.vercel.app）即为您的环境 id
总结
本篇文章转载于twikoo的官方文档