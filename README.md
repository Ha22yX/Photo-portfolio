<div align="center">
  <h1>Photo Portfolio</h1>
  <p>A lightweight Flask photo portfolio with categorized galleries, thumbnail generation, and admin upload tools.</p>

  <p>
    <a href="README.zh-CN.md">Chinese</a>
    &middot;
    <a href="#quickstart">Quickstart</a>
    &middot;
    <a href="#features">Features</a>
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

## Overview

This project is a small self-hosted photo site for presenting personal photography without rebuilding static pages by hand.

It focuses on practical gallery operations: upload photos, generate lighter thumbnails, group work into categories, and keep the public browsing experience simple.

## Features

- Public gallery pages for browsing photo work.
- Login-protected admin flow for uploading and managing images.
- Thumbnail/cache generation for large high-resolution photos.
- Folder-style organization for categories and portfolio sections.
- Simple Flask deployment path for a personal website or small VPS.

## How It Works

1. Place original photos in the configured photo storage path or upload them through the admin UI.
2. The app builds thumbnail/cache files so gallery pages stay responsive.
3. Visitors browse public templates while admin routes stay behind login.
4. Runtime folders keep photos, uploads, cache, and logs outside the README/documentation layer.

## Quickstart

Run the project locally with the commands below.

```bash
git clone https://github.com/Ha22yX/Photo-portfolio.git
cd Photo-portfolio
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Open `http://127.0.0.1:5001`. Change the default admin password before exposing the app publicly.

## Configuration

| Item | Purpose |
| --- | --- |
| `SECRET_KEY` | Set a long random value for sessions. |
| Admin account | The development default is for local testing only; change it before deployment. |
| Photo folders | Keep originals, uploads, and generated cache backed up. |
| Large uploads | The app is configured for large images, so server limits may also need adjustment. |

## Tech Stack

| Layer | Technology | Role |
| --- | --- | --- |
| Backend | Flask | Routes, upload flow, gallery rendering. |
| Images | Pillow, pyexiv2 | Thumbnail generation and metadata/image handling. |
| Auth | Flask-Login, Werkzeug | Admin session and password helpers. |
| Frontend | Jinja templates | Public gallery and admin pages. |

## Project Layout

```text
app.py                  Flask application
templates/              public and admin templates
requirements.txt        Python dependencies
app.log                 local runtime log
.github/assets/         README overview asset
```

## Status

Portfolio utility project for personal use. It is suitable for local or small-server deployment after credentials, upload paths, and access controls are configured.

## License

No project-wide open-source license has been declared yet.
