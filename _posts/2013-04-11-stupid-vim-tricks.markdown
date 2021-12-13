---
author: Jason Gallant
author_profile: true
comments: false
date: 2013-04-11 09:08:28+00:00
title: Working with VIM
tags: [code]
---

I've now realized that the build in UNIX text editor nano just doesn't cut the mustard, so I'm switching to VIM.  So far, I like it though it is a little hard for a fervent nano & sublime text editor to get used to.  But, there are some ways to tweak it to get it feeling a bit more familiar.  Create a text file in your home directory called ".vimrc" that reads as following:

`
set mouse=a
set number
`

Save the file and fire up vim.  Now you have a mouse scrolling text editor, with line numbers!  Already better than nano!
My installation (on BU's Katana Cluster) has syntax highlighting enabled by default.. but it looked wierd compared to my usual sublime text background.  I'm using iTerm2 (MacOSX), so it supports 256 colors.  This enables me to use a "rich" color scheme.  To prepare, I have to add the following to bash profile:

` TERM=xterm-256color; export TERM`

Next, I had to create a user .vim directory, and somewhere to put the color schemes I download.  Vim looks in $HOME/.vim/colors:

`
mkdir ~/.vim
mkdir ~/.vim/colors
`

Download the color scheme you like... sublime text is closely emulated by [](https://github.com/tomasr/molokai).  Then, going back to my .vimrc file:

`
set mouse=a
set number
syntax enable
colorscheme molokai
set background =dark
`

Now, open up your favorite script and behold the sublime-text like color scheme!

If you want to copy and paste from the VIM window in your terminal, you can disable the vim mouse mode by pressing option.
