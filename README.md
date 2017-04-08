
This documents tells how to use Auto Resize Textview reusable component.

Below steps need to follow while integrating this component into your application.

1.	Copy `AutofitHelper.java` and `AutofitTextView.java` files and paste into your application source folder.
2.	Change the package names as per your requirement, by default its         
            `com.avinash.autoresizetextviewlibrary`.

3.	Copy `attrs.xml` file and paste it into `res/values` folder of your project.

4.	To add the following xml snippet into your xml file.

```xml
<com.avinash.autoresizetextviewlibrary.AutofitTextView
            android:id="@+id/output_autofit"
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:maxLines="2"
            android:gravity="center"
            android:text="@string/sample"
            android:textSize="50sp"
            autofit:minTextSize="8sp" />
```
  Note: Change the package name, as per your application.

5.	To Initialize and set text to ResizeTextview in your Activity / Fragment .

```java
private  AutofitTextView mAutofitOutput;

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
mAutofitOutput = (AutofitTextView) findViewById(R.id.output_autofit);
mAutofitOutput.setText("This is AutoResizeTextview sample");
}
```

Note: All TextView properties are applicable to this AutoResizeTextView.
