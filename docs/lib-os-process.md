os/Process
-

### The API of `os/Process` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)

### The API of `os/Process` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [release](#release)
+ [kill](#kill)
+ [wait](#wait)
+ [signal](#signal)

#### ==

```aquarius
(proc == any) -> bool
```

#### !=

```aquarius
(proc != any) -> bool
```

#### to_s

```aquarius
(proc to_s) -> string
```

#### to_b

```aquarius
(proc to_b) -> true
```

#### type

```aquarius
(proc type) -> string
```

#### release

Releases any resources associated with the `proc`.

```aquarius
(proc release) -> nil
```

#### kill

Kill causes the `proc` to exit immediately.

```aquarius
(proc kill) -> nil
```

#### wait

Waits for the `proc` to exit, and then returns a 
[os/ProcessState](lib-os-processstate.md) describing its status.

```aquarius
(proc wait) -> state
```

#### signal

Sends a signal to the Process.

|Signal|Desc|
|----|----|
|SIGABRT|0x6|
|SIGALRM|0xe|
|SIGBUS|0xa|
|SIGCHLD|0x14|
|SIGCONT|0x13|
|SIGEMT|0x7|
|SIGFPE|0x8|
|SIGHUP|0x1|
|SIGILL|0x4|
|SIGINFO|0x1d|
|SIGINT|0x2|
|SIGIO |0x17|
|SIGIOT|0x6|
|SIGKILL|0x9|
|SIGPIPE|0xd|
|SIGPROF|0x1b|
|SIGQUIT|0x3|
|SIGSEGV|0xb|
|SIGSTOP|0x11|
|SIGSYS|0xc|
|SIGTERM|0xf|
|SIGTRAP|0x5|
|SIGTSTP|0x12|
|SIGTTIN|0x15|
|SIGTTOU|0x16|
|SIGURG|0x10|
|SIGUSR1|0x1e|
|SIGUSR2|0x1f|
|SIGVTALRM|0x1a|
|SIGWINCH|0x1c|
|SIGXCPU|0x18|
|SIGXFSZ|0x19|


```aquarius
(proc signal s(string)) -> nil
```
