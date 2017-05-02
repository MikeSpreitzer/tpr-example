# Intro

Cloned from https://github.com/yvespp/tpr-example and updated to work
with https://github.com/kubernetes/client-go commit
623dbc3dc4e22ddd57b7d1d73b9afa9c9448e8f5 (which was master on or about
April 24, 2017) and apimachinery commit
22062ea7ff0c73d5114c07ad4a0875c15a8a9826.

Following is a summary of the changes.

* Removed the vendoring.  That makes this fragile.  I am new to Go
  development and am looking for suggestions of the right way to fix
  this.

* Mostly changing import statements, but also a few bits of actual
  code had to change which imported package they refer to.

* I introduced an import and use of `glog`.

* Added an explanation, and printing of request and response details,
  in the common case of panics --- which is the known (see client-go
  issue #95) delay between defining a new Kind of object and being
  able to use that Kind.

* I also extended the function that pretty-prints an `Example` value.

* I also slowed down the resync frequency in the informer.
