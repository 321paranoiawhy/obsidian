
# Callable Class

[Callable classes - dart.dev](https://dart.dev/guides/language/language-tour#callable-classes)

Implement `call()` method:

```dart
class CallableClass {
	String call(String a, String b, String c) => "$a $b $c!";
}

void main() => print(CallableClass()("Hi", "there", "dart"));
```