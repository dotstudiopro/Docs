# Installation

### DotstudioPRO
DotstudioPRO Android Player SDK is published to Maven as independent modules. To utilize the player include the dependencies listed below in your app/build.gradle file.

##
Requirements
<ul>
<li>sourceCompatibility 1.8</li>
<li>targetCompatibility 1.8</li>
<li>minSdkVersion 18</li>
<li>targetSdkVersion 28</li>
<li>multiDexEnabled true</li>
</ul>

###Include the player library
Add the following lines to your build.gradle
```
dependencies {
    // DotstudioPRO library for models (Required)
    implementation 'com.github.dotstudiopro:dotstudiopro-android-model:1.0.16'

    // DotstudioPRO library for dspplayer (Required)
    implementation 'com.github.dotstudiopro:dotstudiopro-android-dspplayer:2.2.54.2'
}
```

# Usage & Configuration
Include the view int he respective xml layout file
```
<fragment
        android:id="@+id/dspPlayerViewController"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:name="com.dotstudioz.dotstudioPRO.dspplayer.DSPPlayerViewController"
        />
```

# Configuration Parameters in the Activity where Player is to be included
<ul>
  <li>apikey      : Pass Company Api Key</li>
</ul>

# Referencing & Using DSPPlayerViewController
Assigning reference to the above declared fragment view
```
public DSPPlayerViewControllerPublic getDSPPlayerViewController() {
    if(dspPlayerViewController == null)
        dspPlayerViewController = ((DSPPlayerViewControllerPublic) getSupportFragmentManager().findFragmentById(R.id.dspPlayerViewController));
    return dspPlayerViewController;
}
```

# Initializing the player
```
getDSPPlayerViewController().initializationConfiguration(
    apikey
);
```