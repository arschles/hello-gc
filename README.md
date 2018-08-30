# Hello GopherCon!

We're going to use [Go Modules](https://github.com/golang/go/wiki/Modules) to download a dependency
from a proxy server - not a VCS!

Run this command to do it:

```console
GO111MODULE=on GOPROXY=https://microsoftgoproxy.azurewebsites.net go get github.com/arschles/hello-gc-dep@v1
```

Let's break it down:

- `GO111MODULE=on` tells the `go` toolchain to use the new Go Modules feature
- `GOPROXY` tells the `go` toolchain to download dependencies (AKA modules) from a server, and _not_ from a VCS (version control system, like GitHub)
- `go get github.com/arschles/hello-gc-dep@v1` tells the `go` toolchain to ask the server for `github.com/arschles/hello-gc-dep` at version `v1`
    - Once again, this is not going to the VCS
