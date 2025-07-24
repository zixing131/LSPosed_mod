# 编译报错参考：
https://github.com/libxposed/api/issues/47
https://github.com/JingMatrix/LSPosed/issues/251

# 打包命令:

`
./gradlew zipAll
` 

# Release 打包命令:

`
./gradlew generateWebRoot
`

`
./gradlew zipZygiskRelease
`


# LSPosed Framework

[![Build](https://img.shields.io/github/actions/workflow/status/JingMatrix/LSPosed/core.yml?branch=master&event=push&logo=github&label=Build)](https://github.com/JingMatrix/LSPosed/actions/workflows/core.yml?query=event%3Apush+branch%3Amaster+is%3Acompleted) [![Crowdin](https://img.shields.io/badge/Localization-Crowdin-blueviolet?logo=Crowdin)](https://crowdin.com/project/lsposed_jingmatrix) [![Download](https://img.shields.io/github/v/release/JingMatrix/LSPosed?color=orange&logoColor=orange&label=Download&logo=DocuSign)](https://github.com/JingMatrix/LSPosed/releases/latest) [![Total](https://shields.io/github/downloads/JingMatrix/LSPosed/total?logo=Bookmeter&label=Counts&logoColor=yellow&color=yellow)](https://github.com/JingMatrix/LSPosed/releases)

## Introduction 

A Zygisk module trying to provide an ART hooking framework which delivers consistent APIs with the OG Xposed, leveraging LSPlant hooking framework.

> Xposed is a framework for modules that can change the behavior of the system and apps without touching any APKs. That's great because it means that modules can work for different versions and even ROMs without any changes (as long as the original code was not changed too much). It's also easy to undo. As all changes are done in the memory, you just need to deactivate the module and reboot to get your original system back. There are many other advantages, but here is just one more: multiple modules can do changes to the same part of the system or app. With modified APKs, you have to choose one. No way to combine them, unless the author builds multiple APKs with different combinations.

## Supported Versions

Android 8.1 ~ 16

## Install

1. Install Magisk v26+
2. [Download](#download) and install LSPosed in Magisk app
3. Reboot
4. Open LSPosed manager from notification
5. Have fun :)

## Download

- For stable releases, please go to [Github Releases page](https://github.com/JingMatrix/LSPosed/releases)
- For canary build, please check [Github Actions](https://github.com/JingMatrix/LSPosed/actions/workflows/core.yml?query=branch%3Amaster)

Note: debug builds are only available in Github Actions.

## Get Help
**Only bug reports from **THE LATEST DEBUG BUILD** will be accepted.**
- GitHub issues: [Issues](https://github.com/JingMatrix/LSPosed/issues/)
- (For Chinese speakers) 本项目只接受英语**标题**的issue。如果您不懂英语，请使用[翻译工具](https://www.deepl.com/zh/translator)

## For Developers

Developers are welcome to write Xposed modules with hooks based on LSPosed Framework. A module based on LSPosed framework is fully compatible with the original Xposed Framework, and vice versa, a Xposed Framework-based module will work well with LSPosed framework too.

- [Xposed Framework API](https://api.xposed.info/)

We use our own module repository. We welcome developers to submit modules to our repository, and then modules can be downloaded in LSPosed.

- [LSPosed Module Repository](https://github.com/Xposed-Modules-Repo)

## Community Discussion

[Troubleshooting guide](https://github.com/JingMatrix/LSPosed/issues/123) and [Disscusions](https://github.com/JingMatrix/LSPosed/discussions).

## Translation Contributing

You can contribute translation [here](https://crowdin.com/project/lsposed_jingmatrix).

## Credits 

- [Magisk](https://github.com/topjohnwu/Magisk/): makes all these possible
- [XposedBridge](https://github.com/rovo89/XposedBridge): the OG Xposed framework APIs
- [LSPlant](https://github.com/JingMatrix/LSPlant): the core ART hooking framework
- [Dobby](https://github.com/JingMatrix/Dobby): inline hooker for `LSPlant` and `native_api` implement
- [EdXposed](https://github.com/ElderDrivers/EdXposed): fork source
- [xz-embedded](https://github.com/tukaani-project/xz-embedded): decompress `.gnu_debugdata` header section of stripped `libart.so`
- ~~[Riru](https://github.com/RikkaApps/Riru): provides a way to inject code into zygote process~~
- ~[SandHook](https://github.com/ganyao114/SandHook/): ART hooking framework for SandHook variant~
- ~[YAHFA](https://github.com/rk700/YAHFA): previous ART hooking framework~
- ~[dexmaker](https://github.com/linkedin/dexmaker) and [dalvikdx](https://github.com/JakeWharton/dalvik-dx): to dynamically generate YAHFA hooker classes~
- ~[DexBuilder](https://github.com/LSPosed/DexBuilder): to dynamically generate YAHFA hooker classes~

## License

LSPosed is licensed under the **GNU General Public License v3 (GPL-3)** (http://www.gnu.org/copyleft/gpl.html).
