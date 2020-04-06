# SHRP Recovery Device configuration for Motorola Moto Z2 Force (nash)

Copyright 2018 - The OmniROM Project

For building SHRP Recovery for Motorola Moto Z2 Force & Moto Z 2018 ONLY.

### Kernel Source
Check here: https://github.com/motoz2-force/android_kernel_motorola_msm8998

### SHRP Recovery Source
SHRP Recovery Source: https://github.com/SKYHAWK-Recovery-Project

### How to build recovery

###-----First,Sync source

mkdir SHRP

cd SHRP

repo init -u git://github.com/SKYHAWK-Recovery-Project/platform_manifest_twrp_omni.git -b 9.0

repo sync -j8 --force-sync

mkdir -p device/motorola

cd device/motorola

git clone https://github.com/Remim7/SHRP_device_motorola_nash -b shrp_9.0 nash

###-----Next,Build Recovery

cd SHRP

source build/envsetup.sh

export ALLOW_MISSING_DEPENDENCIES=true

export LC_ALL="C"

lunch omni_nash-eng && mka recoveryimage

### Device specifications
=====================================

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core (4x2.45 GHz Kryo & 4x1.9 GHz Kryo)
CHIPSET | Qualcomm MSM8998 Snapdragon 835
GPU     | Adreno 540
Memory  | 4/6GB
Shipped Android Version | 7.1 (Nougat)
Storage | 64/128GB
Battery | 2730 mAh
Dimensions | 155.8 x 76 x 6.1 mm
Display | 1440 x 2560 pixels/5.5" P-OLED
Rear Camera  | Dual 12 MP
Front Camera | 5 MP
