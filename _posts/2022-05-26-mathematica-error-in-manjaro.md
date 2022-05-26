---
layout: post
title: "Solving the errors to open Mathematica 11.3 in Manjaro"
categories: Linux
tags: [en-us, linux, wolfram-mathematica]
published: true
---

I have changed from KDE Neon to Manjaro KDE Plasma in the middle of the last week. I had no problems by installing Wolfram Mathematica 11.3, however this one did not open properly. So I decided open it by terminal and found a couple of errors in sequence. All of them are reported in the Mathematica post from the [Archlinux Wiki](https://wiki.archlinux.org/title/Mathematica). The last error solution was my contribution to community.

All of these errors happen because Mathematica includes a number of its own libraries which conflict with system libraries. The Mathematica libraries are in the following directory:

```
cd <INSTALL_DIR>/SystemFiles/Libraries/Linux-x86-64
```

In order to solve these issues one needs to identify from which library does the error emerge. 

## [ERROR 1] undefined symbol: FT_Done_MM_Var

Let us see the first error I got: 

![Error 1](/assets/screenshots/mathematica-error-1.png)

This error is related to the freetype library. 

The Mathetica must be forced to use the system version of the library. It can be done if we delete its file or rename it:

```
cd <INSTALL_DIR>/SystemFiles/Libraries/Linux-x86-64
mv libfreetype.so.6 libfreetype.so.6.old
```

## [ERROR 2] zlib not found

Let us see the second error I got:

![Error 2](/assets/screenshots/mathematica-error-2.png)

This error is explicitly due to the zlib library, thus force the Mathematica to use the system version of the zlib:

```
cd <INSTALL_DIR>/SystemFiles/Libraries/Linux-x86-64
mv libz.so.1 libz.so.1.old
```

## [ERROR 3] undefined symbol: hb_ot_tags_from_script_and_language

Let us see the third error I got:

![Error 3](/assets/screenshots/mathematica-error-3.png)

This last error was not in Archlinux wiki. From which library is this undefined symbol? If we search in google for this "hb_ot_tags_from_script_and_language", then a git repository of HarfBuzz is found. Thus let us force Mathematica to use the system version of the harfbuzz library: 

```
cd <INSTALL_DIR>/SystemFiles/Libraries/Linux-x86-64
mv libharfbuzz.so.0 libharfbuzz.so.0.old
```

Done! No more errors so far.