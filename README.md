## Android App Base template
When you're starting to write  an app, there are certain classes, methods and lines of code you
implement over and over. So, I thought I should have base template usable across all my apps.
I hope to write an Android Studio plugin to generate this automatically later in the future.

This template contains some of my favourite packages, config, classes and  methods.
In my research, I found alot of boiler plate templates, some of which I adapted some techniques
and structures from. This is still under development, and many ideas were sourced from various places.


##Features

1. Dependency Injection using Dagger: This section is still not fully developed;
I'm just wrapping my head around DI with dagger
2. `Navigator` class to handle Navigation.
3. `MediaPickerFragment` (with Android Marshmallow Permission).
4. Base classes - `BaseActivity`, `BaseFragment`, `BasePresenter`
6. Util classes & methods
  1. `AppUtils` with the following util methods:
        1. `getAppVersion()`
        2. `isTablet()`
        3. `isServiceRunning()`
        4. `hideKeyboard()`
  2. `BitmapUtils` with the following util methods:
        1. `decodeBitmapFromStream()`
        2. `calculateInSampleSize()`
  3. `DateUtils` with the following util methods:
        1. `getDay()`
        2. `getMonthShort()`
        3. `getMonth()`
  4. `DeviceUuidFactory` to retrieve the device id of the device.
  5. `DialogUtils`
  6. `ListUtils`
  7. `Logger` - for logging. Different from `android.util.Log` by a flag `DEBUG_ON` which you can use to toggle whether or not you want to show the log
  8. `NetworkUtils` with the following util methods:
        1. `isNetworkConnected()`
  9. `PreferenceUtils` - very much like a Preference manager for your SharedPreferences
  10. `StringUtils` - String utils with the following util methods:
        1. `isEmpty()` - that returns true if the String is null, empty or "null"
        2. `nullify()` - to return the value of a string or null if the string is empty
  11. `UriUtils` - utils to convert a URI to a file path. This is useful when you're picking files from the device.
  File picking is fragmented and occurs differently on different versions of Android.
  This class helps to convert such into file paths.

##Usage
This part is still work in progress :)

##Todo
1. Add Usage
2. Add testing templates
3. Write AndroidStudio/IntelliJ template to automatically crate this, with the correct package name
