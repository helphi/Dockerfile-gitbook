# 中文搜索

<https://plugins.gitbook.com/plugin/search-pro>

Search Pro 插件支持中文搜索, 需要将默认的 search 插件去掉, 注意: 如果标题中有包含的关键字, 标题的样式会有所变化

```json
"plugins": [
    "-lunr", "-search", "search-pro"
],
"pluginsConfig": {
    "search-pro": {
        "cutWordLib": "nodejieba",
        "defineWord" : ["Gitbook Use"]
    }
}
```