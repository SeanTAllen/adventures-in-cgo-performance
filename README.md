# Adventures in Cgo Performance

## Abstract

Cgo is a powerful tool in the Go programmer’s arsenal. It allows Go programmers to interoperate with other languages. However, Cgo documentation is scarce and best practices for performance are hard to come by. In this tutorial session, I discuss lessons I've has learned working on the Go API for [Wallaroo](https://github.com/wallaroolabs/wallaroo), a high-performance distributed stream processor written in Pony.

I cover hard-won knowledge about using Cgo in performance sensitive code including: ways in which Cgo makes interoperation with other languages difficult, how you can work around common sources of performance and scaling problems, and an issue with the Go runtime that can't be worked around.

## Versions of this talk

* GopherCon 2018 - [Slides]()

## Links

* [Wallaroo](https://github.com/wallaroolabs/wallaroo)
* [Wallaroo Labs' Twitter](https://twitter.com/wallaroolabs)
* [My Twitter](https://twitter.com/seantallen)
* [My Personal Website](https://www.monkeysnatchbanana.com/)
* [Pony](https://www.ponylang.org/)
* [Pony Twitter](https://twitter.com/ponylang)

## Blog posts by me on cgo

* [Adventures with cgo: Part 1- The Pointering](https://blog.wallaroolabs.com/2018/04/adventures-with-cgo-part-1--the-pointering/)
* [Adventures with cgo: Part 2- Locks and other things that go bump in the night](https://blog.wallaroolabs.com/2018/04/adventures-with-cgo-part-2--locks-and-other-things-that-go-bump-in-the-night/)

## Wallaroo references

* [Wallaroo](https://github.com/wallaroolabs/wallaroo)
* [Wallaroo Go API introduction](https://blog.wallaroolabs.com/2018/01/go-go-go-stream-processing-for-go/)
* [Wallaroo Word Count example](https://github.com/WallarooLabs/wallaroo/tree/3b9446807df1ca34ba7171e07b0409d531bff26d/examples/go/word_count)

## Learning cgo references

* [Golang website's cgo overview](https://golang.org/cmd/cgo/)
* [cgo is not Go](https://dave.cheney.net/2016/01/18/cgo-is-not-go)
* [The cost and complexity of cgo](https://www.cockroachlabs.com/blog/the-cost-and-complexity-of-cgo/)
* [cgo: Passing Pointers](https://golang.org/cmd/cgo/#hdr-Passing_pointers)

## Additional References

* [Copying Garbage Collection](http://www.cs.cornell.edu/courses/cs312/2003fa/lectures/sec24.htm)
* [Go Atomic Package](https://golang.org/pkg/sync/atomic/)
* [RWMutex scales poorly with CPU count](https://github.com/golang/go/issues/17973)
* [DRWMutex vs RWMutex benchmark](https://github.com/jonhoo/drwmutex/)
* [Wallaroo Concurrent Map](https://github.com/WallarooLabs/wallaroo/blob/e0953b6326327dff9f5f34d23239ec95e568e514/go_api/go/src/wallarooapi/concurrent_map.go)
* [runtime/proc.go line 1771](https://golang.org/src/runtime/proc.go#L1771)
* [Pony](https://www.ponylang.org/)
* [FFI](https://en.wikipedia.org/wiki/Foreign_function_interface)
