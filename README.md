
# Ex.No:12 Design an application that draws basic graphical primitives on the screen.


## AIM:

To create and design an android application that draws basic graphical primitives on the screen using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “graphical″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Draw basic object details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

### Program to create and design an android application that draws basic graphical primitives on the screen.
### Developed by: DIVYA PRIYA S
### Registeration Number : 212225240037
## MainActivity.java
```
package com.example.shapes;

import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.os.Bundle;
import android.widget.ImageView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        ImageView imageView = findViewById(R.id.imageView);

        Bitmap bitmap = Bitmap.createBitmap(
                1080,
                1920,
                Bitmap.Config.ARGB_8888
        );

        Canvas canvas = new Canvas(bitmap);

        // Background
        canvas.drawColor(Color.parseColor("#FFF8F8"));

        // Text Paint
        Paint textPaint = new Paint();
        textPaint.setAntiAlias(true);
        textPaint.setColor(Color.RED);
        textPaint.setTextSize(60);
        textPaint.setTextAlign(Paint.Align.CENTER);

        // Shape Paint
        Paint shapePaint = new Paint();
        shapePaint.setAntiAlias(true);
        shapePaint.setColor(Color.BLUE);

        // Circle
        canvas.drawCircle(300, 450, 180, shapePaint);
        canvas.drawText("Circle", 300, 700, textPaint);

        // Rectangle
        canvas.drawRect(600, 300, 900, 650, shapePaint);
        canvas.drawText("Rectangle", 750, 800, textPaint);

        // Square
        canvas.drawRect(150, 1000, 500, 1350, shapePaint);
        canvas.drawText("Square", 325, 1450, textPaint);

        // Line
        shapePaint.setStrokeWidth(10);
        canvas.drawLine(740, 1000, 740, 1350, shapePaint);
        canvas.drawText("Line", 740, 1450, textPaint);

        // Display bitmap
        imageView.setImageBitmap(bitmap);
    }
}
```
## activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:scaleType="fitCenter"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT

<img width="1907" height="1010" alt="image" src="https://github.com/user-attachments/assets/a56336e8-62ad-4dfc-a7e1-5f3d3825d33c" />

<img width="1907" height="1014" alt="image" src="https://github.com/user-attachments/assets/a2d4e323-866a-4972-9d94-61d98be3402b" />


## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
