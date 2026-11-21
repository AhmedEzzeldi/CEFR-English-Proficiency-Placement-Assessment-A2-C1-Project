# 🎯 CEFR English Proficiency Placement Assessment (A2 – C1)

[![Live Demo](https://img.shields.io/badge/Live_Demo-Launch_Assessment-10b981?style=for-the-badge&logo=google-chrome&logoColor=white)](https://ahmedezzeldi.github.io/CEFR-English-Proficiency-Placement-Assessment-A2-C1-Project/)

A zero-dependency, client-side **CEFR English Proficiency Placement Platform** designed to evaluate candidates across **A2 (Elementary)**, **B1–B2 (Intermediate/Upper-Intermediate)**, and **C1 (Advanced)** bands. Built as a single-file web application, it combines strict anti-cheating proctoring, timed multi-skill diagnostics, live speech-to-text transcription, and automated PDF report generation.

👉 **[Try the Live Assessment Portal Here](https://ahmedezzeldi.github.io/CEFR-English-Proficiency-Placement-Assessment-A2-C1-Project/)**

## ✨ Key Features

### 1. Comprehensive 5-Section Assessment Architecture

* **Part 1 — Grammar & Vocabulary (10 Items):** Graded Multiple-Choice Questions (MCQs) and single-word gap-fills testing syntactic accuracy, tense consistency, inversion, and lexical range.
* **Part 2 — Reading Comprehension (12 Items):** Three progressively complex passages (A2 workplace routines, B1-B2 habit psychology, C1 algorithmic bias in AI) with timed comprehension and scanning tasks.
* **Part 3 — Listening Comprehension (8 Items):** Dynamic Text-to-Speech (`SpeechSynthesis API`) audio prompts with a strict **2-play limit** per clip to simulate authentic exam conditions.
* **Part 4 — Writing Assessment (2 Tasks):** Timed practical email (B1, 80–110 words) and analytical essay (C1, 140–180 words) with live word counters.
* **Part 5 — Speaking Assessment (3 Prompts):** Zero-prep spoken prompts with a 7-second reading countdown followed by automatic `MediaRecorder` audio capture (`.webm`) and continuous `Web Speech API` transcription with Words-Per-Minute (WPM) fluency metrics.

### 2. Automated Section Briefings & Paced Timers

* **12-Second Section Overview Screens:** Before each of the 5 sections begins, candidates receive an automated briefing detailing question count, task format, and allocated time limits.
* **Strict Individual Timers:** Questions auto-submit upon expiration with no backward navigation to ensure authentic proficiency measurement.

### 3. Proctoring, Security & Input Validation

* **Tab & Visibility Tracking:** Uses the `Page Visibility API` to log tab/window switches and total time away from the assessment.
* **Clipboard & Shortcut Lockdown:** Blocks `copy`, `cut`, `paste`, `drop`, right-click context menus, and developer shortcuts across all inputs and passages.
* **Global English-Only Enforcement:** Real-time ASCII input scrubbing ensures all candidate names, phone numbers, and exam answers contain valid English characters and digits.
* **Dynamic Canvas Watermark:** Renders a non-intrusive, session-specific watermark displaying the candidate's name and contact details across the viewport.
* **In-App Browser Guard:** Automatically detects restricted WebViews (WhatsApp, Facebook, Instagram) and prompts users to open in Chrome or Safari so microphone permissions work seamlessly.

### 4. Automated Official PDF Reporting

* Generates a clean, formatted A4 diagnostic report off-screen using `html2pdf.js`, complete with CEFR band accuracy breakdowns, skill scores, integrity logs, writing submissions, and speaking transcripts—plus downloadable `.webm` audio recordings for human pronunciation review.

## 🛠️ Tech Stack & Web APIs

* **Core:** Semantic HTML5, Modern CSS3 (CSS Variables, Flexbox/Grid), Vanilla JavaScript (ES6+)
* **Browser APIs:**
  * `MediaDevices.getUserMedia` & `MediaRecorder API` (Audio capture & `.webm` export)
  * `Web Speech API` (`SpeechRecognition` for continuous live transcription & `SpeechSynthesis` for listening prompts)
  * `Page Visibility API` (Anti-cheating focus tracking)
  * `HTML5 Canvas API` (Dynamic session watermarking)
* **External Library (CDN):** [`html2pdf.js`](https://github.com/eKoopmans/html2pdf.js) for client-side PDF generation

## 🚀 Getting Started

Because the entire application is engineered into a self-contained `index.html` file with zero build steps, deployment is instantaneous:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ahmedezzeldi/CEFR-English-Proficiency-Placement-Assessment-A2-C1-Project.git
   cd CEFR-English-Proficiency-Placement-Assessment-A2-C1-Project
   ```

2. **Run locally:**

   > **Note:** For microphone access and continuous `SpeechRecognition` to function properly, serve the file over `localhost` or `https://` rather than opening it directly via `file://`.

   * Using VS Code **Live Server**: Right-click `index.html` → *Open with Live Server*.
   * Or using Python:

     ```bash
     python -m http.server 8000
     ```

3. **Live Deployment:**
   * Hosted permanently via GitHub Pages at: [https://ahmedezzeldi.github.io/CEFR-English-Proficiency-Placement-Assessment-A2-C1-Project/](https://ahmedezzeldi.github.io/CEFR-English-Proficiency-Placement-Assessment-A2-C1-Project/)

## 📂 Project Structure

```text
CEFR-English-Proficiency-Placement-Assessment-A2-C1-Project/
├── index.html      # Complete single-file application (UI, Styles, Exam Engine, Proctoring, PDF Generator)
└── README.md       # Project documentation
```

## 👨‍💻 Author

**Ahmed Elaraby**

* Built to streamline accurate, proctored CEFR placement diagnostics for English language learners and educators.

## 📄 License

This project is licensed under the **MIT License** — feel free to fork, customize the question bank, or adapt it for your own educational assessments.
