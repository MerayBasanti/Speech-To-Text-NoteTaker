# Speech-To-Text-NoteTaker
NoteTaker that takes Speech from the user then retrieves transcript, summary, and title. 

# 📝 Offline Voice Note Taker

A **web-first note-taking app** that lets you record voice, transcribe it locally, generate a **title** and a **paragraph summary** using open-source models — all **offline, no server required**.  

---

## 🚀 Features
- 🎙️ Record voice directly in browser (offline).  
- 📝 Automatic transcription using **Whisper.cpp (WASM)**.  
- 📰 Auto-generated **titles** and **paragraph summaries** with **Transformers.js**.  
- 💾 Local storage with **IndexedDB** (your notes never leave your device).  
- 📱 PWA support → installable on desktop/mobile.  
- 🔍 Offline search across notes.  

---

## 🛠️ Tech Stack & Tools

### Core
- **React / Next.js** → Web frontend.  
- **IndexedDB + Dexie.js** → Local database for audio, transcripts & summaries.  

### AI Models
- **[Whisper.cpp](https://github.com/ggerganov/whisper.cpp)** (compiled to WebAssembly) → Speech-to-Text.  
  - Model: `tiny.en` (small, fast for browser).  
- **[Transformers.js](https://github.com/xenova/transformers.js)** → In-browser summarization & title generation.  
  - Models:  
    - `t5-small` (lightweight, faster).  
    - `facebook/bart-base` (better summaries, heavier).  

### UI & UX
- **MediaRecorder API** → Voice capture.  
- **HTML5 Audio** → Playback recorded notes.  
- **Service Worker + manifest.json** → Offline-ready PWA.  
