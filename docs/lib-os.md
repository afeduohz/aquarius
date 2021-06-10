os
-

### The API of `os` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [stdin](#stdin)
+ [stdout](#stdout)
+ [stderr](#stderr)
+ [platform](#platform)
+ [arch](#arch) 
+ [exit](#exit)
+ [get_env](#get_env)
+ [get_env_ex](#get_env_ex)
+ [set_env](#set_env)
+ [unset_env](#unset_env)
+ [clear_env](#clear_env)
+ [environ](#environ)
+ [user_home_dir](#user_home_dir)
+ [user_config_dir](#user_config_dir)
+ [user_cache_dir](#user_cache_dir)
+ [hostname](#hostname)
+ [uid](#uid)
+ [gid](#gid)
+ [euid](#euid)
+ [egid](#egid)
+ [groups](#groups)
+ [start_process](#start_process)
+ [find_process](#find_process)


#### ==

```aquarius
(os == any) -> bool
```

#### !=

```aquarius
(os != any) -> bool
```

#### to_s

```aquarius
(os to_s) -> string
```

#### to_b

```aquarius
(os to_b) -> true
```

#### type

```aquarius
(os type) -> string
```

#### stdin
open [File](./file.md) pointing to the standard input file descriptor.
```aquarius
(os stdin) -> file
```

#### stdout
open [File](./file.md) pointing to the standard output file descriptor.
```aquarius
(os stdout) -> file
```

#### stderr
open [File](./file.md) pointing to the standard error file descriptor.
```aquarius
(os stderr) -> file
```

#### platform 
it is `runtime.GOOS` in Golang.
```aquarius
(os platform) -> string
```

#### arch 
it is `runtime.GOARCH` in Golang.
```aquarius
(os arch) -> string
```

#### exit
exit causes the current program to exit with the given status code. Conventionally, 
code zero indicates success, non-zero an error. The program terminates immediately, 
`finally` sub-expression in `try` will not execute.
```aquarius
(os exit code(int)) -> nil
```

#### get_env
Return the value of the environment variable named by the `key`. It returns the value, 
which will be empty if the variable is not present.
```aquarius
(os get_env key(string)) -> string
```

#### get_env_ex
Return a 2-element list value of the environment variable named by the `key` and bool 
value which indicate whether the `key` exists. 
```aquarius
(os get_env_ex key(string)) -> [string,bool]
```

#### set_env
Sets the value of the environment variable named by the `key`. It returns an `error`, if any.
```aquarius
(os set_env key(string) val(string)) -> nil
```

#### unset_env
Unsets a single environment variable. It returns an `error`, if any.
```aquarius
(os unset_env key(string)) -> nil
```

#### clear_env
Deletes all environment variables.
```aquarius
(os clear_env) -> nil
```

#### environ
Returns a dict of strings representing the environment.
```aquarius
(os environ) -> dict
```

#### user_home_dir
Returns the current user's home directory. It returns an `error`, if any.
```aquarius
(os user_home_dir) -> string
```

#### user_config_dir
Returns the default root directory to use for user-specific 
configuration data. Users should create their own application-specific 
subdirectory within this one and use that. It returns an `error`, if any.
```aquarius
(os user_config_dir) -> string
```

#### user_cache_dir
Returns the default root directory to use for user-specific cached data. 
Users should create their own application-specific subdirectory within 
this one and use that. It returns an `error`, if any.
```aquarius
(os user_cache_dir) -> string
```

#### hostname
Returns the host name reported by the kernel. It returns an `error`, if any.
```aquarius
(os hostname) -> string
```

#### uid
Returns the numeric user id of the caller.
```aquarius
(os uid) -> int
```

#### gid
Returns the numeric group id of the caller.
```aquarius
(os gid) -> int
```

#### euid
Returns the numeric effective user id of the caller.
```aquarius
(os euid) -> int
```

#### egid
Returns the numeric effective group id of the caller.
```aquarius
(os egid) -> int
```

#### groups
Returns a list of the numeric ids of groups that the caller belongs to. 
It returns an `error`, if any.
```aquarius
(os groups) -> [int...]
```

#### start_process

Starts a new process with the program, arguments and 
attributes specified by name, args.

```aquarius
(os start_process name(string) args(any)...) -> process
```

#### find_process

Looks for a running process by its `pid`.

```aquarius
(os find_process pid(int)) -> process
```