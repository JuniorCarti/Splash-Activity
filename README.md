# Splash-Activity
package com.example.alicehealth.activities;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;

import com.example.alicehealth.R;

public class SplashActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_splash);

        Thread thread = new Thread(){
            @Override
            public void run() {
                super.run();

                try {
                    sleep(3000);

                }
                catch (Exception e){
                    e.printStackTrace();

                }finally {
                    startActivity(new Intent(SplashActivity.this, LoginActivity.class));

                }
            }
        };
        thread.start();
    }
}
