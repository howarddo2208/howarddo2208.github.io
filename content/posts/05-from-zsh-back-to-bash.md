---
title: "From Zsh Back to Bash"
date: 2023-07-12T12:57:03+07:00
draft: true
categories:
series:
tags:
---

I'm considering switching back to bash, after some time doing shell scripting, I noticed many flaws that I didn't see before.

Zsh most of the time behaves like bash but if you are not aware of their differences, it would break disastrously when you least expect it. Unlike fish, which doesn't strive to be POSIX compliant at all, so I can fully be aware and rewrite every script I'm trying to use into fish. All that make such a pain to write and share public scripts if you are using `zsh`.

> For example, `read -p "input: " var`, this script which print out the message and get the user input into `var` would run on `sh` and any POSIX-compliant shell but not on `zsh`. And how to alleviate this problem? I have to add `sh -c` at the start and nest the script inside quotations.

> Another example is the `history` command, which normally print out all the history. But on zsh I have to run `history 0` in order for it to function like other shells. I only discovered when trying to use a script from another person on the internet, and I had to spend quite some time to troubleshoot it.

Don't get me wrong, I do love zsh very much and spent lot of my time configuring it. But now that I want to expand to writing and sharing my work, it wouldn't fit me anymore. If you're working on your own desktop, zsh is ok. So in this post I will put out all I have learned about it as a final farewell.

# What I did for my zsh

TODO leave zsh dotfile link.

TODO shit on oh-my-zsh: bloat, slow on older machine, full of junk alias, plugins are not that good

TODO minimal plugin manager written by chrismachine

TODO Useful tools: Atuin, starship

# What I just configured with my bash?

# Links

[Don\'t Ever Use Zsh](https://rwx.gg/advice/dont/zsh/) 
