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

个人摄影网站应该容易维护，而不是每次都手工重做页面。本应用提供一个小型自托管流程，用于上传、生成缩略图、整理并展示摄影作品。

## 工作流

- 通过后台流程上传照片。
- 生成缩略图，降低公开相册页面负担。
- 按分类或目录组织照片。
- 提供响应式作品集页面供访客浏览。

## 核心功能

- 基于 Flask 的相册和后台页面。
- 使用 Pillow 生成缩略图。
- 带登录保护的后台管理流程。
- 响应式 Jinja 模板用于浏览照片分类。

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

## 技术栈

| 层级 | 技术 | 作用 |
| --- | --- | --- |
| 后端 | Flask | 路由、上传流程和相册渲染。 |
| 图片 | Pillow | 缩略图生成和图像处理。 |
| 认证 | Flask-Login, Werkzeug | 后台会话和密码工具。 |
| 前端 | Jinja templates | 相册和后台界面。 |

## 项目结构

```text
app.py                  Flask application
templates/              public and admin templates
requirements.txt        Python dependencies
app.log                 local runtime log
```

## 项目说明

公开部署前请配置后台账号、上传目录和访问权限。
