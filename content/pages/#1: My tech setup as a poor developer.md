---
type:
- blogs
tags:
- setup
title: #1: My tech setup as a poor developer
categories:
date: 2023-05-04
lastMod: 2023-05-04
---
Hi, welcome to my first blog, in this article I will list out all the tech that I use daily with my Macbook and Android phone. I hope that you can find something useful in this curated list and use them in your setup.

I'm a poor boy in a third-world country, so my setup would include many free, pirated stuffs, don't arrest me please :P

All the tech listed here will be updated over time when I found better alternatives or add something new

# 1. development tools

  + Node.js: I'm a typescript developer so I will list some tools related to it

    + nodejs version manager - [fnm](https://github.com/Schniz/fnm): I find this perform better that nvm I used before, and it is written in Rust too, so of course it is blazingly fast! :D

    + [pnpm](https://pnpm.io/installation): fasted node package manager I know to date

  + code editor

    + [Neovim](https://github.com/neovim/neovim) is my main code editor. If you find neovim hard to get started, you can consider using [NvChad](https://nvchad.com/), [LunarVim](https://github.com/lunarvim/lunarvim) or any other preconfiged neovim setup

    + [Visual Studio Code](https://code.visualstudio.com/)

  + Terminal setup:

    + here is my [dotfiles](https://github.com/howarddo2208/dotfiles), have a look! My terminal setup highly revolves around zsh shell, neovim config and tmux (a terminal multiplexer).

    + Terminal Emulator - [Wezterm](https://github.com/wez/wezterm): I choose this over allacritty, kitty and iTerm because it support all platforms and got nice feature right out of a box like copy mode without mouse, etc

    + some other useful terminal stuffs here

      + [cheat.sh: the only cheat sheet you need](https://github.com/chubin/cheat.sh)

      + [lazygit: simple terminal UI for git commands](https://github.com/jesseduffield/lazygit)

  + [Docker](https://www.docker.com/): quickly setup dev environment with image and containers

  + [ngrok](https://ngrok.com/): for sharing localhost ports (I rarely use it)

# 2. productivity

  + personal knowledge management - [logseq](https://github.com/logseq/logseq) + [Notion](https://www.notion.so/): I think there is no need to talk about notion because you probably knew about it already, but Logseq is the best app I've ever used to take notes, manage my knowledge and everything in my life. Its block approach makes it really easy to connect existing data, and ideas in your graph together, and it is open-source with a big collection of tutorials/plugins for its user base too. The data are fully managed by you. I highly recommend you try it.

![my logseq graph](/assets/image_1683208325478_0.png)

  + peer-to-peer syncing: [Syncthing](https://syncthing.net/): One caveat of using logseq is that if you don't spend money to support the current development, you have to find your own way to sync data. So many people turn to this app to sync their data, after using it for a while, now I think it is the best syncing app out there, it use P2P network and not store your data on any of the cloud service. Right now I use it to sync my logseq graph and downloaded musics, videos, series, etc between my phone and laptop.

  + translator: [Reverso]( https://www.reverso.net/)

  + flashcards: [Anki](https://apps.ankiweb.net/) + logseq flashcards feature

  + video editor - [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve/): the free version is good. I don't want to pay for expensive Adobe apps at all

  + sites, appblocker

    + Mobile - [Stay Focused](https://play.google.com/store/apps/details?id=com.stayfocused&gl=US): I find this especially useful to limit my phone usage, if you want to buy it, there is a lifetime plan, no more annoying subscription plan. It got an iOS app too, but I don't have a iPhone to test it

    + Mac - [Self Control](https://github.com/SelfControlApp/selfcontrol/): free and open source website blocker for macOS, once you decide to block a website, you can't revert the action no matter what.

  + book + article reader + highlight reviewer - [Readwise](https://readwise.io/) and [Reader](https://read.readwise.io/): amazing combo to read and review your highlights, covered under 1 subscription. If you are in a 3rd world country like me or you are a student, you can email them to get a big discount too.

  + scheduler, time blocking day: [Google Calendar](https://calendar.google.com/) +  [Cron](https://calendar.cron.com/)

  + Todo app + Pomodoro timer - [Focus To-do](https://www.focustodo.cn/): supports all platforms (no Linux desktop client, but you can install it as Chrome extension), PRO version is 1-time payment and it is good enough.

  + time tracker for freelance: [Toggl Track](https://toggl.com/track/)

  + password manager - [Bitwarden](https://bitwarden.com/): open-source and reliable password manager, its free tier is enough for personal usage.

  + AI assistant client - [ChatGPT Desktop Application](https://github.com/lencx/ChatGPT) + [Poe](https://poe.com/): Poe is really fast and support multiple AI model, and if you want to open ChatGPT as an app, download the client for desktop on github

# 3. Medias and entertainment

  + In this section, I will introduce you to all the free solutions so you can get rid of your subscription service and live like a cheapskate like I am XD

  + movies and series streaming

    + [Stremio](https://www.stremio.com): my main source of movies/series streaming. You can install straight at the app store but after you need to install the hidden addons to access variety of torrent streams.

      + [hidden addons](https://danamag.github.io/stremio-addons-list/): best one are torentino and the pirate bay. Install trakt addon if wanting to track your history.

    + [Cloudstream](https://github.com/recloudstream/cloudstream): android only, I just discovered it and it seems nice, got the download functionality out of the box, but I will stick with Stremio because of the trakt itegration

  + music

    + I mainly use adblocked Spotify

      + desktop: [SpotX: Modified Spotify client. Blocks ads and updates](https://github.com/amd64fox/SpotX)

      + android [xManager](https://github.com/xManager-App/xManager): install, manage and update ad-free Spotify for android

    + music downloader - [SpotiFlyer](https://github.com/Shabinder/SpotiFlyer): download audio from various sources, I use it along with [Music Player & MP3 Player](https://play.google.com/store/apps/details?id=musicplayer.musicapps.music.mp3player)

  + videos

    + youtube client - [NewPipe](https://newpipe.net/) - minimal, free and open-source client to get ad-free youtube + other features. If you want to have google account built in, you should look into revanced as the old youtube vanced just got shutdown by google.

    + video downloader - [dvd](https://github.com/yausername/dvd)+[Seal](https://github.com/JunkFood02/Seal): both are open-source GUI downloader powered by [yt-dlp](https://github.com/yt-dlp/yt-dlp), best tool to download videos from youtube

  + manga - [Tachiyomi](https://tachiyomi.org/): Android app to read manga pulled from multiple sources by installing additional extensions

  + books - [Anna's Archive](https://annas-archive.org/): Search engine of shadow libraries: books, papers, comics, magazines. After the public website of Zlib got shutdown, I discovered this and it is amazing

  + audiobooks - [audiobookbay](https://audiobookbay.is/): best source of free audiobooks, I use it with [Smart Audiobook Player](https://play.google.com/store/apps/details?id=ak.alizandro.smartaudiobookplayer) on android

# 4. Other apps for my mac

  + [Pastebot](https://tapbots.com/pastebot/): I find this especially useful when copying multiple code snippets with the sequential copy/paste feature, but it is a paid app and for mac only. I will add a link to windows/linux alternative if I find one

  + hide excess menu bar icons: [hidden](https://github.com/dwarvesf/hidden): if you have too many menu bar icons, this free app can help you, if you got some money, you can consider getting [Bartender](https://www.macbartender.com/) as I heard it is better

  + keyboard mappers: [Karabiner-Elements](https://karabiner-elements.pqrs.org/)

  + quick file transfer, sharing with drag and drop drawer - [Dropover](https://dropoverapp.com/): I bought it by 1-time payment, really useful. Another alternative I heard is DropZone, you can try it out

  + better screenshot capture - [Shottr](https://shottr.cc/): way better than default capture, if you got money then pay for CleanShotX is the best

  + custom launcher, spotlight replacement - [Raycast](https://www.raycast.com/): highly recommend for any mac user, you can assign custom hotkey, install plugins to add more functionality to your existing Spotlight
