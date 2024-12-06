# sui

`sui` is an HTTP server for the [Neut](https://vekatze.github.io/neut/) programming language.

```sh
neut get sui https://github.com/vekatze/sui/raw/main/archive/0-1-29.tar.zst
```

## Types

```neut
// The definition of an HTTP server
data server {
| Server(
    address: &text,
    number-of-threads: int,
    port: int16,
    act: (request) -> response,
  )
}

// Starts an HTTP server
inline serve(s: server): unit
```

## Example

```sh
# see source/test.nt
neut build test --execute

# from another terminal
curl -X POST --silent "http://127.0.0.1:8080/foo/bar/buz" -d "whatever"

# => {"body-byte-length": 8}
```
