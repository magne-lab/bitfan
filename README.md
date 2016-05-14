# logstack

Logstash in GO.

## QuickStart with a configfile
```
$ go get -u github.com/vjeantet/logstack
$ logstack -f $GOPATH/src/github.com/vjeantet/logstack/examples.d/simple.conf
```

now paste this in your console

```127.0.0.1 - - [11/Dec/2013:00:01:45 -0800] "GET /xampp/status.php HTTP/1.1" 200 3891 "http://cadenza/xampp/navi.php" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:25.0) Gecko/20100101 Firefox/25.0"```

### TODO

- [x] parse logstash config file
- [x] generic input support
- [x] generic filter support
- [x] generic output support
- [x] configuration condition (if else) support
- [x] dynamic %{field.key} support in config file
- [x] gracefully stop
- [x] gracefully start
- [x] name all contributors, imported packages, similar projects
- [ ] codec support
- [ ] log to file



# supported inputs, filters and outputs 
can be found here : https://github.com/veino/processors

## input
* beats
* exec
* file
* stdin
* twitter

## filter
* date
* drop
* grok
* json
* mutate
* split
* uuid

## output
* elasticsearch
* mongodb
* null
* stdout

## Used package
* spf13/cobra - A Commander for modern Go CLI interactions
* kardianos/govendor Go vendor tool that works with the standard vendor file
* bbuck/go-lexer (a forked version) - Lexer based on Rob Pike's talk on YouTube
* veino/processors - all plugins used in logstack 

## Similar projets in go

* tsaikd/gogstash - Logstash like, written in golang
* packetzoom/logzoom - A lightweight replacement for logstash indexer in Go
* hailocab/logslam - A lightweight lumberjack protocol compliant logstash indexer

