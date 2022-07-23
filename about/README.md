## The arb file format
* [https://github.com/google/app-resource-bundle/wiki/ApplicationResourceBundleSpecification]

## Errors when we send a request
* So the error we give when the status code is 400 bad request
* It looks like
```json
{
  "errors": [
    "[!] The errors we give when the status code is 400 Bad request",
    "This password is not valid",
    "device_name field must be provided",
    "Password is not more than 7 chars"
  ]
}
```

## How to get app theme mode
```dart
// no context
var brightness = SchedulerBinding.instance!.window.platformBrightness;
bool isDarkMode = brightness == Brightness.dark;

// with context
var brightness = MediaQuery.of(context).platformBrightness;
bool isDarkMode = brightness == Brightness.dark;
```


## If i want add a new method for type String or any other type i can use:
```dart
extension EmailValidator on String {
  bool isValidEmail() {
    return !RegExp(
            r'^(([^<>()[\]\\.,;:\s@\"]+(\.[^<>()[\]\\.,;:\s@\"]+)*)|(\".+\"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$')
        .hasMatch(this);
  }
}
```


