# `?`

`A?`, 定义可空变量, 初始值为 `null`:

```dart
String? str; // 等价于 String str = null;
print(str); // null
```

# `?:`

==ternary operator==

`A ? B : C`, 如果 `A` 不为 `null`, 返回 `B`, 否则返回 `C`:

```dart
void main() {
	String isNull(dynamic parameter) {
		return parameter == null ? "$parameter is null." : "$parameter is not null.";
	}
	print(isNull(null)); // null is null.
	print(isNull([])); // [] is not null.
}
```

# `?.`

==null-aware access==

[Dart 1.12 Released, with Null-Aware Operators and more](https://news.dartlang.org/2015/08/dart-112-released-with-null-aware.html)

`A?.B`, 如果 `A` 为 `null`, 返回 `A`, 否则返回 `A.B`:

```dart
class Person {
	final String name;
	Person(this.name);
};

void main() {
	Person person = Person("admin");
	
	print(person.name); // admin
	
	// The receiver can't be null, so the null-aware operator '?.' is unnecessary.
	// Try replacing the operator '?.' with '.'.
	// dart[invalid_null_aware_operator](https://dart.dev/diagnostics/invalid_null_aware_operator)
	print(person?.name); // admin
	
	// The getter 'age' isn't defined for the type 'Person'
	// Try importing the library that defines 'age', correcting the name to the name of an existing getter, or defining a getter or field named 'age'.
	// dart[undefined_getter](https://dart.dev/diagnostics/undefined_getter)
	print(person.age);
	
	// print(person?.age);
}
```

==null-aware method invocation==

`A?.B()`, 如果 `A` 为 `null`, 返回 `A`, 否则返回 `A.B()`:

# `??`

==if null operator==

`A??B`, 如果 `A` 为 `null`, 返回 `B`, 否则返回 `A`:

```dart
void main() {
	String? isNull; // isNull 被初始化为 null; 如无再次赋值, isNull 将始终为 null
	String isNotNull = "is not null";
	print(isNull ?? "is null"); // is null
	print(isNotNull ?? "is null"); // is not null
}
```

# `??=`

==null-aware assignment==

`A ??= B`, 如果 `A` 为 `null`, 则将 `B` 赋值给 `A`, 否则 `A` 仍为原来的值 `A`:

```dart
void main() {
	String? isNull; // isNull 被初始化为 null; 如无再次赋值, isNull 将始终为 null
	String isNotNull = "is not null";
	isNull ??= "new value"; // isNull = "new value"
	isNotNull ??= "new value"; // do nothing
	print(isNull); // new value
	print(isNotNull); // is not null
}
```

# `...?`

==null-aware spread operator==

[Spread Collections - spread operator proposal](https://github.com/dart-lang/language/blob/master/accepted/2.3/spread-collections/feature-specification.md)

```dart
void main() {
	List? nullList; // null list
	List nonNullableList = [1, 2, 3];
	print([0, ...?nullList]); // [0]
	print([0, ...nonNullableList]); // [0, 1, 2, 3]
}
```

# `?..`

==null-shorting cascade== 

```ad-tip
`null-shorting cascade` 需要 `dart` 版本不低于 `2.12`.
```

[Language versioning - dart.dev](https://dart.dev/guides/language/evolution#language-versioning)

```dart
void main() {
	List? nullList;
	
	nullList?..add(1)..add(2);
	print(nullList); // null
	
	List nonNullableList = [];
	
	nonNullableList?..add(1)..add(2);
	print(nonNullableList); // [1, 2]
}
```

# Reference

[what are the double question marks in dart - stackoverflow](https://stackoverflow.com/questions/54031804/what-are-the-double-question-marks-in-dart/54031805#54031805)