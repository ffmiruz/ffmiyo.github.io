---
template: post.html
title: Go Deeper
date: 2020-06-29
---
### The new() Function
Built-in function new(<type>) allocates the appropriate memory for a zero-value of the specified type.
The function then returns the __**address**__ for the newly created __**zero-value**__.

### Interface Type
An interface value is a two word structure.
```golang
type interface struct {
    type uintptr
    data uintptr
}
```
Interface values record both the value and the type of the value. And can hold any value, reguardless of their type.

### String Struct
Go string is itself a struct.
```golang
type string struct {
    ptr *[]byte
    len int
}
```
string is immutable. For []byte to string conversion, []byte is copied to a backing []byte of the string.