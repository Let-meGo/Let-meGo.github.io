---
layout: post
title: IE与FF兼容问题
date: 2017-12-06 10:01:26
comments: true
tags: Javascript
toc: true
---
### 如何处理IE和Firefox如果处理事件兼容性

 获取事件
```javascript
    function et(e) {
        let event = window.event || e
    }
```
***

 键盘值的获取： Firfox下event.which和IE的event.keyCode相当
```javascript
    let key = event.keyCode || event.which
```
***
<!-- more -->
 事件源的获取：
```javascript
    let target = event.srcElement || event.target
```
***
 事件监听:
```javascript
    IE: element.attacthEvent('on' + eventName, function(){})
    Firfox: element.addEventListener(eventName, handler, false)
```
***
 鼠标位置： 在IE下，event对象有x、y属性，在Firfox下，event有PageX, PageY属性 所有获取鼠标位置时：
```javascript
   let x = event.x || event.pageX
```
***
 阻止默认浏览器行为：
```javascript
    e.preventDefault() || event.returnValue = false
```
***
 阻止冒泡事件：
```javascript
   e.stopPropagation() || event.cancelBubble = true
```
