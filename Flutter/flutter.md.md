# 强制横屏

```dart
// 这一行必加, 否则报错
WidgetsFlutterBinding.ensureInitialized();

//强制竖屏
SystemChrome.setPreferredOrientations([ 
DeviceOrientation.portraitUp, 
DeviceOrientation.portraitDown ]);

//强制横屏
SystemChrome.setPreferredOrientations([ 
DeviceOrientation.landscapeLeft, 
DeviceOrientation.landscapeRight ]);
```

# 获取当前屏幕方向

```dart
// 1. 媒体查询
MediaQuery.of(context).orientation;

// 2. OrientationBuilder
// orientation 取值: Orientation.portrait / Orientation.landscape
OrientationBuilder(
  builder: (context, orientation) {
    return GridView.count(
      // Create a grid with 2 columns in portrait mode,
      // or 3 columns in landscape mode.
      crossAxisCount: orientation == Orientation.portrait ? 2 : 3,
    );
  },
),
```

参考链接:

[Update the UI based on orientation](https://docs.flutter.dev/cookbook/design/orientation)
[OrientationBuilder class](https://api.flutter.dev/flutter/widgets/OrientationBuilder-class.html)
[Screen Orientation In Flutter](https://medium.flutterdevs.com/screen-orientation-in-flutter-96526f2c1e7f)
[OrientationBuilder - Flutter | 老孟](http://laomengit.com/flutter/widgets/OrientationBuilder.html#orientationbuilder)

# 获取页面宽度和高度

```dart
// 宽度
MediaQuery.of(context).size.width;
// 高度
MediaQuery.of(context).size.height;
```

# 隐藏页面的几种方式

## `Opacity`

## `Offstage`

## `Visibility`

## `if (condition)`

参考链接:

[Visibility vs Offstage vs Opacity, which is best in hiding a child from widget tree?](https://stackoverflow.com/questions/62355547/visibility-vs-offstage-vs-opacity-which-is-best-in-hiding-a-child-from-widget-t)

# Stack Layout

[层叠布局](https://book.flutterchina.club/chapter4/stack.html#_4-6-%E5%B1%82%E5%8F%A0%E5%B8%83%E5%B1%80-stack%E3%80%81positioned)

# 运行至 `web`

```dart
flutter run -d chrome
```
