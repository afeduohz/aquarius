http/Client
-

### The API of `http/Client` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [http](#http)
+ [https](#https)

### The API of `http/Client` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [proxy](#proxy)
+ [ttl](#ttl)
+ [do](#do)


#### ==

```aquarius
(http/Client == any) -> bool
```

#### !=

```aquarius
(http/Client != any) -> bool
```

#### to_s

```aquarius
(http/Client to_s) -> string
```

#### to_b

```aquarius
(http/Client to_b) -> true
```

#### type

```aquarius
(http/Client type) -> string
```


#### http

Returns a `http` client.

```aquarius
(http/Client http) -> client
```

#### https

Return a `https` client.

```aquarius
(http/Client https certfilepath(string) keyfilepath(string)) -> client
```

#### proxy

Set the `proxy` of request. Return itself, or an `error`, if any.

```aquarius
(client proxy url(string)) -> self
```

#### ttl

Set the `TTL` of request. Return itself, or an `error`, if any.

```aquarius
(client ttl dur(duration)) -> self
```

#### do

Sends [http/Request](lib-http-request.md) and returns
[http/Response](lib-http-response.md), or an `error`, if any.

```aquarius
(client do request(request)) -> response
```