# Ex-No_2-Intent(Implicit & Explicit)
Develop program to perform explicit and implicit intent by creating a buttons using Android Studio
## AIM:
To develop a program to perform explicit and implicit intent by creating a buttons using Android Studio
## EQUIPMENTS REQUIRED
Android Studio(Min. required Artic Fox)
## ALGORITHM
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as Intent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Create a Layout and two buttons named as explicit intent and implicit Intent

Step 7: By clicking Implict Intent button open google page using Implicit Intents in MainActivity file.

Step 8: By clicking Explicit Intent button open second page using Explicit Intents in MainActivity file.

Step 7: Save and run the application.
## PROGRAM
```
/*
Program to create and design an android application for Sending  SMS using Intent.
Developed by: GAUTHAM KRISHNA S
RegisterNumber:  212223240036
*/
```
#### MainActivity.java
```java
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
    Button button1,button2;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button1=(Button)findViewById(R.id.explicit_intent);
        button2=(Button)findViewById(R.id.implicit_intent);
       // button1.setText("Explicit Intent");
       // button2.setText("Implicit Intent");
        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(getBaseContext(),activity_second.class);
                startActivity(intent);
            }
        });
        button2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent1=new Intent(Intent.ACTION_VIEW);
                intent1.setData(Uri.parse("https://gmail.com"));
                startActivity(intent1);
            }
        });
    }
}
```
#### activity_second.java
```java
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.Toast;
public class activity_second extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);
        Toast.makeText(getApplicationContext(),"We moved to Second activity",Toast.LENGTH_LONG).show();
    }
}
```
#### activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:paddingBottom="@dimen/activity_vertical_margin"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="?android:attr/textAppearanceMedium"
        android:text="@string/description"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:layout_alignParentTop="true"
        android:layout_alignParentStart="true"
        android:clickable="false"
        android:background="#3e7d02"
        android:textColor="#ffffff"/>
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/button1"
        android:id="@+id/explicit_intent"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="147dp"/>
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/button2"
        android:id="@+id/implicit_intent"
        android:layout_centerHorizontal="true"
        android:layout_centerVertical="true"/>

</RelativeLayout>
```
#### activity_second.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:background="#CCEEAA"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:paddingBottom="@dimen/activity_vertical_margin"
    tools:context="com.example.myapplication.activity_second">
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="?android:attr/textAppearanceLarge"
        android:text="@string/secondact"
        android:id="@+id/textView"
        android:layout_centerVertical="true"
        android:layout_centerHorizontal="true" />

</RelativeLayout>
```
#### strings.xml
```xml
<resources>
    <string name="app_name">My Application</string>
    <string name="description">If you click on Explicit example we will navigate to second activity within App and if you click on Implicit example AbhiAndroid Homepage will open in Browser</string>
    <string name="button1">Explicit Intent</string>
    <string name="button2">Implicit Intent</string>
    <string name="secondact">This is Second Activity</string>
</resources>
```
#### dimens.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <dimen name="activity_vertical_margin">8dp</dimen>
    <dimen name="activity_horizontal_margin">8dp</dimen>
</resources>
```
## OUTPUT
![Screenshot 2024-03-09 145751](https://github.com/Nijeesh-bit/Ex-No_2-Intent-Implicit-Explicit-/assets/89188014/dc60dc5b-7f97-4264-8963-863b3f63f7f5)
![Screenshot 2024-03-09 145800](https://github.com/Nijeesh-bit/Ex-No_2-Intent-Implicit-Explicit-/assets/89188014/7d308ae5-c7c3-4e9b-abee-a48bf4c0270e)
![Screenshot 2024-03-09 145849](https://github.com/Nijeesh-bit/Ex-No_2-Intent-Implicit-Explicit-/assets/89188014/de6ef7ef-9c32-4698-acba-3f794d155e85)

## RESULT
Thus a Simple Android Application to open google page using Implicit Intents in Android Studio was developed and executed successfully.
