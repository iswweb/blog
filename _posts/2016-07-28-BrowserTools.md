---
layout:     post
title:      BrowserTools
category: blog
author: www.iswweb.com
description: BrowserTools主要是一系列的基于浏览器收藏夹栏的快捷小工具，使用非常简单，不需要安装。
---


## BrowserTools是什么?
BrowserTools主要是一系列的基于浏览器收藏夹栏的快捷小工具，使用非常简单，不需要安装，只是一些简单的Javascript代码，可以实现一些常用的功能，而无需安装臃肿的插件。最主要的是它可以在任何浏览器里使用，无需担心兼容性问题，使用非常简单，只需要将他们拖动到收藏夹栏就可以了！

## BrowserTools使用方式?

* 拖动下面的 例如`@发送到手机`到收藏夹栏就可以，使用的时候直接点击就行了。
* 如果你喜欢比较简洁的收藏夹栏 拖动下面的 例如`@M`也可以，你可以自由编辑任何你记得住的名字。
* 假如你的浏览器不支持直接拖动\(一般情况下都支持，例外的也有\)的话，你可以按照下面的方式做

		新建一个收藏，将名字命名为 `@发送到手机` ，然后把下面的代码复制进去，做为网址，然后保存即可。使用方法更简单，只要在浏览器栏里显示收藏夹就可以了，在打开的网页点击 `@发送到手机`就可以把当前页面生成二维码了！同样的其他功能也是一样的使用方法！

## BrowserTools目前支持哪些功能?

* 1.将当前页面生成一个二维码通过手机扫描发送到手机上。

<a href="javascript:(function(){var u=document.URL;var w=window.open('http://qr.liantu.com/api.php?text='+encodeURIComponent(u),'_blank');w.focus();})();">`@发送到手机`</a>   <a href="javascript:(function(){var u=document.URL;var w=window.open('http://qr.liantu.com/api.php?text='+encodeURIComponent(u),'_blank');w.focus();})();">`@M`</a>

```javascript
javascript:(function(){var u=document.URL;var w=window.open('http://qr.liantu.com/api.php?text='+encodeURIComponent(u),'_blank');w.focus();})();
```

* 2.将当前页面生成一个可以模拟响应式效果的工具中。

<a href="javascript:(function(){var u=document.URL;var w=window.open('http://xys.iswweb.com/?url='+encodeURIComponent(u),'_blank');w.focus();})();">`@模拟响应式`</a>  <a href="javascript:(function(){var u=document.URL;var w=window.open('http://xys.iswweb.com/?url='+encodeURIComponent(u),'_blank');w.focus();})();">`@B`</a>

```javascript
javascript:(function(){var u=document.URL;var w=window.open('http://xys.iswweb.com/?url='+encodeURIComponent(u),'_blank');w.focus();})();
```


* 3.切换百度搜索为GOOGLE搜索，在google界面切换回百度搜索。

<a href="javascript:(function(){var u=document.URL;var ua=u.split('=');if (ua[0].indexOf('baidu')>0){var ub=u.split('wd=');var uc=ub[1].split('&');var nu='http://guge.hntvchina.com/search?hl=zh-CN&q='+uc[0];}else{var ub=ua[2].split('&');nu='https://www.baidu.com/s?wd='+ub[0];}location=nu;})();">`@百度谷歌切换`</a> <a href="javascript:(function(){var u=document.URL;var ua=u.split('=');if (ua[0].indexOf('baidu')>0){var ub=u.split('wd=');var uc=ub[1].split('&');var nu='http://guge.hntvchina.com/search?hl=zh-CN&q='+uc[0];}else{var ub=ua[2].split('&');nu='https://www.baidu.com/s?wd='+ub[0];}location=nu;})();">`@S`</a>

```javascript
javascript:(function(){var u=document.URL;var ua=u.split('=');if (ua[0].indexOf('baidu')>0){var ub=u.split('wd=');var uc=ub[1].split('&');var nu='http://guge.hntvchina.com/search?hl=zh-CN&q='+uc[0];}else{var ub=ua[2].split('&');nu='https://www.baidu.com/s?wd='+ub[0];}location=nu;})();
```

* 4.生成一个随机的密码。

<a href="javascript:var randPwd=function(){var text=['abcdefghijklmnopqrstuvwxyz','ABCDEFGHIJKLMNOPQRSTUVWXYZ','1234567890'];var rand=function(min,max){return Math.floor(Math.max(min,Math.random()*(max+1)))};var len=rand(10,12);var pw='';for(i=0;i<len;++i){var strpos=rand(0,2);pw+=text[strpos].charAt(rand(0,text[strpos].length))}return pw};var pwd=randPwd();if(window.clipboardData){window.clipboardData.setData('Text',pwd);};var p=prompt('请复制密码',pwd);if(p){alert(p);};">`@生成随机密码`</a>  <a href="javascript:var randPwd=function(){var text=['abcdefghijklmnopqrstuvwxyz','ABCDEFGHIJKLMNOPQRSTUVWXYZ','1234567890'];var rand=function(min,max){return Math.floor(Math.max(min,Math.random()*(max+1)))};var len=rand(10,12);var pw='';for(i=0;i<len;++i){var strpos=rand(0,2);pw+=text[strpos].charAt(rand(0,text[strpos].length))}return pw};var pwd=randPwd();if(window.clipboardData){window.clipboardData.setData('Text',pwd);};var p=prompt('请复制密码',pwd);if(p){alert(p);};">`@P`</a>

```javascript
javascript:var randPwd=function(){var text=['abcdefghijklmnopqrstuvwxyz','ABCDEFGHIJKLMNOPQRSTUVWXYZ','1234567890'];var rand=function(min,max){return Math.floor(Math.max(min,Math.random()*(max+1)))};var len=rand(10,12);var pw='';for(i=0;i<len;++i){var strpos=rand(0,2);pw+=text[strpos].charAt(rand(0,text[strpos].length))}return pw};var pwd=randPwd();if(window.clipboardData){window.clipboardData.setData('Text',pwd);};var p=prompt('请复制密码',pwd);if(p){alert(p);};
```

* 5.打开有道云笔记的网页剪辑器。

<a href="javascript:(function(){CLIP_HOST='http://note.youdao.com/yws';try{var x=document.createElement('SCRIPT');x.type='text/javascript';x.src=CLIP_HOST+'/YNoteClipper.js?'+(new Date().getTime()/100000);x.charset='utf-8';document.getElementsByTagName('head')[0].appendChild(x);}catch(e){alert(e);}})();">`@有道云笔记`</a> <a href="javascript:(function(){CLIP_HOST='http://note.youdao.com/yws';try{var x=document.createElement('SCRIPT');x.type='text/javascript';x.src=CLIP_HOST+'/YNoteClipper.js?'+(new Date().getTime()/100000);x.charset='utf-8';document.getElementsByTagName('head')[0].appendChild(x);}catch(e){alert(e);}})();">`@N`</a>

```javascript
javascript:(function(){CLIP_HOST='http://note.youdao.com/yws';try{var x=document.createElement('SCRIPT');x.type='text/javascript';x.src=CLIP_HOST+'/YNoteClipper.js?'+(new Date().getTime()/100000);x.charset='utf-8';document.getElementsByTagName('head')[0].appendChild(x);}catch(e){alert(e);}})();
```
