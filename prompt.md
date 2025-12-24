# Prompt Instructions

## System Prompt
You are an expert Frontend Web Developer specializing in building lightweight, dependency-free utilities. 

Your goal is to write clean, modern, and accessible code. 
- You must output a SINGLE HTML file containing all HTML, CSS, and JavaScript. 
- Do not use frameworks like React, Vue, or Angular.
- Do not require a build step (Node.js, Webpack, etc.).
- You may use CDNs only for fonts or icons (e.g., FontAwesome), but logical libraries should be avoided unless necessary.
- Your code should be mobile-responsive and adhere to semantic HTML5 standards.
- After each code change prepare a summary that could be used as a Git commit message.

## User Prompt
Please build a single-page Dictionary Application designed for language learners who use Anki. 

The application must be a single HTML file with the following specific requirements:

### 1. API & Data
- Use the **Free Dictionary API** (https://dictionaryapi.dev/) to fetch definitions.
- Input: A text field for the word.
- Output: Display the word, phonetic transcription, and a list of meanings grouped by part of speech (noun, verb, etc.).

### 2. Anki Export (Core Feature)
- The app must generate and download a `.csv` file for Anki import.
- **Format:** The CSV must have two columns: "Front" and "Back".
  - **Front:** The word + phonetic transcription.
  - **Back:** The full definitions formatted as an HTML list (`<ul><li>...</li></ul>`).
- **Separator Configuration:** Include a dropdown menu (`<select>`) to let the user choose the CSV separator. 
  - Options: Semicolon (default), Comma, Tab, and Pipe.
- **Method:** Use client-side `Blob` creation to trigger the download.

### 3. WYSIWYG Editing
- The search result container must be editable. 
- Add a button "Edit" that toggles `contenteditable="true"` on the result area.
- When in "Edit" mode, change the button text to "Save".
- The Anki Export function must grab the *current* HTML from the DOM (including user edits) rather than the original API data.

### 4. URL Automation
- Support a query parameter `w`. 
- Example: If the user visits `index.html?w=serendipity`, the app should automatically populate the input and trigger the search on load.

### 5. Styling & Theme
- **Palette:** Use the **Solarized** color scheme strictly.
- **Theming:** Include a Light/Dark mode toggle button.
  - Use CSS variables for colors.
  - Persist the user's choice using `localStorage`.
  - Default to the system's `prefers-color-scheme` if no preference is saved.
- **Mobile Design:** Ensure the layout is fully responsive. On mobile devices, buttons should be large (touch-friendly), and the action buttons should stack vertically.

### 6. External Assets
- Use FontAwesome (via CDN) for UI icons (search, download, edit, moon/sun).

Please provide the complete, ready-to-run HTML code.
