http
-

### The API of `http` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [get](#get)
+ [post](#post)
+ [post_form](#post_form)
+ [post_json](#post_json)
+ [put_form](#put_form)
+ [put_json](#put_json)
+ [patch_form](#patch_form)
+ [patch_json](#patch_json)
+ [delete](#delete)
+ [head](#head)
+ [options](#options)


#### ==

```aquarius
(http == any) -> bool
```

#### !=

```aquarius
(http != any) -> bool
```

#### to_s

```aquarius
(http to_s) -> string
```

#### to_b

```aquarius
(http to_b) -> true
```

#### type

```aquarius
(http type) -> string
```

#### get
Send a http `GET` request with [http/Query](lib-http-query.md) optionally, and return a [http/Response](lib-http-response.md).
```aquarius
(http get url(string) [query(query)]) -> response
```

#### post
Send a http `POST` request with `any` data, and return a [http/Response](lib-http-response.md).
```aquarius
(http post url(string) data(any)) -> response
```

#### post_form
Send a http `POST` request with [http/Query](lib-http-query.md), and return a [http/Response](lib-http-response.md).
Header entity `Content-Type`: `application/x-www-form-urlencoded` is attached.
```aquarius
(http post_form url(string) data(query)) -> response
```

#### post_json
Send a http `POST` request with `any` data that will be encoded as `json`, and return a [http/Response](lib-http-response.md).
Header entity `Content-Type`: `application/json` is attached.
```aquarius
(http post_json url(string) data(query)) -> response
```

#### put_form
Send a http `PUT` request with [http/Query](lib-http-query.md), and return a [http/Response](lib-http-response.md).
Header entity `Content-Type`: `application/x-www-form-urlencoded` is attached.
```aquarius
(http put_form url(string) data(query)) -> response
```

#### put_json
Send a http `PUT` request with `any` data that will be encoded as `json`, and return a [http/Response](lib-http-response.md).
Header entity `Content-Type`: `application/json` is attached.
```aquarius
(http put_json url(string) data(query)) -> response
```

#### patch_form
Send a http `PATCH` request with [http/Query](lib-http-query.md), and return a [http/Response](lib-http-response.md).
Header entity `Content-Type`: `application/x-www-form-urlencoded` is attached.
```aquarius
(http path_form url(string) data(query)) -> response
```

#### patch_json
Send a http `PATCH` request with `any` data that will be encoded as `json`, and return a [http/Response](lib-http-response.md).
Header entity `Content-Type`: `application/json` is attached.
```aquarius
(http patch_json url(string) data(query)) -> response
```

#### delete
Send a http `DELETE` request, and return a [http/Response](lib-http-response.md).
```aquarius
(http delete url(string)) -> response
```

#### head
Send a http `HEAD` request, and return a [http/Response](lib-http-response.md).
```aquarius
(http head url(string)) -> response
```

#### options
Send a http `OPTIONS` request, and return a [http/Response](lib-http-response.md).
```aquarius
(http options url(string)) -> response
```