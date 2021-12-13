---
title: Count specific characters per line using AWK
tags:
  - code
  - medicine
  - big data
author: Jason Gallant
member: jason-gallant
author_profile: true
comments: false
date: 2012-08-28 23:00:00+00:00
---

I just figured out to use the handy little UNIX utility AWK, which makes parsing text files a breeze, if you know how to speak its language.  For the uninitated, there is a great list of little AWK one liners that you can check out here:

http://sparky.rice.edu/awk.html

http://awk.info/?awk1line

One thing I couldn't seem to google was how to extract specific characters on a per-line, per column basis.  After some mashing together and trial and error, I came up with a code that will count the number of 1's and 0's in a column seperated file (in this case, from column 3 and 4 respectively from the file).  Give it a shot, and feel free to use as you see fit ;)

https://gist.github.com/3520003
