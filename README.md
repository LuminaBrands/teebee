# TeeBee

TeeBee is a calm, parent-controlled home screen for Google TV, made for families with toddlers. You pick a few shows and movies from your phone, a gentle timer runs along the bottom while they watch, and when time is up the show fades to a calm goodbye.

**TeeBee is an early prototype.** Thank you for trying it. It is not in the Google Play Store yet.

## Download

**[TeeBee.apk (latest version)](https://github.com/LuminaBrands/teebee/releases/latest/download/TeeBee.apk)**

```
https://github.com/LuminaBrands/teebee/releases/latest/download/TeeBee.apk
```

Works on Google TV devices (Google TV Streamer, Chromecast with Google TV, onn 4K Pro, TVs with Google TV built in). Tested on the Google TV Streamer.

## Install on your Google TV

### Without a computer (using the free Downloader app)

1. On the TV, open the **Google Play Store**, search for **Downloader** and install it.
2. Open **Downloader**. When it asks, allow it to install apps. (If it doesn't ask: **Settings > Apps > Security & restrictions > Unknown sources**, turn on **Downloader**.)
3. In Downloader's address box, type **luminabrands.github.io/teebee** and select **Go**. Then select **Download TeeBee** and **Install**.
4. Open **TeeBee**, press **Up, Up, Down, Down** on the remote for the grown-up menu, and choose **Turn on the timer over other apps** and **Turn on episode detection**. Each opens the TV's own setting: switch TeeBee on, then press Back.
5. To keep **Home** on the remote on TeeBee: in the grown-up menu choose **Keep the Home button on TeeBee**. The TV's Accessibility settings open: choose **TeeBee Home button**, switch it on, then press Back. **Go to Google TV** in the grown-up menu lets a grown-up use Google TV until TeeBee is opened again.

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

Open TeeBee on the TV and scan the code with your phone's camera (phone and TV on the same Wi-Fi). A short welcome helps pick shows and movies, and the first time one is picked TeeBee asks how long they can watch.

Grown-ups: press **Up, Up, Down, Down** on the remote for settings.

## Updating later

Download and install the latest version the same way; your shows, movies and settings stay. When TeeBee arrives in Google Play, you'll need to uninstall this version first.
