# 小米手机打开开发者模式

```ad-tip
设置 -> 我的设备 -> 全部参数 -> 连续点击多次 `MIUI` 版本 -> 提示已进入开发者模式
```

# 小米手机开启 `USB` 调试

```ad-tip
设置 -> 更多设置 -> 开发者选项 -> 调试 -> `USB` 调试 (连接 `USB` 后启用调试模式)
```

参考链接: [小米手机开发者选项和USB调试打开步骤](https://miuiver.com/enable-miui-advanced-options/)

# 查看当前设备

```bash
adb devices
```

```ad-info
List of devices attached
adb server version (41) doesn't match this client (36); killing...
daemon started successfully
92d6a5e5        device
emulator-5554   device
```

上述 `92d6a5e5` 的设备即为小米手机。

同时在 `VS Code` 右下角可查看到 `Readmi K30 (android-arm64)` 设备已连接。

```ad-info
Launching lib\main.dart on Redmi K30 in debug mode...
```

```ad-warning
adb: failed to install ... Failure [INSTALL_FAILED_USER_RESTRICTED: Install canceled by user]
Error launching application on Redmi K30.
```

出现上述问题的原因是手机未打开 **允许通过 `USB` 安装应用** 选项。

# 允许通过 `USB` 安装应用

```ad-tip
设置 -> 更多设置 -> 开发者选项 -> 调试 -> `USB` 安装 (允许通过 `USB` 安装应用)
```

# Reference

* [Android Debug Bridge (adb)](https://developer.android.google.cn/studio/command-line/adb)