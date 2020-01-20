# Player


# Initialize/Create Player reference
```
DSPPlayerViewControllerPublic dspPlayerViewController;

public DSPPlayerViewControllerPublic getDSPPlayerViewController() {
    if(dspPlayerViewController == null)
        dspPlayerViewController = ((DSPPlayerViewControllerPublic) getSupportFragmentManager().findFragmentById(R.id.dspPlayerViewController));
    return dspPlayerViewController;
}
```

# Declaring "DSPPlayerViewController" in respective XML
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

# Initializing the player
```
getDSPPlayerViewController().initializationConfiguration(
    apikey
);
```

# Playing a Video object to play the video
```
//initialize a video object and pass it to the player
DSPVideo dspVideo = new DSPVideo();
dspVideo.setVideoID("5db1760099f815b22ad3255b");

//start playback
getDSPPlayerViewController().playVideo(dspVideo);
```