This repo offers a runnable React Native project. The setup is performed following the [official instruction](https://github.com/facebook/react-native/wiki/Building-from-source). Issues found are also fixed along the way.

To made the current project runnable, please remove the following line 

```
task packageReactNdkLibs(dependsOn: buildReactNdkLib, type: Copy) {
    from("$buildDir/react-ndk/all")
    into("$buildDir/react-ndk/exported")
    exclude("**/libjsc.so")  <-----------------------remove this line
}
in build.gradle of ReactAndroid project
```

from `build.gradle` of `ReactAndroid` project

2019-6-7

