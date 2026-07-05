# Contributing to YT Video Summarizer

Thank you for considering contributing to YT Video Summarizer! Contributions of all kinds are welcome — bug fixes, new features, documentation improvements, and suggestions.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)
- [Style Guidelines](#style-guidelines)

## Code of Conduct

Be respectful and constructive. This project welcomes contributors of all experience levels, and we want it to remain a friendly, harassment-free space for everyone.

## Getting Started

1. Fork the repository on GitHub.
2. Clone your fork locally:
   ```bash
   git clone https://github.com/adhvaith267/yt-video-summarizer.git
   cd yt-video-summarizer
   ```
3. Create a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
4. Create a `.env` file in the project root with your Gemini API key:
   ```env
   GEMINI_API_KEY=YOUR_API_KEY_HERE
   ```
5. Run the app locally to confirm everything works:
   ```bash
   python app.py
   ```

## How to Contribute

1. Create a new branch for your change:
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Make your changes, following the [Style Guidelines](#style-guidelines) below.
3. Test your changes locally to make sure nothing is broken, especially the transcript fetching (`services/youtube.py`) and Gemini summarization (`services/gemini.py`) flows.
4. Commit your changes with a clear message:
   ```bash
   git commit -m "Add: short description of your change"
   ```
5. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
6. Open a Pull Request against the `master` branch of the original repository.

## Pull Request Guidelines

- Keep pull requests focused on a single feature or fix.
- Write a clear title and description of what your PR does and why.
- Reference any related issues (e.g. `Fixes #12`).
- Ensure the app runs without errors and streams summaries correctly before submitting.
- Be responsive to review feedback.

## Reporting Bugs

If you find a bug, please open an issue and include:

- A clear, descriptive title
- Steps to reproduce the issue (including the YouTube URL used, if relevant)
- Expected vs. actual behavior
- Any error messages or console output
- Your environment (OS, Python version, browser)

## Suggesting Features

Feature suggestions are welcome. Please open an issue describing:

- The problem your feature would solve
- How you imagine it working
- Any alternatives you've considered

## Style Guidelines

- Follow [PEP 8](https://peps.python.org/pep-0008/) conventions for Python code.
- Keep route handlers in `routes/` thin; put business logic in `services/`.
- Use descriptive variable and function names.
- Comment non-obvious logic, especially around streaming responses and Gemini API calls.
- Keep frontend markup consistent with the existing Tailwind CSS conventions in `templates/`.
- Never commit your `.env` file or API keys.

---

Thank you for helping improve YT Video Summarizer!
