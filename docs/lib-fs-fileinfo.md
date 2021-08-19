fs/FileInfo
-

### The API of `fs/FileInfo` module:

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
+ [name](#name)
+ [size](#size)
+ [mode](#mode)
+ [modified_time](#modified_time)

#### ==

```aquarius
(info == any) -> bool
```

#### !=

```aquarius
(info != any) -> bool
```

#### to_s

```aquarius
(info to_s) -> string
```

#### to_b

```aquarius
(info to_b) -> true
```

#### type

```aquarius
(info type) -> string
```

#### dir?

Alias of `dir?` of [fs/FileMode](lib-fs-filemode.md).

```aquarius
(info dir?) -> bool
```

#### name

File base name.

```aquarius
(info name) -> string
```

#### size

Returns length in bytes for regular files.

```aquarius
(info size) -> int
```

#### mode

Returns file mode [fs/FileMode](lib-fs-filemode.md) bits.

```aquarius
(info mode) -> mode
```

#### modified_time

Returns modification time [Time](lib-time-time.md).

```aquarius
(info modified_time) -> time
```
