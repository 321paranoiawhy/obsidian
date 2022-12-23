* [intl - pub.dev](https://pub.dev/packages/intl)
* [intl - GitHub](https://github.com/dart-lang/intl)
* [Flutter Intl - VS Code extension](https://github.com/localizely/flutter-intl-vscode)
* [Flutter Intl API Reference](https://marketplace.visualstudio.com/items?itemName=localizely.flutter-intl)

# `Flutter` 引入

`pubspec.yaml`:

```yaml
# pubspec.yaml
dependencies:
    # Other dependencies...
    flutter_localizations:
	    sdk: flutter

	# 第三方库
	intl: 0.17.0
```

`main.dart`:

```
// main.dart
return MaterialApp(
    localizationsDelegates: const [
        S.delegate,
        GlobalMaterialLocalizations.delegate,
        GlobalWidgetsLocalizations.delegate,
        GlobalCupertinoLocalizations.delegate,
    ],
    supportedLocales: S.delegate.supportedLocales,
	locale: const Locale('en'), // 设置默认语言为 English
	// locale: const Locale('zh'),
);
```

## `IOS` 配置

`ios/Runner/Info.plist` 应加入以下配置:

```plist
<key>CFBundleLocalizations</key>
<array>
	<string>en</string>
	<string>zh_HK</string>
</array>
```

其中: 文本 `en` 和 `zh_HK` 与文件名 `lib/l10n/intl_en.arb` 和 `lib/l10n/intl_zh_HK.arb` 一致。

# `VS Code`

`Ctrl Shift P (Windows)` 或 `Command Shift P (MacOS)` 打开命令面板, 输入 `Flutter Intl: Initialize` 即可创建如下目录结构:

```bash
lib/l10n/intl_en.arb
lib/generated
```

# `切换语言`

```dart
S.load(Locale('en')); // 切换至英文
S.load(Locale('zh', 'HK')); // 切换至繁体中文
S.load(Locale('de', 'DE')); // 切换至德文
```

# `获取当前语言`

```dart
Intl.getCurrentLocale();
```

# `获取国际化文本`

```dart
// 传入 context
S.of(context).example;
// 不传入 context
S.current.example;
```