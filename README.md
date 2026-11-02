# Bedrock Launcher (Android)

A Minecraft: Bedrock launcher shell for Android with a Minecraft-launcher look.
Kotlin + Jetpack Compose, no third-party libraries beyond AndroidX.

## What it does
- **Play**: detects Minecraft Bedrock and launches it; imports `.mcpack` / `.mcaddon` / `.mcworld` files.
- **Add-ons**: curated filters (Popular, Performance, Quality of life, Building, Survival) on live CurseForge data, one-tap install.
- **Shaders**: shader packs from CurseForge, one-tap install.
- **CurseForge**: full search of CurseForge's Bedrock content.
- **Boost**: FPS presets (settings checklist) and shortcuts to the Android settings that affect performance.

Installing hands the downloaded file to Minecraft, which shows its own import screen.
That is the supported way on Android 11+, where apps can't write into Minecraft's folders.

## Get the APK (no Android Studio needed)
1. Create a GitHub repo and upload this folder's contents (keep the `.github` folder).
2. Open the **Actions** tab, run **Build APK**, then download `bedrock-launcher-apk`.
3. Unzip it, copy `app-debug.apk` to your phone, and allow "install unknown apps".

## Or build locally
Open the folder in Android Studio (Koala or newer) and choose Build > Build APK(s).

## CurseForge key
Create a free key at https://console.curseforge.com and paste it in the **CurseForge** tab.
You can bake one into your own build with `CURSEFORGE_API_KEY` in `local.properties`,
but never share an APK built that way; the key can be extracted from it.

## Not done / limits
- Not compiled or run on a device yet: this was written without an Android SDK available.
  Expect to fix a few small build errors on first compile.
- It can't raise FPS beyond the game's settings, set CPU priority for other apps, or kill
  background apps; Android doesn't allow that without root.
- No game patching, no code injection, and no bundled third-party shader (licenses forbid redistribution).
