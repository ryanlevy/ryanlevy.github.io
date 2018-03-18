---
layout: single
title:  "Cleaning Homebrew Installs Without Pinned Script"
categories:
  - programming
tags:
  - brew
  - OSX
excerpt: Cleanup homebrew repositories without cleaning specific and/or pinned repositories
#categories: programming 
---
Because [Homebrew](https://brew.sh/) never uninstalls old versions, installations can begin to pile up. Thankfully there's a built in cleanup tool `brew cleanup` which deletes older versions but sometimes it's useful to keep older versions around. Particularly, `cmake`, `eigen`, and different compilers I like to keep on hand as certain software has hard coded paths to specific versions. 

Unfortunately, homebrew never implemented a solid feature to not upgrade. So I set about writing a shell script for it. An easier alternative would be to keep a file of all repositories you want to not clean and `grep -v` that file, but I wanted this to be flexible with whatever I have pinned at the time. 

{% gist 262e9c4256d6bef999851b4b7a160cd2 %}

Here's a sample output:
```bash
$ ./cleanup_homebrew.sh y
Not removing: boost|cmake|gcc|numpy|open-mpi|python|scipy|eigen|lmod
Removing: /usr/local/Cellar/aalib/1.4rc5... (82 files, 686.8KB)
Removing: /usr/local/Cellar/arpack/3.5.0... (20 files, 1.4MB)
Removing: /usr/local/Cellar/automake/1.15... (130 files, 2.9MB)
Removing: /usr/local/Cellar/bash/4.4.18... (146 files, 8.8MB)
Removing: /usr/local/Cellar/check/0.11.0... (42 files, 517.2KB)
Removing: /usr/local/Cellar/cloc/1.74... (84 files, 1.4MB)
Removing: /usr/local/Cellar/cloog/0.18.4_1... (35 files, 442.4KB)
Removing: /usr/local/Cellar/diff-so-fancy/1.1.1... (8 files, 32.3KB)
Warning: Skipping doxygen: most recent version 1.8.14 not installed
...
```
