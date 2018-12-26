# GitBook 基本配置

GitBook 配置文件为 `book.json`，其基本配置项如下：

## title

设置书本的标题

```json
"title" : "Gitbook Use"
```

## author

作者的相关信息

```json
"author" : "GitBookkkkkkk"
```

## description

本书的简单描述

```json
"description" : "记录Gitbook的配置和一些插件的使用"
```

## language

Gitbook使用的语言, 版本2.6.4中可选的语言如下：

```
en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw
```

配置使用简体中文

```json
"language" : "zh-hans",
```

## links

在左侧导航栏添加链接信息

```json
"links" : {
    "sidebar" : {
        "Home" : "http://gitbook.com"
    }
}
```

## styles

自定义页面样式， 默认情况下各generator对应的css文件

```json
"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
```

例如使 `<h1>` `<h2>` 标签有下边框， 可以在 `website.css` 中设置

```css
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}
```