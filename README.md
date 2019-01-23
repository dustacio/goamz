# goamz - An Amazon Library for Go

[![Build Status](http://travis-ci.org/dustacio/goamz.png?branch=master)](https://travis-ci.org/dustacio/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services. 

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/dustacio/goamz/contributors)! Currently this fork is no longer actively maintained and users are advised to switch to the [official AWS supported Golang SDK](https://github.com/aws/aws-sdk-go)

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/dustacio/goamz/autoscaling
github.com/dustacio/goamz/aws
github.com/dustacio/goamz/cloudformation
github.com/dustacio/goamz/cloudfront
github.com/dustacio/goamz/cloudwatch
github.com/dustacio/goamz/dynamodb
github.com/dustacio/goamz/ecs
github.com/dustacio/goamz/ec2
github.com/dustacio/goamz/elb
github.com/dustacio/goamz/iam
github.com/dustacio/goamz/rds
github.com/dustacio/goamz/route53
github.com/dustacio/goamz/s3
github.com/dustacio/goamz/sqs
github.com/dustacio/goamz/sts

github.com/dustacio/goamz/exp/mturk
github.com/dustacio/goamz/exp/sdb
github.com/dustacio/goamz/exp/sns
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/dustacio/goamz](http://godoc.org/github.com/dustacio/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/dustacio/goamz/ec2`
* `$ go get github.com/dustacio/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get gopkg.in/check.v1`

Then run go test as usual:

`$ go test github.com/dustacio/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

$ gotest -i
