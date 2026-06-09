# elhubski

A Chrome extension that detects and answers Coursera quiz questions using Google's Gemini API, with optional auto-submit and course-item completion.

> **Disclaimer**: This tool is provided for educational and research purposes. Automating graded assessments may violate Coursera's Terms of Service and your institution's academic-integrity policy. You are responsible for how you use it.

## Features

- Question detection for both Quiz and Testing (graded) modes
- Answer generation via the Gemini API (model selectable in-panel)
- Optional answer highlighting and auto-check
- Optional auto-submit for Quiz and Testing modes
- Retry flow for questions that fail to match
- Auto-complete for course items (videos, readings, widgets, labs)
- Draggable, resizable floating control panel

## Requirements

- Google Chrome (or any Chromium-based browser with Manifest V3 support)
- A free Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)

## Installation

1. Download this repository (Code -> Download ZIP) and unzip it.
2. Open `chrome://extensions`.
3. Enable **Developer mode** (top-right).
4. Click **Load unpacked**.
5. Select the unzipped folder.

The **elhubski** panel appears on the right side of any Coursera page.

## Configuration

The extension reads its API key from the in-panel settings, stored locally in `chrome.storage`.

1. Open any Coursera page and locate the **elhubski** panel on the right.
2. Open the **API Key** tab.
3. Paste your Gemini API key, click **Test**, then **Save**.

## Usage

### Answer a quiz or test

1. Open a Coursera quiz or graded-assignment page.
2. In the **elhubski** panel, configure detection, highlight, auto-check, and auto-submit as needed.
3. Click **Start Detection**.

In Testing mode the extension advances through each question until the assignment is complete.

### Auto-complete course items

1. Open the course content page.
2. Open the **Auto Complete** tab.
3. Select the item types to mark, then run the action. The page reloads when finished.

## Privacy

- No telemetry and no external servers beyond the Gemini API.
- The API key is stored locally in `chrome.storage` and never leaves your browser except to call Gemini.
- Quiz content is sent to the Gemini API only to generate answers.

## License

MIT. See [LICENSE](LICENSE).
