os/ProcessState
-

### The API of `os/ProcessState` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)

### The API of `os/ProcessState` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [pid](#pid)
+ [exited?](#exited?)
+ [success?](#success?)
+ [system_time](#system_time)
+ [user_time](#user_time)

#### ==

```aquarius
(state == any) -> bool
```

#### !=

```aquarius
(state != any) -> bool
```

#### to_s

```aquarius
(state to_s) -> string
```

#### to_b

```aquarius
(state to_b) -> true
```

#### type

```aquarius
(state type) -> string
```

#### pid

Returns the process id of the exited process.

```aquarius
(state pid) -> pid
```

#### exited?

Reports whether the program has exited.

```aquarius
(state exited?) -> bool
```

#### success?

Reports whether the program exited successfully, 
such as with exit status 0 on Unix.

```aquarius
(state success?) -> bool
```

#### system_time

Returns the system CPU time [time/Duration](lib-time-duration.md) of
the exited process and its children.

```aquarius
(state system_time) -> duration
```

#### user_time

Returns the user CPU time [time/Duration](lib-time-duration.md) of 
the exited process and its children.

```aquarius
(state user_time) -> duration
```
