---
template: post.html
title: Slice and Empty Struct
date: 2020-06-19
---
From [github.com/bradfitz/iter](https://github.com/bradfitz/iter/blob/master/iter.go) the code below does not allocate.
```golang
// It does not cause any allocations.
func N(n int) []struct{} {
  return make([]struct{}, n)
}
```

Slice is actually a struct type. Usually called slice header.
```golang
package runtime

type slice struct {
        ptr   unsafe.Pointer
        len   int
        cap   int
}
```
The three fields of slice header are copied on pass, return, assign and subslice.

Empty struct `struct{}` is a struct type that has no fields. Empty struct contains no data and therefore
consumes zero bytes of storage.

So, what is returned in the N function above is the copied value of a slice header struct.
