# Genymotion_A11_libhoudini
Genymotion ARM, ARMv7, ARMv8/ARM64 Translation for Android 11
![genymotion](https://user-images.githubusercontent.com/45286708/216748207-2ea2f5e3-5b70-4baa-8762-324e9522e799.png)


How to install:

1. Open the Android 11 emulator 
2. Copy and paste this to `/system/build.prop` and `/system/vendor/build.prop`
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
3. Download [libhoudini](https://github.com/niizam/Genymotion_A11_libhoudini/releases/download/1.0/system.zip) from releases page.
4. Drag and drop `system.zip` to emulator
5. Restart the emulator

To edit `build.prop` in step 2 you need [adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) installed.
```
adb shell
su
mount -o rw,remount /
vi /system/build.prop
vi /system/vendor/build.prop
```

Tested game
![game](https://user-images.githubusercontent.com/45286708/216749410-4aae71e1-dd50-482a-8b71-b32318ec6fd1.png)
