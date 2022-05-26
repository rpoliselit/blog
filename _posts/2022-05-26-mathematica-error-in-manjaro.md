---
layout: post
title: "Solving the errors to open Mathematica 11.3 in Manjaro"
categories: Linux
tags: [en-us, linux, wolfram-mathematica]
published: false
---

I have changed from KDE Neon to Manjaro KDE Plasma in the middle of the last week. I had no problems by installing Wolfram Mathematica 11.3, however this one did not open properly. So I decided open it by terminal and found a couple of errors in sequence. All of them are reported in the Mathematica post from the [Archlinux Wiki](https://wiki.archlinux.org/title/Mathematica). The last one was my contribution to community.

All of these errors happen because Mathematica includes a number of its own libraries which conflicts with system libraries. The Mathematica libraries are in the following directory:

```
cd <INSTALL_DIR>/SystemFiles/Libraries/Linux-x86-64
```

In order to solve these issues one needs to identify from which library does the error emerge. Let us see the first error I got: 

![My helpful screenshot](/assets/screenshot.jpg)

This error is related with freetype library. 

The Mathetica is force to use the system version of the library if we delete its file or rename it:

```
mv libfreetype.so.6 libfreetype.so.6.old
```

![My helpful screenshot](/assets/screenshot.jpg)

This erros is explicity due a zlib, thus force the Mathematica to use the system version of the zlib:

```
mv libz.so.1 libz.so.1.old
```

![My helpful screenshot](/assets/screenshot.jpg)

This last one was not in Archlinux wiki. From which library is this undefined symbol? If we search in google for this "hb_ot_tags_from_script_and_language", then a git repository of HarfBuzz is found. Thus let us force Mathematica to use the system version of the harfbuzz library: 

```
mv libharfbuzz.so.0 libharfbuzz.so.0.old
```

Done! No more errors here so far.