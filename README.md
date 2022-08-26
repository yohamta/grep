# grep

[![codecov](https://codecov.io/gh/yohamta/grep/branch/main/graph/badge.svg)](https://codecov.io/gh/yohamta/grep)
[![GoDoc](https://pkg.go.dev/badge/github.com/yohamta/grep)](https://pkg.go.dev/github.com/yohamta/grep)

The grep searches given pattern in given file and returns matched lines.

## Usage

```go

import "github.com/yohamta/grep"

opts := &grep.Options{
  IsRegexp: true,
  Before:   2,
  After:    2,
}

matches, err := grep.Grep("target_file.txt", fmt.Sprintf("(?i)%s", pattern), opts)

for _, m := range matches {
  println(fmt.Sprintf("Matched Line: %s", m.Line))
  println(fmt.Sprintf("Line Number: %s", m.LineNumber))
  println(fmt.Sprintf("Start Line: %s", m.StartLine))
}
```

# License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
