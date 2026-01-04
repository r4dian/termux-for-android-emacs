# Termux APK signed for Android Emacs, works on Android 13

This repo contains an Android Termux APK, that I downloaded from Github actions CI, and re-signed with the Android Emacs key.

I downloaded the APK 2026-01-04 around 15:50 GMT.
The version is "termux-app_v0.118.0+bcb61c3-apt-android-7-github-debug_universal".

It was downloaded from: https://github.com/termux/termux-app/actions/runs/20686132456

I downloaded the signing key from here: https://github.com/emacs-mirror/emacs/tree/master/java/emacs.keystore

I used the following command to sign the APK. It was derived from https://github.com/emacs-mirror/emacs/tree/master/java/Makefile.in

```
cd C:\Users\████\AppData\Local\Android\Sdk\build-tools\36.1.0
.\apksigner.bat sign --v2-signing-enabled --ks D:\Downloads\emacs.keystore -debuggable-apk-permitted --ks-pass pass:emacs1 D:\Downloads\termux-app_v0.118.0+bcb61c3-apt-android-7-github-debug_universal.apk
```

This APK works for me on my Android device, that at the date of writing have an older version of Android provided by Sony respectively:
- Sony Xperia 10 III aka  XQ-BT52

To install apksigner, just install [the Android Studio](https://developer.android.com/studio) and launch it once so you can agree to everything, then it will add the build-tools folder.
