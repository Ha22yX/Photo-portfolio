<div align="center">
  <h1>Photo Portfolio</h1>
  <p>一个轻量 Flask 摄影作品集网站，支持分类相册、缩略图和后台上传管理。</p>

  <p>
    <a href="README.md">English</a>
    &middot;
    <a href="#快速开始">快速开始</a>
    &middot;
    <a href="#技术栈">技术栈</a>
  </p>

  <p>
    <img alt="Python: Flask" src="https://img.shields.io/badge/Python-Flask-3776AB?style=for-the-badge&logo=python&logoColor=white" />
    <img alt="Images: Pillow" src="https://img.shields.io/badge/Images-Pillow-287866?style=for-the-badge" />
    <img alt="Portfolio: gallery" src="https://img.shields.io/badge/Portfolio-gallery-7d73b7?style=for-the-badge" />
  </p>
</div>

<p align="center">
  <img src=".github/assets/readme-hero.svg" alt="Photo Portfolio 项目概览图" width="100%" />
</p>

## 项目价值

个人摄影网站应该能轻松维护，而不是每次都重做页面。本项目聚焦简单流程：上传照片、生成缩略图、按分类浏览。

## 快速开始

```bash
git clone https://github.com/Ha22yX/Photo-portfolio.git
cd Photo-portfolio
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

服务启动后打开 `http://127.0.0.1:5001`。

## 核心功能

- 按分类展示摄影作品，适合个人作品集。
- 使用 Pillow 生成缩略图，降低页面加载压力。
- 提供后台上传和管理流程。
- 响应式模板适配不同屏幕浏览。

## 技术栈

| Layer | Technology | Role |
| --- | --- | --- |
| 后端 | Flask | 路由、上传流程和相册渲染。 |
| 图片 | Pillow | 缩略图生成和图像处理。 |
| 认证 | Flask-Login, Werkzeug | 简单后台会话与密码工具。 |
| 前端 | Jinja templates | 相册和后台页面。 |


## 项目说明

这是个人作品集应用，不是公共托管服务。公开部署前请配置账号、图片目录和访问权限。
