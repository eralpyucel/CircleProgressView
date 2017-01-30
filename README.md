# CircleProgressView
An Android component to show progress in percentage.

####Screenshots:
![](https://github.com/eralpyucel/CircleProgressView/blob/master/preview.gif)
<img src="https://github.com/eralpyucel/CircleProgressView/blob/master/preview_image.png" width="300">

## Gradle

Add it in your root build.gradle at the end of repositories:

```
dependencies {
    ...
    maven { url 'https://jitpack.io' }
}
```

Add the dependency:

```
dependencies {
     compile 'com.github.eralpyucel:CircleProgressView:v1.1'
}
```


##Usage
###XML:
```xml
<com.eralp.circleprogressview.CircleProgressView
            android:id="@+id/circle_progress_view"
            android:layout_width="0dp"
            android:layout_weight="1"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            app:cpv_circle_color="#27375c"
            app:cpv_circle_width="6dp"
            app:cpv_background_circle_width="1dp"
            app:cpv_background_circle_color="#5b253048"
            app:cpv_text_prefix="%"
            app:cpv_text_size="40"
            app:cpv_text_color="#27375c"/>
```

###Activity:
```java
mCircleProgressView = (CircleProgressView) findViewById(R.id.circle_progress_view);
mCircleProgressView.setTextEnabled(false);
mCircleProgressView.setInterpolator(new AccelerateDecelerateInterpolator());
mCircleProgressView.setStartAngle(45);
mCircleProgressView.setProgressWithAnimation(85, 2000);
        
mCircleProgressView.addAnimationListener(new ProgressAnimationListener() {
            @Override
            public void onValueChanged(float value) {
                
            }

            @Override
            public void onAnimationEnd() {
                Toast.makeText(MainActivity.this, "Animation of CircleProgressView done", Toast.LENGTH_SHORT).show();
            }
        });
				
```
