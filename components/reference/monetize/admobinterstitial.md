# AdMob Interstitial

In this tutorial, we'll show you how to easily monetize your apps using **AdMobInterstitial **component. This component can be used to create AdMob full screen ADs

#### Assumption:

You have already created an AdMob AdUnitId. If you haven't, please follow Steps 1-6 from source [HERE](https://quickappninja.zendesk.com/hc/en-us/articles/115000826865-How-to-create-Banner-Admob-Ad-unit-ID-?mobile_site=true).

#### Ad Guidance:

Please see AdMob video guide below. It is very important to follow their Terms of Service \(ToS\) and guide:

[https://support.google.com/admob/answer/6128877?hl=en](https://support.google.com/admob/answer/6128877?hl=en)

#### Setup:

Create a new AppyBuilder project and name it TestAdmobFullScreen

From Monetize category, drag-and-drop AdMobInterstitial onto layout screen

![](/assets/book-admob-1.png)Select this component and for its designer AdUnitId, enter your AdUnitId. _**NOTE: For testing, you should use TEST AdUnitId. See link **_[_**HERE **_](https://developers.google.com/admob/android/test-ads)_**for these IDs. **_![](/assets/bookAdMob1.png)

![](/assets/book-admob-2.png)

Next, Select Screen1 and set the Screen1 **Sizing **to **Responsive**:

![](/assets/book-admob-responsive.png)

This component has blocks / events that are shown in image blow. **LoadAd **block is executed automatically on startup. If Ad is successfully loaded, the **AdLoaded **event will be triggered. DO NOT use LoadAd block in this event because it will create an infinite loop. If the Ad fails to load, then **AdFailedToLoad **will be triggered and you can check the Error or message parameters to inspect why Ad was not served

**ShowInterstatialAd **block can be used to display the AD that was last loaded.

**AdClosed **block, gets triggered when AD is closed. In this block, you can use LoadAd block to load the next ad and prepare for next AD display.

![](/assets/book-admob-3.png)

The AD can be displayed when changing screens or when user clicks a button. DO NOT encourage user to click in order to display the AD. Please follow Ad Guidance shown above.

##### From [iNetAjmer](http://community.appybuilder.com/u/inetajmer) AppyBuilder Member

You can also check the error message that may give some idea about the issue:![](/assets/AdMobBlocksErrorChecking.png)

