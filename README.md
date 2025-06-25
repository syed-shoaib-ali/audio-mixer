# 🎷 Audio Mixer – Public Documentation

This repository contains public documentation for the [`audio-mixer`](https://www.npmjs.com/package/audio-mixer) npm package.

> ⚠️ **Note:** The source code is private. This repo is for documentation only.

---

## 📦 Installation

```bash
npm install @syyedshoaib/audio-mixer
```

---

## 🔧 Basic Usage

```ts
import { AudioMixer, addAudioMixerPlaybackEndedListener } from 'audio-mixer';

// Load a track
const { sound, status } = await AudioMixer.loadSoundAsync(
  playerId,       // number
  localUri        // string
);

// Set volume (optional)
await AudioMixer.setVolumeAsync(playerId, 0.8);

// Play the track
await AudioMixer.playAsync(playerId, true); // true = loop playback

// Listen for when a track finishes
 const sub = AudioMixer.addListener("onPlaybackEnded", ({ playerId }) => {
    callback(playerId);
  });

// Stop a specific track
await AudioMixer.stopAsync(playerId);

// Unload all tracks
await AudioMixer.unloadAllAsync();
```

---

## 📚 Features

* 🎹 Add and mix multiple audio tracks
* 🎷 Volume and playback control
* 🦨 Lightweight and dependency-free
* ⚙️ Built specifically for **Expo (iOS)** environments

---

## 📄 License

**MIT**

---

## 📬 Contact

For feature requests, bug reports, or access to the private source code (if you’re a collaborator), contact:

**Syed Shoaib Ali**
🔗 [GitHub – syed-shoaib-ali](https://github.com/syed-shoaib-ali)
📧 [syyedshoaib.official@gmail.com](mailto:syyedshoaib.official@gmail.com)

---

Let me know if you'd like to:

* 📘 Add API reference or advanced examples
* 🌐 Convert it to a GitHub Pages site
* 🔁 Auto-sync it from your private repo
