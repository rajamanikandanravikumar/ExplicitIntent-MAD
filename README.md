# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1. Start the application.
2. Create a new Android project in Android Studio.
3. Design the first screen with:
4. One EditText to accept a number.
5. One Button labeled FACTORIAL.
6. Create a second activity to display the result.
7. In MainActivity, read the number entered by the user.
8. Create an Explicit Intent to open SecondActivity.
9. Pass the entered number to SecondActivity using putExtra().
10. In SecondActivity, receive the number using getIntent().getStringExtra().
11. Convert the received value into an integer.
12. Calculate the factorial of the number using a for loop.
13. Display the factorial result in a TextView.
14. Run the application.
15. Verify that the second screen displays the correct factorial.
16. Stop the application.




## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: Rajamanikandan R
Registeration Number : 212223220082
*/
```
### MainActivity.java:
````
package com.example.explicit_intent;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


    }
    public void newsScreen(View view)
    {
        Intent i = new Intent(getApplicationContext(), MainActivity2.class);
        startActivity(i);
    }
}
````
### activity_main.xml
````
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="View Page 1"
        android:textSize="20sp"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.5"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.5" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Go to Second page"
        android:textSize="20sp"
        android:onClick="newsScreen"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.5"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.5" />
</androidx.constraintlayout.widget.ConstraintLayout>
````

### MainActivity2.java
````
package com.example.explicit_intent;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);

    }
    public void homeScreen(View view)
    {
        Intent i = new Intent(getApplicationContext(),MainActivity.class);
        startActivity(i);
    }
}
````

### activity_main2.xml
````
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity2">

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="View Page 2"
        android:textSize="24sp"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.5"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.5" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Back to Home"
        android:onClick="homeScreen"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.5"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2"
        app:layout_constraintVertical_bias="0.5" />
</androidx.constraintlayout.widget.ConstraintLayout>
````
## OUTPUT

#### View page 1:
<img width="1911" height="1023" alt="Screenshot 2026-07-26 205435" src="https://github.com/user-attachments/assets/5a944cda-8336-4b0a-b20f-6746a7f7425b" />

#### View page 2:
<img width="1917" height="1020" alt="Screenshot 2026-07-26 205403" src="https://github.com/user-attachments/assets/137baf37-b2e4-4088-aa65-85eb4da846b2" />





## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


