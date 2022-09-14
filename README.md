# Basic-AndroidStudio

## Program:

### MainActivity.java:
```
package com.example.project;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast toast=Toast.makeText(getApplicationContext(),"OnCreate Executed",Toast.LENGTH_LONG);
        toast.show();
    }
    protected void onStart(){
        super.onStart();
        Toast toast=Toast.makeText(getApplicationContext(),"OnStart Executed",Toast.LENGTH_LONG);
        toast.show();
    }
    protected void onResume(){
        super.onResume();
        Toast toast=Toast.makeText(getApplicationContext(),"OnResume Executed",Toast.LENGTH_LONG);
        toast.show();
    }
    protected void onPause(){
        super.onPause();
        Toast toast=Toast.makeText(getApplicationContext(),"OnPause Executed",Toast.LENGTH_LONG);
        toast.show();
    }
    protected void onStop(){
        super.onStop();
        Toast toast=Toast.makeText(getApplicationContext(),"OnStop Executed",Toast.LENGTH_LONG);
        toast.show();
    }
    protected void onRestart(){
        super.onRestart();
        Toast toast=Toast.makeText(getApplicationContext(),"OnRestart Executed",Toast.LENGTH_LONG);
        toast.show();
    }
    protected void onDestroy(){
        super.onDestroy();
        Toast toast=Toast.makeText(getApplicationContext(),"OnDestroy Executed",Toast.LENGTH_LONG);
        toast.show();
    }
}

```

### activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

### Output:

<img width="1440" alt="1" src="https://user-images.githubusercontent.com/93427011/190208753-1c08d2e5-bd52-45a8-96da-a371dc54f7c6.png">

<img width="1440" alt="2" src="https://user-images.githubusercontent.com/93427011/190208899-40c96c1e-9243-4358-910c-47a125508773.png">

<img width="1440" alt="3" src="https://user-images.githubusercontent.com/93427011/190208993-56550005-eea8-4e23-bb2e-70f9202e43cd.png">

<img width="1440" alt="4" src="https://user-images.githubusercontent.com/93427011/190209106-20887131-9380-46c2-bcd5-8ef7c135aff3.png">

<img width="1440" alt="5" src="https://user-images.githubusercontent.com/93427011/190209185-65c7f639-4545-42d0-bbbf-1abcf238b67e.png">

<img width="1440" alt="6" src="https://user-images.githubusercontent.com/93427011/190209240-03299c3e-b156-4b23-973b-90e063074919.png">

<img width="1440" alt="7" src="https://user-images.githubusercontent.com/93427011/190209329-a0fdd57f-7fd3-4d43-8885-36807fb3a188.png">
