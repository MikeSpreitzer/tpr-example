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

* I also added logging before each panic, I was getting no info on panics.

* I also extended the function that pretty-prints an `Example` value.

* I also slowed down the resync frequency in the informer.

* I introduced an import and use of `glog`.
