# 🌿 Eternal Garden

> A secure, single-page sanctuary for encrypted echoes, real-time media synchronization, and peer-to-peer streaming.

Eternal Garden is an interactive, browser-based chat application designed to provide a highly secure and aesthetically immersive experience. It features end-to-end WebCrypto AES-CBC encryption, completely locking down communications, alongside a rich Dark Forest UI. The environment is designed as a locked, single-page experience—preventing standard body scrolling to maintain immersion while handling scroll boundaries strictly within the chat container.

## ✨ Key Features

### 🔐 Cryptography & Security
* **End-to-End Encryption:** Utilizes native WebCrypto API (AES-256-CBC) to encrypt all payloads before they leave the browser.
* **Ephemeral Keys:** Keys are derived using PBKDF2 with a user-provided passkey and room ID as the salt.
* **Zero-Knowledge Server:** The Firebase database only stores ciphertext and base64 initialization vectors. 

### 🎬 Media & Synchronization
* **Peer-to-Peer Local Video Hosting:** Stream `.mp4`, `.webm`, or `.ogg` files directly from your local machine to other users in the room using WebRTC via PeerJS, bypassing server bandwidth limits.
* **Synchronized YouTube Playback:** Paste a YouTube URL to instantly sync video playback states (play, pause, seek) across all active clients in the room via the YouTube IFrame API.
* **Smart Media Layer:** A dedicated, non-intrusive 16:9 media player that seamlessly overlays the chat when active.

### 🎨 Dark Forest UI & Interactive Design
* **Immersive Aesthetic:** A deep charcoal and midnight black UI layered with drifting, golden firefly animations.
* **Dynamic User Colors:** Generates a unique, natural palette (Yellow, Violet, Orange, Green) based on string-hashing the user's name, complete with matching text tints and border accents.
* **Strict Single-Page Architecture:** Viewport is strictly locked (`overflow: hidden` on the body) to prevent native window scrolling, providing a native app-like feel.
* **Custom Branding:** Features a minimalist, inline SVG heart (`💗`) favicon to replace default browser/platform icons.

### 🎲 Gamification & Interactions
* **Interactive Mentions:** Usernames are dynamically highlighted with their generated accent colors when mentioned in the chat.
* **Truth or Dare Module:** Typing specific trigger phrases (e.g., "T or D?") deploys an interactive voting module directly into the chat flow, gamifying the conversation.
* **Contextual Replies:** Double-click any message to instantly generate a targeted reply banner.

## 🛠️ Tech Stack & Architecture

* **Frontend Layout:** HTML5, CSS3, Tailwind CSS (via CDN for rapid utility styling).
* **Typography:** *Cinzel* (majestic headers), *Playfair Display* (ethereal accents), and *Inter* (readable body text).
* **Backend / State Management:** Firebase Realtime Database (Modular SDK v12+).
* **WebRTC / P2P:** PeerJS (v1.5.2).
* **Media API:** YouTube IFrame API.

## 🚀 Getting Started

Because Eternal Garden uses a serverless frontend architecture, installation is incredibly simple.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Mayborg/eternal-garden.git](https://github.com/Mayborg/eternal-garden.git)
