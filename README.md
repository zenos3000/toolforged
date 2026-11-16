# TextureForge

An original Android app with three tools, in the same category as "SebTools"
(mobile sports-game texture/graphics editing) — built from scratch, not a
copy of any existing app's code, assets, or branding.

## Features

1. **UV Texture Editor** — load any image, pan/pinch-zoom/rotate it with
   touch gestures over a UV grid overlay, then export the result as a PNG.
2. **Face Texture Editor** — same gesture-based editor, with a face-outline
   guide (oval + eye/nose lines) instead of a grid, for positioning a head
   photo onto a texture template.
3. **Scorebug Maker** — type two team names and scores, cycle through color
   presets per team, and generate/export a scoreboard overlay PNG.

All three save to `Pictures/TextureForge` in the device gallery.

## This is a source project, not a compiled .apk

This sandbox has no Android SDK, no Gradle wrapper binaries, and no network
access to download them, so I could not compile an installable `.apk` here.
What you have is a complete, standard Android Studio project.

## How to build it yourself

1. Install [Android Studio](https://developer.android.com/studio) (free).
2. Open this `TextureForge` folder as a project (File > Open).
3. Let Gradle sync — it will download the Android Gradle Plugin, Kotlin
   plugin, and the AndroidX/Material dependencies listed in
   `app/build.gradle.kts` automatically.
4. Build > Build Bundle(s)/APK(s) > Build APK(s), or just press Run on a
   connected device/emulator.

Minimum SDK 26 (Android 8.0), target SDK 34.

## Project layout

```
TextureForge/
  settings.gradle.kts
  build.gradle.kts
  app/
    build.gradle.kts
    src/main/
      AndroidManifest.xml
      java/com/example/textureforge/
        MainActivity.kt
        UvEditorActivity.kt
        FaceEditorActivity.kt
        ScorebugMakerActivity.kt
        EditableImageView.kt   (shared pan/zoom/rotate view)
        ImageSaver.kt          (shared gallery export helper)
      res/layout/   (4 screens)
      res/values/   (strings, colors, theme)
```
