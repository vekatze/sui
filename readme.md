# sui

`sui` is a HTTP server for Neut.

```sh
neut get sui https://github.com/vekatze/sui/raw/main/archive/0-1-18.tar.zst
```

## Exampl

```sh
# see source/test.nt
neut build --execute

# from another terminal
curl -X POST --silent "http://127.0.0.1:8000/foo/bar/buz" -d "whatever"

# => {"body-byte-length": 8}
```
