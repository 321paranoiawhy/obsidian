# `Numbers`

`Numbers` 可由 `num` 、 `int` 和 `double` 定义, 其中 `num` 包含 `int` 整形 和 `double` 浮点数两种类型:

```dart
num a = 1;
int b = 1;
double c = 1.0;
```

```ad-note
`int` 和 `double` 是 `num` 的子类。
```

# `String`

```dart
String a = 'a';
String b = "b";

String c = 'c"c"';
String d = 'd"d"';
// 多行字符串
String e = '''
e
e
''';
String f = """
f
f
""";
```

# `bool`

`bool` 包含 `true` 和 `false`:

```dart
bool a = true;
bool b = false;
```

# `List`

```dart
List list = [1, 2, 3];
list is List; // true
```

# `Map`

```dart
Map map = {
	"name": "unknown",
};
map is Map; // true
```

# `Set`

`Set` 类似数学中的集合, 其元素不可重复:

```dart
Set<String> set = {"name", "age"};
```

# `Queue`

```dart
import 'dart:collection';
```

# `Symbol`

```dart
// # 符号声明, 自动转换为 Symbol
#symbolOne;
#symbolOne is Symbol; // true
Symbol symbolTwo = Symbol("symbolTwo");
symbolTwo is Symbol; // true
```

# `Enum`

```dart
enum Status { 
   none, 
   running, 
   stopped, 
   paused 
}

// 获取 running 的索引
Status.running.index; // 1
// 获取所有枚举值
Status.values; // [Status.none, Status.running, Status.stopped, Status.paused]
Status.values is List; // true

var running = Status.running;
switch(running) {
	case none: print("none");
	break;
	case running: print("running");
	break;
	case stopped: print("stopped");
	break;
	case paused: print("paused");
	break;
} // running
```

枚举类型有如下限制:

* 不能子类化 (`subclass`)，混合 (`mixin`) 或实现 (`implement`) 枚举;
* 不能显式实例化一个枚举类。

# 类型检查

```dart
int a = 1;
// is
print(a is int); // true
// is !
print(a is !String); // true
```