# TWallet Prototypes

The purpose of this repository is to provide the code for the Apps developed to serve as a proof-of-concept for the designed TWallet System.

## Folder structure

This repository is organized as the following:

- App: contains the project of a crypto wallet based on ZainMustafaaa's Android Ethereum Wallet [[1]](#references).
- TWallet App: contains the same project, but with some minor modifications to include the TWallet system
- apks: contains the already generated apks from both wallets, in case the user only pretends to test the applications

## Pre-requisites

Considering the TWallet App that includes the TWallet system, it is necessary to have the [TWallet System components][twallet_system] already installed in your system, before trying to execute the application.

Additionally, both applications were developed using the Android Studio [[2]](#references) and therefore, its advisable to use it for visualization, edition and compilations.

## Installation setup

To run the Apps, you must install them as a system app. The procedure to do that consists in:

- Connect your Hikey 960 board to your computer through ADB
- Using the apk pre-generated, or an apk generated by you, transfer it to the hikey board using the commands:

```
adb shell mount -o rw,remount /system
adb push [name-of-apk].apk /system/priv-app/
adb shell chmod 644 /system/priv-app/[name-of-apk].apk
adb shell mount -o remount,ro /
```

- Reboot the system to have it installed in your computer

```
adb reboot
```

After this process, the applications must be installed an ready to be used.

## References

1. ZainMustafaaa. Web3j-Android-Ether-Wallet-Ethereum-Client. 2019. url: https://github.com/ZainMustafaaa/Web3j-Android-Ether-Wallet-Ethereum-Client
2. Android Developers. Android Studio 2020.3.1. 2021. url: https://developer.android.com/studio/

[twallet_system]: <https://github.com/rafagameiro/TWallet_system>
  