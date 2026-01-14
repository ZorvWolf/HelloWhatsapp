🔧 Setup Instructions
1️⃣ Android App

Build and install the app

App starts a local HTTP server at:

http://127.0.0.1:8080

2️⃣ Flask Server (PC)
from flask import Flask, request



Run:

python app.py

3️⃣ Start Ngrok
ngrok http 5000


Ngrok gives:

https://xxxx.ngrok.io

4️⃣ Android → Server Upload

The Android app sends screen frames and files via:

POST https://xxxx.ngrok.io/upload

🌐 Remote Access

Open in any browser:

https://xxxx.ngrok.io


You now have:

📺 Live screen

📁 File gallery

⬇️ File downloads

⚠️ Important Notes

No embedded Ngrok/SSH binaries (Android restrictions)

Works on Android 10+

Reverse proxy approach avoids execution permission issues

Designed for educational & research purposes

## 📺 Demo — Working in Action


[![Watch the demo](https://img.youtube.com/vi/tmnopqbYMRM/0.jpg)](https://youtu.be/tmnopqbYMRM)

▶️ Click the image to watch the full demo on YouTube



🧩 Future Improvements

Authentication (token / password)

WebSocket-based streaming

Multi-device support

File upload from web

Session-based access

⚖️ Disclaimer

This project is intended for educational, research, and personal use only.
The author is not responsible for misuse.

👤 Author

ZorvWolf
Android | Networking | Reverse Engineering | Security Research
