
# Ex.No: 07 Design an application that draws basic graphical primitives on the screen.


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
```
/*
Program to create and design an android application that draws basic graphical primitives on the screen.
Developed by: SANDHIYA M
Registeration Number : 212224220086
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FFF8FC"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView3"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="20dp"
        android:layout_marginTop="44dp"
        android:layout_marginEnd="20dp"
        android:background="#737A85"
        android:gravity="center"
        android:padding="15dp"
        android:text="GRAPHICAL PRIMITIVES"
        android:textColor="#FFFFFF"
        android:textSize="22sp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <ImageView
        android:id="@+id/imageView1"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:layout_marginTop="10dp"
        android:layout_marginBottom="15dp"
        android:adjustViewBounds="true"
        android:scaleType="fitCenter"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/textView3"
        app:layout_constraintVertical_bias="1.0" />

</androidx.constraintlayout.widget.ConstraintLayout>

```
## mainactivity.java
```

package com.example.graphics;

import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Bitmap;
import android.graphics.Canvas;
import android.graphics.Color;
import android.graphics.Paint;
import android.os.Bundle;
import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Bitmap bg = Bitmap.createBitmap(720, 1280, Bitmap.Config.ARGB_8888);

        ImageView i = findViewById(R.id.imageView1);

        Canvas canvas = new Canvas(bg);

        // Paint for Shapes
        Paint shapePaint = new Paint();
        shapePaint.setColor(Color.parseColor("#FF9800"));
        shapePaint.setAntiAlias(true);

        // Paint for Text
        Paint textPaint = new Paint();
        textPaint.setColor(Color.parseColor("#263B5E"));
        textPaint.setTextSize(50);
        textPaint.setTypeface(android.graphics.Typeface.DEFAULT_BOLD);
        textPaint.setAntiAlias(true);

        // Circle
        canvas.drawText("Circle", 120, 150, textPaint);
        canvas.drawCircle(200, 350, 150, shapePaint);

        // Rectangle
        canvas.drawText("Rectangle", 420, 150, textPaint);
        canvas.drawRect(400, 200, 650, 700, shapePaint);

        // Square
        canvas.drawText("Square", 120, 800, textPaint);
        canvas.drawRect(50, 850, 350, 1150, shapePaint);

        // Line
        canvas.drawText("Line", 500, 800, textPaint);
        shapePaint.setStrokeWidth(8);
        canvas.drawLine(520, 850, 520, 1150, shapePaint);

        i.setImageBitmap(bg);
    }
}


```

## OUTPUT

<img width="1920" height="1200" alt="Screenshot 2026-11-25 110026" src="https://github.com/user-attachments/assets/bfea7b63-eef1-48da-888b-960c3bf2670b" />



## RESULT
Thus a Simple Android Application to create and design an android application that draws basic graphical primitives on the screen using Android Studio is developed and executed successfully.
