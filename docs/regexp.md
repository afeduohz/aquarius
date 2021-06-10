RegExp
-

It is wrapper of Golang RegExp. 

### The API of `RegExp` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `regexp` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [match?](#match?) 
+ [expr](#expr)
+ [groups](#groups)
+ [names](#names)
+ [literal_prefix](#literal_prefix)
+ [find](#find)
+ [find_all](#find_all)



#### ==

```aquarius
(RegExp == any) -> bool
```

#### !=

```aquarius
(RegExp != any) -> bool
```

#### to_s

```aquarius
(RegExp to_s) -> string
```

#### to_b

```aquarius
(RegExp to_b) -> true
```

#### type

```aquarius
(RegExp type) -> string
```

#### :
Returns a new regular expression value.
```aquarius
(RegExp: expr(string)) -> RegExp
```

#### match?
Reports whether `source` contains any match of the regular expression.
```aquarius
(RegExp match? source(string)) -> bool
```

#### expr
Returns source text to compile regular expression.
```aquarius
(RegExp expr) -> string
```

#### groups
Returns the number of parenthesized subexpressions in the regular expression.
```aquarius
(RegExp groups) -> int
```

#### names
Returns the names of the parenthesized subexpressions in the regular expression.
```aquarius
(RegExp names) -> [string...]
```

#### literal_prefix
Returns a 2-element list [`literal` `boolean`], where `literal` string that must begin any 
match of the regular expression. It returns the `boolean` true if the `literal` string 
comprises the entire regular expression.
```aquarius
(RegExp literal_prefix) -> [string, boolean]
```

#### longest
Makes future searches prefer the leftmost-longest match.
```aquarius
(RegExp longest) -> self
```

#### find
Returns a string holding the text of the leftmost match in s of the regular expression. 
If there is no match, the return value is an empty string, but it will also be empty if 
the regular expression successfully matches an empty string.
```aquarius
(RegExp find s(string)) -> string
```

#### find_all
Returns a list of all successive matches of the expression.
`i` finger out number of results you want.
```aquarius
(RegExp find_all s(string) [i(int)]) -> [string...]
```