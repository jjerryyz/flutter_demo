# flutter_demo

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.io/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.io/docs/cookbook)

For help getting started with Flutter, view our 
[online documentation](https://flutter.io/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.

#### 在国内安装flutter

国内下载flutter有专门的链接，并且需要对基础仓库源进行客制化，详情参考https://flutter.dev/community/china

下载完毕，按照



#### initialing gradle...一直不消失

原因是gradle没法下载成功，解决方法是:

- 离线下载 gradle-all.zip（尽量新的版本）

- 修改 <flutter_project>/android/gradlew.bat（windows用户使用.bat结尾的编译），修改两个地方的引用:

  - ```powershell
    @rem set CLASSPATH=%APP_HOME%\gradle\wrapper\gradle-wrapper.jar
    set CLASSPATH=D:\gradle-5.5.1\lib\gradle-launcher-5.5.1.jar
    ```

  - ```powershell
    @rem "%JAVA_EXE%" ... "%CLASSPATH%" org.gradle.wrapper.GradleWrapperMain ...
    "%JAVA_EXE%" ... "%CLASSPATH%" org.gradle.launcher.GradleMain ...
    ```

#### 选择正确的模拟器运行

为了方便调试，我们想在pc上的模拟器跑flutter程序，模拟器需要符合一下标准

根据这个[链接](https://developer.android.com/ndk/guides/abis)，我们的平台不能是x86的，因此网易的mumu就pass了

实测在genymotion平台上的虚拟机可以运行

