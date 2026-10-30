# Motorola Edge 40 Neo (manaus) Device Tree

This repository contains the device-specific configuration and makefiles for building Android 17 (RisingOS / LineageOS) on the **Motorola Edge 40 Neo** (codename `manaus`).

## Device Specifications

| Feature | Details |
| :--- | :--- |
| **SoC** | MediaTek Dimensity 7030 (MT6879) |
| **CPU** | 2x 2.2 GHz Cortex-A78 & 6x 2.0 GHz Cortex-A55 |
| **GPU** | IMG BXM-8-256 |
| **Architecture** | ARM64 (64-bit only) |
| **Display** | 6.55" Curved pOLED, 144Hz, FHD+ (1080 x 2400) |
| **Battery** | 5000 mAh (68W TurboPower) |
| **Storage & RAM** | 128GB/256GB UFS 2.2, 8GB/12GB LPDDR4X |
| **Biometrics** | Under-display optical fingerprint scanner |
| **Audio** | Stereo speakers, Dolby Atmos, Hi-Res Audio, LHDC v3/v5, LDAC |

## Directory Path in Source Tree

```bash
device/motorola/manaus
```

## Dependencies

This device tree requires the following companion repositories:
* [Common Tree](https://github.com/motorola-manaus/android_device_motorola_mt6879-common): `device/motorola/mt6879-common`
* [Kernel Source](https://github.com/motorola-manaus/android_kernel_motorola_mt6879): `kernel/motorola/mt6879`
* [Device Vendor Blobs](https://github.com/motorola-manaus/proprietary_vendor_motorola_manaus): `vendor/motorola/manaus`
* [Common Vendor Blobs](https://github.com/motorola-manaus/proprietary_vendor_motorola_mt6879-common): `vendor/motorola/mt6879-common`
* [MediaTek SEPolicy](https://github.com/motorola-manaus/device_mediatek_sepolicy_vndr): `device/mediatek/sepolicy_vndr`
* [MediaTek Hardware](https://github.com/motorola-manaus/hardware_mediatek): `hardware/mediatek`
* [Dolby Atmos HAL](https://github.com/motorola-manaus/hardware_dolby): `hardware/dolby`

## How to Build

From your AOSP / RisingOS root directory:

```bash
# Initialize build environment
source build/envsetup.sh

# Target setup
lunch lineage_manaus-ap4a-userdebug
# or for RisingOS:
# lunch rising_manaus-userdebug

# Build ROM
m rising
```

## License

* SPDX-License-Identifier: Apache-2.0
