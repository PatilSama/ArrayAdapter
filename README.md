# ArrayAdapter
// layout Code.  * list_layout *
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ListView
        android:divider="@color/black"
        android:dividerHeight="2dp"
        android:listSelector="@android:color/holo_red_dark"
        android:id="@+id/lstName"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" >
    </ListView>
    <TextView
        android:textColor="@color/white"
        android:textSize="20dp"
        android:textStyle="bold"
        android:id="@+id/txtName"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"></TextView>

</LinearLayout>

// Java Code.
public class ArrayAdapterr extends AppCompatActivity {
    ListView lstName;
    TextView txtName;
    @Override
    protected void onCreate(@Nullable Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.list_layout);
        lstName = findViewById(R.id.lstName);
        txtName = findViewById(R.id.txtName);
        lstName.setAdapter(new ArrayAdapter<String>(getApplicationContext(),R.layout.list_layout,R.id.txtName,new String[]{"sama","Viju","Yash"}));
    }
}
