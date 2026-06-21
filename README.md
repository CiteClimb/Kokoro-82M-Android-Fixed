# Kokoro-82M-Android
A fixed version of the minimal Android demo app for **Kokoro-82M** TTS model in int8 quantization.

### Changes from the [Original Repository](https://github.com/puff-dayo/Kokoro-82M-Android):
- Original version had a backend bug that closed the OrtSession after generating a single message, causing an error message to pop up after consecutive attempts to generate audio.
- Original version also didn't fit my screen vertically in the Mixer tab, and could potentially not fit some screens vertically in the Home tab, so I decreased the height of the slider, the maxmimum line count of the Text to speak box to 10 in both, decreased the minimum to 1 in both, and also allowed the entire page to scroll up and down in both tabs in case even these vertical height optimizations aren't enough.
- The tab icons were slightly misleading: the Home and Build icons for "Basic" and "Mixer". I have now made them "Single-model" with the Voice Selection icon and "Multi-model" with the Merge icon.
- Many button labels were also misleading, like the "Apply Mix" button in the Mixer/Multi-model tab for example, which doesn't just apply the mix settings, but also generates audio from the text above and plays it.
- Speaking of this tab, I changed the default mix to some very unique voices for contrast and to show how the mix combines multiple qualities.
- Also, the spherical interolation implementation is broken, though I do not know why, so I will just mark it with [BROKEN] for now.
- Another UI thing I noticed was that the sliders for speak speed are not very high accuracy even though Kokoro supports any float, so I set them to go to the hundredths place.
- Finally, I decreased the build SDK to 34 (Android 14) so the prebuilt binary is slightly more compatible. You can still change this in Project/app/build.gradle.kts though.

### How to Build
1. Download/install Android Studio (I used Panda, but some other IDE versions also work)
2. Upgrade/downgrade to AGP 8.x (I used 8.13.2)
3. Gradle Sync
   *(If you want to, modify the build and target SDK version in Project/app/build.gradle.kts)*
4. Build APK file and click "[locate](this-link-is-just-for-formatting-purposes-because-the-locate-text-is-blue-in-the-android-studio-notification.lol)" to jump to output .apk file location

### Prebuilt .apk file
See [release](https://github.com/CiteClimb/Kokoro-82M-Android-Fixed/releases/).

### Screenshots
<img width="540" height="1170" alt="Single-model Kokoro-82M-Android-Fixed" src="https://github.com/user-attachments/assets/b5139579-c53c-4735-a568-36c2b8a31c14" />
<img width="540" height="1170" alt="Multi-model Top Kokoro-82M-Android-Fixed" src="https://github.com/user-attachments/assets/c29cd7b1-9a59-4fc3-b080-7cfe069dbd56" />
<img width="540" height="1170" alt="Multi-model Bottom Kokoro-82M-Android-Fixed" src="https://github.com/user-attachments/assets/08fe08aa-bb4e-460b-ae52-480bf2b1b322" />
