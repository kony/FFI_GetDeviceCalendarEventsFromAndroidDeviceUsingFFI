# FFI_GetDeviceCalendarEventsFromAndroidDeviceUsingFFI
This application gets the calendar events from the device (Android device) calendar for a given date. It uses FFI to fetch the calendar events from the device

# To run this app

1. Download the project zip (FFICalendarEvent.zip) file.
2. Unzip the project to any folder
3. Launch Kony Visualizer Enterprise version 7.0.
4. Import the project by selecting the FFICalendarEvent folder.
5. Build & run the app for Android.
6. Click on a date in the calendar shown (Ensure you have some events created for that date using the device calendar application)
7. The list of events are shown below the calendar

# Supported platforms:
**Mobile**
 * Android

**Supported Kony Visualizer Enterprise Version:** 7.0

#Note
Native source code (Android studio project file) is available in CalendarLibApp.zip


# Important Notes if you want create a new FFI jar using Android Studio

Create a new application<br>
Create a new module (Choosing Android Library)<br>
If you need to obtain the application context:<br>
	Copy konywidgets.jar into libs folder<br>
	Use the following API to get the context object:<br>
        Context context = KonyMain.getAppContext();<br>
If there is a requirement of returning object containing another object or array of objects, please use vector of vectors as that is the only mechanism supported using FFI<br>

When you build the android studio project (with module), you would get .aar file<br>
Rename the .aar file to .zip file<br>
Extract the zip file<br>
The classes.jar file would be present in the extracted folder. This is the .jar that needs to be included in the Kony Application<br>
