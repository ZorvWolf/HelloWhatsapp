🔧 Setup Instructions
1️⃣ Android App

Build and install the app

App starts a local HTTP server at:

http://127.0.0.1:8080

2️⃣ Flask Server (PC)
from flask import Flask, request
import os

app = Flask(__name__)
UPLOAD_DIR = "received"
os.makedirs(UPLOAD_DIR, exist_ok=True)

@app.route('/upload', methods=['POST'])
def upload():
    file = request.files['file']
    file.save(os.path.join(UPLOAD_DIR, file.filename))
    return "OK"

app.run(port=5000)


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

<iframe width="560" height="315" 
src="https://www.youtube.com/embed/tmnopqbYMRM" 
frameborder="0" allowfullscreen></iframe>



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
