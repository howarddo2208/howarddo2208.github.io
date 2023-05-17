---
title: "Practical guide to Nix package manager, and how to replace Homebrew with it"
date: 2023-05-17T16:32:42+07:00
series: "nix journey"
draft: true
---
this is the first post in series of short articles documenting how I use Nix to enhance my dev workflow, in this post I will show you your first step to use nix to replace your current package manager
----------------
# Why nix? How to start using it

I first came across nix package from a youtube [video of Mental Outlaw](https://youtu.be/BwEIXIjLTNs) and was fascinated to learn that I can use the power of Nix to automate the migration of my development environment to other machines, so I started to use it to replace Homebrew on my macOS machine. The thing about Homebrew is it when you install a package, it also installs a bunch of dependencies and when you call `brew list`, you will see that those dependencies are also listed just like the packages you tell Homebrew to install, which is kinda messy. It's not the case with nix though, it only list out what you explicitly tell it to install

Nix has massive amount of packages, works on both macOS, linux and windows WSL. To start using it as a beginner, just head to their [website](https://nixos.org/) to get started. After installing, you may now start using it with 2 most basic feature: `nix-shell` and `nix-env`.

## Quick bits 
- To search for a package, the easiest way is to head to https://search.nixos.org/ and choose the unstable channel for the latest package version.
- `nix-collect-garbage`: a quick way to clean up your nix store from experiment packages, or old generations, etc

## Nix-shell
think of it as a shell you can experiment all kind of package you want to try but not sure wanting to install yet. A quick command to pull packages and then experiemnt with them is `nix-shell -p <pkg-1> <pkg-2>`. This will launch a bash shell which only contains the packages you listed in it. When you are done with the experiment, press `Ctrl+D` or execute `exit` to get out of the nix shell.

## Nix-env
When comes to permanently modify the local profile of packages, you use `nix-env`. I'll just cut to the chase and give you a bunch of example for basic package management here, you can read more information on the [official documentation](https://nixos.org/manual/nix/stable/package-management/basic-package-mgmt.html) :
  - search for package: `nix-env -qaP neovim`
  - install package: `nix-env -iA nixpkgs.neovim`
  - remove package: `nix-env -e neovim`
  - upgrade a package: `nix-env -uA nixpkgs.neovim`, upgrade all packages: `nix-env -u`

A quick way you can install package is just to head to the [search site](https://search.nixos.org/), search for the package you want and copy the script to install to your terminal, remember choose unstable channel and nix-env script though.

# Remove packages from Homebrew
That's it, now you know how to use nix to install your packages, now if you are using Homebrew and want to migrate away from it, here are some command I will give you for the job. 
