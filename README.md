# Acrux kernel for MI 8 Lite (sdm660) source

![logo](https://telegra.ph/file/d1db0b03507f710adc8c7.png)

## Branches and informaton
```
ten: Current stable release based on CAF's Android 10 tag
staging: Current staging (in-progress branch)
sdm660-em: Where my 660 energy model commits are stored
meme-commits: Well, take a guess
readme: This current branch

Any others are probably temporary/experimental
```

## About device
![mi8litaf](https://telegra.ph/file/9178a36968f4a20820c7a.jpg)

##### MI 8 Lite
```
Device codename - platina
Release date - August 11th, 2019
Release version - 8.1.0 on v4.4.78
Current version - 10.0.0 on v4.4.214 (this will probably be out of date)
```
*Full specifications - [GSM Arena](https://www.gsmarena.com/xiaomi_mi_8_lite-9329.php)*

## Features
As of 20-2-20: Rebasing time
```
- EAS (custom EM)
- Clean imported
- Upstreamed to latest CAF and linux-stable
- sched backports
- Omitted useless dtbs
- GCC 9 or Clang depending on CI
```

## Features you will never see
```
- Overclocking (not possible on a HW level on the SDM660)
- Any governors other than schedutil!!!
- No other I/O schedulers (maybe Anxiety)
- Nothing that comprimises performance - I prefer performance > battery because I'm near an outlet
```

## LICENSE
```
 Copyright (c), The Linux Foundation. All rights reserved.
 
 This software is licensed under the terms of the GNU General Public
 License version 2, as published by the Free Software Foundation, and
 may be copied, distributed, and modified under those terms.
 
 This program is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
 GNU General Public License for more details.
```
> See the accompanying [COPYING](https://github.com/nysascape/kernel_xiaomi_acrux/blob/staging/COPYING) file for more details.

> Also this is kanged from [HERE](https://github.com/whoknowswhoiam/weebmsm8998-pie/blob/README/README.md).
