
# Ex.No:3 Create Your Own Content Providers to get Contacts details.


## AIM:

To create your own content providers to get contacts details using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “ex.no.3″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
Program to print the text create your own content providers to get contacts details.
Developed by:SAI ESWAR KANDUKURI
Registeration Number :212221240020
```
### MainActivity.java
```
package com.example.contentproviderapp;

import androidx.appcompat.app.AppCompatActivity;
import androidx.core.app.ActivityCompat;
import androidx.core.content.ContextCompat;

import android.Manifest;
import android.annotation.SuppressLint;
import android.content.ContentResolver;
import android.content.pm.PackageManager;
import android.database.Cursor;
import android.net.Uri;
import android.os.Bundle;
import android.provider.ContactsContract;
import android.util.Log;
import android.view.View;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


    }
    public void btnGetContacts(View v){
     getPhoneContacts();
    }
    private void getPhoneContacts(){
        if(ContextCompat.checkSelfPermission(this, Manifest.permission.READ_CONTACTS)!= PackageManager.PERMISSION_GRANTED){
            ActivityCompat.requestPermissions(this,new String[]{Manifest.permission.READ_CONTACTS},0);
        }
        ContentResolver contentResolver = getContentResolver();
        Uri uri = ContactsContract.CommonDataKinds.Phone.CONTENT_URI;
        Cursor cursor = contentResolver.query(uri,null,null,null,null,null);
        Log.i("CONTACT_PROVIDER","TOTAL # of CONTACTS ::: "+Integer.toString(cursor.getCount()));

        if(cursor.getCount()>0){
            while(cursor.moveToNext()){
                @SuppressLint("Range") String ContactName = cursor.getString(cursor.getColumnIndex(ContactsContract.CommonDataKinds.Phone.DISPLAY_NAME));
                @SuppressLint("Range") String contactNumber = cursor.getString(cursor.getColumnIndex(ContactsContract.CommonDataKinds.Phone.NUMBER));
                Log.i("CONTACT_PROVIDER_DEMO","Contact Name ::: "+ ContactName+"ph# ::: "+contactNumber);
            }
        }


    }
}
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Get Contacts Details"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="200dp"
        android:onClick="btnGetContacts"/>

</RelativeLayout>
```
### AndroidManifest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.sanath.contentproviderapp">
    <uses-permission android:name="android.permission.READ_CONTACTS"></uses-permission>
    <uses-permission android:name="android.permission.WRITE_CONTACTS"></uses-permission>
    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.ContentProviderApp"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

    </application>

</manifest>
```
## OUTPUT
<img width="781" alt="Screenshot 2022-09-26 at 11 41 07 PM" src="https://user-images.githubusercontent.com/93427224/192350242-763cb0e0-3a8c-4498-94b1-f6bece35b3a4.png">

<img width="785" alt="Screenshot 2022-09-26 at 11 41 41 PM" src="https://user-images.githubusercontent.com/93427224/192350331-91047a7a-8fa1-4c2c-829d-1f50829ec84a.png">

<img width="782" alt="Screenshot 2022-09-26 at 11 42 07 PM" src="https://user-images.githubusercontent.com/93427224/192350387-7bbe4ab9-bb84-4d33-b27e-e78f53cf8b4a.png">

<img width="778" alt="Screenshot 2022-09-26 at 11 42 36 PM" src="https://user-images.githubusercontent.com/93427224/192350440-dabfa2f0-3e51-4738-b2e6-ca555a0ce995.png">

<img width="1010" alt="Screenshot 2022-09-26 at 11 43 08 PM" src="https://user-images.githubusercontent.com/93427224/192350478-8ed319f5-cf2a-4309-8696-a7ff4be82eac.png">

<img width="246" alt="Screenshot 2022-09-26 at 11 43 37 PM" src="https://user-images.githubusercontent.com/93427224/192350549-cfa83307-d387-4a90-85f9-5d9fd0c0ebe1.png">

<img width="253" alt="Screenshot 2022-09-26 at 11 44 06 PM" src="https://user-images.githubusercontent.com/93427224/192350581-30668ea5-d487-4a75-833a-417f967977c3.png">


## RESULT
Thus a Simple Android Application create your own content providers to get contacts details using Android Studio is developed and executed successfully.
