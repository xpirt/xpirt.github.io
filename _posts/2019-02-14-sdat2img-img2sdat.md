---
layout: post
title: "sdat2img & img2sdat: Unpack Android .dat images"
date: 2019-02-14
description: "Tools to convert sparse Android data image (.dat) into filesystem ext4 image (.img) and back"
tags: sdat2img img2sdat android
categories: 
featured: true
---

From Android 5.0 and later, all compiled system images (OEM’s, AOSP, LineageOS, etc) are not compressed anymore the way they used to be, because of their increasing size. The new systems are now packed within custom proprietary .DAT files. The question is: how to decompress them? These tools will help you get started!

For more information about the usage of these tools and tutorials, visit my [XDA-Developers post](https://forum.xda-developers.com/android/software-hacking/how-to-conver-lollipop-dat-files-to-t2978952).

## sdat2img binary

This tool allows you to convert sparse Android data image (.dat) into filesystem ext4 image (.img). It requires Python 2.7 or newer installed on your system. It currently supports Windows, Linux, MacOS & ARM architectures.

**Note**: newer Google’s [Brotli](https://github.com/google/brotli) format (system.new.dat.br) must be decompressed to a valid sparse data image before using `sdat2img` binary.

### Usage
```bash
sdat2img.py <transfer_list> <system_new_file> [system_img]
```

- `<transfer_list>` = input, system.transfer.list from rom zip
- `<system_new_file>` = input, system.new.dat from rom zip
- `[system_img]` = output ext4 raw image file (optional)

Repo: [https://github.com/xpirt/sdat2img](https://github.com/xpirt/sdat2img)

Source code: [https://github.com/xpirt/sdat2img/blob/master/sdat2img.py](https://github.com/xpirt/sdat2img/blob/master/sdat2img.py)

Changelog: [https://github.com/xpirt/sdat2img/commits/master](https://github.com/xpirt/sdat2img/commits/master)


## img2sdat binary

This tool allows you to convert back from filesystem ext4 image (.img) to Android sparse data image (.dat). It requires Python 2.7 or newer installed on your system. It currently supports Windows x86/x64, Linux x86/x64 & arm/arm64 architectures.

### Usage
```bash
img2sdat.py <system_img> [-o outdir] [-v version] [-p prefix]
```

- `<system_img>` = input system image
- `[-o outdir]` = output directory (current directory by default)
- `[-v version]` = transfer list version number (1 – 5.0, 2 – 5.1, 3 – 6.0, 4 – 7.0, will be asked by default, more info on xda thread)
- `[-p prefix]` = name of image (prefix.new.dat)

Repo: [https://github.com/xpirt/img2sdat](https://github.com/xpirt/img2sdat)

Source code: [https://github.com/xpirt/img2sdat/blob/master/img2sdat.py](https://github.com/xpirt/img2sdat/blob/master/img2sdat.py)

Changelog: [https://github.com/xpirt/img2sdat/commits/master](https://github.com/xpirt/img2sdat/commits/master)


## Credits
These two binaries were not possible without the initial help and work by [howellzhu](http://weibo.com/howellzhu) and [luxi78](https://github.com/luxi78).

