# HP Victus Sleep Mode / Hibernation Repair (Linux)

Fixing sleep mode on HP Victus (Intel i7, NVIDIA GTX 3050 mobile)

## Problem
I encountered issues with hibernation on my laptop (running Kubuntu 23.10). Whenever I attempted to put it to sleep, it wouldn't wake up properly. Instead, I was greeted with either a black screen or occasional flickering displaying the last image before hibernation.

## Laptop Specifications
- Model: HP Victus 15-fa0044nm
- Processor: Intel Core i7-12700H
- RAM: 16GB
- Storage: 512GB SSD
- Graphics: NVIDIA GeForce RTX 3050
- Display: 15.6" FHD
- Operating System: Kubuntu 23.10

## Solution
To resolve the issue, follow these steps:

1. Install the `nvidia-driver-535` (proprietary, tested).


   ![Screenshot_20240229_233758](https://github.com/Linux-Alex/HP-Victus-sleep-mode-hibernation/assets/37543086/182fe696-8c89-45b4-b934-e1616a639f11)

2. Edit the `/etc/default/grub` file.

   Change: `GRUB_CMDLINE_LINUX=""`

   To: `GRUB_CMDLINE_LINUX="intel_idle.max_cstate=4"`
3. Run: `sudo update-grub`
