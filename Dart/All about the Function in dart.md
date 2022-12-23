[Functions - dart.dev](https://dart.dev/guides/language/language-tour#functions)
[Function class - api.dart.dev](https://api.dart.dev/stable/2.18.5/dart-core/Function-class.html)

# 基本结构

## 普通函数

```dart
// 判断输入参数是否为 null
bool isNull(dynamic parameter) {
	return parameter == null;
}
// 上面的 bool 和 dynamic 类型标注可省略, dart 会自动推断其类型
isNull(parameter) {
	return parameter == null;
}
```

类比 `JavaScript`:

```JavaScript
function isNull(parameter) {
	return parameter === null;
}
```

## 箭头函数 (`arrow syntax`)

```dart
// 判断输入参数是否为 null
bool isNull(dynamic parameter) => parameter == null;
```

箭头函数是一种简写语法, 箭头函数内只能有一个语句 (`experssion`) 而不能是一个块 (`statement`), 以下写法有误:

```dart
// A value of type 'Set<bool>' can't be returned from the function 'isNull'
// because it has a return type of 'bool'.
bool isNull(dynamic parameter) => {
	return parameter == null;
}
```

类比 `JavaScript`:

```JavaScript
// 省略大括号
const isNull = (parameter) => parameter === null;
// 不省略大括号
const isNull = (parameter) => {
	return parameter === null;
}
```