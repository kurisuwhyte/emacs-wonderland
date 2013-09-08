Wonderland
==========

[![Build Status](https://secure.travis-ci.org/kurisuwhyte/emacs-wonderland.png)](http://travis-ci.org/kurisuwhyte/emacs-wonderland)
[![experimental](http://hughsk.github.io/stability-badges/dist/experimental.svg)](http://github.com/hughsk/stability-badges)

A library for declaratively describing your Emacs configuration. Think Puppet,
but for Emacsen ;)

> **Note:** Wonderland requires lexical binding, thus it's only compatible
> with Emacs 24+


## Example

```el
(require 'wonderland)

(wonderland/defeature paredit
  (package paredit))

(wonderland/defeature clojure
  (need paredit)
  (package clojure-mode)

  (def clojure-mode-font-lock-comment-sexp t)

  (hook clojure-mode-hook (lambda() (paredit-mode +1)))
  (mode clojure-mode "\\.clj$")

  (keymap clojure-mode
          ("C-c v" . slime-eval-buffer)))
```

## Installation

You can grab it from [marmalade](http://marmalade-repo.org):

    M-x package-install wonderland
    

## Documentation

( ... )


## Tests

( ... )


## Licence

MIT.
