---

copyright:
  years: 2015, 2016
lastupdated: "2016-12-01"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}

# 安装 {{site.data.keyword.mobileanalytics_short}} 客户端 SDK
{: #mobileanalytics_sdk}

目前，Android、iOS、WatchOS 和 Cordova 可以使用 {{site.data.keyword.mobileanalytics_short}} 客户端 SDK。
{: #shortdesc}

## 安装 Android 客户端 SDK
{: #install-sdk-android}

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.ibm.mobilefirstplatform.clientsdk.android/analytics/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.ibm.mobilefirstplatform.clientsdk.android/analytics)

{{site.data.keyword.mobileanalytics_short}} 客户端 SDK 通过 Gradle 进行分发；Gradle 是用于 Android 项目的依赖关系管理器。Gradle 会自动从存储库下载工件，并将其提供给 Android 应用程序。

1. 创建 [Android Studio](http://developer.android.com/sdk/index.html) 项目或打开现有项目。

2. 打开**应用程序模块**中的 `build.gradle` 文件。

  **提示**：Android 项目可能具有两个 `build.gradle` 文件：一个用于项目，另一个用于应用程序模块。请确保使用**应用程序模块**文件。

3. 找到 `build.gradle` 文件的 `Dependencies` 部分，并添加 {{site.data.keyword.mobileanalytics_short}} 客户端 SDK 的编译依赖关系。您的存储库语句应该类似下列代码示例：

	```
      dependencies {
        compile 'com.ibm.mobilefirstplatform.clientsdk.android:analytics:1.+'
    	// other dependencies  
      }
  ```
  	{: codeblock}

4. 通过单击**工具 &gt; Android &gt; 使用 Gradle 文件同步项目**来使用 Gradle 同步项目。

5. 打开 Android 项目的 `AndroidManifest.xml` 文件。您可以在**应用程序 > 清单**中找到此文件。在 `<manifest>` 元素下添加因特网访问许可权：

	```
	 <uses-permission android:name="android.permission.INTERNET" />
   ```
   {: codeblock}
   
6. 您现在已安装 Android 客户端 SDK。接下来，[导入并初始化](sdk.html#initalize-ma-sdk) Analytics 客户端 SDK。   

## 安装 Swift SDK
{: #installing-sdk-ios}

![与 CocoaPods 兼容](https://img.shields.io/cocoapods/v/BMSAnalytics.svg)

使用 {{site.data.keyword.mobileanalytics_full}} SDK，您可以检测移动应用程序。iOS 和 watchOS 可以使用 Swift SDK。

### 开始之前
{: #before-you-begin-ios}

确保正确设置 Xcode。要了解如何设置 iOS 开发环境，请参阅 [Apple 开发人员 Web 站点](https://developer.apple.com/support/xcode/)。阅读客户端 SDK Swift Analytics 的 [Xcode 需求](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-swift-analytics/tree/development#requirements)。

{{site.data.keyword.mobileanalytics_short}} SDK 通过 [CocoaPods](https://cocoapods.org/) 和 [Carthage](https://github.com/Carthage/Carthage#getting-started) 进行分发，它们是用于 Cocoa 项目的依赖关系管理器。CocoaPods 和 Carthage 会自动从存储库下载工件，并将其提供给您的应用程序。选择 CocoaPods 或 Carthage：

#### CocoaPods
{: #cocoapods}

1. 遵循 GitHub 上的 [{{site.data.keyword.Bluemix_notm}} Mobile Services Swift SDK 指示信息](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-swift-analytics/tree/development#cocoapods)以使用 Cocoapod 安装 `BMSAnalytics` 并将其添加到您的 Podfile。 
	
2. 在已安装 iOS 客户端 SDK 之后，[导入并初始化](sdk.html#initalize-ma-sdk) Analytics 客户端 SDK。   

#### Carthage
{: #carthage}

如果您没有使用 CocoaPods，您可以使用 [Carthage](https://github.com/Carthage/Carthage#if-youre-building-for-ios-tvos-or-watchos) 将框架添加到项目。

1. 遵循 GitHub 上的 [Carthage 安装指示信息](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-swift-analytics/tree/development#carthage)以安装 `BMSAnalytics`。

2. 在已安装 iOS 客户端 SDK 之后，[导入并初始化](sdk.html#initalize-ma-sdk) Analytics 客户端 SDK。

## 安装 Cordova 插件
{: #installing-sdk-cordova}

使用 {{site.data.keyword.mobileanalytics_full}} Cordova 插件，您可以检测移动应用程序。 

1. 将 Android 和 iOS 平台添加到您的 Cordova 应用程序。从命令行运行以下一个或全部两个命令：
   
   Android：

	 ```
	 cordova platform add android
```
	 {: codeblock}
	
   iOS：
   	
	```
	cordova platform add ios
```
   {: codeblock}
	
2. 如果您已添加了 Android 平台，您必须向 Cordova 应用程序的 `config.xml` 文件添加支持的最低 API 级别。打开 `config.xml` 文件，并将以下行添加到 `<platform name="android">` 元素：

	```
	<platform name="android">  
  	<preference name="android-minSdkVersion" value="15"/>
  	<preference name="android-targetSdkVersion" value="23"/>
  	<!-- add minimum and target Android API level declaration -->
  	</platform>
	```
   {: codeblock}

 *minSdkVersion* 值必须高于 `15`。请参阅 [Android 平台指南](https://cordova.apache.org/docs/en/latest/guide/platforms/android/)以了解 Android SDK 的最新受支持 *targetSdkVersion* 。


3. 如果已添加了 iOS 操作系统，使用目标声明更新 `<platform name="ios">` 元素：

	```
	<platform name="ios">
    <preference name="deployment-target" value="8.0"/>
     <!-- add deployment target declaration -->
  	</platform>
	```
	{: codeblock}

4. 安装 {{site.data.keyword.mobileanalytics_short}} Cordova 插件。当前支持 Cordova-CLI V6.3.0 或更低版本：

 	```
	cordova platform add android@5.2.2
	```
	{: codeblock}

5. 通过运行以下命令验证插件是否安装成功：
	
	```
	cordova plugin list
	```
	{: codeblock}
	
6. 您现在已安装 Cordova 插件。接下来，[导入并初始化](sdk.html#initalize-ma-sdk) Analytics 客户端 SDK。

# 相关链接

## SDK
* [Android SDK](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-android-analytics){: new_window}  
* [iOS SDK](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-swift-analytics){: new_window}
* [Cordova 插件核心 SDK](https://www.npmjs.com/package/bms-core){: new_window}

## API 参考
{: #api}
* [REST API](https://mobile-analytics-dashboard.{DomainName}/analytics-service/){:new_window}
