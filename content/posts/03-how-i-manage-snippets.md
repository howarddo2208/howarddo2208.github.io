---
title: "How I Manage Snippets"
date: 2023-07-10T12:35:08+07:00
categories:
series:
tags:
  - snippets
  - CLI
  - tmux
---

Snippet manager is not something I pay attention to until recently, but when I do, I want to make it blend into my workflow smoothly. I will share my tool and process in this blog

# The tool

[Nap](https://github.com/maaslalani/nap) is the tool of choice for me. It runs on the terminal, have a nice terminal UI. I don't really like GUI solutions as they are not accessible while I'm coding, and I need to alt-Tab to search for my snippets. So read the nap's README, give it a try, store some snippets and initialize a git repo for them.

# Integrate nap into my workflow

Currently, I'm using Neovim and Tmux for coding, so I want a keybindings to trigger the fuzzy finding for the snippets then. Here's a minimal script for this in `tmux.conf`. You need `fzf` installed for this

```sh
bind s display-popup -E "nap $(nap list | fzf) | pbcopy"
```

Replace the `s` key for whatever key you want, and replace `pbcopy` by `xclip -selection clipboard` if you are on Linux (not sure tho). Now `<prefix>+s` should work for you!

But I want my search to have code preview and be more customizable, so here's my script and I store it inside `~/.local/bin` and I give it executable permission

```sh
# ~/.local/bin/napfzf
find "$NAP_HOME" -type f ! -name "snippets.json" \
  | fzf --delimiter / --with-nth -1 --preview "bat --color=always {}"\
  --bind "enter:execute($EDITOR {})+abort" --bind "ctrl-y:execute-silent(cat {} | pbcopy)+abort"\
  --header 'Press CTRL-y to yank snippet into clipboard'

```

```sh
# tmux.conf
# I give the popup bigger size here for the code preview
bind s display-popup -h 80% -w 80% -E "napfzf"
```

Here you need `$NAP_HOME` environment set which point to the snippet directory, I use `bat` for code preview with syntax highlighting. When you press enter it will open in your default text editor `$EDTITOR` (in my case it is `nvim`), and `Ctrl-y` to copy the snippet

Here's the result
![nap demo GIF](/assets/03-napfzf-demo.gif)

# Conclusion

Here's how I manage my snippets for now, maybe I will create a key bind for creating snippet in nap when using Tmux, but now I don't see it's necessary.
