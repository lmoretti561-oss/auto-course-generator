# 🤖 Auto Course Generator

This repository powers an **AI-driven course generator** that connects to **Base44** (or any no-code tool) to automatically create and publish online courses as Markdown files.

Every time a new course is generated and sent via API → it’s saved here → GitHub Pages publishes it live automatically.

---

### 🧠 How it Works

1. Base44 AI Flow generates a course in Markdown format.
2. The generated Markdown file is committed to `/content` via GitHub API.
3. GitHub Pages automatically rebuilds and publishes your updated course site.

---

### 🪄 Example API Request (from Base44)
**POST**
https://api.github.com/repos/YOUR_USERNAME/auto-course-generator/contents/content/COURSE_TITLE.md

**Headers**
Authorization: Bearer YOUR_TOKEN
Accept: application/vnd.github+json

**Body**
{
  "message": "Add new course COURSE_TITLE",
  "content": "BASE64_ENCODED_MARKDOWN"
}

---

### 🌐 Live Site
Once enabled under **Settings → Pages**, your generated courses appear at:
https://YOUR_USERNAME.github.io/auto-course-generator/

---

### 🧩 Folder Structure
/content/       ← All AI-generated courses go here
/index.html     ← Displays list of published courses
/.github/workflows/deploy.yml ← Auto-publish config
