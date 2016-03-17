---
layout: post
title: Kaa: a toy Lisp implementation in Python
---

Disclaimer: I've never implemented a Lisp before, so lots or all of this will
probably seem naive and silly to more experienced Lispers.

I took some from Clojure, and some from Common Lisp, depending on ease of
implementation.

For example, given this Clojure-style function:
```
(defn do-something
  ([foo] (do-something-with-only-foo))
  ([foo bar] (do-something-with-foo-and-bar)))
```
and this roughly equivalent CL-style function:
```
(defun do-something (foo &optional bar)
  (if bar
      (do-something-with-foo-and-bar)
    (do-something-with-only-foo)))
```
it was easier to implement the latter, and so I did that.

This is an interpreted language. There is no "compilation" step. E.g. macro
forms in the body of a lambda are expanded on every invocation of that lambda.
Exceptions to this include the quasiquote/unquote operators, which are rolled
into the reader for ease of implementation.
