<div align="center">

# YT Video Summarizer

A sleek, modern web application for fetching YouTube video transcripts and generating high-quality summaries using Google Gemini.

[![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.x-black.svg)](https://flask.palletsprojects.com/)
[![Gemini](https://img.shields.io/badge/AI-Google%20Gemini-4285F4.svg)](https://aistudio.google.com/)
[![Tailwind CSS](https://img.shields.io/badge/CSS-Tailwind-38B2AC.svg)](https://tailwindcss.com/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Gemini Model](#gemini-model)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Usage](#usage)
- [Project Structure](#project-structure)

## Overview

YT Video Summarizer fetches YouTube video transcripts and generates concise, high-quality summaries powered by Google Gemini. It features a clean, responsive dark-mode interface built with Tailwind CSS, and streams AI-generated summaries to the client in real time.

## Features

- **Modern Dark-Mode UI** built with Tailwind CSS
- **Gemini-Powered Summaries** using `models/gemini-2.5-flash`
- **Multi-Language Support** — English, German, French, Spanish, Japanese, Korean, and the original transcript language
- **Real-Time Streaming** of summaries, delivered chunk-by-chunk
- **Efficient Transcript Fetching** using `yt-dlp`

## Gemini Model

This project uses the following Gemini model:

```
models/gemini-2.5-flash
```

### Why this model

- Fast and cost-effective
- Large context window
- Supports streaming
- Available in modern Gemini projects

Model usage is defined in `services/gemini.py`.

## Tech Stack

| Layer     | Technology                             |
|-----------|------------------------------------------|
| Backend   | Python, Flask                           |
| AI        | Google Gemini API (`google-genai` SDK)  |
| Frontend  | HTML, Tailwind CSS, Vanilla JavaScript  |
| Other     | yt-dlp, python-dotenv                   |

## Prerequisites

- Python 3.11 or higher
- A Google Gemini API key

### Getting a Gemini API Key

1. Visit [aistudio.google.com](https://aistudio.google.com/)
2. Create or select a project
3. Enable the Gemini API
4. Generate an API key

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/yt-summarizer.git
cd yt-summarizer
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
```

**macOS / Linux**
```bash
source venv/bin/activate
```

**Windows**
```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project root:

```env
GEMINI_API_KEY=YOUR_API_KEY_HERE
```

> **Note:** Do not wrap the key in quotes.

## Usage

Run the application:

```bash
python app.py
```

Then open your browser and navigate to:

```
http://localhost:5000
```

Paste a YouTube video URL, select your preferred summary language, and watch the summary stream in real time.

## Project Structure

```
yt-summarizer/
├── routes/
│   └── main.py            # Application routes
├── services/
│   ├── gemini.py          # Gemini API integration and summarization logic
│   └── youtube.py         # YouTube transcript fetching (yt-dlp)
├── templates/
│   └── index.html         # Main frontend template
├── .gitignore
├── app.py                 # Application entry point
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```
<div align="center">
Built with Flask, Gemini, and Tailwind CSS
</div>
