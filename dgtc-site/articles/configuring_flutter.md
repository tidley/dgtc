## Confirming Android licenses

### `flutter doctor --android-licenses` gives `Exception in thread "main" java.lang.NoClassDefFoundError:`

This is probably caused by Flutter not being able to find the java runtime.

Fix it by installing Java runtime 8 and in your `.bash-rc` file add these lines:

```
export JAVA_HOME='/usr/lib/jvm/java-8-openjdk/jre'
export PATH=$JAVA_HOME/bin:$PATH

export ANDROID_SDK_ROOT='/opt/android-sdk'
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools/
export PATH=$PATH:$ANDROID_SDK_ROOT/tools/bin/
export PATH=$PATH:$ANDROID_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/tools/
```

Arch Linux setup tips https://dev.to/awais/configure-flutter-development-environment-on-manjaro-arch-linux-4a0a

Helpful tips for telling Flutter where Android SDK lives https://stackoverflow.com/questions/62503437/unable-to-locate-android-sdk-for-flutter-doctor