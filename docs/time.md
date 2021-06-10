Time
-

### The API of `Time` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [ANSIC](#formats)
+ [UnixDate](#formats)
+ [RubyDate](#formats)
+ [RFC822](#formats)
+ [RFC822Z](#formats)
+ [RFC850](#formats) 
+ [RFC1123](#formats)
+ [RFC1123Z](#formats)
+ [RFC3339](#formats)
+ [RFC3339Nano](#formats)
+ [Kitchen](#formats)
+ [Stamp](#formats)
+ [StampMilli](#formats)
+ [StampMicro](#formats)
+ [StampNano](#formats)


### The API of `time` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [format](#format)
+ [clock](#clock)
+ [year](#year)
+ [month](#month)
+ [day](#day)
+ [hour](#hour)
+ [minute](#minute)
+ [second](#second)
+ [nanosecond](#nanosecond)
+ [weekday](#weekday)
+ [date](#date)
+ [iso_week](#iso_week)
+ [zero?](#zero?)
+ [local](#local)
+ [location](#location)
+ [zone](#zone)
+ [unix](#unix)
+ [unix_nano](#unix_nano)
+ [year_day](#year_day)
+ [UTC](#UTC)
+ [add_date](#add_date)
+ [add](#add)
+ [sub](#sub)
+ [round](#round)
+ [truncate](#truncate)
+ [in](#in)
+ [after?](#after?)
+ [before?](#before?)
+ [equal?](#equal?)


#### ==

```aquarius
(Time == any) -> bool
```

#### !=

```aquarius
(Time != any) -> bool
```

#### to_s

```aquarius
(Time to_s) -> string
```

#### to_b

```aquarius
(Time to_b) -> true
```

#### type

```aquarius
(Time type) -> string
```

#### formats

|key|value|
|----|-----|
|ANSIC|Mon Jan _2 15:04:05 2006|
|UnixDate|Mon Jan _2 15:04:05 MST 2006|
|RubyDate|Mon Jan 02 15:04:05 -0700 2006|
|RFC822|02 Jan 06 15:04 MST|
|RFC822Z|02 Jan 06 15:04 -0700|
|RFC850|Monday, 02-Jan-06 15:04:05 MST|
|RFC1123|Mon, 02 Jan 2006 15:04:05 MST|
|RFC1123Z|Mon, 02 Jan 2006 15:04:05 -0700|
|RFC3339|2006-01-02T15:04:05Z07:00|
|RFC3339Nano|2006-01-02T15:04:05.999999999Z07:00|
|Kitchen|3:04PM|
|Stamp|Jan _2 15:04:05|
|StampMilli|Jan _2 15:04:05.000|
|StampMicro|Jan _2 15:04:05.000000|
|StampNano|Jan _2 15:04:05.000000000|

#### format
Returns a textual representation of the time value formatted according to [layout](#formats).
```aquarius
(Time format layout(string)) -> string
```

#### clock
Returns the hour, minute, and second within the day specified by `Time`.
```aquarius
(Time clock) -> [hour(int),min(int),sec(int)]
```

#### year
Returns the year in which `Time` occurs.
```aquarius
(Time year) -> int
```

#### month
Returns the month of the year specified by `Time`.
```aquarius
(Time month) -> [int, string]
```

#### day
Returns the day of the month specified by `Time`.
```aquarius
(Time day) -> int
```

#### hour
Returns the hour within the day specified by `Time`, in the range [0, 23].
```aquarius
(Time hour) -> int
```

#### minute
Returns the minute offset within the hour specified by `Time`, in the range [0, 59].
```aquarius
(Time minute) -> int
```

#### second
Returns the second offset within the minute specified by `Time`, in the range [0, 59].
```aquarius
(Time second) -> int
```

#### nanosecond
Returns the nanosecond offset within the second specified by `Time`, in the range [0, 999999999].
```aquarius
(Time nanosecond) -> int
```

#### weekday
Returns the day of the week specified by `Time`.
```aquarius
(Time weekday) -> [int, string]
```

#### date
Returns the year, month, and day in which `Time` occurs.
```aquarius
(Time date) -> [int, [int, string], int]
```

#### iso_week
Returns the ISO 8601 year and week number in which `Time` occurs. Week ranges from 1 to 53. 
Jan 01 to Jan 03 of year n might belong to week 52 or 53 of year n-1, and Dec 29 to Dec 31 
might belong to week 1 of year n+1.
```aquarius
(Time iso_week) -> [int, int]
```

#### zero?
Reports whether `Time` represents the zero time instant, January 1, year 1, 00:00:00 UTC.
```aquarius
(Time zero?) -> bool
```

#### local
Returns `Time` with the location set to local time.
```aquarius
(Time local) -> time
```

#### location
Returns the time zone information associated with `Time`.
```aquarius
(Time location) -> time
```

#### zone
Computes the time zone in effect at time `Time`, returning the 
abbreviated name of the zone (such as "CET") and its offset 
in seconds east of UTC.
```aquarius
(Time zone) -> [string, int]
```

#### unix
Returns t as a Unix time, the number of seconds elapsed since January 1, 1970 UTC. 
The result does not depend on the location associated with `Time`.
```aquarius
(Time unix) -> int
```

#### unix_nano
Returns `Time` as a Unix time, the number of nanoseconds elapsed since January 1, 1970 UTC.
```aquarius
(Time unix_nano) -> int
```

#### year_day
Returns the day of the year specified by `Time`, in the range [1,365] for non-leap years, 
and [1,366] in leap years.
```aquarius
(Time year_day) -> int
```

#### UTC
Returns `Time` with the location set to UTC.
```aquarius
(Time UTC) -> time
```

#### add_date
Returns `Time` with the location set to UTC.
```aquarius
(Time add_date year(int) month(int) day(int)) -> time
```

#### add
Returns the time `Time`+`dur`.
```aquarius
(Time add dur(duration)) -> time
```

#### sub
returns the duration `Time`-`time`.
```aquarius
(Time sub time(time)) -> duration
```

#### round
Returns the result of rounding `Time` to the nearest multiple of `dur` (since the zero time).
```aquarius
(Time round dur(duration)) -> time
```

#### truncate
Returns the result of rounding `Time` down to a multiple of `dur` (since the zero time).
```aquarius
(Time truncate dur(duration)) -> time
```

#### in
Returns a copy of t representing the same time instant, but with the copy's location information 
set to `loc` for display purposes.
```aquarius
(Time in loc(string)) -> time
```

#### after?
reports whether the time instant `Time` is after `t`.
```aquarius
(Time after? t(time)) -> bool
```

#### before?
reports whether the time instant `Time` is before `t`.
```aquarius
(Time before? t(time)) -> bool
```

#### equal?
reports whether `Time` and `t` represent the same time instant.
```aquarius
(Time equal? t(time)) -> bool
```