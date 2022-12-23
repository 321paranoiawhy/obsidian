#TextField
# `controller`

[TextEditingController class - api.dart.dev](https://api.flutter.dev/flutter/widgets/TextEditingController-class.html)

```dart
// 定义一个 TextEditingController
TextEditingController inputController = TextEditingController();

// 使用 inputController 作为 TextField 的 controller
TextField(controller: inputController)

// 清空输入框
inputController.clear();
// (getter) 获取输入框的值 (String 类型)
// https://api.flutter.dev/flutter/widgets/TextEditingController/text.html
inputController.text;
// (setter) 赋值 (如初始值、中间值)
inputController.text = "initial value";
// 获取选中的值
// https://api.flutter.dev/flutter/widgets/TextEditingController/selection.html
inputController.selection;
```

# `focusNode`

```dart
// 定义一个 FocusNode
FocusNode inputFocusNode = FocusNode();

// 使用 inputFocusNode 作为 TextField 的 focusNode
TextField(focusNode: inputFocusNode)

// 聚焦至当前输入框
inputFocusNode.requestFocus();
```

# Reference

* [Flutter 关于 TextField 你能知道的一切](https://juejin.cn/post/6844903889829888014)