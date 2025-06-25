# Audio Mixer – Public Documentation

This repository contains public documentation for the [`audio-mixer`](https://www.npmjs.com/package/audio-mixer) npm package.

> ⚠️ The source code is private. This repo is for documentation only.

---

## 📦 Installation

```bash
npm install audio-mixer

🔧 Basic Usage

import { AudioMixer } from 'audio-mixer';


// Add tracks (pseudo example)
//playerId:int  //localUri:string 
const { sound, status } = await AudioMixer.loadSoundAsync(
      playerId,
      localUri
    );

await AudioMixer.setVolumeAsync(playerId, 0.8); //optional if you want to adjust each track specifically
//playerId:int  //isLoop:boolean 
await AudioMixer.playAsync(playerId,isLoop);

const unsubscribe = addAudioMixerPlaybackEndedListener((playerId) => {
      console.log("Track ended globally", playerId);

      // You can trigger your custom logic here, like:
      // playNextTrack(playerId);
    });

//if you want to stop the specific one
await AudioMixer.stopAsync(playerId);

//if you want to unload all at once
await AudioMixer.unloadAllAsync(playerId);


📚 Features
	•	🎚️ Add and mix multiple audio tracks
	•	🎛️ Volume and timing control
	•	🪶 Lightweight and dependency-free
	•	⚙️ Built for expo environment specifically for IOS

📄 License

MIT


📬 Contact

For feature requests, bug reports, or access to the private source code (if you’re a collaborator), contact:

Syed Shoaib Ali
🔗 github.com/syed-shoaib-ali
📧 syyedshoaib.official@gmail.com


Let me know if you'd like to:

- Add API reference or advanced examples  
- Convert it to a GitHub Pages site later  
- Auto-sync it from your private repo


