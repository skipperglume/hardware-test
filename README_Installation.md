
```bash
sudo apt update

sudo apt install -y \
    stress-ng \
    memtester \
    memtest86+ \
    smartmontools \
    nvme-cli \
    fio \
    hdparm \
    lm-sensors \
    powertop \
    pciutils \
    usbutils \
    dmidecode \
    lshw \
    ethtool \
    iperf3 \
    iw \
    rfkill \
    bluez \
    imagemagick \
    feh \
    mesa-utils \
    vulkan-tools \
    git \
    build-essential \
    cmake \
    python3-venv \
    python3-pip \
    ubuntu-drivers-common
```





| Package | Tests |
|---|---|
| `stress-ng` | CPU + RAM + general system stability |
| `memtester` | RAM from within Linux |
| `memtest86+` | RAM outside Linux at boot |
| `smartmontools` | SSD SMART health |
| `nvme-cli` | detailed NVMe health/status |
| `fio` | SSD performance/stability |
| `hdparm` | basic disk information/performance |
| `lm-sensors` | CPU/system temperatures |
| `powertop` | power consumption/power states |
| `pciutils` | PCI devices: GPU, Wi-Fi, audio, etc. |
| `usbutils` | USB devices/controllers |
| `dmidecode` | RAM slots, BIOS, motherboard |
| `lshw` | complete hardware inventory |
| `ethtool` | Ethernet |
| `iperf3` | network performance |
| `iw` | Wi-Fi |
| `rfkill` | Wi-Fi/Bluetooth radio state |
| `bluez` | Bluetooth |
| `imagemagick` | generate pixel-test images |
| `feh` | fullscreen screen tests |
| `mesa-utils` | OpenGL tests |
| `vulkan-tools` | Vulkan/GPU detection |
| `git/build-essential/cmake` | build GPU-test utilities |
| `ubuntu-drivers-common` | NVIDIA driver management |


## Installing essentials:

```bash
sudo apt update
sudo apt install -y \
    git \
    curl \
    vim \
    htop \
    tmux \
    build-essential \
    cmake \
    gpg
```

## Installing QT for CopyQ:
```bash
sudo apt update
sudo apt install qt6-base-dev qt6-base-private-dev libqt6svg6-dev qt6-tools-dev qt6-tools-dev-tools
sudo apt install libqca-qt6-dev
sudo apt install qtkeychain-qt6-dev
sudo apt install extra-cmake-modules
sudo apt install libxfixes-dev libxtst-dev
sudo apt install qt6-declarative-dev
# For wayland:
sudo apt install libwayland-dev wayland-protocols

rm -rf CMakeCache.txt
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr/local -DWITH_NATIVE_NOTIFICATIONS=OFF -DWITH_STATUS_NOTIFIER_ITEM=OFF -DWITH_AUDIO=OFF  . 
make
sudo make install


```




## Check Current Desktop Session

```bash
echo $XDG_SESSION_TYPE
```