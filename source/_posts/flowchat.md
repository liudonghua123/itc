---
title: flowchat
date: 2017-11-24 13:50:35
tags:
---

# This is flowchat demo!

```flow
st=>start: 开始申请|past:>http://www.ynu.edu.cn[blank]
e=>end: 流程结束:>http://www.ynu.edu.cn
op1=>operation: 第一个步骤|past
op2=>operation: 做点什么事情|current
sub1=>subroutine: 做点其他事情|invalid
cond=>condition: 是 不是?|同意:>http://www.google.com
c2=>condition: 是否完成|rejected
io=>inputoutput: 获取中...|request

st->op1(down)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```