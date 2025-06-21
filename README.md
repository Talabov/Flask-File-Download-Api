# 📁 Flask File Download API
---

🚀 **Need a ready-to-deploy version?**

Includes Docker, setup guide, sample responses, and full API structure.

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

A simple and effective Flask API for uploading and downloading files. Supports multiple file types and serves files via a public download link. Files are stored locally with unique names to prevent collisions.

---

## ✅ Key Features

- 📤 Upload files (images, PDFs, text) via `/upload`
- 📥 Download files using generated link `/download/<filename>`
- 🧾 Returns direct download URL after upload
- 🔒 Max file size: 5MB
- 🧼 Secure filenames with UUID + `secure_filename()`
- 🧪 Modular codebase, Docker-ready

---

## 🚀 Endpoints

### Upload File

**POST** `/upload`

**Request (form-data):**
- `file`: any file (jpg, png, jpeg, pdf, txt)

**Response:**
```json
{
  "filename": "uuid_filename.pdf",
  "url": "/download/uuid_filename.pdf"
}
```

---

### Download File

**GET** `/download/<filename>`

- Downloads the file as an attachment
- Must match exact filename from upload

**Response:**
- Returns the file or:
```json
{
  "error": "File not found"
}
```

---

## ⛔ Errors

```json
{ "error": "No file part" }

{ "error": "No selected file" }

{ "error": "Invalid file type" }

{ "error": "File not found" }
```

---

## ⚙️ Requirements

```bash
pip install -r requirements.txt
```

- Flask  
- Werkzeug

---

## 🖥 How to Run

```bash
python app.py
```

Or using Docker:

```bash
docker build -t file-download-api .
docker run -p 5000:5000 file-download-api
```

Server runs at:
```
http://127.0.0.1:5000/
```

---

## 🧪 Example Screenshots

- ✅ Successful upload (form-data)
- ✅ Download file via browser
- ❌ Invalid file type
- ❌ File not found error

> Screenshots saved in `/screens`

---

## 💼 Ready-to-Use Version

This project includes Docker support, modular code, and full functionality:

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

## 📬 Contacts

- Email: talabov.ali72@gmail.com  
- Telegram: [@talabovali](https://t.me/talabovali)

---

**Need this in another language/stack (Node.js, Go, etc)?**  
Custom dev available — just reach out.
