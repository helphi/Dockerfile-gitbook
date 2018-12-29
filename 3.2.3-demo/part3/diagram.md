# 图表

- 序列图：<https://plugins.gitbook.com/plugin/sequence>
- 流程图：<https://plugins.gitbook.com/plugin/flow>

```json
"plugins": [
    "sequence",
    "flow"
]
```

## 示例

代码：

    ```sequence
        Title: Here is a title
        A->B: Normal line
        B-->C: Dashed line
        C->>D: Open arrow
        D-->>A: Dashed open arrow
    ```
    
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

```sequence
    Title: Here is a title
    A->B: Normal line
    B-->C: Dashed line
    C->>D: Open arrow
    D-->>A: Dashed open arrow
```

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