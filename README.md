# adds-up
calculator application
package com.example.android.addsup;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
float q = 0;
int n = 0;
float q2;
int operator;
String a = "";

    public void click1(View view) {
        n = 1;
        q = (q * 10) + n;
        display(q);
        a = a + "1";
        type(a);
    }
    public void click2(View view) {
        n = 2;
        q = (q * 10) + n;
        display(q);
        a = a + "2";
        type(a);
              }

    public void click3(View view) {
        n = 3;
        q = (q * 10) + n;
        display(q);
        a = a + "3";
        type(a);
     }

    public void click4(View view) {
        n = 4;
        q = (q * 10) + n;
        display(q);
        a = a + "4";
        type(a);
    }


    public void click5(View view) {
        n = 5;
        q = (q * 10) + n;
        display(q);
        a = a + "5";
        type(a);
    }

    public void click6(View view) {
        n = 6;
        q = (q * 10) + n;
        display(q);
        a = a + "6";
        type(a);
    }

    public void click7(View view) {
        n = 7;
        q = (q * 10) + n;
        display(q);
        a = a + "7";
        type(a);
    }

    public void click8(View view) {
        n = 8;
        q = (q * 10) + n;
        display(q);
        a = a + "8";
        type(a);
    }

    public void click9(View view) {
        n = 9;
        q = (q * 10) + n;
        display(q);
        a = a + "9";
        type(a);
    }

    public void click0(View view) {
        n = 0;
        q = (q * 10) + n;
        display(q);
        a = a + "0";
        type(a);
    }
    public void clickC(View view) {
        q = 0;
        display(q);
        a = "";
        type(a);
    }
    public void
    clickPlus(View view) {
        q2 = q;
        q = 0;
        operator = 1;
        a = a + "+";
        type(a);

        }
    public void
    clickMinus(View view) {
        q2 = q;
        q = 0;
        operator = 2;
        a = a + "-";
        type(a);
        }
    public void
    clickMultiply(View view) {
        q2 = q;
        q = 0;
        operator = 3;
        a = a + "*";
        type(a);
       }
    public void
    clickDivide(View view) {
        q2 = q;
        q = 0;
        operator = 4;
        a = a + "/";
        type(a);
    }
    public void clickEquals(View view) {
        float answer = 0;
        if (operator == 1){
        answer = q2 + q;}
        if (operator == 2){
            answer = q2 - q;}
        if (operator == 3){
            answer = q2 * q;}
        if (operator == 4){
            answer = (float) q2 / q;}
        display(answer);
        a = a + "=";
        type(a);
        q = answer;
        a = answer + "";

    }
    private void display(float number) {
        TextView displayTextView = (TextView) findViewById(
                R.id.display);
        displayTextView.setText("" + number);
    }
    private void type(String text) {
        TextView displayTextView = (TextView) findViewById(
                R.id.type);
        displayTextView.setText("" + text);
    }
}
