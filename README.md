# Kokoro-82M-Android
A minimal Android demo app for **Kokoro-82M** TTS model in int8 quantization.
Original version had a backend bug that closed the OrtSession after generating a single message, causing an error message to pop up after consecutive attempts to generate audio.

## Screenshot(s)
<p align="center">
  <img src="https://github.com/user-attachments/assets/e44217f7-92b3-4f28-9d87-7a1797c80819" width="25%" />
  <img src="https://github.com/user-attachments/assets/81736bf6-cc51-4aae-aeb2-daae648fb7f9" width="25%" />
</p>


## How to Build
Android Studio (I used Panda, but some other IDE versions also work)
Upgrade/downgrade to AGP 8.x (I used 8.13.2)
Gradle Sync and Build

## Prebuilt apk files
See [release](https://github.com/CiteClimb/Kokoro-82M-Android-Fixed/releases/).
