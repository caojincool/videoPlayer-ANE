# Video Player ANE V2.9.2 (Android+iOS)
video player ANE supported on Android and iOS 64-bit lets you play video files in android or iOS players. your videos can be locally availble on your device or they can be online. in the sample codes we have also used our YouTube link parser found here: https://github.com/myflashlab/AS3-youtube-parser-video-link/ and with that you can easily play YouTube videos too.

checkout here for the commercial version: http://www.myflashlabs.com/product/video-player-ane-adobe-air-native-extension/
you may like to see the ANE in action? check this out: https://github.com/myflashlab/videoPlayer-ANE/raw/master/FD/dist/theApp.apk

**NOTICE: the demo ANE works only after you hit the "OK" button in the dialog which opens. in your tests make sure that you are NOT calling other ANE methods prior to hitting the "OK" button.**

![Video Player ANE](http://www.myflashlabs.com/wp-content/uploads/2015/11/product_adobe-air-ane-extension-video-player-595x738.jpg)

# AS3 API:
```actionscript
import com.myflashlab.air.extensions.player.VideoPlayer;
import com.myflashlab.air.extensions.player.VideoType;

var _ex:VideoPlayer = new VideoPlayer();

// play from documentsDirectory
var vid:File = File.documentsDirectory.resolvePath("exVideoPlayer.mp4");
_ex.play(vid.nativePath, VideoType.ON_SD_CARD); // in demo ANE, this method works only if you have hit the "ok" button in the demo dialog.

// or play online
_ex.play("http://myflashlabs.com/showcase/Bully_Scholarship_Edition_Trailer.mp4", VideoType.ON_LINE);

// you can also play YouTube videos! please see the sample usage code for YouTube in the sample FlashDevelop project
```

This extension does not require any special setup in the air manifest .xml file

# Changelog
* Nov 04, 2014	>> V1.0: 	beginning of the journey!

* Nov 10, 2014	>> V2.0: 	Added online video playback for iOS
  *		>> V2.0: 	Supports youtube playback

* Jan 27, 2015 	>> V2.1: 	added support for iOS 64-bit

* Apr 21, 2015 	>> V2.2: 	removed android-support-v4.jar dependency in the android side

* Nov 03, 2015	>> V2.9:	doitflash devs merged into MyFLashLab Team.
* Dec 20, 2015 	>> V2.9.1: 	minor bug fixes

* Jan 20, 2016 	>> V2.9.2: 	bypassing xCode 7.2 bug causing iOS conflict when compiling with AirSDK 20 without waiting on Adobe or Apple to fix the problem.
  *							This is a must have upgrade for your app to make sure you can compile multiple ANEs in your project with AirSDK 20 or greater.
  *							https://forums.adobe.com/thread/2055508
  *							https://forums.adobe.com/message/8294948