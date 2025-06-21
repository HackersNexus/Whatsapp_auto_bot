# 🤖 WhatsApp Gemini AI Bot (Termux Compatible)

A smart WhatsApp bot built using [@whiskeysockets/baileys](https://github.com/WhiskeySockets/Baileys) and powered by **Google Gemini AI**, designed to run directly on **Termux** or any system with **Node.js**. This bot connects to WhatsApp Web and replies to incoming messages using Gemini's AI responses.

---

## 📱 Features

- 📲 QR Code authentication for WhatsApp Web  
- 🤖 Auto-replies to incoming messages using **Gemini AI**  
- 🔁 Reconnects automatically if disconnected (unless logged out)  
- 🧠 Uses Multi-File Auth for session persistence  
- 💻 Runs on Termux, Linux, Windows  

---

## 📦 Installation

### 1. Termux Setup

```bash
pkg update && pkg upgrade -y
pkg install nodejs git -y
apt update -y
apt upgrade -y
```

### 2. Clone the Repository

```bash
git clone https://github.com/HackersNexus/Whatsapp_auto_bot
cd Whatsapp_auto_bot
```

### 3. Install Dependencies

```bash
npm install @whiskeysockets/baileys qrcode-terminal pino
```

---

## 🚀 Run the Bot

```bash
node main.js
```

- A QR code will appear in the terminal.  
- Scan it using **WhatsApp > Linked Devices**.  
- Once connected, the bot will auto-reply using Gemini AI.  

---

## 🔑 Setup Gemini API Key

To use Gemini AI, you need an API key:

1. Go to [https://makersuite.google.com](https://makersuite.google.com)  
2. Generate your Gemini API key  
3. Open `index.js` and replace this line:

```js
const GEMINI_API_KEY = "your-api-key-here";
```

---

## 🗂 Folder Structure

```
whatsapp-gemini-bot/
├── auth_info/       # Auto-created: stores session credentials
├── main.js         # Main bot script file
└── README.md        # This file
```

---

## 🔐 Authentication

- The `auth_info/` folder is created automatically to save your WhatsApp session.  
- Don’t delete it unless you want to reset and re-scan the QR code.  

---

## 📌 Notes

- Handles plain text messages by default.  
- You can extend it to support media, group chats, or command logic.  
- Works offline after login (session stored locally).  
- Use it responsibly — don't spam or violate WhatsApp's policies.  

---

## 🧑‍💻 Author

Made with ❤️ by **HackersNexus**  
📺 [Subscribe on YouTube](https://youtube.com/@HackersNexus)  
Feel free to fork, modify, and improve the bot.  

---

## 📄 License

This project is licensed under the **MIT License**.  
You are free to use, share, and modify with credit.
