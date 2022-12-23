# 导入

参考链接: [Add the http package - docs.flutter.dev](https://docs.flutter.dev/cookbook/networking/fetch-data#1-add-the-http-package)

```yaml
# pubspec.yaml

dependencies:
  flutter:
    sdk: flutter
  flutter_localizations:
    sdk: flutter
  http: 0.13.5 # http 包
```

```dart
// api.dart

// 导入
import 'package:http/http.dart' as http;
```

```xml
<!-- android/app/src/profile/AndroidManifest.xml -->
<!-- Required to fetch data from the internet. -->

<uses-permission android:name="android.permission.INTERNET" />
```

# `Uri`

```dart
String baseURL = "https://jsonplaceholder.typicode.com/posts";
Uri url = Uri.parse(baseURL);
```

# `FutureBuilder`

* [FutureBuilder class - api.dart.dev](https://api.flutter.dev/flutter/widgets/FutureBuilder-class.html)
* [Display the data - docs.flutter.dev](https://docs.flutter.dev/cookbook/networking/fetch-data#5-display-the-data)

```dart
FutureBuilder(
	future: _makeRequest,
	builder: (BuildContext context, AsyncSnapshot<String> snapshot) {
		if (snapshot.hasData) {
			return successWidget;
		} else if (snapshot.hasError) {
			return errorWidget;
		} else {
			return loadingWidget;
		}
	}
)
```


# `initState`

```dart
@override
void initState() {
	super.initState();
	_makeRequest();
}
```