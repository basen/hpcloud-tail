[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=basen_hpcloud-tail&metric=alert_status)](https://sonarcloud.io/dashboard?id=basen_hpcloud-tail)

# Go package for tail-ing files

A Go package striving to emulate the features of the BSD `tail` program. 

```Go
t, err := tail.TailFile("/var/log/nginx.log", tail.Config{Follow: true})
for line := range t.Lines {
    fmt.Println(line.Text)
}
```

See [API documentation](http://godoc.org/github.com/hpcloud/tail).

## Log rotation

Tail comes with full support for truncation/move detection as it is
designed to work with log rotation tools.

## Installing

    go get github.com/hpcloud/tail/...

## Windows support

This package [needs assistance](https://github.com/hpcloud/tail/labels/Windows) for full Windows support.
