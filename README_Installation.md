
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