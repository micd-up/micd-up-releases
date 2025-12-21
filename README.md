# HotDictation

A lightweight macOS menu bar app for voice-to-text transcription powered by OpenAI's Whisper. All processing happens locally on your Mac — no internet required, complete privacy guaranteed.

## Features

- **Global Hotkey** — Press Option+Space (customizable) to start dictating from anywhere
- **Local Processing** — Uses whisper.cpp for on-device transcription, no data leaves your Mac
- **Multiple Models** — Choose from 6 model sizes (75 MB to 3 GB) based on your accuracy/speed needs
- **99+ Languages** — Supports transcription in virtually any language
- **Flexible Output** — Paste directly, copy to clipboard, or save to history
- **Push-to-Talk or Toggle** — Choose your preferred recording mode

## Download

Download the latest release from the [Releases page](https://github.com/AmbientRun/HotDictation-releases/releases).

## Installation

1. Download `HotDictation.dmg` from the latest release
2. Open the DMG and drag HotDictation to your Applications folder
3. Launch HotDictation from Applications

### First Launch (Important)

Since HotDictation is distributed outside the Mac App Store, macOS may block it on first launch. To fix this:

```bash
xattr -cr /Applications/HotDictation.app
```

Then launch the app again.

Alternatively, you can right-click the app and select "Open" to bypass Gatekeeper.

## Permissions

HotDictation requires the following permissions to function:

| Permission | Why It's Needed |
|------------|-----------------|
| **Microphone** | To record your voice for transcription |
| **Accessibility** | To detect global hotkeys and paste text into other apps |

Grant these permissions when prompted, or add them manually in **System Settings → Privacy & Security**.

## Troubleshooting

### App won't open / "App is damaged" error

Run this command in Terminal:

```bash
xattr -cr /Applications/HotDictation.app
```

### Hotkey not working

1. Ensure Accessibility permission is granted in **System Settings → Privacy & Security → Accessibility**
2. Try removing and re-adding HotDictation from the list
3. Restart the app

### No audio being recorded

1. Check that Microphone permission is granted in **System Settings → Privacy & Security → Microphone**
2. Verify your microphone is working in other apps
3. Check the input device in System Settings → Sound

### Transcription is slow

- Try a smaller model (Settings → Model)
- Smaller models like "Tiny" or "Base" are much faster but less accurate
- Larger models provide better accuracy but require more processing time

### Text not pasting into apps

1. Verify Accessibility permission is enabled
2. Some apps may block automated pasting — try the "Copy to Clipboard" output mode instead

## System Requirements

- macOS 14.0 (Sonoma) or later
- Disk space varies by model (75 MB – 3 GB)

## Privacy

HotDictation processes all audio locally using whisper.cpp. No audio or transcriptions are ever sent to external servers. Your voice data stays on your Mac.

## License

Copyright 2024 Ambient Run. All rights reserved.
