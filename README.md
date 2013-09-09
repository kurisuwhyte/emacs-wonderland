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
  ;; Installs a package using package-install
  (package paredit))

(wonderland/defeature clojure
  ;; Declares a dependency on some other feature
  (need paredit)

  (package clojure-mode)

  ;; Sets some state
  (def clojure-mode-font-lock-comment-sexp t)

  ;; Adds a hook
  (hook clojure-mode-hook (lambda() (paredit-mode +1)))

  ;; Defines an auto-mode
  (mode clojure-mode "\\.clj$")

  ;; Defines a keymap for the mode (use 'global to define a global keymap)
  (keymap clojure-mode
          ("C-c v" . slime-eval-buffer)))

;; Loads the clojure feature (and the paredit dependency)
(wonderland/load-feature 'clojure) 
```

## Installation

You can grab it from [marmalade](http://marmalade-repo.org) or [MELPA](http://melpa.milkbox.net/):

    M-x package-install wonderland
    

## Documentation

( ... )


## Tests

( ... )


## Licence

MIT.
