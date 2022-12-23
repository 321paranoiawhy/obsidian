#GET
# 无参数

[HTTP GET Response in Flutter - geeksforgeeks](https://www.geeksforgeeks.org/http-get-response-in-flutter/)

```dart
import 'dart:convert';

import 'package:http/http.dart' as http;

Future getPosts() async {
	String baseURL = "https://jsonplaceholder.typicode.com/posts";
	Uri url = Uri.parse(baseURL);
	var response = await http.get(url);
	print(response.statusCode);
	print(response.body);
	if(response.statusCode == 200) {
		return json.decode(response.body);
	}
	else {
		throw "Error";
	}
}
```

# 有参数

```dart
import 'dart:convert';

import 'package:http/http.dart' as http;

String token = "123456";
String contentType = "application/json";
var response = await http.get(baseURL, headers: {"token": token, "content-type": contentType});
```



