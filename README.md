# dwmblocks
Statuscmd patch applied and disappearing block issues fixed version of dwmblocks.
# usage
To use dwmblocks first run 'make' and then install it with 'sudo make install'.
After that you can put dwmblocks in your xinitrc or other startup script to have it start with dwm.
# modifying blocks
The statusbar is made from text output from commandline programs.
Blocks are added and removed by editing the blocks.h header file.
By default the blocks.h header file is created the first time you run make which copies the default config from blocks.def.h.
This is so you can edit your status bar commands and they will not get overwritten in a future update.
# Signaling
You can update blocks by their update signal. Add 34 to signal number of block.
```sh
rtmin_plus=$((34 + 'signal number of block'))
kill -$rtmin_plus $(pidof dwmblocks)
```
