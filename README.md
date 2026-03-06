# Puppeteer Upload Image to Notion

A dual-purpose project containing:
1. **Puppeteer Script** - Automates uploading images to Notion pages
2. **FastAPI Backend** - Class-based REST API with user and item views

---

## 📁 Project Structure

```
├── main.js              # Puppeteer automation script
├── main.py              # FastAPI backend entry point
├── views.py             # API route handlers (users, items)
├── models.py            # Pydantic data models
├── config.json          # Configuration (image paths, Notion settings)
├── package.json         # Node.js dependencies
├── requirements.txt     # Python dependencies
├── image/               # Image assets for upload
└── run.sh               # Shell script to run the automation
```

---

## 🚀 Getting Started

### Puppeteer Script (Node.js)

**Prerequisites:**
- Node.js 16+
- Chrome/Chromium browser

**Install dependencies:**
```bash
npm install
```

**Configure:**
1. Edit `config.json` with your Notion API key and page ID
2. Place images in the `image/` directory
3. Update `CHROME_PROFILE_PATH` in `main.js` to your Chrome profile

**Run:**
```bash
node main.js
```

**Or use the shell script:**
```bash
./run.sh
```

### FastAPI Backend (Python)

**Prerequisites:**
- Python 3.8+

**Install dependencies:**
```bash
pip install -r requirements.txt
```

**Run:**
```bash
uvicorn main:app --reload
```

**API Endpoints:**
- `GET /` - Welcome message
- `GET /users` - List users
- `POST /users` - Create user
- `GET /items` - List items
- `POST /items` - Create item

**Docs:** Visit `http://localhost:8000/docs` for Swagger UI

---

## ⚙️ Configuration

### config.json
```json
{
  "notionApiKey": "your_notion_integration_token",
  "pageId": "your_notion_page_id",
  "imagePaths": ["path/to/image1.png", "path/to/image2.png"]
}
```

### Chrome Remote Debugging
For Puppeteer to work, launch Chrome with remote debugging:

**macOS:**
```bash
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --remote-debugging-port=9222
```

**Windows:**
```cmd
chrome.exe --remote-debugging-port=9222
```

---

## 📦 Dependencies

### Node.js
- `puppeteer` - Browser automation
- `@notionhq/client` - Notion API client
- `chrome-cookies-secure` - Cookie handling

### Python
- `fastapi` - Web framework
- `uvicorn` - ASGI server
- `pydantic` - Data validation

---

## 📝 Notes

- Both branches (`main` and `master`) are now synchronized
- The project contains both JavaScript (Puppeteer) and Python (FastAPI) code
- Image assets are stored in the `image/` directory

---

## 🤝 Contributing

1. Create a feature branch
2. Make your changes
3. Submit a pull request

---

## 📄 License

ISC
