# Ex.No:10 Design an application that draws basic graphical primitives on the screen.

## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed By: Sai Eswar Kandukuri
Register Number: 212221240020
*/
```

### MainActivity.java:
```
package com.example.graphics;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.graphics.drawable.BitmapDrawable;
import android.os.Bundle;
import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Bitmap bg = Bitmap.createBitmap(720, 1280,
                Bitmap.Config.ARGB_8888);
        ImageView i = (ImageView) findViewById(R.id.ImageView);
        i.setBackgroundDrawable(new BitmapDrawable(bg));
        Canvas canvas = new Canvas(bg);
        Paint paint = new Paint();
        Paint paint1 = new Paint();
        paint1.setColor(Color.BLUE);
        paint.setColor(Color.RED);
        paint1.setTextSize(50);
        canvas.drawText("Rectangle", 420, 150, paint1);
        canvas.drawRect(450, 200, 650, 700, paint);
        canvas.drawText("Circle", 120, 150, paint1);
        canvas.drawCircle(200, 350, 150, paint);
        canvas.drawText("Square", 120, 800, paint1);
        canvas.drawRect(100, 850, 300, 1050, paint);
        canvas.drawText("Line", 480, 800, paint1);
        canvas.drawLine(520, 850, 520, 1150, paint);

    }
}
```

### activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout android:layout_height="match_parent"
    android:layout_width="match_parent"
    xmlns:android="http://schemas.android.com/apk/res/android">
    <ImageView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:id="@+id/ImageView"/>
</RelativeLayout>
```
## OUTPUT:

<img width="960" alt="10 1" src="https://user-images.githubusercontent.com/93427522/204132561-95fc117d-e6f5-48c4-8a32-812cbabb4ccc.png">
<img width="960" alt="10 2" src="https://user-images.githubusercontent.com/93427522/204132563-80f1263b-dc59-4882-b5b8-aed7a8d6bd18.png">
<img width="188" alt="10 3" src="https://user-images.githubusercontent.com/93427522/204132569-af4dc5dd-6ee5-449b-9238-964aafe59a07.png">

## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
