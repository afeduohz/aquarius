time/Duration
-

### The API of `time/Duration` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type) 
+ [Nanosecond](#Nanosecond)
+ [Microsecond](#Microsecond)
+ [Millisecond](#Millisecond)
+ [Second](#Second)
+ [Minute](#Minute)
+ [Hour](#Hour)

### The API of `time/Duration` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [nanoseconds](#nanoseconds)
+ [microseconds](#microseconds)
+ [milliseconds](#milliseconds)
+ [seconds](#seconds)
+ [minutes](#minutes)
+ [hours](#hours)
+ [round](#round)
+ [truncate](#truncate)


#### ==

```aquarius
(time/Duration == any) -> bool
```

#### !=

```aquarius
(time/Duration != any) -> bool
```

#### to_s

```aquarius
(time/Duration to_s) -> string
```

#### to_b

```aquarius
(time/Duration to_b) -> true
```

#### type

```aquarius
(time/Duration type) -> string
```


#### Nanosecond

Create a time/Duration value, `int` is 1 as default.

```aquarius
(time/Duration Nanosecond [int]) -> duration
```

#### Microsecond

Create a time/Duration value, `int` is 1 as default.

```aquarius
(time/Duration Microsecond [int]) -> duration
```

#### Millisecond

Create a time/Duration value, `int` is 1 as default.

```aquarius
(time/Duration Millisecond [int]) -> duration
```

#### Second

Create a time/Duration value, `int` is 1 as default.

```aquarius
(time/Duration Second [int]) -> duration
```

#### Minute

Create a time/Duration value, `int` is 1 as default.

```aquarius
(time/Duration Minute [int]) -> duration
```

#### Hour

Create a time/Duration value, `int` is 1 as default.

```aquarius
(time/Duration Hour [int]) -> duration
```

#### nanoseconds

Returns the duration as an integer nanosecond count.

```aquarius
(time/Duration nanoseconds) -> int
```

#### microseconds

Returns the duration as an integer microsecond count.

```aquarius
(time/Duration microseconds) -> int
```

#### milliseconds

Returns the duration as an integer millisecond count.

```aquarius
(time/Duration milliseconds) -> int
```

#### seconds

Returns the duration as a floating point number of seconds.

```aquarius
(time/Duration seconds) -> float
```

#### minutes

Returns the duration as a floating point number of minutes.

```aquarius
(time/Duration minutes) -> float
```

#### hours

Returns the duration as a floating point number of hours.

```aquarius
(time/Duration hours) -> float
```

#### round

Returns the result of rounding `time/Duration` to the nearest multiple of 
`duration`. The rounding behavior for halfway values is to round away from 
zero. If the result exceeds the maximum (or minimum) value that can be stored 
in a Duration, round returns the maximum (or minimum) duration. 
If `duration` <= 0, round returns `time/Duration` unchanged.

```aquarius
(time/Duration round duration) -> duration
```

#### truncate

Returns the result of rounding `time/Duration` toward zero to a multiple of 
`duration`. If `duration` <= 0, truncate returns `time/Duration` unchanged.

```aquarius
(time/Duration truncate duration) -> duration
```