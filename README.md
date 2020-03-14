# git autotag

forked from github.com/calmh/git-autotag
improve some features:
+ get the closest tag
+ if the commit of the closest tag is the same current commit -> return ''

## Installation

Get and compile it using Go:

```go get github.com/nvhoc/git-autotag```


## Usage

```
$ git describe
v0.11.18-3-gb1dd704
$ git autotag
v0.11.19
$ git describe
v0.11.19
$ git autotag -l minor
v0.12.0
$ git config autotag.sign true
$ git config user.signingkey release@syncthing.net
$ git autotag -l patch
v0.12.1

You need a passphrase to unlock the secret key for
user: "Syncthing Release Management <release@syncthing.net>"
2048-bit RSA key, ID D26E6ED000654A3E, created 2014-12-29

$ 
```

