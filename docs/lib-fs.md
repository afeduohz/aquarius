fs
-

### The API of `fs` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [perm](#perm)
+ [remove](#remove)
+ [open](#open)
+ [open_file](#open_file)
+ [create](#create)
+ [exist?](#exist?)
+ [read_all](#read_all)
+ [read_line](#read_line)
+ [chtimes](#chtimes)
+ [move](#move)
+ [remove_all](#remove_all)
+ [chdir](#chdir)
+ [walk](#walk)
+ [chmod](#chmod)
+ [chown](#chown)

#### FileMode `type`

|Mode|Desc|
|----|-----|
|ModeDir|d: is a directory
|ModeAppend|a: append-only
|ModeExclusive|l: exclusive use
|ModeTemporary|T: temporary file; Plan 9 only
|ModeSymlink|L: symbolic link
|ModeDevice|D: device file
|ModeNamedPipe|p: named pipe (FIFO)
|ModeSocket|S: Unix domain socket
|ModeSetuid|u: setuid
|ModeSetgid|g: setgid
|ModeCharDevice|c: Unix character device
|ModeSticky|t: sticky
|ModeIrregular|?: non-regular file; nothing else is known about this file

#### FileMode `permission`

Normally, use expression such as `(fs perm 777)` to generate a permission
`FileMode`.

####  flag

Exactly one of O_RDONLY, O_WRONLY, or O_RDWR must be specified.
The remaining values may be or'ed in to control behavior.

|Flag|Desc|
|----|-----|
|O_RDONLY|open the file read-only|
|O_WRONLY|open the file write-only|
|O_RDWR|open the file read-write|
|O_CREATE|create a new file if none exists|
|O_EXCL|used with O_CREATE, file must not exist|
|O_APPEND|append data to the file when writing|
|O_TRUNC|truncate regular writable file when opened|
|O_SYNC|open for synchronous I/O|


#### ==

```aquarius
(fs == any) -> bool
```

#### !=

```aquarius
(fs != any) -> bool
```

#### to_s

```aquarius
(fs to_s) -> string
```

#### to_b

```aquarius
(fs to_b) -> true
```

#### type

```aquarius
(fs type) -> string
```

#### perm

Create a permission [fs/FileMode](lib-fs-filemode.md).

```aquarius
(fs perm p(int)) -> filemode
```

#### remove

Remove the file `name`. It returns an `error`, if any.

```aquarius
(fs remove name(string)) -> nil
```

#### open

Open the file `name`. It returns an `error`, if any.

```aquarius
(fs open name(string)) -> file
```

#### open_file

Open file for generalize purple. Users can use [OS_RDONLY](#flag)
flag for reading, [OS_WRONLY](#flag) flag for writing, etc.

```aquarius
(fs open_file name(string) flag(int) mode(filemode)) -> file
```

#### create

Create a new file `name`. It returns an `error`, if any.

```aquarius
(fs create name(string)) -> file
```

#### exist?

Test whether the file `name` exists.

```aquarius
(fs exist? name(string)) -> bool
```

#### read_all

Read all content in file `name`. It returns an `error`, if any.

```aquarius
(fs readall name(string)) -> string
```

#### read_line

Read lines in file `name` by calling the `callback` for each line.
Every line as first parameter of `callback`.
It returns an `error`, if any.

```aquarius
(fs read name(string) callback(lambda)) -> nil
```

#### chtimes

Changes the access and modification times of the `name` file

```aquarius
(fs chtimes name(string) atime(time) mtime(time)) -> nil
```

#### move

Moves `source` to `target`. If `target` already exists and is 
not a directory, `move` replaces it.

```aquarius
(fs move source(string) target(string)) -> nil
```

#### remove_all

Removes `path` and any children it contains.

```aquarius
(fs remove_all path(string)) -> nil
```

#### chdir

Changes the current working directory to `path`.

```aquarius
(fs chdir path(string)) -> nil
```

#### walk

Walks the file tree rooted at `root`, calling `callback` for each 
file or directory in the tree, including `root`.
file path is as `callback` first parameter,
file info is as `callback` second parameter.

```aquarius
(fs walk root(string) callback(lambda)) -> nil
```

#### chmod

Changes the mode of the `name` file to `mode`.

```aquarius
(fs chmod name(string) mode(filemode)) -> nil
```

#### chown

Changes the numeric uid and gid of the `name` file.
On Windows, it will raise error.

```aquarius
(fs chown name(string) uid(int) gid(int)) -> nil
```
