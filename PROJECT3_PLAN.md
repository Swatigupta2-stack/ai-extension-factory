# Project 3: Chrome Extension Generator (Extensio.ai)

## Project Overview
Build a no-code platform where users describe a Chrome extension requirement in plain English, and AI generates all necessary files (manifest.json, content.js, popup.html), zips them, and provides an instant download.

## Tech Stack
- **Backend**: Node.js + Express (existing)
- **AI**: Google Gemini 1.5 Flash (already integrated)
- **File Processing**: archiver (npm package)
- **Frontend**: React (existing)

## Implementation Plan

### Week 1: The Prompt Engineer ✅

#### Goal: Perfect LLM prompt to output valid Chrome V3 extension files

**Tasks Completed:**
- [x] Designed system prompt for JSON output
- [x] Tested with simple extension requests
- [x] Validated JSON parseability
- [x] Ensured manifest.json follows Chrome V3 spec

**Sample Prompts Tested:**
| Requirement | Status |
|-------------|--------|
| "Block all images and replace with red squares" | ✅ |
| "Change background color to dark mode" | ✅ |
| "Highlight all links on a page" | ✅ |

### Week 2: File System & Zipping (In Progress)

#### Goal: Convert JSON to downloadable zip file

**Tasks:**
- [ ] Write files to temporary directory
- [ ] Create zip archive using archiver
- [ ] Serve zip file for download
- [ ] Clean up temporary files

## API Endpoint

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/extensions/generate` | Generate extension zip from requirement |

## Request/Response Example

**Request:**
```json
{
  "requirement": "Create a Chrome extension that blocks all images and replaces them with a red square"
}
