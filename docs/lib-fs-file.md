fs/File
-

### The API of `fs/File` module:

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
+ [info](#info)
+ [chmod](#chmod)
+ [chown](#chown)
+ [read](#read)
+ [read_line](#read_line)
+ [write](#write)
+ [write_line](#write_line)
+ [close](#close)


#### ==

```aquarius
(File == any) -> bool
```

#### !=

```aquarius
(File != any) -> bool
```

#### to_s

```aquarius
(File to_s) -> string
```

#### to_b

```aquarius
(File to_b) -> true
```

#### type

```aquarius
(File type) -> string
```

#### info

Returns the [fs/FileInfo](lib-fs-fileinfo.md) structure describing file.

```aquarius
(file info) -> fileinfo
```

#### chmod

Changes the mode of the file to `mode`.

```aquarius
(file chmod mode(filemode)) -> self
```

#### chown

Changes the numeric uid and gid of the named file.
On Windows, it will raise error.

```aquarius
(file chown uid(int) gid(int)) -> self
```

#### read

For each character, calling `callback`. If `callback`
return `false`, loop will exit.

```aquarius
(file read callback(lambda)) -> nil
```

#### read_line

For each line, calling `callback`. If `callback`
return `false`, loop will exit.

```aquarius
(file read_line callback(lambda)) -> nil
```

#### write

All parameters are first converted into strings, and then written to the file.
It returns an `error`, if any.

```aquarius
(file write any...) -> nil
```

#### write_line

All parameters are first converted into strings, and then written to the file. 
At last, append a new line.
It returns an `error`, if any.

```aquarius
(file write_line any...) -> nil
```

#### close

Close the file to release the resource.
It returns an `error`, if any.

```aquarius
(file close) -> nil
```