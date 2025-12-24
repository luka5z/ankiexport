# Dictionary & Anki Exporter

A lightweight, single-file vocabulary study tool designed to bridge the gap between finding a new word and memorizing it.

It serves as a mobile-friendly dictionary that generates formatted flashcards for [Anki](https://apps.ankiweb.net/), supporting custom edits, themes, and configurable export formats.

## 🚀 Features

*   **Instant Lookup:** Queries the [Free Dictionary API](https://dictionaryapi.dev/) for definitions, phonetics, and parts of speech.
*   **Anki Integration:** Exports results to a CSV file pre-formatted for Anki (HTML supported).
*   **Customizable Export:** Choose your preferred CSV separator (Semicolon `;`, Comma `,`, Tab, or Pipe `|`). Default is **Semicolon**.
*   **WYSIWYG Editing:** Click "Edit" to modify definitions, add notes, or fix typos directly on the screen before exporting.
*   **Deep Linking:** Auto-search using URL parameters (e.g., `dictionary.html?w=serendipity`).
*   **Solarized Theme:** Beautiful Light and Dark modes based on the Solarized palette, with preference persistence.
*   **Mobile Optimized:** Responsive design with touch-friendly targets and layout adjustments for phones.
*   **Zero Dependencies:** Single HTML file. No build steps, no frameworks, no node_modules.

## 🛠 How to Use

### Basic Usage
1.  **Open:** Double-click `dictionary.html` in any web browser.
2.  **Search:** Type a word and hit Enter (or use the URL param: `?w=yourword`).
3.  **Edit (Optional):** Click the **Edit** button to modify the text directly. Click **Save** when done.
4.  **Configure:** Select your preferred separator from the dropdown (Default: `Sep: ;`).
5.  **Export:** Click the **CSV** download button.

### Importing to Anki
1.  Open Anki on your desktop.
2.  Go to **File > Import**.
3.  Select the downloaded `.csv` file.
4.  **Important Import Settings:**
    *   **Field Separator:** Ensure this matches what you selected in the app (e.g., Semicolon).
    *   **Allow HTML in fields:** ✅ Checked.
    *   **Field 1** mapped to: `Front` (The Word).
    *   **Field 2** mapped to: `Back` (The Definitions).

## 🎨 Personalization
The app uses the **Solarized** color scheme.
*   Toggle between **Light** and **Dark** modes using the icon in the header.
*   Your preference is saved automatically to your browser's local storage.

## 💻 Technical Details
Built entirely with **Vanilla JavaScript**, CSS Variables, and HTML5.
*   **Data Source:** `api.dictionaryapi.dev`
*   **File Generation:** Client-side `Blob` creation for CSV download.
*   **State Management:** `contenteditable` DOM for editing; `localStorage` for themes.
