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
	
    安全性:Aneuan关于安全性的回答也不错：
	
	* 防止SQL注入，XSS，CSRF攻击等，文件上传（限制后缀），多用户并发问题，权限控制，数据库安全（备份与恢复），身份验证，敏感信息加密，日志记录，session和cookie等。

[SQL注入](http://baike.baidu.com/link?url=w7qyuWKP-20FL29eLg6Xzac50g_ZYdyjkKv1rNYqyT5IcbLI2hzQVaGraIU1D3xmE6a3cL10BTw4Wq8plahUxK)：所谓SQL注入，就是通过把SQL命令插入到Web表单提交或输入域名或页面请求的查询字符串，最终达到欺骗服务器执行恶意
	的SQL命令。具体来说，它是利用应用程序，将（恶意）的SQL命令注入到后台数据引擎执行的能力，它可以通过在Web表单中输入（恶意）SQL语句得到一个存在一
	个存在安全漏洞的网站上的数据库，而不是按照设计者意图去执行SQL语句。比如先前的很多影视网站泄露VIP会员密码大多就是通过WEB表单递交查询字符暴出的，
	这类表单特别容易受到[SQL注入式攻击](http://baike.baidu.com/view/195362.htm)；

[XSS](http://baike.baidu.com/link?url=66sDZyfb6sasAwjt8rO21Z43S5T08sh1GoYHvEFebDjJUevUcRt0IYRu7SfXZ_p2KfLsl82ASa9qiZ4JsM8I2a)：跨站脚本攻击(Cross Site Scripting),为不和层叠样式表(Cascading Style Sheets,CSS)的缩写混淆，
	故将跨站脚本攻击缩写为XSS，恶意攻击者往Web页面里插入恶意Script代码，当用户浏览该页之时，嵌入其中Web里面的Script代码会被执行，从而达到恶意攻击用户的特殊目的；

[CSRF](http://baike.baidu.com/link?url=rHCHqVmFqqcWN-RCODaSXG45IOYRSV0n14LcHY2_WHCsnJ8sFeNg_FtkSu3uqhhwhv0WscaR6liuMySqv80NWq)：跨站请求伪造(Cross-site request forgery)，
	也被称为"One Click Attack"或者Session Riding，通常缩写为CSRF或者XSRF，是一种对网站的恶意利用。尽管听起来像跨站脚本(XSS)，但它与XSS非常不同，并且攻击方式几乎相左。XSS利用站点内的信任用户，而CSRF则通过伪装来自受信任用户的请求来利用受信任的网站。与XSS攻击相比，CSRF攻击往往不大流行（因此对其进行防范的资源也
	相对稀少)和难以防范，所以被认为比XSS更具危险性。
	
<font color="#F095BC">SEO:</font>

	* When it comes to SEO, I refer to my approach as “the new old school.” That is, I don’t believe there is any “magic in your meta” tags and I encourage business owners to simply create content that is relevant to your business, write clearly and often, advertise when necessary, make sure your site is mobile 
	friendly, that sharing your content is easy, and you have control of your Google, Twitter, Facebook, Yahoo, Bing, Foursquare, Pinterest, Instagram (insert hot new here…) accounts, and everything really does fall into place. As your business grows, more visitors come, more people share and the search engines notice.
	
	SEO：
	
	* 提到SEO，我把我的方法称为“新的老学校“。那就是，我不相信有什么”meta标签魔法“，并且我会鼓励企业所有人仅仅写和你的企业有关的内容就好了，清楚的写，经常写，在必要的时候做做广告，确保你的网站是移动端有好的，这样可以确保分享你的内容很容易，你也要控制你的Google,Twitter,Facebook,Yahoo,Bing,Foursquare,Pinterest,Instagram(在这
	发布一些炫酷的新奇的东西)账户，确保一切都真的井然有序。随着企业的成长，更多的浏览者会光临，更多的人会分享，搜索引擎就会注意到。
	
	SEO:Aneuan关于SEO的回答更偏向实际操作：
	
	* 域名选择要正确，网站标题优化(一般是把关键字嵌入到title里面，但是分隔符一定要注意，谷歌识别的是字母“，”，百度识别的是“_”)，关键字和描述的优化(不能频繁更改，而且密度不能过高，保持10%以下)，网站结构优化（尽量不要使用table），图片的title和alt属性优化，站内链接优化（做到无死链），适当主动提交搜索引擎入口（http://tool.lusongsong.com/addurl.html），
	友情链接，当然还有些非技术的方法。

<font color="#F095BC">Maintainability and Technology Considerations:</font>

	* Use tooling that is more flexible and adhere’s to a standard. A great example of this is PostCSS, where the concept is, you write plain old CSS – and NEW CSS as well, including syntax not yet implemented in browsers and let a plugin process your css and manipulate the output so it’s browser ready. Then as time passes, W3C syntax is agreed upon, 
	pre-fix use subsides, and you can re-process your CSS with less and less manipulation.
	
	可维护性以及技术因素的考虑:
	
	* 使用更灵活、更符合标准的工具。一个典型的例子就是PostCss,它的概念就是，你写普通的老旧的CSS，同时也写新的CSS，其中包括在浏览器端还没有实现的语法，这时你让插件处理你的CSS并让它控制输出知道浏览器准备好了。接着，随着时间的流逝，W3C语法受到认可，前缀用法被淘汰，你就可以用越来越少的控制预处理你的CSS。
	
	可维护性：Aneuan简短的回答
	
	* 代码编写规范，注释明确，扩展性强
	
	技术因素：Aneuan简短的回答
	
	* 根据不同性质的网站要选择不同的框架



		
		

	
