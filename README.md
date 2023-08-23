# Ubuntu Issues

This repository is a collections of solutions and notes for the issues faced while using Ubuntu.

## Booting
- Stuck in Login Screen (Loop)
  - Wrong Permission for .Xauthority or /tmp [link](https://www.makeuseof.com/fix-ubuntu-login-loop-issue/)
  - extra file in /etc/X11 (remove xorg.conf) [link](https://forums.developer.nvidia.com/t/after-doing-prime-select-nvidia-blank-freeze-screen-after-login/121050)
- Black screen (stuck at file checks)
  - prime-select intel and reboot [link](https://forums.developer.nvidia.com/t/ubuntu-20-04-boot-to-black-screen-when-selecting-nvidia-as-prime-after-kernel-update/219727/4)

## Brightness
In some rare cases, or when you have external monitors, you won't be able to tune your monitor's brightness with the slider bars provided by Ubuntu.
But fret now, here is your friendly command to do it!
```bash
# First Identify your monitor by running the following command
xrandr -q | grep "connected "
# After that just send the brigtness value to the respective monitor
xrandr --output LVDS-0 --brightness 0.7
```
