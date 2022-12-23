# `String` ↔ `int / double`

```dart
// String -> int
print(int.parse("1")); // 1 (整形 1)

// int -> String
print(1.toString()); // 1 (字符串 1)

// String -> double
print(double.parse("1.5")); // 1。5 (浮点数 1.5)

// double -> String
print(1.5.toString()); // 1.5 (字符串 1.5)

// 空字符串
// Unhandled exception:
// FormatException: Invalid number (at character 1)
print(int.parse(""));

// 含字母的字符串
// Unhandled exception:
// FormatException: Invalid radix-10 number (at character 1)
print(int.parse("a"));

// 解决方法
// 1. int.tryParse() / double.tryParse()

print(int.tryParse("")); // null

// 2. onError
// 'onError' is deprecated and shouldn't be used.
print(int.parse("", onError: (String source) {
	return 0;
})); // 0

// 3. try catch
try { 
	int.parse(""); 
} catch(err) { 
	print(0); 
} // 0

// 4. 事先判断字符串长度或非空
String str = "";
if(str.length != 0) {}
if(str.isNotEmpty) {}
if(!str.isEmpty) {}
```

# `int` ↔ `double`

```dart
// int -> double
print(1.toDouble()); // 1.0

// double -> int
print(1.2.floor()); // 1 (向下取整)
print(1.2.ceil()); // 2 (向上取整)

// 四舍五入
print(1.2.round()); // 1
print(1.8.round()); // 2
```

# `int / double` ↔ `BigInt`

[BigInt class - api.dart.dev](https://api.dart.dev/stable/2.18.5/dart-core/BigInt-class.html)

```dart
// int -> BigInt
print(BigInt.from(1)); // 1

// double -> BigInt
print(BigInt.from(1.2)); // 1
print(BigInt.from(1.8)); // 1

// BigInt -> int
print(BigInt.from(1).toInt()); // 1
print(BigInt.from(1).toDouble()); // 1.0
```