# 图表

<https://plugins.gitbook.com/plugin/chart>

绘制图表

```json
"plugins": [
    "chart"
]
```

## 示例

代码：

```
{% chart %}
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 1500, 2500],
            ["data2", 50, 100, 300, 450, 650, 250, 1320]
        ]
    },
    "axis": {
        "y": {
            "tick": {
                "format": d3.format("$,")
            }
        }
    }
}
{% endchart %}
```

效果：

{% chart %}
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 1500, 2500],
            ["data2", 50, 100, 300, 450, 650, 250, 1320]
        ]
    },
    "axis": {
        "y": {
            "tick": {
                "format": d3.format("$,")
            }
        }
    }
}
{% endchart %}