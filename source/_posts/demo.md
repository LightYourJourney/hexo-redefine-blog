---
title: Redefine 主题使用指南
date: 2022-9-28 11:45:14
tags:
    - "Demo"
    - "Hexo"
    - "Hexo Theme"
    - "Hexo Theme Redefine"
categories: [Hexo]
sticky: 999 <!-- 要实现顶置的文章，需在文章页添加 sticky 属性，sticky 值越大，顶置的文章越靠前 -->
thumbnail: "IMAGE_LINK" <!-- 首页缩略图 -->
excerpt: "这是文章摘要 This is the excerpt of the post"
excerpt: false <!-- 是否显示文章摘要 -->
banner: "图片链接" <!-- 文章页头图 或者 (cover: "图片链接")-->
<!-- 如果你设置了 首页缩略图 thumbnail ，文章封面也会自动选择为 thumbnail 链接，当然，banner 和 cover 的优先级最高。如果你不想设置文章封面却想保留首页头图，请把 cover 或者 banner 设置成 false -->
expires: 2023-08-31 23:59:59 <!-- 文章过期时间 -->
---

大号提示块

{% notel [颜色] [可选: 自定义图标] [标题] %}
内容
支持换行
{% endnotel %}

{% notel default fa-info 信息 %}
换行测试
换行测试
换行测试
{% endnotel %}
 
{% notel blue 提示 %}
换行测试
换行测试
换行测试
{% endnotel %}
 
{% notel red 自定义标题 %}
换行测试
换行测试
换行测试
{% endnotel %}

小号提示块

{% note [样式/颜色] [可选: 自定义图标] %}
笔记内容
{% endnote %}

{% note  %}
默认 提示块标签
{% endnote %}
 
{% note default  %}
default 提示块标签
{% endnote %}
 
{% note primary  %}
primary 提示块标签
{% endnote %}
 
{% note success  %}
success 提示块标签
{% endnote %}
 
{% note info  %}
info 提示块标签
{% endnote %}
 
{% note warning  %}
warning 提示块标签
{% endnote %}
 
{% note danger  %}
danger 提示块标签
{% endnote %}
 
{% note red fa-bolt%}
自定义提示块标签
{% endnote %}

按钮模块 {% btn [可选大小]::[名称]::[url]::[可选图标] %}

不设置任何参数的 {% btn 按钮:: / %} 适合融入段落中。
 
regular 按钮适合独立于段落之外：
 
{% btn regular::示例博客::https://www.ohevan.com::fa-solid fa-play-circle %}
 
{% btn regular::示例博客::https://www.ohevan.com::fa-solid fa-play-circle %}
 
large 按钮更具有强调作用，建议搭配 center 使用：
 
{% btn center large::开始使用::https://redefine-docs.ohevan.com::fa-solid fa-download %}

[可选大小] :

center, regular, large, center large, center regular

Folding 折叠模块

{% folding [颜色]::[标题] %}
 
需要写的内容
 
{% endfolding %}

Tabs 分栏模块
通过本模块可以在页面中添加多个栏目，用户可以通过点击标签页来切换内容。

{% tabs 页面内不重复的ID %}
<!-- tab 栏目1名称 -->
内容
<!-- endtab -->
<!-- tab 栏目2名称 -->
内容
<!-- endtab -->
{% endtabs %}

其中，页面内不重复的ID 为你为这个选项卡创建的唯一标识符，可以随便取。