
# Easy Splash Screen Android
Easily create your company splash screen

<img src="/resources/intro.png" width="80%" alt="Android Easy Splash Screen"/>

Easy splash screen library allows you to generate beautiful and customizable Splash screens with less effort



## Usage
### Setup
This library is available on Jcenter.

```groovy
compile 'gr.pantrif:easy-android-splash-screen:0.0.1'
```


### Available options
```java
View easySplashScreenView = new EasySplashScreen(MainActivity.this)
                .withFullScreen()
                .withTargetActivity(TargetActivity.class)
                .withSplashTimeOut(4000)
                .withBackgroundResource(android.R.color.holo_red_light)
                .withHeaderText("Header")
                .withFooterText("optnio studio")
                .withBeforeLogoText("My cool company")
                .withLogo(R.drawable.logo)
                .withAfterLogoText("Some more details")
                .create();

setContentView(easySplashScreenView);
```

### Customize views
```java
 EasySplashScreen config = new EasySplashScreen(MainActivity.this)
                .withFullScreen()
                .withTargetActivity(TargetActivity.class)
                .withSplashTimeOut(4000)
                .withBackgroundResource(android.R.color.holo_red_light)
                .withHeaderText("Header")
                .withFooterText("optnio studio")
                .withBeforeLogoText("My cool company")
                .withLogo(R.drawable.logo)
                .withAfterLogoText("Some more details with custom font");
    //add custom font
    Typeface pacificoFont = Typeface.createFromAsset(getAssets(), "Pacifico.ttf");
    config.getAfterLogoTextView().setTypeface(pacificoFont);
    
    //change text color
    config.getHeaderTextView().setTextColor(Color.WHITE);
    
    //finally create the view
    View easySplashScreenView = config.create();
    setContentView(easySplashScreenView);
```
