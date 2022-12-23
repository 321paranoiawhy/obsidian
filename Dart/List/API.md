# 创建列表

```dart
// 1. 字面量
List list = []; // 创建空列表
List list = [0, 1, 2]; // 创建带初始值的列表

// 2. List constructor 构造器
// https://api.flutter.dev/flutter/dart-core/List/List.html
List(3); // 创建固定长度 3 的列表: [null, null, null]

// 3. List.filled
// https://api.flutter.dev/flutter/dart-core/List/List.filled.html
List<int>.filled(3, 0); // 创建固定长度 3 且元素均为 0 的列表: [0, 0, 0]
List<int>.filled(3, 0, true);// 创建当前长度 3 且元素均为 0 的列表 (长度可变): [0, 0, 0]

// 4. List.from
// https://api.flutter.dev/flutter/dart-core/List/List.from.html
List.from([1, "2", "3", 4]); // [1, "2", "3", 4]

// 5. List.of
// https://api.flutter.dev/flutter/dart-core/List/List.of.html
List.of([1, "2", "3", 4]); // [1, "2", "3", 4]

// 5. List.generate
// https://api.flutter.dev/flutter/dart-core/List/List.generate.html
List.generate(3, (value) => value + 1); // [1, 2, 3]

// 6. List.unmodifiable
// https://api.flutter.dev/flutter/dart-core/List/List.unmodifiable.html
List.unmodifiable([1, 2, 3]); // (长度和元素) 不可变列表: [1, 2, 3]
```

```ad-note
List constructor cannot be used in null-safe code.
列表构造器不能在空安全代码中使用, 否则会报错 `Error: Can't use the default List constructor.`
```

# 获取元素

```dart
List list = [1, 2, 3, 4];

// first
list.first; // 1
// last
list.last; // 4
```

# 获取长度及判空

```dart
List list = [1, 2, 3, 4];

list.length; // 4
list.isEmpty; // false 等价于 list.length == 0
list.isNotEmpty; // true  等价于 list.length != 0
```

# 获取哈希值

```dart
List list = [1, 2, 3, 4];

// https://api.flutter.dev/flutter/dart-core/Object/hashCode.html
list.hashCode; // 714804807 (形如此)
```

# 添加元素

```dart
List list = [];
// 添加 1 至列表末尾
list.add(1); // [1]
// 添加 2 至列表末尾
list.insert(1, 2); // [1, 2]
// 添加 0 至列表开头
list.insert(0, 0); // [0, 1, 2]

// 添加多个元素
list.addAll([3, 4, 5]); // [0, 1, 2, 3, 4, 5] 类似 js 的 concat 方法
```

# 交换两个元素

```dart
List list = [1, 2];

// 1. temp 临时变量
int temp = list[0];
list[0] = list[1];
list[1] = temp;

// 2. removeAt + insert
list.insert(1, list.removeAt(0)); // list.insert(0, list.removeAt(1));
```