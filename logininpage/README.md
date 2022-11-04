# Ex.No:5 Develop a program to accept username and password from the end user using Text View and Edit Text and display personal information of the student.


## AIM:

To develop a program to accept username and password from the end user using Text View and Edit Text and display personal information of the student using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as studentinfo and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Accept username and password from the end user and the display information give in MainActivity file.

Step 7: Save and run the application.
 
### PROGRAM:
```
*/
Program to display login page.
Developed by: Sai Eswar Kandukuri
Registeration Number:212221240020
/*
```

### MainActivity.java
```
package com.example.exno5;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {
    EditText editName, editPassword;
    TextView result;
    Button buttonSubmit, buttonReset;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        editName = (EditText) findViewById(R.id.e1);
        editPassword = (EditText) findViewById(R.id.e2);
        result = (TextView) findViewById(R.id.textView);
        buttonSubmit = (Button) findViewById(R.id.button3);
        buttonReset = (Button) findViewById(R.id.button4);

        buttonSubmit.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String name = editName.getText().toString();
                String password = editPassword.getText().toString();
                result.setText("Name:\t" + name + "\nPassword:\t" + password );
            }
        });

        buttonReset.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editName.setText("");
                editPassword.setText("");
                result.setText("");
                editName.requestFocus();
            }
        });
    }
}

```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="205dp"
        android:layout_height="68dp"
        android:layout_marginBottom="52dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintHorizontal_bias="0.191"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.773"
        app:layout_constraintTop_toBottomOf="@+id/button3" />

    <Button
        android:id="@+id/button3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Submit"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.179"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.543" />

    <Button
        android:id="@+id/button4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Reset"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.772"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.543"
        app:layout_constraintStart_toEndOf="@+id/button3" />

    <Button
        android:id="@+id/button"
        android:layout_width="114dp"
        android:layout_height="48dp"
        android:text="Name"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.148"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.193" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Password"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.148"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.342"
        app:layout_constraintTop_toBottomOf="@+id/button" />

    <EditText
        android:id="@+id/e1"
        android:layout_width="192dp"
        android:layout_height="48dp"
        android:ems="10"
        android:inputType="textPersonName"
        android:minHeight="48dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.835"
        app:layout_constraintStart_toEndOf="@+id/button"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.196"
        tools:ignore="SpeakableTextPresentCheck" />

    <EditText
        android:id="@+id/e2"
        android:layout_width="193dp"
        android:layout_height="49dp"
        android:ems="10"
        android:inputType="textPersonName"
        android:minHeight="48dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.84"
        app:layout_constraintStart_toEndOf="@+id/button2"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/e1"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.341"
        tools:ignore="SpeakableTextPresentCheck" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
###  OUTPUT

### MainActivity.java


![Screenshot (11)](https://user-images.githubusercontent.com/93427522/199950496-af8c1a71-f0f3-4abd-af5b-2df6b2b6c37a.png)

<img width="316" alt="MainActivity java" src="https://user-images.githubusercontent.com/93427522/199949764-ba526a9a-5250-4e0c-bdc1-0d8994399bed.png">


### activity_main.xml


![Screenshot (12)](https://user-images.githubusercontent.com/93427522/199950532-b8067ca6-1d8b-4c5c-8617-6acfadf440ed.png)

<img width="314" alt="activity_main xml" src="https://user-images.githubusercontent.com/93427522/199949795-d16df9d7-f0ae-47db-ac76-4fbed2cd1052.png">

### RESULT
Thus a Simple Android Application develop a program to accept username and password from the end user using Text View and Edit Text and display personal information of the student using Android Studio is developed and executed successfully.
