#JSON #dart

# `decode`

`JSON` 处理工具位于 `Dart` 的核心库 `convert` 中, 使用前需引入:

```
// 引入 convert 库
import 'dart:convert';
```

```dart
// 引入 convert 库
import 'dart:convert';

String data = '{ "name": "Pizza da Mario", "cuisine": "Italian"}';

// {name: Pizza da Mario, cuisine: Italian}
print(json.decode(data));
print(jsonDecode(data));
print(json.decode(data) is Map); // true
print(json.decode(data)["name"]); // Pizza da Mario
```

## Reference

* [JsonDecoder class - api.dart.dev](https://api.dart.dev/stable/2.18.5/dart-convert/JsonDecoder-class.html)

# `encode`

```dart
// 引入 convert 库
import 'dart:convert';

Map data = { "name": "Pizza da Mario", "cuisine": "Italian"};

// {"name":"Pizza da Mario","cuisine":"Italian"}
print(json.encode(data));
print(jsonEncode(data));
print(json.encode(data) is String); // true

// {name: Pizza da Mario, cuisine: Italian}
print(data.toString());
```

## Reference

* [JsonEncoder class - api.dart.dev](https://api.dart.dev/stable/2.18.5/dart-convert/JsonEncoder-class.html)

# Reference

* [dart:convert library - api.dart.dev](https://api.dart.dev/stable/2.18.5/dart-convert/dart-convert-library.html)
* [How to Parse JSON in Dart/Flutter: The Essential Guide](https://codewithandrea.com/articles/parse-json-dart/)