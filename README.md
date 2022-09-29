# zsh-prompt-simple

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://github.com/atanvarno69/zsh-prompt-simple/blob/master/LICENSE)
[![Latest Version](https://img.shields.io/github/release/atanvarno69/zsh-prompt-simple.svg?style=flat-square)](https://github.com/atanvarno69/zsh-prompt-simple/releases)

A simple prompt for [zsh](https://www.zsh.org) displaying the present working directory.

# Requirements

-  [zsh](https://www.zsh.org) >= 5.8

# Installation

Clone this repo.

To install locally as a user, copy or symlink `prompt_simple_setup` to somewhere in your
[`$fpath`](https://zsh.sourceforge.io/Doc/Release/Parameters.html#index-fpath).

To install globally as root, copy or symlink `prompt_simple_setup` to `/usr/share/zsh/functions/Prompts/`.

# Usage

Then to initialize, add this to your `.zshrc`:

```zsh
autoload -Uz promptinit; promptinit
prompt simple
```

You can preview the prompt with:

```zsh
prompt -p simple
```

## Color

To change the default green color, pass a color argument:

```zsh
prompt -p simple blue
```

See the [zsh documentation](https://zsh.sourceforge.io/Doc/Release/Zsh-Line-Editor.html#Character-Highlighting) for
valid color options.

## Condensed

To only show the present working directory basename, without the leading full path, use the option `-c` or
`--condensed`.

```zsh
prompt -p simple --condensed
```

## Clock

To display a clock on the righthand side of the terminal, use the option `-t` or `--time`.

```zsh
prompt -p simple --time
```
