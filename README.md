# CEH-Practice-Exam
CEH AI Practice Exam
# CEH v12 AI Practice Test — Local Setup

## Prerequisites
- Node.js 18+ installed → https://nodejs.org

## Setup (one time)

```bash
# 1. Unzip and enter the folder
cd ceh-app

# 2. Install dependencies
npm install

# 3. Add your API key
# Open src/App.jsx and replace:
#   const API_KEY = "YOUR_API_KEY_HERE";
# with your actual Anthropic API key from:
#   https://console.anthropic.com/settings/api-keys
```

## Run

```bash
npm run dev
```

Then open **http://localhost:5173** in your browser.

## Notes
- The app calls the Anthropic API directly from the browser using `anthropic-dangerous-direct-browser-access: true`
- Your API key is only in your local file — never committed or shared
- Retry logic handles 529 overload errors automatically (4 attempts, 5s–20s backoff)
- Each session generates 25 fresh questions — unlimited unique batches

Expanded Read-Me
- Step 1 — Prerequisites: Install Node.js
Node.js is the engine that runs the app on your computer. If you don't have it yet, go to nodejs.org and download the LTS version (the one labeled "Recommended for most users"). Install it like any normal program. To confirm it worked, open your terminal and type:
node -v
You should see a version number like v20.x.x.

Step 2 — Unzip and enter the folder
After downloading ceh-app.zip, unzip it. You'll get a folder called ceh-app. Then open your terminal, navigate to where you unzipped it, and run:
cd ceh-app
cd just means "change directory" — it moves you into that folder.

Step 3 — Install dependencies
npm install
This downloads all the third-party packages the app needs (React, Vite, etc.). It only takes 30–60 seconds. You'll see a node_modules folder appear — that's normal, don't touch it.

Step 4 — Add your API key
Open the file src/App.jsx in any text editor (Notepad, VS Code, whatever you have). Find this line near the top:
jsconst API_KEY = "YOUR_API_KEY_HERE";
Replace YOUR_API_KEY_HERE with your real key from console.anthropic.com/settings/api-keys. It looks like sk-ant-api03-.... Save the file.

Step 5 — Run it
npm run dev
This starts a local web server. You'll see output saying something like Local: http://localhost:5173. Open that URL in your browser and the app is live.
