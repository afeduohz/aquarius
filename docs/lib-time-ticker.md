time/Ticker
-

### The API of `time/Ticker` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)

### The API of `time/Ticker` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [>>](#>>)


#### ==

```aquarius
(time/Ticker == any) -> bool
```

#### !=

```aquarius
(time/Ticker != any) -> bool
```

#### to_s

```aquarius
(time/Ticker to_s) -> string
```

#### to_b

```aquarius
(time/Ticker to_b) -> true
```

#### type

```aquarius
(time/Ticker type) -> string
```

#### \>>

`lambda` will be executed with [Time](./Time.md) value as the first parameter, 
in every [Duration](./lib-time-duration.md) of time/Ticker. If you want to exit 
the loop calling, let `lambda` return `true`.

```aquarius
(time/Ticker >> lambda) -> nil
```