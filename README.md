## Starter for writing latex documents in vscode
---

This depends on https://github.com/blang/latex-docker
which supplies a docker environment for compiling latex document.
This way you don't have to pollute your machine with latex stuff.
Make sure those scripts are in your $PATH.

Start and stop docker daemon with vscode tasks.

Also edit "latexdockerdaemoncmd.sh" and remove the "-it" part. vscode throws an error, "the input device is not a TTY"

Compiling on save is done with https://github.com/James-Yu/LaTeX-Workshop which is a vscode extension. This extension also has other goodies.
Install with
```bash
code --install-extension James-Yu.latex-workshop
```

