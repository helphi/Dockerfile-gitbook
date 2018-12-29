# 图表

## 序列图

<https://plugins.gitbook.com/plugin/sequence>

代码：

    ```sequence
        Title: Here is a title
        A->B: Normal line
        B-->C: Dashed line
        C->>D: Open arrow
        D-->>A: Dashed open arrow
    ```

效果：

```sequence
    Title: Here is a title
    A->B: Normal line
    B-->C: Dashed line
    C->>D: Open arrow
    D-->>A: Dashed open arrow
```

## 流程图

<https://plugins.gitbook.com/plugin/flow>

代码：

    ```flow
    st=>start: Start|past:>http://www.google.com[blank]
    e=>end: End:>http://www.google.com
    op1=>operation: My Operation|past
    op2=>operation: Stuff|current
    sub1=>subroutine: My Subroutine|invalid
    cond=>condition: Yes
    or No?|approved:>http://www.google.com
    c2=>condition: Good idea|rejected
    io=>inputoutput: catch something...|request
    
    st->op1(right)->cond
    cond(yes, right)->c2
    cond(no)->sub1(left)->op1
    c2(yes)->io->e
    c2(no)->op2->e

    ```

效果：

```flow
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```

## echarts

<https://plugins.gitbook.com/plugin/echarts>

代码：

    ```chart
    {
        "title": {
            "text": "Fruits number"
        },
        "tooltip": {},
        "legend": {
            "data":["Number"]
        },
        "xAxis": {
            "data": ["Apple","Banana","Peach","Pear","Grape","Kiwi"]
        },
        "yAxis": {},
        "series": [{
            "name": "Number",
            "type": "bar",
            "data": [5, 20, 36, 10, 10, 20]
        }]
    }
    ```

效果：

```chart
{
    "title": {
        "text": "Fruits number"
    },
    "tooltip": {},
    "legend": {
        "data":["Number"]
    },
    "xAxis": {
        "data": ["Apple","Banana","Peach","Pear","Grape","Kiwi"]
    },
    "yAxis": {},
    "series": [{
        "name": "Number",
        "type": "bar",
        "data": [5, 20, 36, 10, 10, 20]
    }]
}
```

## UML

<https://plugins.gitbook.com/plugin/nomnoml>


代码：

```
{% nomnoml %}

#fill: #d5e7ee; #8ebff2

[<frame>Decorator pattern|
  [<abstract>Component||+ operation()]
  [Client] depends --> [Component]
  [Decorator|- next: Component]
  [Decorator] decorates -- [ConcreteComponent]
  [Component] <:- [Decorator]
  [Component] <:- [ConcreteComponent]
]  

{% endnomnoml %}
```

效果：

{% nomnoml %}

#fill: #d5e7ee; #8ebff2

[<frame>Decorator pattern|
  [<abstract>Component||+ operation()]
  [Client] depends --> [Component]
  [Decorator|- next: Component]
  [Decorator] decorates -- [ConcreteComponent]
  [Component] <:- [Decorator]
  [Component] <:- [ConcreteComponent]
]  

{% endnomnoml %}