# How to connect your mobile to your laptop for debugging .NET MAUI Blazor application

https://developer.android.com/tools/adb#wireless-adb-android-11

To install and set up **Android Debug Bridge (adb)** for debugging a Flutter application on your mobile phone, follow these steps:

## 1. Step 1: Install Android Studio

Download and Install Android Studio: Download Android Studio from the official Android developer website

https://developer.android.com/studio

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/f86926a5-a306-4c66-85d8-0f808879eee9)

Install Android SDK: During the installation, ensure that the Android SDK is installed

We press in the three dots button and we select the option **SDK Manager**

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/dcff12f6-465d-4a56-83dc-5ccbd3e03778)

We have to select the **SDK Tools** tab and then install **Android SDK Command-Line Tools**

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/f55270bf-8ebf-4e78-b465-56d883f7a20f)

## 2. Step 2: Set Up adb

Open Android Studio:

Launch Android Studio and go to the **SDK Manager**

Navigate to **Configure > SDK Manager**

Install SDK Platform Tools:

In the SDK Manager, go to the **SDK Tools** tab

Check the box for **Android SDK Platform-Tools**

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/8c4a8152-757d-4c23-b967-51ca86c927ed)

Click **OK** to install the package

## 3. Step 3: Add adb to System PATH

Find adb Location:

The **adb** executable is located in the platform-tools directory inside the Android SDK directory

Common default paths:

**Windows: C:\Users\<Your-Username>\AppData\Local\Android\Sdk\platform-tools**

macOS: ~/Library/Android/sdk/platform-tools

Linux: ~/Android/Sdk/platform-tools

**Add to PATH**:

Windows:

Open Control **Panel > System and Security > System > Advanced system settings**

Click on **Environment Variables**

Under **System variables**, find the **Path** variable, and click **Edit**

Click New and add the path to the platform-tools directory

Click OK to save the changes

**C:\Users\luisc\AppData\Local\Android\Sdk\platform-tools**

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/e8decfb6-d6cf-4b33-86cf-188cf60fcc3a)

## 4. Step 4: Enable USB Debugging on Your Mobile Phone

We first press the **Settings** button

![image](https://github.com/user-attachments/assets/9f01744a-a79a-442f-8b2c-28c3b759461d)

We select the menu option **Settings/About the Phone**

![image](https://github.com/user-attachments/assets/0f9f1a03-e1a3-4cc8-944f-747b0c0a6481)

Then we select the option **Software Information**

![image](https://github.com/user-attachments/assets/6c95669c-49a2-45d5-ab97-3de98eeede1f)

For enabling the Develper options we have to tap on the **Build Number** sevent times:

![image](https://github.com/user-attachments/assets/2cdb8ac3-38e2-4fcf-a0b4-015d76120bb3)

We enter the Mobile device password if required

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/82f224aa-3de2-40d6-954c-d5bb8a7c7786)

We receive a message **Developer mode has been turned on**

![image](https://github.com/user-attachments/assets/4967a3a0-1d0a-4ed4-9164-649bd9ef3e3b)

Now we can verify the **Developer options** are available in our mobile phone:

![image](https://github.com/user-attachments/assets/33713972-6bff-445b-bd3c-06dd9a9d7c15)

We can **Enable USB Debugging**:

Go to **Settings > System > Developer** options

Enable **USB debugging**

![image](https://github.com/user-attachments/assets/459aeaae-b232-4337-aca6-e3e5a41de13b)

We also have to connect the Mobile to the Laptop with an **USB wire**

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/edbdda99-a8a9-4f6f-8f01-cf9ddf89115e)

We can also **revoke the USB debugging authorization** for detecting the mobile phone


And then accept the message in your mobile phone to authorize to connect the mobile to the laptop

## 5. Step 5: Verify adb Installation

Connect Your Phone:

Connect your Android phone to your computer using a **USB cable**

**Verify adb Connection**:

Open a terminal (Command Prompt on Windows, Terminal on macOS/Linux)

Run the following command:

```
adb devices
```

You should see your device listed. If prompted on your phone, **authorize the connection**

![image](https://github.com/luiscoco/Flutter_Connect_Mobile_lesson2/assets/32194879/e453ae4d-50bd-487c-9427-c9ff584b8627)

## 6. Step 6: Create in Visual Studio 2022 a MAUI Blazor Application

Build and Debug the mobile application

![image](https://github.com/user-attachments/assets/65cd1e77-b1fa-494a-b45b-487710e5b92a)

Before pressing the run button check the Configuration Manager options are set properly

![image](https://github.com/user-attachments/assets/8d59f4b6-1f31-4ade-acc7-76672add4823)

![image](https://github.com/user-attachments/assets/ce7fb95b-f235-41cc-b09d-ace2269f8f84)

After running the application you will see it in the Visual Studio IDE 

![image](https://github.com/user-attachments/assets/a94d18a0-e2f4-4869-a2f0-63e1e9b2788d)

Also see your application is running in your Mobile

![image](https://github.com/user-attachments/assets/54963291-ac4e-48b0-b5ca-8855c7b33836)


