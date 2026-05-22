# ai-extension-factory
# 🧩 Extensio.ai — AI Chrome Extension Generator

**No code. Just describe. AI builds it. Download and install.**

---

## ✨ What It Does

| Step | Action |
|------|--------|
| 1 | User types what extension should do |
| 2 | AI generates manifest.json, content.js, popup.html |
| 3 | Backend zips all files |
| 4 | User downloads and installs in Chrome |

---

## 🎯 Examples

| You Say | You Get |
|---------|---------|
| "Block all images and replace with red squares" | Image blocker extension |
| "Change every website to dark mode" | Dark mode extension |
| "Highlight all links in yellow" | Link highlighter |
| "Remove all ads from YouTube" | Ad blocker |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Node.js + Express |
| AI | Google Gemini 1.5 Flash |
| File Processing | archiver |
| Frontend | React + Vite |

---

## 📋 Week 1: The Prompt Engineer ✅

- [x] Designed system prompt for Chrome V3 manifest
- [x] AI outputs valid JSON with all extension files
- [x] JSON validation and retry logic
- [x] Latency tracking

**File:** `backend/services/extensionService.js`

---

## 📋 Week 2: File System & Zipping ✅

- [x] Temporary file creation
- [x] ZIP archive generation using archiver
- [x] Download handler with proper headers
- [x] Automatic cleanup of temp files

**File:** `backend/services/zipService.js`

---

## 🚀 API Endpoint

```http
POST /api/extensions/generate
Content-Type: application/json

{
  "requirement": "Block all images and replace with red squares"
}

Response: extension.zip (download)
