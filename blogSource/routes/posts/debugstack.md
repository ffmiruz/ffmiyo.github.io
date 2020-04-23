---
template: post.html
title: Who call that function?
date: 2020-04-23
---
Quickly see where a function is called in go
```golang
import "runtime/debug"

...

func aFunc() {
    log.Println(string(debug.Stack()))
}
```