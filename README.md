# Snapreel

A lightweight, single-file screen recorder that runs entirely in the browser. No installs, no sign-ups, no uploads — recordings stay on your device.

## Getting started

1. Download `snapreel.html`
2. Open it in Chrome or Edge
3. Click **Start recording**, choose a screen or window, and go

That's it.

## Features

- Record your screen, a specific window, or a browser tab
- Capture system audio and/or microphone
- Pause and resume mid-recording
- Preview recordings in-app before downloading
- Three quality presets (High / Medium / Low)
- Dark mode support

## Browser support

| Browser | Supported |
|---|---|
| Chrome 72+ | Yes |
| Edge 79+ | Yes |
| Firefox 66+ | Partial — no system audio capture |
| Safari | No — `getDisplayMedia` not supported |

## Quality presets

| Preset | Bitrate | Best for |
|---|---|---|
| High | 2.5 Mbps | Detailed UI walkthroughs, tutorials |
| Medium | 1 Mbps | General use (default) |
| Low | 400 Kbps | Quick clips, small file sizes |

## Output format

Recordings are saved as `.webm` (VP9/Opus). This plays natively in Chrome, Edge, and Firefox. To convert to MP4, you can use [HandBrake](https://handbrake.fr/) (free) or FFmpeg:

```bash
ffmpeg -i recording.webm -c:v libx264 -c:a aac output.mp4
```

## Privacy

All recording and processing happens locally in your browser. No data is sent to any server.

## Contributing

Issues and pull requests are welcome. Please open an issue first for any significant changes.

## Dependencies

- [Tabler Icons](https://tabler.io/icons) — loaded from jsDelivr CDN for the UI icons. Everything else is vanilla HTML, CSS, and JavaScript.

## License

This project is licensed under the [GNU Affero General Public License v3.0](LICENSE). If you modify and deploy Snapreel, you must make your source code available under the same license.
