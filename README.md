It works with `go test`
```bash
$ go test ./...
ok     	github.com/rosenhouse/ginkgo-build-flags-issue/integration     	0.012s
?      	github.com/rosenhouse/ginkgo-build-flags-issue/program 	[no test files]

$ echo $?
0
```

But it doesn't work with `ginkgo`
```bash
$ ginkgo -r
[1473748507] Integration Suite - 1/1 specs • SUCCESS! 52.654µs PASS
Failed to compile program: output file "/var/folders/fk/2jkck0n96_d1g6w3jlv_cm5r0000gn/T/ginkgo126282887/program.test" could not be found
Ginkgo ran 2 suites in 1.142344381s
Test Suite Failed
$ echo $?
1
```
