# ⚡ Lightning

**Lightning** is a lightweight, cross-platform peer-to-peer (P2P) file transfer tool built with **Go**, **WebRTC**, and **WebSocket**. It enables **secure, fast, and direct file transfers** between devices without relying on intermediate servers.

---

## 📦 Version

Current version: **v0.0.1**

---

## ✨ Features

- ♾️ **No File Size Limit**  
- 🤖 **No Registration Required**  
- 🔒 **End-to-End Encrypted Transfer**  
- 💻 **Frontend / Backend Decoupled Architecture**  
- 🔄 **Auto-Update Support**  
- 📁 **Folder Compression + Streaming Transfer**  
- 🧠 **File or Folder Auto Detection**  
- 🪵 **Structured Logging (zap, debug level)**  

---

## 🔧 How It Works

### 🖥️ Frontend

- Displays file/folder transfer progress  
- Communicates with backend over WebSocket  
- Provides connection link to receiver

### 🧠 Backend (written in Go)

- Handles file/folder transmission  
- Compresses folders on the fly  
- Uses WebRTC + WebSocket for peer connection  
- Applies AES encryption for secure data  
- Detects and processes file vs folder  
- Logs every step using `zap` at debug level  

---

## 🔁 File Transfer Flow

1. **Right-click** a file/folder and choose to open with Lightning
2. Lightning client starts and **retrieves path**
3. Connects to signaling server to **create room ID** and generates a **share link**
4. Receiver opens the share link to connect
5. Once connected:
    - If path is a **file** → Directly transferred via WebRTC  
    - If it's a **folder** → Folder is compressed on-the-fly and streamed
6. After transfer completes → App exits automatically

---

## 🚀 Getting Started

Coming soon...

> Support for right-click integration, standalone `.exe` launcher, and auto-update logic will be documented soon.

---

## 🛠️ Tech Stack

| Layer     | Tech                  |
|-----------|------------------------|
| Language  | Go (Golang)            |
| Frontend  | HTML + JavaScript      |
| Backend   | WebRTC, WebSocket, zap |
| Update    | [go-github-selfupdate](https://github.com/rhysd/go-github-selfupdate) |
| Crypto    | AES (planned)          |

---

## ✅ TODOs

- [ ] Folder compression and streaming  
- [ ] Auto-copy room link to clipboard / open in browser  
- [ ] Improve update strategy & fallback  
- [ ] Add optional encryption support  
- [ ] Optimize transfer speed and memory usage  

---

## 🧠 Future Plans

- GUI interface (Electron or Wails)
- QR code sharing support
- Portable build for Windows & Linux
- Optional password-protected rooms

---

## 📝 License

MIT License

---

Made with ❤️ by [Wenbo Xu](https://github.com/xuwenbolan)
