---

copyright:
  years: 2016, 2017
lastupdated: "2017-01-17"

---
{:new_window: target="_blank"}

# What's new in the Mobile dashboard
{: #what_is_new}

### New as of: December 2016
{: #dec-2016}

The December 2016 update of the {{site.data.keyword.Bluemix}} Mobile dashboard introduced the following changes:

   * You can remove a connected service from a project so it can be deleted or reused with another project. 
   * You can add an existing service to a project.
   * You can create or connect an existing CloudantNoSQL service as a data source when you use a code starter.
   * Where it is supported, you can create or connect an existing Object Storage service as a data source for your project.
   * You can customize the navigation design of the app that you are creating with a UI starter. 
   

### New as of: November 2016
{: #nov-2016}

The November 2016 update of the {{site.data.keyword.Bluemix}} Mobile dashboard introduced the following changes:

   * You can now generate SDK artifacts for your projects from the **Code** page.
   * Cordova is now supported for the Basic Code Starter.
   * You can now [report network events ![External link icon](../icons/launch-glyph.svg "External link icon")](/docs/services/mobileanalytics/sdk.html#network-requests){: new_window} and [monitor network requests ![External link icon](../icons/launch-glyph.svg "External link icon")](/docs/services/mobileanalytics/app-monitoring.html#monitor-network-requests){: new_window} in the **Network Requests** page of the {{site.data.keyword.mobileanalytics_short}} Console.
   * You can now [export data to dashDB ![External link icon](../icons/launch-glyph.svg "External link icon")](/docs/services/mobileanalytics/app-monitoring.html#dashdb){: new_window} in the {{site.data.keyword.mobileanalytics_short}} Console.


### New as of October 2016
{: #oct-2016}

The October 2016 update of the {{site.data.keyword.Bluemix_notm}} Mobile dashboard introduced the following changes:

   * You can now add {{site.data.keyword.mobilepushshort}} and Analytics capabilities to your project directly from the dashboard.
   * [Code Starters](starters.html#Code_Starter) are now available.
   * You can add Authentication to your projects that you created from a Code Starter.
   * Swift is now supported.


#### Analytics
{: #analytics}

   * Demo mode is enabled by default when you add the Analytics capability. You can toggle off demo mode to view your analytics after you run your app.


#### UI Builder
{: #ui_builder}

   * The **{{site.data.keyword.mobilepushshort}}** capability is now accessed from the project.
   * The **Project Settings** tab has been renamed to the **Settings** tab.
   * The **Authentication** tab has been renamed to **User Access** tab.


#### Code
{: #code}

   * The generated Objective-C and Swift code for iOS now uses CocoaPods to manage dependencies. This means that you need to install CocoaPods. To install it, run `sudo gem install cocoapods`. After CocoaPods is installed, run `pod setup` to configure it (if not configured already). Finally, run `pod install` to download and install the required project dependencies prior to opening your `.xcworkspace` file in Xcode. Additional details are available in the `README.md` file in the downloaded code archive. Read about [Prerequisite Developer Tools](get_code.html#prereq-dev-tools) for more information.

Check back often to stay current with new updates.
