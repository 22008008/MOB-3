# EXPERIMENT:03  Implement an application that uses Intent(Implicit) using Android Studio.
Design an Android application with a text field and an "Open in Browser" button. On pressing the button, the app should fetch the URL from the text field and open it in a browser using an Implicit Intent.

# AIM:
To design an Android application with a TextField and a button labeled "Open in Browser." Upon pressing the button, the application should retrieve the URL entered in the TextField and open it in the device's web browser using an implicit intent.

# EQUIPMENTS REQUIRED:
Latest Version Android Studio

```
Program to print the text “Implicitintent”.
Developed by:  Sri Ranjaani Priya.P
Registeration Number :212222220049
```


# PROGRAM:
### MainActivity.java:
```
package com.example.Exp_3;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    Button button;

    EditText editText;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final EditText editText = (EditText) findViewById(R.id.urlText);
        Button btn = (Button) findViewById(R.id.btnNavigate);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String url = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```
# activitymain.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/urlText"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="100dp"
        android:ems="10" />
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btnNavigate"
        android:layout_below="@+id/urlText"
        android:text="Navigate"
        android:layout_centerHorizontal="true" />
</RelativeLayout>
```

# OUTPUT:
![image](https://github.com/user-attachments/assets/740ce2ef-0edf-4c19-8227-30325c8bc677)

![image](https://github.com/user-attachments/assets/eaa050b9-8dd8-4202-bf58-6b477b24c13f)

![image](https://github.com/user-attachments/assets/f48d7f9e-c525-4f86-9a0a-504219d73a7e)




# RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the web page using Android Studio was developed and executed successfully.
