## React Native

#### React-native Android SDK Error: 
When you start to new project in react native, if you want run in your android device you will be greeted with an error like this: 
_`SDK location not found. Define location with an ANDROID_SDK_ROOT environment variable or by setting the sdk.dir path in your project's local properties file at '...'`_
The solution is very simple. All you have to do is create a file `local.properties` in the `android/` folder in the main directory of the project and write the following: 
_`sdk.dir = /Users/[USERNAME]/Library/Android/sdk`_
