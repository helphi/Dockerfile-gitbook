# GitBook 常用插件

`book.json` 中 `plugins` 和 `pluginsConfig` 两个属性主要用于配置插件，插件可以到 <https://plugins.gitbook.com/> 中搜索。

## plugins

配置使用的插件

```json
"plugins": [
    "disqus"
]
```

添加新插件之间需要运行 `gitbook install` 来安装新的插件

Gitbook默认带有5个插件：

1. highlight
1. search
1. sharing
1. font-settings
1. livereload

如果要去除自带的插件， 可以在插件名称前面加减号 `-`，如下为去除自带的搜索插件：

```json
"plugins": [
    "-search"
]
```

## pluginsConfig

在 `plugins` 属性中配置插件后可以在 `pluginsConfig` 属性中配置插件相关的属性

```json
"pluginsConfig": {
    "fontsettings": {
        "theme": "sepia",
        "family": "serif",
        "size":  1
    }
}
```