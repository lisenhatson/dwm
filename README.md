# Li's build of dwm

Forked and heavily modified from [Luke's dwm build](https://github.com/LukeSmithxyz/dwm)
![The dwm](/dwm.png)

## Keybindings

This is suckless, mmmbud, the source code is the documentation! Check out [config.h](config.h).

Okay, okay, actually I keep a readme in `larbs.mom` for my whole system, including the binds here.
Press <kbd>super+F1</kbd> to view it in dwm (zathura is required for that binding).
I haven't kept `man dwm`/`dwm.1` updated though. PRs welcome on that, lol.

## Patches and features

- [Clickable statusbar](https://dwm.suckless.org/patches/statuscmd/) with my build of [dwmblocks](https://github.com/lukesmithxyz/dwmblocks).
- Reads [xresources](https://dwm.suckless.org/patches/xresources/) colors/variables (i.e. works with `pywal`, etc.).
- scratchpad: Accessible with <kbd>mod+shift+enter</kbd>.
- New layouts: bstack, fibonacci, deck, centered master and more. All bound to keys <kbd>super+(shift+)t/y/u/i</kbd>.
- True fullscreen (<kbd>super+f</kbd>) and prevents focus shifting.
- Windows can be made sticky (<kbd>super+s</kbd>).
- [hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/) hides tags with no windows.
- [stacker](https://dwm.suckless.org/patches/stacker/): Move windows up the stack manually (<kbd>super-K/J</kbd>).
- [shiftview](https://dwm.suckless.org/patches/nextprev/): Cycle through tags (<kbd>super+g/;</kbd>).
- [vanitygaps](https://dwm.suckless.org/patches/vanitygaps/): Gaps allowed across all layouts.
- [swallow patch](https://dwm.suckless.org/patches/swallow/): if a program run from a terminal would make it inoperable, it temporarily takes its place to save space.
> I have no idea why Luke did not link scratchpad, true fullscreen, and sticky windows patches.

### Lisen's additional patch

- [Attachdirection](https://dwm.suckless.org/patches/attachdirection): New clients attach at the bottom of the stack instead of the top.
- [Barpadding](https://dwm.suckless.org/patches/barpadding/): adds padding to dwm bar for looks, I'm not using it by default.
- [Xrdb](https://dwm.suckless.org/patches/xrdb/): I did not realize xresources' patch, but this will force dwm to read ```dwm.*``` variables.
- [Systray](https://dwm.suckless.org/patches/systray/): Manually patched systray that bloats the code.

## Installation

```bash
git clone https://github.com/LisenHatson/dwm.git
cd dwm
sudo make install
```

There is also a `PKGBUILD` usable on distributions with pacman. Run `makepkg -si` instead of `sudo make install`.
