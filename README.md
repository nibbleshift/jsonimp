# jsonimp

# Overview

Provide a json module that has a `encoding/json` compatible interface that allows you to use a more optimal json on backend such as go-json, sonic, etc


# Example

On amd64 systems, this code will automatically use [Sonic](https://github.com/bytedance/sonic) to parse JSON.  
```go
package main

import (
  "fmt"
  json "github.com/nibbleshift/jsonimp"
)

func main() {

  a, err := json.Marshal([]string{"foo", "bar", "baz"})

  if err != nil {
    fmt.Println(err)
    return
   }
   fmt.Println(string(a))
}

```


# TODO

- [ ] Add feature flag for sonic
- [ ] Add feature flag for go-json
- [ ] Add feature flag for encoding/json
- [ ] Add default for amd64 (sonic)
- [ ] Add default for arm64 (go-json)
- [ ] Add additional usage documentation
- [ ] Implement generic tests for all available json implementations.
- [ ] Implement benchmarks for all available json implementations.
