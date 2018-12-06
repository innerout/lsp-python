[![MELPA](https://melpa.org/packages/lsp-python-badge.svg)](https://melpa.org/#/lsp-python)

Python support for lsp-mode using [python-language-server](https://github.com/palantir/python-language-server).

## Installation

Install [`lsp-mode`](https://github.com/emacs-lsp/lsp-mode) first, and either clone
this repository, or install from MELPA. Add the following to your `.emacs`:

#### use-package

```emacs-lisp
(use-package lsp-mode
  :commands lsp
  :config (require 'lsp-clients))

(use-package lsp-python
  :ensure t
  :defer t
  :commands (lsp-python-enable))
(add-hook 'python-mode-hook (lambda () (require 'lsp-python) (lsp)))
```
