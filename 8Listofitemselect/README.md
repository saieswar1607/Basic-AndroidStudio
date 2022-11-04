# Ex.No:8 Build a program to show five checkboxes and toast selected checkboxes.


## AIM:

To create a list using checkbox to display selected checkbox item using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as "listofitemselect" and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the list using checkbox in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to display check list item”.
Developed by:
Registeration Number :
*/
```

### MainActivity.java
```
package com.example.ex8;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    private CheckBox chkAndroid, chkJava, chkPhp, chkCpp, chkC;

    @Override
    public void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        chkAndroid = findViewById(R.id.chkAndroid);
        chkJava = findViewById(R.id.chkJava);
        chkPhp = findViewById(R.id.chkPhp);
        chkCpp = findViewById(R.id.chkCpp);
        chkC = findViewById(R.id.chkC);
    }

    public void showSelected(View view) {

        String selected = "You selected: \n";

        if(chkAndroid.isChecked())
            selected += "Android";

        if(chkJava.isChecked())
            selected += "\nJava";

        if(chkPhp.isChecked())
            selected += "\nPHP";

        if(chkCpp.isChecked())
            selected += "\nCPP";

        if(chkC.isChecked())
            selected += "\nC";

        Toast.makeText(MainActivity.this, selected, Toast.LENGTH_SHORT).show();
    }
}
```

### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:gravity="center"
        android:text="Select Your favourite Programming language"
        style="@style/TextAppearance.AppCompat.Large"
        android:layout_margin="10dp"
        android:textStyle="bold"/>

    <CheckBox
        android:id="@+id/chkAndroid"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Android"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkJava"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Java"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkPhp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="PHP"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkCpp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="CPP"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <CheckBox
        android:id="@+id/chkC"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="C"
        style="@style/TextAppearance.AppCompat.Headline"/>

    <Button android:id="@+id/btnDisplay"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Display"
        android:layout_marginTop="20dp"
        android:onClick="showSelected"/>

</LinearLayout>
```

## OUTPUT

<img width="1440" alt="1" src="https://user-images.githubusercontent.com/93427011/200035475-170488b4-6aba-40f4-8f25-6b8b0f01f201.png">

<img width="479" alt="2" src="https://user-images.githubusercontent.com/93427011/200035583-b8b8108c-f454-4043-bc4d-e0595c2c2ca2.png">

<img width="1440" alt="3" src="https://user-images.githubusercontent.com/93427011/200035619-abe53ca4-dfbb-440c-8981-ea515b961902.png">

<img width="474" alt="4" src="https://user-images.githubusercontent.com/93427011/200035760-6cb82b05-fd69-4c13-bac5-ab8dba17ffd6.png">



## RESULT
Thus a Simple Android Application create a list using checkbox to display selected checkbox using Android Studio is developed and executed successfully.
