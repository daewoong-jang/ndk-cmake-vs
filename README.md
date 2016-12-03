# ndk-cmake-vs
Demonstrates buiilding a multi-platform Android NDK development environment using CMake and Visual Studio. The project is derived from old Android NDK sample `hello-jni`.

## Prerequisite
* CMake - 3.3.2 or later.
* Android NDK - r12b. r13 is not tested.
* Android SDK
* Java JDK
* Apache Ant
* Nsight Tegra - 3.4, For Windows development.
* Visual Studio 2015 - For Windows.

## Running CMake
From command line, do something like below:
```
set ANDROID_NDK=<path-to-android-ndk>
set ANDROID_SDK=<path-to-android-sdk>
set APACHE_ANT=<path-to-apache-ant>
mkdir build
cd build
cmake -DCMAKE_TOOLCHAIN_FILE=..\android.toolchain.cmake -DCMAKE_BUILD_TYPE=Debug -DANDROID_NATIVE_API_LEVEL=17 -DANDROID_TOOLCHAIN_NAME=clang -DANDROID_ABI="armeabi-v7a with NEON" ..
```
