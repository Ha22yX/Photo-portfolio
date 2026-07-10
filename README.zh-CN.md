<div align="center">
  <h1>Photo Portfolio</h1>
  <p>一个轻量级 Flask 摄影作品集，支持分类相册、缩略图生成和后台上传管理。</p>

  <p>
    <a href="README.md">English</a>
    &middot;
    <a href="#快速开始">快速开始</a>
    &middot;
    <a href="#核心能力">核心能力</a>
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

## 项目概览

这个项目是一个自托管摄影作品展示站，用来发布个人摄影作品，而不需要每次手动重建静态页面。

它关注实际维护流程：上传照片、生成较轻的缩略图、按分类组织作品，并保持公开浏览体验简单清晰。

## 核心能力

- 公开相册页面，用于浏览摄影作品。
- 带登录保护的后台上传和管理流程。
- 针对高分辨率图片的缩略图/缓存生成。
- 按分类或文件夹思路组织作品。
- 适合个人网站或小型 VPS 的 Flask 部署方式。

## 工作方式

1. 把原图放入配置的图片目录，或通过后台上传。
2. 应用生成缩略图和缓存，让公开页面加载更轻。
3. 访客浏览公开模板，管理操作放在登录后的后台。
4. 照片、上传文件、缓存和日志属于运行时数据，应独立备份。

## 快速开始

可以用下面的命令在本地运行项目。

```bash
git clone https://github.com/Ha22yX/Photo-portfolio.git
cd Photo-portfolio
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

打开 `http://127.0.0.1:5001`。公开部署前请修改默认管理员密码。

## 配置项

| 项目 | 作用 |
| --- | --- |
| `SECRET_KEY` | 用于会话安全，部署时应设置为随机长字符串。 |
| 管理员账号 | 开发默认值只适合本地测试，公开部署前必须修改。 |
| 图片目录 | 原图、上传文件和生成缓存需要单独备份。 |
| 大文件上传 | 应用允许较大图片，服务器/反向代理限制也可能需要同步调整。 |

## 技术栈

| 层级 | 技术 | 作用 |
| --- | --- | --- |
| 后端 | Flask | 路由、上传流程和相册渲染。 |
| 图片处理 | Pillow, pyexiv2 | 缩略图生成和图片/元数据处理。 |
| 认证 | Flask-Login, Werkzeug | 后台会话和密码工具。 |
| 前端 | Jinja templates | 公开相册和后台页面。 |

## 项目结构

```text
app.py                  Flask 应用
templates/              公开页面和后台模板
requirements.txt        Python 依赖
app.log                 本地运行日志
.github/assets/         README 概览图
```

## 项目状态

这是面向个人使用的作品集工具。配置好凭据、上传路径和访问控制后，可用于本地或小型服务器部署。

## 许可证

当前仓库尚未声明项目级开源许可证；公开复用或分发前建议先补充 License。
