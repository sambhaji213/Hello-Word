# Hello-Word
This article will guide you to create your first Android application. This application called "Hello World"
Let us start actual programming with Android Framework. Before you start writing your first example using Android SDK, you have to make sure that you have set-up your Android development environment properly as explained in Android - Environment Set-up tutorial. I also assume that you have a little bit working knowledge with Android studio.

So let us proceed to write a simple Android Application which will print "Hello World!".

<h2>Create Android Application</h2>
The first step is to create a simple Android Application using Android studio. When you click on Android studio icon, it will show screen as shown below
<br><br>
<a href="url"><img src="https://github.com/sambhaji213/Hello-Word/blob/master/screenshot/studio1.jpg" ></a>
<br><br>
You can start your application development by calling start a new android studio project. in a new installation frame should ask Application name, package information and location of the project.−
<br><br>
<a href="url"><img src="https://github.com/sambhaji213/Hello-Word/blob/master/screenshot/studio2.jpg" ></a>
<br><br>
After entered application name, it going to be called select the form factors your application runs on, here need to specify Minimum SDK, in our tutorial, I have declared as API23: Android 6.0(Mashmallow) −
<br><br>
<a href="url"><img src="https://github.com/sambhaji213/Hello-Word/blob/master/screenshot/studio3.jpg" ></a>
<br><br>
The next level of installation should contain selecting the activity to mobile, it specifies the default layout for Applications.
<br><br>
<a href="url"><img src="https://github.com/sambhaji213/Hello-Word/blob/master/screenshot/studio4.jpg" ></a>
<br><br>
At the final stage it going to be open development tool to write the application code.
<br><br>
<a href="url"><img src="https://github.com/sambhaji213/Hello-Word/blob/master/screenshot/studio5.jpg" ></a>
<br><br>
<h3>Anatomy of Android Application</h3>
Before you run your app, you should be aware of a few directories and files in the Android project −
<br><br>
<a href="url"><img src="https://github.com/sambhaji213/Hello-Word/blob/master/screenshot/studio6.jpg" ></a>
<br><br>

Sr.No. | Folder, File & Description
------------ | -------------
1 | <b>Java</b><br> This contains the .java source files for your project. By default, it includes an MainActivity.java source file having an activity class that runs when your app is launched using the app icon.
2 | <b>res/drawable-hdpi</b><br>This is a directory for drawable objects that are designed for high-density screens.
3 | <b>res/layout</b><br>This is a directory for files that define your app's user interface.
4 | <b>res/values</b><br>This is a directory for other various XML files that contain a collection of resources, such as strings and colours definitions.
5 | <b>AndroidManifest.xml</b><br>This is the manifest file which describes the fundamental characteristics of the app and defines each of its components.
6 | <b>Build.gradle</b><br>This is an auto generated file which contains compileSdkVersion, buildToolsVersion, applicationId, minSdkVersion, targetSdkVersion, versionCode and versionName
<br>

**MainActivity**
```<java>
package com.sambhaji.helloworld;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
   @Override
   protected void onCreate(Bundle savedInstanceState) {
      super.onCreate(savedInstanceState);
      setContentView(R.layout.activity_main);
   }
}
```

**Manifest File**
```<java>
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.sambhaji.helloword">

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/AppTheme">
        <activity
            android:name=".MainActivity"
            android:label="@string/app_name"
            android:theme="@style/AppTheme.NoActionBar">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```
**activity_main.xml**
```<xml>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
   xmlns:tools="http://schemas.android.com/tools"
   android:layout_width="match_parent"
   android:layout_height="match_parent" >
   
   <TextView
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"
      android:layout_centerHorizontal="true"
      android:layout_centerVertical="true"
      android:padding="@dimen/padding_medium"
      android:text="@string/hello_world"
      tools:context=".MainActivity" />
      
</RelativeLayout>
```

This is an example of simple RelativeLayout which we will study in a separate chapter. The TextView is an Android control used to build the GUI and it have various attributes like android:layout_width, android:layout_height etc which are being used to set its width and height etc.. The @string refers to the strings.xml file located in the res/values folder. Hence, @string/hello_world refers to the hello string defined in the strings.xml file, which is "Hello World!".

**Running the Application**
Let's try to run our Hello World! application we just created. I assume you had created your AVD while doing environment set-up. To run the app from Android studio, open one of your project's activity files and click Run Eclipse Run Icon icon from the tool bar. Android studio installs the app on your AVD and starts it and if everything is fine with your set-up and application, it will display following Emulator window −

<br><br>
<a href="url"><img src="https://github.com/sambhaji213/Hello-Word/blob/master/screenshot/device-2017-04-21-104901.png" align="left" height="480" width="250"></a>
<br><br>
