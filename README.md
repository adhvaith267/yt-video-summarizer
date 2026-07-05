# YT Video Summarizer

A sleek, modern web application for fetching YouTube video transcripts and generating high-quality summaries using **Google Gemini**.  
The frontend is built with **Tailwind CSS**, featuring a clean, responsive dark-mode UI, while the backend streams AI summaries in real time.


## 🚀 Features

- 🌙 **Modern Dark-Mode UI** built with Tailwind CSS
- 🤖 **Gemini-Powered Summaries** using `models/gemini-2.5-flash`
- 🌍 **Multi-Language Support** (English, German, French, Spanish, Japanese, Korean, and original transcript language)
- ⚡ **Real-Time Streaming** summaries (chunk-by-chunk)
- 🎥 **Efficient Transcript Fetching** using `yt-dlp`


## 🧠 Gemini Model

This project uses the following Gemini model:

```
models/gemini-2.5-flash
```

### Why this model?
- Fast and cost-effective
- Large context window
- Supports streaming
- Available in modern Gemini projects

Model usage is defined in:

```
services/gemini.py
```


## 🛠 Technology Stack

### Backend
- Python
- Flask

### AI
- Google Gemini API (`google-genai` SDK)

### Frontend
- HTML
- Tailwind CSS
- Vanilla JavaScript

### Other
- yt-dlp (transcript fetching)
- python-dotenv (environment variables)



## ⚙️ Setup & Installation

### 1️⃣ Prerequisites

- Python **3.11+**
- A **Google Gemini API Key**


### 2️⃣ Get Your Gemini API Key

1. Visit: https://aistudio.google.com/
2. Create or select a project
3. Enable the **Gemini API**
4. Generate an API key


### 3️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/yt-summarizer.git
cd yt-summarizer
```


### 4️⃣ Create & Activate Virtual Environment

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


### 5️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```


### 6️⃣ Configure Environment Variables

Create a `.env` file in the project root:

```env
GEMINI_API_KEY=YOUR_API_KEY_HERE
```

⚠️ **Do NOT wrap the key in quotes**  


### 7️⃣ Run the Application

```bash
python app.py
```

Open in your browser:

```
http://localhost:5000
```



