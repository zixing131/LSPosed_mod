# How does LSPosed work ?

`LSPosed` utilise the `postAppSpecialize` [Zygisk API](https://github.com/topjohnwu/Magisk/blob/master/native/src/core/zygisk/api.hpp) to inject into target process, and provides [Xposed Framework API](https://api.xposed.info/reference/packages.html) for modules to hook Java methods.
We recommend the [Development tutorial](https://github.com/rovo89/XposedBridge/wiki/Development-tutorial) by [rovo89](rovo89) for a better understanding of the purpose of Xposed.
`LSPosed` also provides [Native Hook API](https://github.com/LSPosed/LSPosed/wiki/Native-Hook) to facilite the routine of hooking functions in loaded native libraries.
