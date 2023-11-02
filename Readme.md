# Once

[![Go Reference](https://pkg.go.dev/badge/github.com/livebud/once.svg)](https://pkg.go.dev/github.com/livebud/once)

Utilities for calling functions only once. Safe for concurrent use. Supports generics.

## Install

```sh
go get github.com/livebud/once
```

## Usage

```go
count := 0
fn := once.Func(func() (int, error) {
  count++
  return count, nil
})
res, err := fn()
// 1
res, err = fn()
// 1
```

## Contributors

- Matt Mueller ([@mattmueller](https://twitter.com/mattmueller))

## License

MIT
