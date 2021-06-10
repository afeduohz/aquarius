exec/Cmd
-
developing...

### The API of `exec/Cmd` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)

### The API of `exec/Cmd` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [Output](#Output)
+ [CombinedOutput](#CombinedOutput)
+ [Run](#Run)
+ [Start](#Start)
+ [Wait](#Wait)


#### ==

```aquarius
(cmd == any) -> bool
```

#### !=

```aquarius
(cmd != any) -> bool
```

#### to_s

```aquarius
(cmd to_s) -> string
```

#### to_b

```aquarius
(cmd to_b) -> true
```

#### type

```aquarius
(cmd type) -> string
```

#### Output
Runs the command and returns its standard output. It returns an `error`, if any.
```aquarius
(cmd Output) -> string
```

#### CombinedOutput
Runs the command and returns its combined standard output and standard error.
It returns an `error`, if any.
```aquarius
(cmd CombinedOutput) -> string
```

#### Run
Starts the specified command and waits for it to complete. It returns an `error`, if any.
```aquarius
(cmd Run) -> nil
```

#### Start
Starts the specified command but does not wait for it to complete.
It returns an `error`, if any.
```aquarius
(cmd Start) -> nil
```

#### Wait
Waits for the command to exit and waits for any copying to stdin or 
copying from stdout or stderr to complete. It returns an `error`, if any.
```aquarius
(cmd Wait) -> nil
```