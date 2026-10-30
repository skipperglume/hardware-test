sudo lshw -short

lspci -nn

lspci | grep -Ei 'VGA|3D|Display|Network|Ethernet|Audio|USB'


```bash
magick -size 2560x1600 xc:black black.png
magick -size 2560x1600 xc:white white.png
magick -size 2560x1600 xc:red red.png
magick -size 2560x1600 xc:green green.png
magick -size 2560x1600 xc:blue blue.png
magick -size 2560x1600 xc:"#808080" gray50.png
magick -size 2560x1600 xc:"#1A1A1A" gray10.png
```