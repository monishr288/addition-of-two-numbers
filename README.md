# Mobile-application-to-add-to-two-numbers
## AIM:
To create a simple Android application that accepts two numbers from the user and displays their summation result when the button is clicked.
## EQUIPMENTS REQUIRED:
Latest Version Android Studio
## ALGORITHM:
Step 1: Start

Step 2: Enter first number

Step 3: Enter second number

Step 4: Click ADD button

Step 5: Read both numbers

Step 6: Add the numbers

Step 7: Display the result

Step 8: Stop
## PROGRAM:
```
/*
Developed by: MONISH R
Registeration Number : 212223220061
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:layout_width="250dp"
        android:layout_height="wrap_content"
        android:hint="Enter First Number"
        android:inputType="number"/>

    <EditText
        android:id="@+id/num2"
        android:layout_width="250dp"
        android:layout_height="wrap_content"
        android:hint="Enter Second Number"
        android:inputType="number"
        android:layout_marginTop="15dp"/>

    <Button
        android:id="@+id/btnAdd"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="ADD"
        android:layout_marginTop="20dp"/>

    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Result"
        android:textSize="24sp"
        android:layout_marginTop="20dp"/>

</LinearLayout>
```
## MainActivity.java
```
package com.example.addition;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button btnAdd;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        btnAdd = findViewById(R.id.btnAdd);
        result = findViewById(R.id.result);

        btnAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                int a = Integer.parseInt(num1.getText().toString());
                int b = Integer.parseInt(num2.getText().toString());

                int sum = a + b;

                result.setText("Sum = " + sum);
            }
        });
    }
}
```
## OUTPUT
<img width="379" height="854" alt="594451130-d9e6b3aa-98c3-4003-8903-7db2e3675448" src="https://github.com/user-attachments/assets/4b7a385c-91c8-44e2-b6d3-5018eb5f35f4" />
## RESULT
Thus, a simple Android Application for Addition of Two Numbers using Android Studio was developed and executed successfully. The application accepts two input numbers from the user, performs the addition operation when the ADD button is clicked, and displays the summation result successfully on the screen.

