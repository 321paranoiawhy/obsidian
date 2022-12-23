
#  100.w / 100.sw

	根据当前屏幕宽度适配尺寸

```dart
// 效果同 100.w / 100.sw
ScreenUtil().setWidth(100);
```

```dart
// 获取屏幕宽度
ScreenUtil().screenWidth;
MediaQuery.of(context).size.width;
```

# 100.h / 100.sh

	根据当前屏幕高度适配尺寸

```dart
// 效果同 100.h / 100.sh
ScreenUtil().setHeight(100);
```

```dart
// 获取屏幕宽度
ScreenUtil().screenHeight;
MediaQuery.of(context).size.height;
```

# 100.r

	根据当前屏幕宽度和高度的较小值适配尺寸: min(width, height)

# 100.sp

	适配字体大小

# 比例

```dart
ScreenUtil().scaleWidth;
ScreenUtil().scaleHeight;
```