---
title: "Fzf Tmux Session Manager"
date: 2023-07-11T21:52:08+07:00
categories:
series:
tags:
  - tmux
  - cli
  - fzf
---

Today I wrote a script to quickly search, delete and add new tmux session with the power of `fzf`. 

## The script

The `--bind` flag of `fzf` took me quite some time to debug because of many escape backslashes I needed to add.

```bash
#!/bin/bash
# ~/.local/bin/tmux-session-manager

FIND_DEFAULT_COMMAND="tmux list-sessions | sed -E 's/:.*$//' | grep -v \"^$(tmux display-message -p '#S')\$\""

tmux list-sessions | sed -E 's/:.*$//' | grep -v "^$(tmux display-message -p '#S')$"\
    | fzf --reverse --bind "ctrl-x:execute(tmux kill-session -t {})+reload(${FIND_DEFAULT_COMMAND})"\
    --bind "ctrl-n:execute(bash -c 'read -p \"Name: \" name; tmux new -d -s \"\$name\"')+reload(${FIND_DEFAULT_COMMAND})" \
    --bind "ctrl-r:reload(${FIND_DEFAULT_COMMAND})"\
    --header 'Enter: switch session | Ctrl-X: kill session | Ctrl-N: new session | Ctrl-R: refresh list'\
    | xargs tmux switch-client -t
```

And I bind it into `s` key to overwrite the default `tmux` behavior.

```bash
# tmux.conf
bind s display-popup -E "tmux-session-manager"
```

## Result

![fzf tmux session demo](/assets/04-fzf-tmux-demo.gif)

Hope you find this useful!
