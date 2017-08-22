# AdMob Rewarded Video

_**This help is in-progress...**_

Rewarded video ads are full screen video ads that users have the option of watching in full in exchange for in-app rewards.

This is a non-visible component that can be found under Monetize category.

![](/assets/rewardedvideo-1.png)

This component requires setting up an AdMob Ad Unit Id that is specifically setup for Rewarded Video. You can setup a new AdUnitId by logging into your AdMob account. _**NOTE:** For testing, you should use TestID so that you can test-out functionality of your app. You can use test-ID of ca-app-pub-3940256099942544/5224354917_.

From Designer, you can enter an AdUnitId \(see below\). This will auto-load and prepare the AD for display.

![](/assets/reward4.png)

Once AD is loaded, it will trigger the **RewardedVideo.AdLoaded **event-block. In this block. If the AD fails to load, it will trigger the **RewardedVideo.AdFailedToLoad** event-block which will include the error-code and the error-message, showing why the AD was not loaded was not loaded

![](/assets/reward7.png)

If the AD is loaded successfully, it meas that it is now ready to display. You now can use RewardedVideo.ShowAd to display the video-AD.

![](/assets/reward8.png)

The user will now be presented with the Video-AD.  The AD will include a count-down timer showing how many seconds of the AD is left. If the user watches the entire video, it will trigger the RewardedVideo.Rewarded event-block. This block will include the 'type' and 'amount' parameter which will include the values that was entered in the AdMob dashboard.

![](/assets/reward9.png)

To prepare the AD for next showing, the AD has to be loaded again using **RewardedVideo.LoadAd **block. A good place to reload the AD is to use the RewardedVideo.AdClosed event-block. This block gets triggered when user closes the video-AD.

![](/assets/reward10.png)

##### 

### 



