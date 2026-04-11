# StudyPlan 📅

StudyPlan is a web-first application designed to eliminate the manual overhead of tracking academic deadlines and study tasks. Users can simply paste any unstructured text — an email, a course brief, a WhatsApp message, or a syllabus excerpt — into the **Smart Paste** zone. The built-in AI will intelligently extract subjects, deadlines, and deliverables, instantly populating an interactive calendar and fully categorised to-do lists.

## ✨ Features

- **Smart AI Extraction**: Powered by Google Gen AI (Gemini), instantly map chaotic, unstructured messages into structured task definitions.
- **Dynamic Task Board**: Categorizes tasks intuitively into '⚠ Due Soon', 'This Week', and 'Completed'.
- **Inline Editing Workspace**: Fast, modal-free inline viewing allows you to adjust dates, subjects, titles, and notes natively within the extraction view before saving.
- **Interactive Global Calendar**: Cycle seamlessly through months, automatically tracks color-coded deadlines, and click on any specific date to natively filter your live task board.
- **Conflict Notifications**: Automatically detects deadline clustering and visually warns you to spread out your study load.
- **Persistent Local DB**: Lightweight, local SQLite tracking for full relational entity mapping (Tasks + Subjects).

## 🛠️ Tech Stack

- **Frontend**: Custom Vanilla HTML, CSS, & Javascript. Engineered with extreme attention to aesthetic detail (Glassmorphism, CSS variable themes, smooth transition animations).
- **Backend API**: Node.js & Express REST architecture.
- **Database**: SQLite3.
- **AI Engine**: `@google/genai` (Google Gemini 2.5 Flash model).

## 🚀 Getting Started Locally

### Prerequisites
- [Node.js](https://nodejs.org/) installed on your machine.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Charushi06/StudyPlan.git
   cd "StudyPlan"
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Enable Full AI Extraction Capabilities:
   Copy `.env.example` to a new file named `.env` in the root directory and paste your Google Gemini API key:
   ```text
   GEMINI_API_KEY=your_gen_ai_key_here
   ```
   *Note: Without a key, the backend utilizes an internally built heuristic fallback mock capable of parsing dates/subjects but lacking complete NLP flexibility.*

4. Boot up the local server:
   ```bash
   node server.js
   ```

5. Launch the application:
   Head perfectly local to [http://localhost:3000](http://localhost:3000) in your modern browser of choice.

## 🚢 Recommended Deployment

Currently, the complete stack relies on a local SQLite database requiring a persistent disk volume.
For successfully hosting on the web, it's recommended to deploy natively on **[Render](https://render.com/)**, **[Railway](https://railway.app/)**, or **[Fly.io](https://fly.io)**, as they fully support persistent servers and disk volumes for NodeJS apps for free. 

> **Important Deployment Note:** Deploying to Netlify without refactoring the API logic will not work seamlessly out of the box because Netlify uses ephemeral serverless functions, which strictly prohibit persistent SQLite disk storage.

---
*Built with speed, aesthetics, and organization in mind. Phase 2 arriving soon.*
