# Project 3: Extensio.ai - Chrome Extension Generator

## Project Status: 🚧 In Development

### Repository
https://github.com/Swatigupta2-stack/ai-extension-factory

### Project Location
`C:\Users\swati\Downloads\aiExtension`

---

## Week 1: The Prompt Engineer ✅

**Goal:** Perfect LLM prompt to output valid Chrome V3 extension files

**Completed:**
- [x] Designed system prompt for JSON output
- [x] Integrated Google Gemini API
- [x] Created extensionService.js with JSON validation
- [x] Tested with multiple extension requirements
- [x] Added retry logic for invalid JSON

**Sample Extensions Working:**
| Requirement | Status |
|-------------|--------|
| "Block all images and replace with red squares" | ✅ |
| "Change background color to dark mode" | ✅ |
| "Highlight all links in yellow" | ✅ |

---

## Week 2: File System & Zipping 🔄

**Goal:** Convert JSON to downloadable zip file

**Completed:**
- [x] Created zipService.js with archiver integration
- [x] Temporary file creation and cleanup
- [x] ExtensionController with download handler
- [x] API routes configured

**Pending:**
- [ ] Frontend component integration
- [ ] End-to-end testing
- [ ] Deployment to production

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Node.js + Express |
| AI | Google Gemini 1.5 Flash |
| File Processing | archiver |
| Frontend | React + Vite (planned) |

---

## API Endpoint

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/extensions/generate` | Generate extension zip from requirement |

---

## Testing

```bash
curl -X POST http://localhost:5000/api/extensions/generate \
  -H "Content-Type: application/json" \
  -d '{"requirement": "Block all images"}' \
  --output extension.zip
