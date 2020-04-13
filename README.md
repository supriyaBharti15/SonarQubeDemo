# SonarQubeDemo
SonarQube integration with android studio project using local host


package com.example.kotlinandroidviewex

import android.content.Intent
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.view.View
import android.widget.Button
import android.widget.ImageView
import android.widget.RadioButton
import android.widget.Toast

class MainActivity : AppCompatActivity(), View.OnClickListener {

    private var mImageViewButton: Button? = null
    private var mRadioButton: Button? = null
    private var mSeekBarButton: Button? = null

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        mImageViewButton = findViewById(R.id.imageViewExmp)
        mRadioButton = findViewById(R.id.radioButtonExmp)
        mRadioButton = findViewById(R.id.seekBarExmp)

        //set clickListener on buttons
        mImageViewButton!!.setOnClickListener(this)
        mRadioButton!!.setOnClickListener(this)
        mRadioButton!!.setOnClickListener(this)
    }

    override fun onClick(v: View) {
        val id = v.getId()
        when (id) {
            R.id.imageViewExmp -> {
               val intent = Intent(this@MainActivity,ImageViewExample::class.java)
                intent.putExtra("userName","Supriya")
                startActivity(intent)
            }
            R.id.radioButtonExmp -> {

            }

            R.id.seekBarExmp -> {

            }
            R.id.progressBarExmp -> {

            }
        }
    }

}
@@@@@@@@@@@@@@@@
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center_horizontal"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/imageViewExmp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="30dp"
        android:background="@color/colorPrimary"
        android:padding="10dp"
        android:text="ImageView in Kotlin"
        android:textAllCaps="false"
        android:textColor="#fff" />

    <Button
        android:id="@+id/radioButtonExmp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="30dp"
        android:background="@color/colorPrimary"
        android:padding="10dp"
        android:text="Radio Buttons in Kotlin"
        android:textAllCaps="false"
        android:textColor="#fff" />

    <Button
        android:id="@+id/seekBarExmp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="30dp"
        android:background="@color/colorPrimary"
        android:padding="10dp"
        android:text="SeekBar in Kotlin"
        android:textAllCaps="false"
        android:textColor="#fff" />

    <Button
        android:id="@+id/webViewExmp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="30dp"
        android:background="@color/colorPrimary"
        android:padding="10dp"
        android:text="WebView in Kotlin"
        android:textAllCaps="false"
        android:textColor="#fff" />

    <Button
        android:id="@+id/progressBarExmp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="30dp"
        android:background="@color/colorPrimary"
        android:padding="10dp"
        android:text="ProgressBar in Kotlin"
        android:textAllCaps="false"
        android:textColor="#fff" />

</LinearLayout>
#####
package com.example.kotlinandroidviewex

import android.os.Bundle
import android.widget.Button
import android.widget.ImageView
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class ImageViewExample : AppCompatActivity() {
    //var is Mutable variable
    //  val is immutable
    val drawbleIds = intArrayOf(R.drawable.tiger, R.drawable.panda, R.drawable.butterfly)
    var intCol = 0;

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_image_view)
        val userName = intent.getStringExtra("userName")
        val buttonClick = findViewById(R.id.changeImageBtn) as Button
        val imageView = findViewById(R.id.imageView) as ImageView
        val textView = findViewById(R.id.textView) as TextView
        textView.setText("Message sent by MAinActivity is:: "+userName)

        buttonClick.setOnClickListener {
            imageView.setImageResource(drawbleIds[intCol % drawbleIds.size])
            intCol++
        }
    }
}
%%%%
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center_horizontal"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="200dp"
        android:layout_height="200dp"
        android:layout_marginTop="30dp"
        android:background="@color/colorPrimary"
        android:src="@mipmap/ic_launcher" />

    <Button
        android:id="@+id/changeImageBtn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="40dp"
        android:text="change Image" />

</LinearLayout>
