# Genymotion_A11_libhoudini
Genymotion ARM, ARMv7, ARMv8/ARM64 Translation for Android 11


How to install:

1. Copy and paste this to `/system/build.prop` and `/system/vendor/build.prop`
```
ro.product.cpu.abilist=x86_64,x86,arm64-v8a,armeabi-v7a,armeabi
ro.product.cpu.abilist32=x86,armeabi-v7a,armeabi
ro.product.cpu.abilist64=x86_64,arm64-v8a
ro.vendor.product.cpu.abilist=x86_64,x86,arm64-v8a,armeabi-v7a,armeabi
ro.vendor.product.cpu.abilist32=x86,armeabi-v7a,armeabi
ro.vendor.product.cpu.abilist64=x86_64,arm64-v8a
ro.odm.product.cpu.abilist=x86_64,x86,arm64-v8a,armeabi-v7a,armeabi
ro.odm.product.cpu.abilist32=x86,armeabi-v7a,armeabi
ro.odm.product.cpu.abilist64=x86_64,arm64-v8a
ro.dalvik.vm.native.bridge=libhoudini.so
ro.enable.native.bridge.exec=1
ro.enable.native.bridge.exec64=1
ro.dalvik.vm.isa.arm=x86
ro.dalvik.vm.isa.arm64=x86_64
ro.zygote=zygote64_32
```
2. Download [libhoudini](https://github.com/niizam/Genymotion_A11_libhoudini/releases/download/1.0/system.zip) from releases page.
3. Drag and drop `system.zip` to emulator

To edit `build.prop` in step 1 you need [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) installed.
```
adb shell
su
mount -o rw,remount /system
vi /system/build.prop
vi /system/vendor/build.prop
```
