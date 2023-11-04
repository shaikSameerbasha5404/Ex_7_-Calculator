# Ex_7_-Develop a simple calculator using android studio.
Develop a program to create a simple calculator using Android Studio.

## AIM:
To develop a program to create a simple calculator using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Perform the Calculator Operation in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create simple calculator using Android Studio.
Developed by: Shaik Sameer Basha
RegisterNumber:  212222240093
*/
```

## MainActivity.java:
```
package com.example.calculator;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    EditText n1,n2;
    Button b1,b2,b3,b4;
    TextView res;
    int s1,s2;
    public boolean getNumbers() {
        n1 = findViewById(R.id.num1);
        n2= findViewById(R.id.num2);
        res=findViewById(R.id.result);
        if((n1.equals(null) && n2.equals(null) )||( n1.equals(" ") && n2.equals(" ")))
        {
            res.setText("Please Enter a valid Values");
            return false;
        }
        else
        {
             s1=Integer.parseInt(n1.getText().toString());
            s2=Integer.parseInt(n2.getText().toString());
        }
        return true;
    }
    public void sum(View view)
    {
        if(getNumbers())
        {
            int su=s1+s2;
            res.setText(s1+" + "+s2+" = "+su);
        }
    }
    public void sub(View view)
    {
        if(getNumbers())
        {
            int sb=s1-s2;
            res.setText(s1+" - "+s2+" = "+sb);
        }
    }
    public void mul(View view)
    {
        if(getNumbers())
        {
            int m=s1*s2;
            res.setText(s1+" * "+s2+" = "+m);
        }
    }
    public void div(View view)
    {
        if(getNumbers())
        {
            double d=s1/s2;
            res.setText(s1+" / "+s2+" = "+d);
        }
    }
}


```




## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Calculator"
        android:textSize="35dp"
        android:textStyle="bold"/>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Number1"
        android:id="@+id/num1"
        android:inputType="number"
        android:layout_marginTop="20dp"/>
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Number2"
        android:id="@+id/num2"
        android:inputType="number"
        android:layout_marginTop="20dp"/>
    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:id="@+id/result"
        android:text="Result"
        android:textStyle="bold"
        android:textSize="30sp"
        android:gravity="center"
        android:layout_marginTop="20dp"
        android:layout_marginBottom="30dp"/>
    <GridLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:columnCount="4">
        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginRight="20dp"
            android:text="+"
            android:textSize="20dp"
            android:id="@+id/btn1"
            android:onClick="sum"/>
        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginRight="20dp"
            android:text="-"
            android:textSize="20dp"
            android:id="@+id/btn2"
            android:onClick="sub"/>
        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginRight="20dp"
            android:text="x"
            android:textSize="20dp"
            android:id="@+id/btn3"
            android:onClick="mul"/>
        <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
            android:text="/"
            android:textSize="20dp"
            android:id="@+id/btn4"
            android:onClick="div"/>
    </GridLayout>

</LinearLayout>
```

## AndroidMainfest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.example.calculator">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.Calculator"
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

## Output:
![Screenshot (225)](https://github.com/shaikSameerbasha5404/Ex_7_-Calculator/assets/118707756/ef4850e2-d5e1-4bfe-a335-1177326facfa)



## Result:
Thus a Simple Android Application to create a calculator using Android Studio was developed and executed successfully.
