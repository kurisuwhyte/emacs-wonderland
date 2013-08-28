Wonderland
==========

A library for declaratively describing your Emacs configuration.


## Example

```emacslisp
(require 'wonderland)

(wonderland/defeature markdown
  (package "markdown-mode")

  (def markdown-command		    "pandoc -r markdown -w html5")
  (def markdown-link-space-sub-char "-")

  (mode markdown-mode ("\\.md$")))
```

## Installation

## Documentation

## Tests

## Licence

MIT.