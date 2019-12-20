# Player


# Create iOS Player
```swift
if let dspPlayerViewController = DSPPlayerViewController.getViewController() {
    dspPlayerViewController.view.frame = self.playerContainerView.bounds
    self.playerContainerView.addSubview(dspPlayerViewController.view)
    let dspVideo = DSPVideo()
    dspVideo.strId = "<video-id>"
    dspPlayerViewController.setCurrentVideo(curVideo: dspVideo)
}
```

