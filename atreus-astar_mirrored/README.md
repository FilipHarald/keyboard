```sh
qmk list-keyboards
qmk config user.keyboard=atreus/astar_mirrored
qmk config user.keymap=filipharald
qmk new-keymap
nvim /home/filip/qmk_firmware/keyboards/atreus/keymaps/filipharald
```

```sh
qmk c2json -km filipharald -kb atreus /home/filip/qmk_firmware/keyboards/atreus/keymaps/filipharald/keymap.c > ~/Documents/map.json
```

first put keyboard in bootloader mode! (`QK_BOOT`)
```sh
qmk compile
lsusb | grep Atreus
qmk flash
```
