## android_device_xiaomi_lavender
For building TWRP for Redmi Note 7 

TWRP device tree for Redmi Note 7 

## Compile
First configure repo, git and java.
Second checkout minimal twrp with omnirom tree:

```
sudo repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
sudo repo sync

```
Use build 3.2.3 (android-9.0)
https://github.com/omnirom/android_bootable_recovery
```

Follow these commands from the terminal:

```
. build/envsetup.sh
lunch omni_lavender-eng
or
breakfast lavender eng
mka adbd recoveryimage ALLOW_MISSING_DEPENDENCIES=true
```

Installation and testing:

```
fastboot flash recovery out/target/product/lavender/recovery.img
```
