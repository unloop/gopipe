gopipe
=======
  
Golang pipe http response
  
## Installation and usage
 
The import path for the package is github.com/unloop/gopipe.
  
To install it, run: `go get unloop/gopipe`
  
## Example
  
```go
package main

import (
  "github.com/unloop/gopipe"
  "net/http"
  "io"
)


func handler(w http.ResponseWriter, r *http.Request) {

  var readCloser io.ReadCloser

  /* do something */

  defer readCloser.Close()
	
  /* do something */

  stream.New(w).SetBuffer(2048).Pipe(&readCloser)

  return
}

func main() {
  http.HandleFunc("/", handler)
  http.ListenAndServe(":3000", nil)
}
```
