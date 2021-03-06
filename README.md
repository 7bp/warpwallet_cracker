# warpwallet_cracker
A brute-force cracker in Go for the WarpWallet Challenge 2: https://keybase.io/warp/

# Usage

```
$ go get ./...
---
$ go build warpwallet_cracker.go
---
$ ./run.sh 
Using address "1MkupVKiCik9iyfnLrJoZLx9RH4rkF3hnA" and salt "a@b.c"
Tried 4 passphrases in 2.269448485s [last passphrase: 2zZM3L1C]
```

# Performance
On a consumer MacBook Pro this achieves ~1.1 hash/sec. At this hashrate it is [not feasible](https://www.wolframalpha.com/input/?i=(62%5E8+%2F+1.1)+seconds+to+years) to enumerate the entire keyspace of 62^8 hashes.

# How-to
Build:

`go build warpwallet_cracker.go`

Params:

`./warpwallet_cracker [Address] [Salt - optional]`

Run (Windows):

`run.bat`

Run (*nix):

`./run.sh`

Run unit tests and benchmark:

`go test -bench=.`
