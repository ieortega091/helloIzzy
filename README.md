package com.izzy.hello.helloizzy;

import android.graphics.Color;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.RelativeLayout;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    private RelativeLayout mRelativeLayout;
    private Button mButtton;
    private TextView mTextView;





    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


        findViewById(R.id.buttonColor).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                ((TextView) findViewById(R.id.textView)).setTextColor(getResources().getColor(R.color.colorAccent));
            }
        });





        mButtton = (Button)findViewById(R.id.button);
        mRelativeLayout = (RelativeLayout)findViewById(R.id.relativeLayout);
        mTextView = (TextView)findViewById(R.id.textView);

        View.OnClickListener listener = new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                String replace = "Android is Awsome";


                mTextView.setText(replace);
            }
        };

        mButtton.setOnClickListener(listener);
    }


}
