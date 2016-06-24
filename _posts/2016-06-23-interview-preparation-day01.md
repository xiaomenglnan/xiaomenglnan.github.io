---
layout: post
title: "2016-06-23-interview-preparation-day01"
date: 2016-06-23 16-20-22
categories: Interview
tags: front-interview preparation questions answers thoughts 
---

* content
{:toc}

本文中的答案，整理自[Peter Dillon](http://peterdoes.it/) from [Adecco Group NA](http://www.adecco.com/default.aspx)、[paddingme](https://github.com/paddingme/Front-end-Web-Development-Interview-Question/blob/master/前端试题/4.md) from Github、[Aneuan](http://aneuan.sinaapp.com/blog/158/)、
以及[砸牛顿的大苹果的果园](https://stenders.github.io/)。

### <font color="#F095BC">1.在制作一个网页应用或网站的过程中，你是如何考虑其UI、安全性、高性能、SEO、可维护性以及技术因素的？</font>

我并不知道SEO是什么，所以先百度一下，是这么说的：[SEO](http://baike.baidu.com/view/1047.htm)是由英文Search Engine Optimization缩写而来，中文意译为
"[搜索引擎](http://baike.baidu.com/view/1154.htm)优化"。[SEO](http://baike.baidu.com/view/1047.htm)是指通过对[网站](http://baike.baidu.com/subview/4232/18338514.htm)内部调整优化及[站外优
化](http://baike.baidu.com/view/5081047.htm)，使网站满足[搜索引擎收录](http://baike.baidu.com/view/1154.htm)排名需求，在搜索引擎中提高[关键词](http://baike.baidu.com/subview/10083/14670061.htm)
排名，从而把精准用户带到网站，获得[免费流量](http://baike.baidu.com/view/12087042.htm),产生直接销售或[品牌推广](http://baike.baidu.com/subview/280567/19228712.htm)。

<font color="#F095BC">UI:</font>

	* Depending on your audience,accessibility can be your biggest challenge and resources such as http://a11yproject.com are great in suggesting patterns to achieve whats needed.Beyond that,a pleasant palette and intuitive interfaces are the foundation,
which arise from well developed style guides containing code snippets that help developers quickly deliver features with pre-themed UI elements tha alleviate common pain points such as non-conforming elements that may distract stake holders during the 
iteration and approval process.

	* 根据你的受众，可访问性是最大的挑战，为了获得所需资源，形如http://a11yproject.com的可采用模式是非常不错的选择。除此之外，一个宜人的调色板和直观的界面起到基础性的作用。这要归功于优良的开发样式指导，其中包含的代码片段可以帮助开发者们迅速的用预定义主题的
UI元素转换特征以消除可能不符合要求的元素，来缓解这些元素在迭代和审批流程中常见的让股权所有者失去兴趣的痛点。

<font color="#F095BC">Security:</font>

	* Login pages should be encrypted
	* Data validation should be done server-side
	* Manage your Web site via encrypted connections

    安全性:

	* 登录页面应该加密
	* 应该在服务器端进行数据验证
	* 通过加密连接管理网站
	
    安全性:先百度几个不知道意思的词，

	* [SQL注入](http://baike.baidu.com/link?url=w7qyuWKP-20FL29eLg6Xzac50g_ZYdyjkKv1rNYqyT5IcbLI2hzQVaGraIU1D3xmE6a3cL10BTw4Wq8plahUxK)：所谓SQL注入，就是通过把SQL命令插入到Web表单提交或输入域名或页面请求的查询字符串，最终达到欺骗服务器执行恶意
	的SQL命令。具体来说，它是利用应用程序，将（恶意）的SQL命令注入到后台数据引擎执行的能力，它可以通过在Web表单中输入（恶意）SQL语句得到一个存在一
	个存在安全漏洞的网站上的数据库，而不是按照设计者意图去执行SQL语句。比如先前的很多影视网站泄露VIP会员密码大多就是通过WEB表单递交查询字符暴出的，
	这类表单特别容易受到[SQL注入式攻击](http://baike.baidu.com/view/195362.htm)；

	* [XSS](http://baike.baidu.com/link?url=66sDZyfb6sasAwjt8rO21Z43S5T08sh1GoYHvEFebDjJUevUcRt0IYRu7SfXZ_p2KfLsl82ASa9qiZ4JsM8I2a)：跨站脚本攻击(Cross Site Scripting),为不和层叠样式表(Cascading Style Sheets,CSS)的缩写混淆，
	故将跨站脚本攻击缩写为XSS，恶意攻击者往Web页面里插入恶意Script代码，当用户浏览该页之时，嵌入其中Web里面的Script代码会被执行，从而达到恶意攻击用户的特殊目的；

	* [CSRF](http://baike.baidu.com/link?url=rHCHqVmFqqcWN-RCODaSXG45IOYRSV0n14LcHY2_WHCsnJ8sFeNg_FtkSu3uqhhwhv0WscaR6liuMySqv80NWq)：跨站请求伪造(Cross-site request forgery)，
	也被称为"One Click Attack"或者Session Riding，通常缩写为CSRF或者XSRF，是一种对网站的恶意利用。尽管听起来像跨站脚本(XSS)，但它与XSS非常不同，并且攻击方式几乎相左。XSS利用站点内的信任用户，而CSRF则通过伪装来自受信任用户的请求来利用受信任的网站。与XSS攻击相比，CSRF攻击往往不大流行（因此对其进行防范的资源也
	相对稀少)和难以防范，所以被认为比XSS更具危险性。

	Aneuan关于安全性的回答也不错：

		* 防止SQL注入，XSS，CSRF攻击等，文件上传（限制后缀），多用户并发问题，权限控制，数据库安全（备份与恢复），身份验证，敏感信息加密，日志记录，session和cookie等。
		

	
