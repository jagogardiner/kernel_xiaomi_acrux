# Acrux kernel for MI 8 Lite (sdm660) source

![logo](https://telegra.ph/file/d1db0b03507f710adc8c7.png)

## Branches and informaton
```
pie: Current stable branch, if you're building inline on ROMs COMPILE DIS (obviously for 9.0 Pie) - EAS > HMP
develop: My developing branch - I force push a lot and if you don't like force pulling use Pie - this branch gets merged between releases if all gud
hmp: (what was) A hmp kernel which tbh is quite old and depriciated, as EAS best now
clean: If I rebase, I use this branch. Fully bootable and stable

From the creation of this README, all releases will be tagged and will have release candidates + full releases under Pie.
I'm planning to add CI/CD support soon but cba to setup Drone.
```

## About device
![mi8litaf](https://telegra.ph/file/9178a36968f4a20820c7a.jpg)

##### MI 8 Lite
```
Device codename - platina
Release date - August 11th, 2019
Release version - 8.1.0 on v4.4.78
Current version - 9.0.0 on v4.4.185 (this will probably be out of date)
```
*Full specifications - [GSM Arena](https://www.gsmarena.com/xiaomi_mi_8_lite-9329.php)*

## Features
Based on Acrux build 13-7-19 - Codename: rc1
```
- 4.4.185 and latest CAF tag merged
- Xiaomi code cleaned up with minimal changes to Android-stable
- Wi-Fi driver imported from CAF and cleaned up
- Energy aware scheduling
- My own, capacity-based energy model included (more battery life and performance compared to any other EM)
- Disable kernel-wide debugging (debug_fs and debug_kernel removed)
- F2FS rapid GC 
- Stune boosting locked to 1
- Compiled with DragonTC 9 (clang with polly optimizations)
- Klapse and kcal
- Wake up all idle CPUs before suspending (helps with idle drain)
- Turn off sched autogrouping
- Set CPUBW governor to bw_hwmon
- Optimize UFS stack
- Improve camera performance and drain
- Use analog dimming
- Use system wide interruptible waits
- Force block requests onto their origin CPU
- mm/ optimizations
- Add dynamic bitclk and fps support to the panel
- Remove some high priority workqueues from useless things
- Link /dev/urandom to /dev/random
- Add and refactor make flags
- Fix memory overlaps
- Fix qcacld-3.0 wifi bug where signal would be 0 in QS/status bar
- VDSO32 enabled
- Speedup EXT4
- Omit useless dtbs
- Use 100Hz timer
- Remove all debugging and tracing drivers
- Debug kernel and debugfs gone
```

## Features you will never see
```
- Overclocking (not possible on a HW level on the SDM660)
- Any governors other than schedutil (they're fucking useless man)
- No other I/O schedulers (maybe Anxiety)
- Nothing that comprimises performance - I prefer performance > battery because I'm near an outlet
- Constant upstreaming - when I can be bothered, I'll upstream
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
> See the accompanying [COPYING](https://github.com/whoknowswhoiam/weebmsm8998-pie/blob/9.0/COPYING) file for more details.

> Also this is kanged from [HERE](https://github.com/whoknowswhoiam/weebmsm8998-pie/blob/README/README.md).
