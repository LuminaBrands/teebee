# TeeBee

TeeBee is a calm, parent-controlled home screen for Google TV, made for families with toddlers. You pick a few shows from your phone, a gentle timer runs along the bottom while they watch, and when time is up the show fades to a calm goodbye.

**TeeBee is an early prototype.** Thank you for trying it. It is not in the Google Play Store yet.

## Download

**[TeeBee.apk (latest version)](https://github.com/LuminaBrands/teebee/releases/latest/download/TeeBee.apk)**

```
https://github.com/LuminaBrands/teebee/releases/latest/download/TeeBee.apk
```

Works on Google TV devices (Google TV Streamer, Chromecast with Google TV, onn 4K Pro, TVs with Google TV built in). Tested on the Google TV Streamer.

## Install on your Google TV

### Without a computer (using the free Downloader app)

1. On the TV, open the **Google Play Store**, search for **Downloader** (by AFTVnews) and install it.
2. Go to **Settings > Apps > Security & restrictions > Unknown sources** and turn on **Downloader**. (On some TVs this is under **Settings > Privacy** or **Settings > Apps > Special app access > Install unknown apps**.)
3. Open **Downloader**, type the link above into its address box and select **Go**. When the download finishes, choose **Install**.
4. Open **TeeBee** from your apps. Its setup screen helps you turn on the two permissions it needs: **Display over other apps** (the timer over shows) and **Notification access** (to know when an episode ends).

This route is new and not yet tested step by step. If something doesn't match your TV, the computer route below always works.

### With a computer

1. On the TV: **Settings > System > About**, press **Android TV OS build** 7 times. Then **Settings > System > Developer options**: turn on **USB debugging** and **Wireless debugging**.
2. On the computer, download Google's free [SDK Platform-Tools](https://developer.android.com/tools/releases/platform-tools), unzip it, and open a terminal in that folder (on a Mac, type `./adb` instead of `adb`):

```
adb connect TV-address
adb install TeeBee.apk
adb shell appops set com.luminabrands.teebee SYSTEM_ALERT_WINDOW allow
adb shell cmd notification allow_listener com.luminabrands.teebee/com.luminabrands.teebee.MediaWatch
```

## Then

Open TeeBee on the TV and scan the code with your phone's camera (phone and TV on the same Wi-Fi). Pick shows, and the first time a show is picked TeeBee asks how long they can watch.

Grown-ups: press **Up, Up, Down, Down** on the remote for settings.

## Updating later

Download and install the latest version the same way; your shows and settings stay. When TeeBee arrives in Google Play, you'll need to uninstall this version first.
