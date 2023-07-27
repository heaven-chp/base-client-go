# base-client-go

## How to add config
 - json type config file add
   - see [config/Sample.config](https://github.com/heaven-chp/base-client-go/blob/main/config/Sample.config)
 - struct add
   - see [config/Sample.go](https://github.com/heaven-chp/base-client-go/blob/main/config/Sample.go)
 - test add
   - see [Sample_test.go](https://github.com/heaven-chp/base-client-go/blob/main/config/Sample_test.go)
 - example of use
   - socketClientConfig of [socket-client/main.go](https://github.com/heaven-chp/base-client-go/blob/main/socket-client/main.go)

<br/>

## How to use client
 - prepare
   - run
     - server must be running
       - [How to use server](https://github.com/heaven-chp/base-server-go#how-to-use-server)
 - grpc
   - build
     - `go build -o ./bin/grpc-client ./grpc-client/`
   - run
     - `./bin/grpc-client -config_file ./config/GrpcClient.config`
   - log
     - `./log/grpc-client_YYYYMMDD.log`
 - socket
   - build
     - `go build -o ./bin/socket-client ./socket-client/`
   - run
     - `./bin/socket-client -config_file ./config/SocketClient.config`
   - log
     - `./log/socket-client_YYYYMMDD.log`

<br/>

## Test and Coverage
 - Test
   - `go clean -testcache && go test -cover ./...`
 - Coverage
   - make coverage file
     - `go clean -testcache && go test -coverprofile=coverage.out -cover ./...`
   - convert coverage file to html file
     - `go tool cover -html=./coverage.out -o ./coverage.html`
