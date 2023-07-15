---
title: "About Privacy: Browsers and Search Engines"
date: 2023-07-14T19:15:41+07:00
categories:
series:
tags:
  - privacy
  - browser
  - search engine
---

Another step into being an open source purist, I decided to change my browser and search engine for better privacy. Not that I'm doing anything illegal and afraid of someone trying to get me, it's just I've read and listened to a lot of [stories of people got screw over by big tech data collection](https://www.youtube.com/watch?v=0aXIXozAsOE).

![Browser Privacy Comparison](/assets/06-browser-privacy.png)

## Browsers

I was surprised to learn that Firefox, even though is an open-source browser, a large part of it is bloat and proprietary and not that privacy-focused. So after digging into [Privacy Test](https://privacytests.org/). I decided to use these browsers from now on:

### Desktop

- [LibreWolf](https://librewolf.net/): a privacy harden fork of Firefox, I will use it as browser to sign in my accounts. I still enabled Firefox sync, and if I want to keep login of a site after exiting I will manually add it into the cookie exception list. Also need to turn off the clear Active login from deleting list.

- [Mullvad Browser](https://mullvad.net/en/browser): for anonymous browsing (slightly less secured compared to Tor but doesn't need to connect to Tor network, hence faster)

- [UnGoogled Chromium](https://github.com/ungoogled-software/ungoogled-chromium): In case I need a Chromium-based browser, Chrome Web Store not function as usual but can be easily worked around.

Accompany these browsers, I also installed uBlock Origin, which is open source as the default ad blocker.

### Android phone

- [Mull](https://gitlab.com/divested-mobile/mull-fenix): Firefox-based, improved on security

## Search Engine

Do you know that Google, Bing collect all of your search request to serve you targeted ads and also sell it to other advertising companies? That's right, so switching the default engine will be your next step. Don't worry if you want to keep the search result quality of Google, we can have both privacy and search quality!

To sum up, you got 3 choices: 

- kinda built from scratch search engine (Brave, Qwant)

- privacy-respected frontend for your current search engine (StartPage, Whoogle)

- Search engine aggregator (SearXNG).

I decided to stick with StartPage or Whoogle for now as it's quite simple to switch to, the UI is also similar to Google. Maybe I will host an SearXNG instance later on if I got into self-hosting.

## Links

Resources I looked into crafting this blog

[Why care about Privacy](https://www.youtube.com/watch?v=0aXIXozAsOE)

[Browser Tier List](https://www.youtube.com/watch?v=j5r6jFE8gic)

[Search Engine Tier List](https://www.youtube.com/watch?v=Yjm6lGwqnGs)

[Privacy Test](https://privacytests.org/)
