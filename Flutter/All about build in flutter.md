#Build #Flutter #Android #IOS
# `Android apk`

```bash
flutter build apk
```

```ad-info
Flutter assets will be downloaded from https://storage.flutter-io.cn. Make sure you trust this source!

 Building with sound null safety 

Flutter assets will be downloaded from https://storage.flutter-io.cn. Make sure you trust this source!
Running Gradle task 'assembleRelease'...                           78.0s
√  Built build\app\outputs\flutter-apk\app-release.apk (20.2MB).
```

构建完成的 `APK` 路径:

```ad-info
build\app\outputs\flutter-apk\app-release.apk
```

# `IOS ipa`

```bash
# 切换至 ios 文件夹路径
cd ios

# 安装依赖
pod install

# 返回上一级目录 (根目录)
cd ..

# build
flutter build ipa
```

构建完成后, 在 `XCode` 中打开 `ios` 文件夹, 点击运行。运行完毕后双击 `build/ios/archive` 下的 `Runner.xcarchive` 文件 (用 `XCode` 打开), 然后一直下一步即可上传成功。

如果过程中报版本不一致的错误, 可进行如下操作:

```bash
cd ios
# 清除缓存
pod cache clean --all
# 删除 Podfile.lock 文件
rm Podfile.lock

cd ..
# 清除缓存
flutter clean
flutter pub get
# 更新
pod update
pod repo update

# 重新安装依赖
pod install
```

## Reference

* [CocoaPods could not find compatible versions for pod - stackoverflow](https://stackoverflow.com/questions/67115523/flutter-sound-cocoapods-could-not-find-compatible-versions-for-pod-tau-sound-co)