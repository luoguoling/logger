# Simple level logging package.

```go
package main

import (
	"log"
	"os"
	"runtime"

	"github.com/chai2010/logger"
)

func main() {
	var logger = logger.NewStdLogger(os.Stderr, "", log.Lshortfile)

	logger.SetLevel("DEBUG")
	logger.Debug(runtime.Version())
	logger.Info("hello")
}
```

Output:

```
hello.go:21: [DEBUG] go1.10
hello.go:22: [INFO] hello
```
