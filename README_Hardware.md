## General Hardware

sudo lshw -short

lspci -nn

lspci | grep -Ei 'VGA|3D|Display|Network|Ethernet|Audio|USB'

## Display

sudo apt install imagemagick

```bash
magick -size 2560x1600 xc:black black.png
magick -size 2560x1600 xc:white white.png
magick -size 2560x1600 xc:red red.png
magick -size 2560x1600 xc:green green.png
magick -size 2560x1600 xc:blue blue.png
magick -size 2560x1600 xc:"#808080" gray50.png
magick -size 2560x1600 xc:"#1A1A1A" gray10.png
# Left -> right: black to white
magick -size 2560x1600 gradient:black-white gradient-horizontal.png
# Top -> bottom: black to white
magick -size 2560x1600 gradient:black-white -rotate 90 gradient-vertical.png

magick -size 3200x3200 gradient:black-white \
    -rotate 45 \
    -gravity center \
    -crop 2560x1600+0+0 +repage \
    gradient-diagonal.png


magick -size 3200x3200 gradient:black-white \
    -rotate -45 \
    -gravity center \
    -crop 2560x1600+0+0 +repage \
    gradient-diagonal-reverse.png

```

gnome-randr

sudo apt install lcdtest

## RAM
sudo dmidecode --type memory
sudo dmidecode --type memory | grep -E 'Size:|Type:|Speed:|Manufacturer:|Part Number:'


### Quick RAM stress test

stress-ng --vm 8 --vm-bytes 80% --verify --timeout 30m --metrics-brief


sudo memtester 50G 2


## NVMe / SSD
lsblk -o NAME,MODEL,SIZE,TYPE,FSTYPE,MOUNTPOINTS
sudo nvme list



```bash
mkdir -p hardware-tests/storage
cd hardware-tests/storage 

fio \
  --name=ssd-test \
  --filename=testfile \
  --size=8G \
  --rw=readwrite \
  --bs=1M \
  --direct=1 \
  --iodepth=16

```


## Temperatures and fans

```bash
# Manual find sensors
sudo sensors-detect
# Audo find sensors
sudo sensors-detect --auto
# List sensors measurments
sensors
# Continuous watch sensors
watch -n 1 sensors
```


## CPU

```bash
lscpu
# Only architecture
lscpu | grep "Architecture"
# Number of CPUs
lscpu | grep "CPU(s)"
# Vendor + Model
lscpu | grep "Model name"
# Check Virtualization (VMs or containers)
lscpu | grep "Virtualization"


```
stress:

```bash
stress-ng --cpu 0 --cpu-method all --verify --timeout 30m --metrics-brief
watch -n 1 sensors
```


## NVidia GPU

```bash
# List devices
ubuntu-drivers devices
sudo ubuntu-drivers install

sudo reboot

nvidia-smi
```

### Check existing nvidia drivers:

```bash
dpkg -l | grep -E 'nvidia|libnvidia'
```





## Battery

```bash
upower -i "$(upower -e | grep BAT)"
```
