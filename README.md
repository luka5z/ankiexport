# Dictionary & Anki Exporter

A lightweight, single-file vocabulary study tool designed to bridge the gap between finding a new word and memorizing it.

## 🎯 Purpose

This application serves three specific purposes:

### 1. Instant Dictionary Lookup
It allows users to quickly query the [Free Dictionary API](https://dictionaryapi.dev/) to get definitions, phonetics, audio, and parts of speech without needing a heavy commercial application or navigating websites cluttered with advertisements.

### 2. Automated Flashcard Creation (Anki Integration)
This is the application's core feature. Typically, language learners must manually copy and paste words and definitions into [Anki](https://apps.ankiweb.net/) (spaced-repetition software).
*   **The Problem:** Manual formatting is tedious and breaks the flow of reading.
*   **The Solution:** This tool generates a pre-formatted `.csv` file containing the **Word** on the "Front" and the **Full Definition** (with HTML styling preserved) on the "Back". This file can be imported directly into Anki for immediate study.

### 3. Technical Demonstration
From a development perspective, this project demonstrates how to build a functional, interactive web utility using **Vanilla JavaScript** (No React, Vue, or Angular) with **no build steps**. It showcases:
*   Fetching data from a public REST API (`fetch`).
*   Dynamic DOM manipulation (rendering HTML from JSON).
*   Client-side file generation (creating and downloading a CSV `Blob` entirely in the browser).

## 🚀 How to Use

1.  **Open:** Simply double-click `dictionary.html` to open it in any web browser.
2.  **Search:** Type a word and press Enter.
3.  **Export:** Click **"Download Anki CSV"** to save the flashcard data.

### Importing to Anki
1.  Open Anki and go to **File > Import**.
2.  Select the generated `.csv` file.
3.  Ensure "Allow HTML in fields" is enabled.
4.  Map Field 1 to **Front** and Field 2 to **Back**.
