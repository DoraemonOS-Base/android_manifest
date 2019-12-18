# DoraemonOS #

<img src="https://raw.githubusercontent.com/DoraemonOS/android_manifest/Quiche/Doraemon.jpeg"> 

Getting Started :
===============
To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Minimum computer :
```bash
   [CPU Intel] [X86_64] [8 Core] {Or Mainboard Dual Socket CPU}
   [Ram] [8Gb] [16Gb] [32Gb]
   [Rom] [500Gb] 
   [OS] [Ubuntu 14.04 64Bit] | [Ubuntu 16.04 64Bit] | [Later Versions 64Bit] | [Debian 64Bit]
```

Package : 
```bash
   sudo apt-get install git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev libgl1-mesa-dev libxml2-utils xsltproc unzip bc repo nano
```

Repo Sync :
===========


To initialize your local repository, use a command like this:

```bash
   repo init -u https://github.com/DoraemonOS/android_manifest.git -b Tester
```




```bash
   repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

Additionally, you can define the number of parallel download repo should do:

```bash
   repo sync -f -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
Or Packages Repo Full :

```bash
   repo sync -j$(nproc --all)
```

And Git Clone Device Tree / Vendor / Kernel :
Source Device Tree :

   [**Device Tree**](https://github.com/DoraemonOS-Devices)
```bash
   Device Tree : ~/repo/device/xxx/yyy
   Vendor : ~/repo/vendor/xxx/yyy
   Kernel : ~/repo/kernel/xxx/yyy
```
```bash
   xxx = brand
   yyy = codename
```
EX:
```bash
   Device : Xiaomi Redmi Note 5 Pro ( Whyred )
   Device Tree : ~/repo/device/xiaomi/whyred
   Vendor : ~/repo/vendor/xiaomi/whyred
   Kernel : ~/repo/kernel/xiaomi/whyred
```
Pack Tree :
```bash
   Xiaomi Redmi Note 5 Pro ( Whyred )
```
```bash
   git clone -b Quiche https://github.com/DoraemonOS-Devices/device_xiaomi_whyred.git devive/xiaomi/whyred
   git clone -b Quiche https://github.com/DoraemonOS-Devices/vendor_xiaomi_whyred.git vendor/xiaomi/whyred
   git clone -b Quiche https://github.com/DoraemonOS-Devices/kernel_xiaomi_whyred.git kernel/xiaomi/whyred
   git clone -b Quiche https://github.com/DoraemonOS-Devices/vendor_MiuiCamera.git vendor/MiuiCamera
```

   
          


Compilation of DoraemonOS :
====================

From root directory of Project, perform following commands in terminal

Source Terminal :
```bash
   source build/envsetup.sh
```
  

Compilation With Brunch :

```bash
   brunch doraemon_<devicecodename>-userdebug
```
EX:
```bash
   Device : Xiaomi Redmi Note 5 Pro ( Whyred )
   Type : brunch doraemon_whyred-userdebug
   Or
   Type : brunch doraemon_whyred-eng
   Type : brunch doraemon_whyred-user
```



Compilation With Lunch :

```bash
   lunch doraemon_<devicecodename>-userdebug
```
EX:
```bash
   Device : Xiaomi Redmi Note 5 Pro ( Whyred )
   Type : lunch doraemon_whyred-userdebug
   Or
   Type : lunch doraemon_whyred-eng
   Type : lunch doraemon_whyred-user
```
```bash
   mka bacon -j$(nproc --all)
```


-----------------------------------------------------------------------------

 Credits :
=======
 * [**CyanogenMod**](https://github.com/Cyanogenmod)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**LotusOS**](https://github.com/Lotus-OS)
 * [**pixel experience**](https://github.com/pixelexperience)
 * [**Cosmic**](https://github.com/Cosmic-OS)
 * [**AOSiP**](https://github.com/aosip)
 * [**bootlegger**](https://github.com/BootleggersROM)
 * [**CherishOS**](https://github.com/CherishOS)
 * [**AOSP**](https://android.googlesource.com)
 
 # Doraemon Maintainer : #
 * [**Nobi Nobita**](https://github.com/dopaemon)
 
 # Doraemon Channel + Group : #
 * [**Telegram-Channel**](https://t.me/DoraemonOS)
 * [**Telegram-Group**](https://t.me/DoraemonOS_Chat)
 * [**Facebook Nobi Nobita**](https://facebook.com/nobita.developer)
 

