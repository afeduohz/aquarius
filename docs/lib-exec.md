exec
-

### The API of `exec` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [Command](#Command)
+ [$](#$)
+ [Pipe](#Pipe)
+ [|](#|)


#### ==

```aquarius
(exec == any) -> bool
```

#### !=

```aquarius
(exec != any) -> bool
```

#### to_s

```aquarius
(exec to_s) -> string
```

#### to_b

```aquarius
(exec to_b) -> true
```

#### type

```aquarius
(exec type) -> string
```

#### Command
Returns the [Cmd](lib-exec-cmd.md) struct to execute the 
named program with the given arguments.
```aquarius
(exec Command name(string) args(string)...) -> cmd
```

#### $
Alias of [Command](#Command).
```aquarius
(exec $ name(string) args(string)...) -> cmd
```

#### Pipe
Executes `cmd` one by one in the pipeline, and returns
a 2-elements list, where first is `stdout` of last cmd, and
second is `stderr` of `cmd`. It returns an `error`, if any.
```aquarius
(exec Piple cmd(cmd)...) -> [stdout, stderr]
```

#### |
Alias of [Pipe](#Pipe).
```aquarius
(exec | cmd(cmd)...) -> [stdout, stderr]
```