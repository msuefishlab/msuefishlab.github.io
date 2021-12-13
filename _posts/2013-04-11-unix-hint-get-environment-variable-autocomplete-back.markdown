---
author: Jason Gallant
author_profile: true
comments: false
date: 2013-04-11 08:27:52+00:00
title: 'UNIX Hint: Get Environment Variable Autocomplete Back'
tags: [code]
---

I have several nested folders that I need to switch between periodically.  I tried making environment variables for these:

directories, but for some silly reason I couldn't tab autocomplete them.  Apparently this is a new "feature" in bash 4.2.  The way to get it back is to add the following line to your ~/.bash_profile file:

complete -r cd

http://ubuntuforums.org/showthread.php?t=1749286

http://stackoverflow.com/questions/103316/in-bash-environmental-variables-not-tab-expanding-correctly
