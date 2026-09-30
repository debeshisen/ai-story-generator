# 📖 AI Story Generator

> An AI-powered interactive storytelling application that transforms user-defined characters, settings, emotions, genres, and story prompts into personalized multi-part stories.

<p align="center">

[![Live Demo](https://img.shields.io/badge/🚀%20Live%20Demo-Streamlit-red?style=for-the-badge)](https://ai-story-generator-q82hadguw8swqtsupma272.streamlit.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge&logo=github)](https://github.com/debeshisen/ai-story-generator)

</p>

---

## 🚀 Overview

**AI Story Generator** is a web-based generative AI application built with **Python and Streamlit**.

The application uses **OpenRouter's API with the Mixtral 8x7B Instruct model** to generate creative stories based on user-provided inputs such as:

- Genre
- Character name
- Story setting
- Story tone
- Character emotion
- Opening sentence
- Desired story length

The application goes beyond one-time text generation by allowing users to **continue stories, listen to AI-generated narration, maintain story history, and export stories as PDF or DOCX files**.

### 🔗 Live Application

**[Launch AI Story Generator →](https://ai-story-generator-q82hadguw8swqtsupma272.streamlit.app/)**

> **Note:** The Streamlit Community Cloud deployment may temporarily sleep after periods of inactivity. If the application is sleeping, opening the link will wake the deployment.

---

# ✨ Features

### 🤖 AI Story Generation
Generate original stories using the **Mixtral 8x7B Instruct LLM** through the OpenRouter API.

### 🎭 Multiple Genres
Choose from:

- Fantasy
- Sci-Fi
- Romance
- Mystery
- Comedy
- Horror

### 🧑 Character Customization
Customize the story using:

- Character name
- Character emotion
- Story tone
- Story setting
- Opening sentence

### 🌍 Custom Story Settings

Choose from different environments including:

- Bookstore
- Town
- Village
- Party
- Forest
- Café
- Castle
- Space Station
- Island
- Unknown

### 🎨 Story Tone

Control the overall atmosphere of the generated story:

- Light
- Whimsical
- Mysterious
- Dramatic
- Dark

### 💓 Character Emotions

Characters can be assigned emotions such as:

- Neutral
- Happy
- Nervous
- Confident
- Sad
- Angry
- Excited
- Scared

### 📝 Automatic Story Titles

The application automatically generates a creative title for each generated story using the LLM.

### 🔄 Continue Story

Continue an existing story with additional AI-generated paragraphs while maintaining the selected genre, tone, and character emotion.

### 🔊 Voice Narration

Convert the generated story into spoken audio using **Google Text-to-Speech (gTTS)**.

### 📄 Export Stories

Download generated stories in:

- PDF format
- DOCX format

### 📚 Story History

Previously generated stories can be stored in the application's session history and accessed through the sidebar.

### 🌓 Light / Dark Mode

Switch between light and dark themes for a customized reading experience.

---

# 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Python** | Core application development |
| **Streamlit** | Interactive web application framework |
| **OpenRouter API** | LLM API integration |
| **Mixtral 8x7B Instruct** | AI story generation |
| **Requests** | API communication |
| **gTTS** | Text-to-speech narration |
| **FPDF** | PDF generation |
| **python-docx** | DOCX generation |
| **python-dotenv** | Environment configuration |
| **Streamlit Session State** | Story and history management |

---

# 🧠 How It Works

The application follows a prompt-driven generation pipeline:

```text
User Input
    │
    ├── Genre
    ├── Character
    ├── Setting
    ├── Tone
    ├── Emotion
    ├── Opening Line
    └── Story Length
          │
          ▼
   Prompt Construction
          │
          ▼
    OpenRouter API
          │
          ▼
 Mixtral 8x7B Instruct
          │
          ▼
  AI Story Generation
          │
          ├───────────────┐
          ▼               ▼
   Story Title       Story Content
          │               │
          └───────┬───────┘
                  ▼
          Streamlit Interface
                  │
        ┌─────────┼──────────┐
        ▼         ▼          ▼
     Continue   Narrate    Export
      Story      Story     PDF/DOCX
