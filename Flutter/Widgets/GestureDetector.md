#GestureDetector
# `behavior`

```dart
// https://api.flutter.dev/flutter/widgets/GestureDetector/behavior.html
// https://api.flutter.dev/flutter/rendering/HitTestBehavior.html
// behavior 可取值
// HitTestBehavior.deferToChild (child 不为 null 时 behavior 的默认值)
// HitTestBehavior.opaque
// HitTestBehavior.translucent (child 为 null 时 behavior 的默认值)

// 使空白处仍可响应点击事件
GestureDetector(
	behavior: HitTestBehavior.opaque,
)
```

# Reference

* [GestureDetector class - api.flutter.dev](https://api.flutter.dev/flutter/widgets/GestureDetector-class.html)