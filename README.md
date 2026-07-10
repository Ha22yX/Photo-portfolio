<div align="center">
  <h1>Photo Portfolio</h1>
  <p>A lightweight Flask photo portfolio with categorized galleries, thumbnails, and admin upload tools.</p>

  <p>
    <a href="README.zh-CN.md">Chinese</a>
    &middot;
    <a href="#quickstart">Quickstart</a>
    &middot;
    <a href="#tech-stack">Tech Stack</a>
  </p>

  <p>
    <img alt="Python: Flask" src="https://img.shields.io/badge/Python-Flask-3776AB?style=for-the-badge&logo=python&logoColor=white" />
    <img alt="Images: Pillow" src="https://img.shields.io/badge/Images-Pillow-287866?style=for-the-badge" />
    <img alt="Portfolio: gallery" src="https://img.shields.io/badge/Portfolio-gallery-7d73b7?style=for-the-badge" />
  </p>
</div>

<p align="center">
  <img src=".github/assets/readme-hero.svg" alt="Photo Portfolio overview image" width="100%" />
</p>

## Why This Exists

A personal photography site should be easy to maintain without rebuilding pages manually. This app gives a small self-hosted workflow for uploading, thumbnailing, organizing, and presenting photo work.

## Workflow

- Upload photos through the admin flow.
- Generate thumbnails to keep the public gallery light.
- Group photos by category or folder-style organization.
- Serve a responsive portfolio page for browsing work.

## Features

- Flask-based gallery and admin pages.
- Thumbnail generation with Pillow.
- Login-protected admin workflow.
- Responsive Jinja templates for browsing photo categories.

## Quickstart

```bash
git clone https://github.com/Ha22yX/Photo-portfolio.git
cd Photo-portfolio
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Open `http://127.0.0.1:5001` after the server starts.

## Tech Stack

| Layer | Technology | Role |
| --- | --- | --- |
| Backend | Flask | Routes, upload flow, and gallery rendering. |
| Images | Pillow | Thumbnail generation and image handling. |
| Auth | Flask-Login, Werkzeug | Admin session and password helpers. |
| Frontend | Jinja templates | Gallery and admin UI. |

## Project Map

```text
app.py                  Flask application
templates/              public and admin templates
requirements.txt        Python dependencies
app.log                 local runtime log
```

## Notes

Configure admin credentials, upload folders, and deployment access before exposing the app publicly.
