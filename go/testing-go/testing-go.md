# go test

## test packages
- [ ] testing
- [ ] testing/quick
- [ ] testing/iotest
- [ ] net/http/httptest

| community project | comments |
| --- | --- |
| [testify](https://github.com/stretchrcom/testify) | assert like |
| [ginkgo](https://github.com/onsi/ginkgo) | behavior-driven-testing |
| [GoConvey](http://goconvey.co) | show result in browser |
| [httpexpect](https://github.com/gavv/httpexpect) | test e2e rest API |
| [gomock](https://github.com/golang/mock) | |
| [go-sqlmock](https://github.com/DATA-DOG/go-sqlmock) | |

- [ ] package_test - black box testing 
- [ ] package - white box testing

## run tests
```
go test
go test ./...
go test -v
go test -run {regexp}

go test -cover
go test -coverprofile cover.out
go tool cover -func cover.out
go tool cover -html cover.out

go test -coverprofile count.out -covermode count
```

## useful test functions
- [ ] Log / Logf
- [ ] Helper
- [ ] Skip / Skipf / SkipNow
- [ ] Run
- [ ] Parallel

## benchmark test
```
func BenchmarkSHA1(b *testing.B) {
    data := []byte("this is a simple string")
    b.StartTimer()
    for i := 0; i < b.N; i++ {
        sha1.Sum(data)
    }
}
```

```
b.N
b.StartTimer
b.StopTimer
b.ResetTimer
b.RunParallel
```

```
go test -bench .
go test -bench . -benchtime 10s

go test -benchmem
go test -trace {trace.out}
go test -bench -{type}profile {file}
    block / cover / cpu / mem / mutex

go test -bench -memprofile profile.out

go tool pprof profile.out
    svg
    https://graphviz.org/download/
```



