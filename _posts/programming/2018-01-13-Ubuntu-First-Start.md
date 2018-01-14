---
layout: single
title:  "Ubuntu First Start"
categories:
  - programming
tags:
  - apt
  - linux
  - ubuntu
excerpt: My initial installation for a new Ubuntu system
#categories: programming linux
---
Similar to my [python post]({{ site.baseurl }}{% post_url /programming/2018-01-13-Ubuntu-First-Start %}), I like to keep track of the _essential_ installations on a new Ubuntu system. 
## The Script
Here is the compact version of everything: 
```bash
$ sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade && sudo apt-get autoremove
$ sudo apt-get install build-essential openmpi-bin openmpi-doc libopenmpi-dev git stow tmux python3-pip python-pip cmake vim liblapack* libblas* caffeine silversearcher-ag
$ sudo apt-get autoremove
```

**Extra Commands:** Most systems come with `gcc` and `python` but if not run `sudo apt-get install gcc g++ python python3` 
{: .notice}

{% capture notice-text %}
The list above is for standard development. On a more frequented machine I'll install LaTeX and [LyX](http://lyx.org)
```bash
$ sudo apt-get install texlive
$ sudo add-apt-repository ppa:lyx-devel/release
$ sudo apt-get update
$ sudo apt-get install lyx
```
{% endcapture %}

<div class="notice--primary">
  <h4>LaTeX Install:</h4>
  {{ notice-text | markdownify }}
</div>

## Details
What does each command do? Why include that software? 
### Line 1
* `apt-get update`- Update the list of packages that Ubuntu can install
* `apt-get upgrade` - Update to newer installed packages
* `apt-get dist-upgrade` - same as upgrade but can add/remove things in a 'smart' way
This just brings the system up to date before installing the extra packages 

### Line 2
Here is where all the non-default programs get installed
* `build-essential` - compiler tools to create programs
* `openmpi-bin openmpi-doc libopenmpi-dev` - message passing code that allows for massively parallel code on a supercomputer
* `git` - version control system
* `stow` - automatically create symlinks; used in conjunction with my dotfiles (see below)
* `tmux` - terminal multiplexer to have multiple terminals in one window. See [this tutorial](https://medium.com/actualize-network/a-minimalist-guide-to-tmux-13675fb160fa)
* `python3-pip python-pip` - "apt-get" for python; see my [python post]({{ site.baseurl }}{% post_url /programming/2018-01-13-Ubuntu-First-Start %})
* `cmake` - I tend to use [cmake](https://en.wikipedia.org/wiki/CMake) in order to maximize cross-plaform compatibility
* `vim` - my preferred text editor
* `liblapack* libblas*` - [BLAS](http://www.netlib.org/blas/) and [LAPACK](http://www.netlib.org/lapack/), effecient matrix and linear algebra tools
* `caffeine` - program to disable the screensaver for those long builds where you want to track progress
* `silversearcher-ag` - a 'search and highlight' program that is [incredibly fast](https://github.com/ggreer/the_silver_searcher#whats-so-great-about-ag); indispensable to find references

### Line 3
`apt-get autoremove` - Finally remove anything that isn't needed anymore due to dependency changes or otherwise. 

---
That's everything! Immediately after this I'll also clone my [dotfiles](https://github.com/ryanlevy/dotfiles) which contain portable preferences for bash, vim, tmux, python, and more.
