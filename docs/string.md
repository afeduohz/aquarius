String
-

### The API of `String` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `string` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [*](#*)
+ [+](#+)
+ [<<](#<<)
+ [>>](#\>>)
+ [capitalize](#capitalize)
+ [capitalize!](#capitalize!)
+ [<=>](#<=>)
+ [center](#center)
+ [chars](#chars)
+ [chr](#chr)
+ [clear](#clear)
+ [delete](#delete)
+ [delete!](#delete!)
+ [lower](#lower)
+ [lower!](#lower!)
+ [upper](#upper)
+ [upper!](#upper!)
+ [each](#each)
+ [empty?](#empty?)
+ [end_with?](#end_with?)
+ [start_with?](#start_with?)
+ [include?](#include?)
+ [index](#index)
+ [rindex](#rindex)
+ [insert](#insert)
+ [size](#size)
+ [ljust](#ljust)
+ [rjust](#rjust)
+ [lstrip](#lstrip)
+ [lstrip!](#lstrip)
+ [rstrip](#rstrip)
+ [rstrip!](#rstrip!)
+ [strip](#strip)
+ [strip!](#strip!)
+ [partition](#partition)
+ [rpartition](#rpartition)
+ [replace](#replace)
+ [reverse](#reverse)
+ [reverse!](#reverse!)
+ [slice](#slice)
+ [slice!](#slice!)
+ [split](#split)


#### ==

```aquarius
(String == any) -> bool
```

#### !=

```aquarius
(String != any) -> bool
```

#### to_s

```aquarius
(String to_s) -> string
```

#### to_b

```aquarius
(String to_b) -> true
```

#### type

```aquarius
(String type) -> string
```

#### :
Return a new string. if `s` is provided, return s [to_s](#to_s).
```aquarius
(String : [s(any)]) -> string
```

#### *
Return a new string that repeat `String` `t` times. If `t` < 1, returns 
empty string.
```aquarius
(String * t(int)) -> string
```

#### +
Return a new string that concat `String` and `s` [to_s](#to_s).
```aquarius
(String + s(any)...) -> string
```

#### <<
Append s `s` [to_s](#to_s) to the end of `String`, and return itself.
```aquarius
(String << s(any)...) -> string
```

#### \>>
Prepend s `s` [to_s](#to_s) to the head of `String`, and return itself.
```aquarius
(String >> s(any)...) -> string
```

#### capitalize
Return a new capitalized string of `String`.
```aquarius
(String capitalize) -> string
```

#### capitalize!
Capitalize `String` in place, and return itself.
```aquarius
(String capitalize!) -> string
```

#### <=>
Compare with s [to_s](#to_s). 
return -1, if `String` > s;
returns 0, when `String` == s;
returns 1, when `String` < s.
```aquarius
(String <=> s(any)) -> int
```

#### center
Centers `String` in `width`. If `width` is greater than the length of `String`, 
returns a new string of length width with `String` centered and padded with 
`pad`; otherwise, returns copy of `String`. Default `pad` is `\s`.
```aquarius
(String center width(int) [pad(string)]) -> string
```

#### chars
Returns an array of characters in `String`.
```aquarius
(String chars) -> list
```

#### chr
Returns the first character in `String`.
```aquarius
(String chr) -> string
```

#### clear
Make `String` empty.
```aquarius
(String clear) -> string
```

#### delete
Return a new copied `String` with `r` deleted.
```aquarius
(String delete r(string)...) -> string
```

#### delete!
Remove all `r` in `String`.
```aquarius
(String delete! r(string)...) -> self
```

#### lower
Return a new copied `String` with all uppercase characters replaced 
with lowercase ones.
```aquarius
(String lower) -> string
```

#### lower!
Replace all uppercase characters to lowercase ones, and return itself.
```aquarius
(String lower!) -> self
```

#### upper
Return a new copied `String` with all lowercase characters replaced
with uppercase ones.
```aquarius
(String upper) -> string
```

#### upper!
Replace all lowercase characters to uppercase ones, and return itself.
```aquarius
(String upper!) -> self
```

#### each
For each character, call `f`, and return itself.
```aquarius
(String each f(lambda)) -> self
```

#### empty?
Returns `true` if `String` is empty.
```aquarius
(String empty?) -> bool
```

#### end_with?
Returns `true` if `String` ends with `s`.
```aquarius
(String end_with? s(string)) -> bool
```

#### start_with?
Returns `true` if `String` starts with `s`.
```aquarius
(String end_with? s(string)) -> bool
```

#### include?
Returns `true` if `String` contains `s`.
```aquarius
(String include? s(string)) -> bool
```

#### index
Returns the index of the first occurrence of the given `s`. 
Returns -1, if `s` is not found.
```aquarius
(String index s(string)) -> int
```

#### rindex
Returns the index of the last occurrence of the given `s`. 
Returns -1, if `s` is not found.
```aquarius
(String rindex s(string)) -> int
```

#### insert
Inserts `s` before the character at the given index `i`, modifying `String`. 
Negative indices count from the end of the `String`, and insert after 
the given character. The intent is insert aString so that it starts at 
the given index.
```aquarius
(String insert i(int) s(string)) -> self
```

#### size
Return length of `String`.
```aquarius
(String size) -> int
```

#### ljust
If `width` is greater than the length of `String`, returns a new string 
of length `width` with `String` left justified and padded with `pad`; 
otherwise, returns copied `String`.
```aquarius
(String ljust width(int) pad(string)) -> string
```

#### rjust
If `width` is greater than the length of `String`, returns a new string
of length `width` with `String` right justified and padded with `pad`;
otherwise, returns copied `String`.
```aquarius
(String rjust width(int) pad(string)) -> string
```

#### lstrip
Returns a copy of the `String` with leading whitespace removed.
```aquarius
(String lstrip) -> string
```

#### lstrip!
Removes leading whitespace from the `String`, and returns itself.
```aquarius
(String lstrip!) -> self
```

#### rstrip
Returns a copy of the `String` with trailing whitespace removed.
```aquarius
(String rstrip) -> string
```

#### rstrip!
Removes trailing whitespace from the `String`, and returns itself.
```aquarius
(String rstrip!) -> self
```

#### strip
Returns a copy of the `String` with heading and trailing whitespace removed.
```aquarius
(String strip) -> string
```

#### strip!
Removes heading and trailing whitespace from the `String`, and returns itself.
```aquarius
(String strip!) -> self
```

#### partition
Searches `sep` in the `String` and returns the part before it, the match, and 
the part after it. If it is not found, returns two empty strings and `String`.
```aquarius
(String partition sep(string)) -> [string, string, string]
```

#### rpartition
Searches `sep` in the `String` from the end and returns the part before it, the match, and
the part after it. If it is not found, returns two empty strings and `String`.
```aquarius
(String rpartition! sep(string)) -> [string, string, string]
```

#### replace
Replaces the contents of `String` with the corresponding values in `other`, and
return itself.
```aquarius
(String replace other(string)) -> self
```

#### reverse
Returns a new string with the characters from `String` in reverse order.
```aquarius
(String reverse) -> string
```

#### reverse!
Reverses `String` in place, and return itself.
```aquarius
(String reverse!) -> self
```

#### slice
Returns a substring containing length `c` characters starting 
at the `i` index. If `c` is provided, and
`c` < 0, returns `nil`;
`c` == 0, returns empty string;
`c` > 0, return length of substring from index `i`.
```aquarius
(String slice i(int) [c(int)]) -> string
```

#### slice!
Deletes the specified portion from `String`, and returns the portion deleted.
```aquarius
(String slice! i(int) [c(int)]) -> string
```

#### split
Divides `String` into substrings based on a `sep`, returning a list of 
these substrings.
```aquarius
(String split sep(string)) -> list
```