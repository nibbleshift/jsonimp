# jsonimp

# Overview

Provide a json module that has a `encoding/json` compatible interface that allows you to use a more optimal json on backend such as go-json, sonic, etc


# Example
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
