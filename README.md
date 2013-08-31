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

(wonderland/defeature markdown
  (package markdown-mode)

  (def markdown-command		        "pandoc -r markdown -w html5")
  (def markdown-link-space-sub-char "-")

  (mode markdown-mode "\\.md$"))
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
