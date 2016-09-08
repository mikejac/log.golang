# Go - Log
## Introduction
Yet another log package for Go :-) This one however, is very simplistic. It only implements to types: INFO and DEBUG. They idea behind it based on [Dave Cheney's blog](http://dave.cheney.net/2015/11/05/lets-talk-about-logging). In essence:


>I believe that there are only two things you should log:

>Things that developers care about when they are developing or debugging software.
Things that users care about when using your software.
Obviously these are debug and info levels, respectively.

>log.Info should simply write that line to the log output. There should not be an option to turn it off as the user should only be told things which are useful for them. If an error that cannot be handled occurs, it should bubble up main.main where the program terminates. The minor inconvenience of having to insert the FATAL prefix in front of the final log message, or writing directly to os.Stderr with fmt.Fprintf is not sufficient justification for a logging package growing a log.Fatal method.

>log.Debug, is an entirely different matter. It is for the developer or support engineer to control. During development, debugging statements should be plentiful, without resorting to trace or debug2 (you know who you are) level. The log package should support fine grained control to enable or disable debug, and only debug, statements at the package or possibly even finer scope.

That part about *fine grained control* is not (at least not yet) implemented in this package.
## The Code
This package is 99.9% based on Googles ```glog``` package.
## Get The Files
```
go get github.com/mikejac/log.golang
```