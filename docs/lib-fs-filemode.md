fs/FileMode
-

### The API of `fs/FileMode` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)

### The API of `file` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [dir?](#dir?)
+ [regular?](#regular?)
+ [mode_type](#mode_type)
+ [mode_perm](#mode_perm)

#### ==

```aquarius
(mode == any) -> bool
```

#### !=

```aquarius
(mode != any) -> bool
```

#### to_s

```aquarius
(mode to_s) -> string
```

#### to_b

```aquarius
(mode to_b) -> true
```

#### type

```aquarius
(mode type) -> string
```

#### dir?

Reports whether `mode` describes a directory.

```aquarius
(mode dir?) -> bool
```

#### regular?

Reports whether `mode` describes a regular file.

```aquarius
(mode regular?) -> bool
```

#### mode_type

Returns type bits.

```aquarius
(mode mode_type) -> mode
```

#### mode_perm

Returns the Unix permission bits.

```aquarius
(mode mode_perm) -> mode
```

#### |

Returns the `or` operation result of `mode` and `mode1`.

```aquarius
(mode | mode1(mode)) -> mode
```