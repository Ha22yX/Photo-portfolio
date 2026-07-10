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

A personal photo site should be easy to update without rebuilding the whole page. This app keeps the workflow simple: upload photos, generate thumbnails, and browse them by category.

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

## Features

- Category-based photo gallery for personal portfolio pages.
- Thumbnail generation with Pillow to reduce page weight.
- Admin-facing upload and management flow.
- Responsive templates for browsing photos on different screens.

## Tech Stack

| Layer | Technology | Role |
| --- | --- | --- |
| Backend | Flask | Routes, upload flow, gallery rendering. |
| Images | Pillow | Thumbnail generation and image handling. |
| Auth | Flask-Login, Werkzeug | Simple admin session and password helpers. |
| Frontend | Jinja templates | Gallery and admin pages. |


## Project Notes

This is a personal portfolio app rather than a hosted service. Configure credentials and image folders before exposing it publicly.
