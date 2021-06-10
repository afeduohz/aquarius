time
-

This module wrappers the Go package time.

### The API of `time` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [now](#now)
+ [parse](#parse)
+ [parse_in_location](#parse_in_location)
+ [unix](#unix)
+ [date](#date)
+ [parse_duration](#parse_duration)
+ [until](#until)
+ [since](#since)
+ [sleep](#sleep)
+ [timer](#timer)
+ [ticker](#ticker) 


#### ==

```aquarius
(time == any) -> bool
```

#### !=

```aquarius
(time != any) -> bool
```

#### to_s

```aquarius
(time to_s) -> string
```

#### to_b

```aquarius
(time to_b) -> true
```

#### type

```aquarius
(time type) -> string
```

#### now

Returns the current local time.

```aquarius
(time now) -> Time
```

#### parse

Parses a formatted string and returns the time value it represents.

```aquarius
(time parse {layout}string {value}string) -> Time
```

#### parse_in_location

Like [parse](#parse), but need one more parameter `localtion`.

`location` is formatted string like `Europe/Berlin`, `Asia/Shanghai`.

```aquarius
(time parse_in_location {layout}string {value}string {location}string) -> Time
```

#### unix

Returns the local Time corresponding to the given Unix time, `sec` seconds 
and `nsec` nanoseconds since January 1, 1970 UTC. It is valid to pass `nsec` 
outside the range [0, 999999999]. Not all `sec` values have a corresponding 
[Time](./time.md) value. One such value is 1<<63-1 (the largest [Int](./int.md) value).

```aquarius
(time unix {sec}int {nsec}int) -> Time
```

#### date

Returns the Time corresponding to
```aquarius
yyyy-mm-dd hh:mm:ss + nsec nanoseconds
```
in the appropriate zone for that time in the given location.

```aquarius
(time date {year}int {month}int {day}int {hour}int {min}int {sec}int {nsec}int {location}string) -> Time
```

#### parse_duration

Parses a `duration` string. A duration string is a possibly signed sequence of decimal 
numbers, each with optional fraction and a unit suffix, such as "300ms", "-1.5h" or 
"2h45m". Valid time units are "ns", "us" (or "µs"), "ms", "s", "m", "h".

```aquarius
(time parse_duration {duration}string) -> duration
```

#### until

Returns the duration until `t`.

```aquarius
(time until {t}time) -> duration
```

#### since

Returns the time elapsed since `t`.

```aquarius
(time since {t}time) -> duration
```

#### sleep

Pauses the current goroutine for at least the duration `dur`. A negative or zero 
duration causes sleep to return immediately.

```aquarius
(time sleep {dur}duration) -> nil
```

#### timer

Creates a new time/Timer.

```aquarius
(time timer {dur}duration) -> timer
```

#### ticker

Returns a new time/Ticker. The period of the ticks is specified by the `dur` argument. 
The ticker will adjust the time interval or drop ticks to make up for slow receivers. 
The duration `dur` must be greater than zero; if not, `ticker` will raise an error.

```aquarius
(time ticker {dur}duration) -> timer
```