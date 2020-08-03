---
template: post.html
title: Javascript Semicolon
date: 2020-08-03
---
Javascript use semicolon `;` to separate statements. The semicolon is optional.
Semicolon is usually omitted if statements are in separate line. Javascript will 
insert the semicolon automatically.
```javascript
let x = 0 // Instead of, let x = 0;
let y = 1 // Instead of, let y = 1;
```

However line break is not treated as hidden semicolon. Javascript inserts semicolon if,
the next line is not the continuation of the current statement. Otherwise the lines is 
merged into a complete statement.
```javascript
let
x
x
=
0
```
the above will be interpreted as `let x;x=0;`

There are exception to the rule mentioned. line break after the keywords
`return`, `break` and `continue` will always get semicolon inserted.
```javascript
return
1;
```
The code above will be interpreted sd `return;1;` not `return 1;`

Another special case is for the operators `--` and `++`. The operators
are not considered as statements ender. 
```javascript
x
++
y
```
will be interpreted as `x;++y` not `x++;y`



