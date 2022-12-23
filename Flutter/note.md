
# `!.`

```dart
Map testMap = {"A": "a", "B": "b", "C": "c"};
testMap!
```

# 定义可空变量 `null`

```dart
int intA = 1;
// 报错
intA = null;
// A value of type 'Null' can't be assigned to a variable of type 'int'.
// Try changing the type of the variable, 
// or casting the right-hand type to 'int'.
// dart[invalid_assignment](https://dart.dev/diagnostics/invalid_assignment)

// 正常运行
int? intB = 2;
intB = null;
```

# `operators`

[Operators - dart.dev](https://dart.dev/guides/language/language-tour#operators)