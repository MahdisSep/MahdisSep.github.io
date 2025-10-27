---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
  dl {
    margin-bottom: 60px; /* 调整这个值以获得合适的间距 */
    clear: both;
  }

  /* 全局文本颜色 */
  body {
    color: #333; /* 主要文本颜色 */
    /* background-image: url('../images/bg.jpg'); 背景图片 */
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
  }

  /* 链接颜色 */
  a {
    color: #0066cc; /* 链接颜色 */
  }

  /* 作者名字颜色 */
  strong {
    color: #000; /* 作者名字颜色 */
  }

  /* 年份标题颜色 */
  .year-title {
    color: #666;
  }

  /* 会议标签样式 */
  .conference-label {
    position: absolute;
    top: 10px;
    left: -5px;
    background-color: #2c3e50;  /* 深蓝色背景 */
    color: white;  /* 白色文字 */
    padding: 6px 12px;
    border-radius: 6px;
    font-size: 0.95em;
    font-weight: 600;
    letter-spacing: 0.5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    z-index: 1;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    font-style: italic;  /* 添加斜体 */
  }

  /* 鼠标悬停效果 */
  .conference-label:hover {
    background-color: #34495e;  /* 悬停时稍微变亮 */
    transition: background-color 0.2s ease;
  }

  dl dt img {
    width: 100%; /* 在移动端默认占满宽度 */
    aspect-ratio: 2/1; /* 设置宽高比为2:1，即高度为宽度的一半 */
    object-fit: cover; /* 确保图片不会被裁剪 */
    display: block;
    margin: 10px 10px 10px 0px; /* 适当的间距 */
    
    /* 添加美化效果 */
    border-radius: 8px; /* 让图片有轻微的圆角 */
    border: 2px solid #ddd; /* 添加淡灰色的边框 */
    box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2); /* 添加轻微阴影 */
    padding: 5px; /* 给图片一些内边距，让它不贴着边框 */
    background-color: #fff; /* 设置背景色，让图片更加干净 */
  }

  /* 在桌面端（宽度大于768px）时固定宽度 */
  @media screen and (min-width: 768px) {
    dl dt img {
      width: 350px;
    }
  }

  dl dt {
    position: relative;
  }

  hr {
    border: 1px solid #ebebeb; /* 调整分隔线的颜色和样式 */
    /* margin: 10px;  */
    clear: both; 
  }

  dl dd {
  margin-top: 5px; 
  margin-bottom: 5px;
}

  dl dd strong {
  font-weight: bold;
  color: black;
  }

  .co-first {
    color: red;
  }

  .down {
    transform: rotate(180deg);
  }

  /* 教育和工作经历卡片样式 */
  .experience-card, .education-card {
    display: flex;
    align-items: center;
    gap: 25px;
    margin-bottom: 15px;
    padding: 20px;
    background: #f8f9fa;
    border-radius: 12px;
    transition: all 0.3s ease;
    border: 1px solid #e9ecef;
  }

  .experience-card:hover, .education-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    border-color: #dee2e6;
  }

  .experience-info, .education-info {
    flex: 1;
  }

  .experience-logo, .education-logo {
    flex-shrink: 0;
    width: 100px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: white;
    border-radius: 10px;
    padding: 10px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
  }

  .experience-logo img, .education-logo img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .experience-title, .education-title {
    font-size: 1.2em;
    margin-bottom: 8px;
    color: #2c3e50;
  }

  .experience-title a, .education-title a {
    color: #2c3e50;
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .experience-title a:hover, .education-title a:hover {
    color: #3498db;
  }

  .experience-role, .education-role {
    color: #666;
    font-style: italic;
    margin-bottom: 5px;
  }

  .experience-topics, .education-topics {
    color: #666;
    font-style: italic;
  }

  .section-title {
    font-size: 1.8em;
    color: #2c3e50;
    margin: 40px 0 20px;
    padding-bottom: 10px;
    border-bottom: 2px solid #ecf0f1;
  }

  /* 奖学金和荣誉部分样式 */
  .honors-list {
    list-style: none;
    padding: 0;
  }

  .honors-list li {
    margin-bottom: 15px;
    padding: 15px 20px;
    background: #f8f9fa;
    border-radius: 8px;
    border-left: 4px solid #3498db;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .honors-list li:hover {
    transform: translateX(5px);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  }

  .honors-list li strong {
    color: #2c3e50;
  }

  .honors-list li a {
    color: #3498db;
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .honors-list li a:hover {
    color: #2980b9;
  }

  /* 服务部分样式 */
  .service-section {
    margin-bottom: 30px;
  }

  .service-section h3 {
    color: #2c3e50;
    font-size: 1.3em;
    margin: 25px 0 15px;
    padding-bottom: 8px;
    border-bottom: 2px solid #ecf0f1;
  }

  .service-list {
    list-style: none;
    padding: 0;
  }

  .service-list li {
    margin-bottom: 12px;
    padding: 12px 15px;
    background: #f8f9fa;
    border-radius: 6px;
    transition: transform 0.3s ease;
  }

  .service-list li:hover {
    transform: translateX(5px);
  }

  .service-list li a {
    color: #3498db;
    text-decoration: none;
    transition: color 0.3s ease;
  }

  .service-list li a:hover {
    color: #2980b9;
  }

.hobbies-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 15px;
  margin-top: 15px;
}

.hobbies-gallery img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 10px;
  box-shadow: 0 3px 8px rgba(0,0,0,0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hobbies-gallery img:hover {
  transform: scale(1.03);
  box-shadow: 0 6px 16px rgba(0,0,0,0.3);
}

/* Force horizontal images into one row */
.wide-row {
  grid-column: 1 / -1; /* span full width of grid */
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 15px;
}


/* === Projects section === */
.projects-section {
  margin: 5px 0 0px;
}

.projects-title {
  font-size: 1.8em;
  color: #2c3e50;
  margin: 0 0 16px;
  padding-bottom: 0px;
  border-bottom: 2px solid #ecf0f1;
}

/* 2 columns on wide screens, 1 column on mobile */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 18px;
}

@media (max-width: 720px) {
  .projects-grid {
    grid-template-columns: 1fr;
  }
}

/* Card */
.project-card {
  background: #fff;
  border: 1px solid #e9ecef;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,.05);
  transition: transform .18s ease, box-shadow .18s ease, border-color .18s ease;
  display: flex;
  flex-direction: column;
}

.project-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 18px rgba(0,0,0,.08);
  border-color: #dee2e6;
}

.project-media {
  position: relative;
  width: 100%;
  aspect-ratio: 16 / 10;
  overflow: hidden;
  background: #fff; /* white background instead of grey */
}

.project-media img,
.project-media video {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: contain;     /* show full image */
  object-position: center; /* centerize horizontally & vertically */
  display: block;
}


/* Optional subtle zoom on hover for a lively feel */
.project-card:hover .project-media img,
.project-card:hover .project-media video {
  transform: scale(1.03);
  transition: transform .3s ease;
}

/* Title + actions */
.project-body {
  padding: 12px 14px 14px;
  display: grid;
  grid-template-columns: 1fr auto;
  align-items: center;
  gap: 10px;
}

.project-title {
  margin: 0;
  font-weight: 700;
  color: #2c3e50;
  font-size: 1.02rem;
  line-height: 1.3;
  letter-spacing: .2px;
}

/* GitHub button */
.project-gh {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 8px 12px;
  border-radius: 8px;
  border: 1px solid #e1e8f0;
  background: #f0f4f8;
  color: #2c3e50;
  text-decoration: none;
  font-weight: 600;
  font-size: .92rem;
  transition: background .18s ease, border-color .18s ease, transform .18s ease;
  white-space: nowrap;
}

.project-gh:hover {
  background: #eaf4ff;
  border-color: #9fb9d6;
  transform: translateY(-1px);
}

.project-gh svg {
  width: 18px; height: 18px;
  fill: currentColor;
  flex-shrink: 0;
}

/* ===== Publications (fixed + light) ===== */
.pub-card {
  display: grid;
  grid-template-columns: 320px 1fr;  /* a bit wider media column */
  gap: 18px;
  align-items: stretch;
  background: #fff;                  /* force light */
  border: 1px solid #e9ecef;
  border-radius: 14px;
  box-shadow: 0 2px 8px rgba(0,0,0,.05);
  padding: 14px;
  margin: 16px 0;
  transition: box-shadow .2s ease, transform .2s ease, border-color .2s ease;
  overflow: hidden;                  /* stop media bleed */
  box-sizing: border-box;
}
.pub-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 22px rgba(0,0,0,.08);
  border-color: #dee2e6;
}

/* Media column */
.pub-media {
  position: relative;     /* so badge can sit inside */
  width: 100%;
  border-radius: 10px;
  overflow: hidden;
  border: 1px solid #eef2f5;
  background: #fff;
  aspect-ratio: 16/10;
  box-sizing: border-box;
}
/* IMPORTANT: no absolute positioning; no hover-zoom */
.pub-media img,
.pub-media video {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;               /* show full content */
  object-position: center;           /* center it */
}

/* Status badge */
.pub-badge {
  position: absolute;     /* pins it inside the pub-media box */
  top: 10px;
  left: 10px;
  background: #edf5ff;
  color: #1d4ed8;
  border: 1px solid #d6e6ff;
  font-size: .78rem;
  font-weight: 700;
  letter-spacing: .2px;
  padding: 6px 10px;
  border-radius: 999px;
  box-shadow: 0 1px 3px rgba(0,0,0,.06);
  z-index: 2;             /* make sure it sits above the image */
}
:root {
  --badge-bg: #edf5ff;
  --badge-fg: #1d4ed8;
  --badge-br: #d6e6ff;
}
.pub-badge,
.pub-badge.is-prep,
.pub-badge.is-progress {
  background: var(--badge-bg);
  color: var(--badge-fg);
  border-color: var(--badge-br);
}


/* Content */
.pub-body { display: grid; gap: 10px; align-content: start; }
.pub-title  { margin: 0; font-size: 1.05rem; line-height: 1.35; color: #2c3e50; font-weight: 800; }
.pub-authors{ margin: 0; color: #555; font-size: .98rem; }
.pub-affils { margin: 4px 0 0 0; color: #666; font-size: .9rem; }

/* Action chips */
.pub-actions { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 2px; }
.pub-chip {
  display: inline-flex; align-items: center; gap: 8px;
  padding: 6px 10px; border-radius: 8px;
  border: 1px solid #e1e8f0; background: #f7f9fc;
  color: #2c3e50; text-decoration: none; font-weight: 600; font-size: .9rem;
  transition: background .15s ease, border-color .15s ease, transform .15s ease;
}
.pub-chip:hover, .pub-chip:focus {
  background: #eaf4ff; border-color: #9fb9d6; transform: translateY(-1px);
  outline: none;
}
.pub-chip svg { width: 16px; height: 16px; fill: currentColor; }

/* Mobile */
@media (max-width: 820px) {
  .pub-card { grid-template-columns: 1fr; padding: 12px; }
  .pub-media { aspect-ratio: 16/9; }
}

/* If you previously added a dark-mode block for .pub-*, remove it.
   Otherwise, this forces light mode specifically for these cards. */

/* Hide projects 7+ until opened (prevents flash of visible content) */
.projects-grid:not(.is-open) .project-card:nth-of-type(n + 7) { 
  display: none !important; 
}

/* Button: full-width blue (keeps your previous styles) */
:root {
  --brand-blue: #1d4ed8;
  --brand-blue-weak: #edf5ff;
}
.load-more {
  grid-column: 1 / -1;
  justify-self: stretch;
  width: 100%;
  display: block;
  padding: 14px 18px;
  border-radius: 12px;
  border: 2px solid var(--brand-blue);
  background: #fff;
  color: var(--brand-blue);
  font-weight: 800;
  font-size: 1rem;
  text-align: center;
  cursor: pointer;
  transition: background .18s ease, border-color .18s ease, color .18s ease, transform .18s ease;
}
.load-more:hover { background: var(--brand-blue-weak); transform: translateY(-1px); }

/* Hide the button once opened (CSS-only) */
.projects-grid.is-open #loadMoreBtn { display: none !important; }

  .endorsements { display: grid; gap: 16px; margin: 12px 0 8px; }
  .endorse-card {
    background: #fff;
    border: 1px solid #e9ecef;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0,0,0,.05);
    padding: 14px;
  }
  .endorse-header {
    display: grid;
    grid-template-columns: 76px 1fr;
    gap: 12px;
    align-items: center;
  }
  .endorse-avatar {
    width: 76px; height: 76px;
    border-radius: 50%;
    overflow: hidden;
    border: 2px solid #ecf0f1;
    background: #fff;
  }
  .endorse-avatar img { width: 100%; height: 100%; object-fit: cover; }
  .endorse-name { margin: 0; font-weight: 800; color: #2c3e50; font-size: 1.02rem; }
  .endorse-affil { color: #666; font-size: .93rem; margin-top: 2px; }
  .endorse-links { display: flex; gap: 8px; margin-top: 6px; flex-wrap: wrap; }
  .endorse-links a {
    display: inline-flex; align-items: center; justify-content: center;
    width: 34px; height: 34px; border-radius: 8px;
    background: #f0f4f8; border: 1px solid #e1e8f0; text-decoration: none;
  }
  .endorse-links svg { width: 18px; height: 18px; fill: #2c3e50; }
  .endorse-quote {
    margin: 12px 2px 2px 2px;
    padding: 12px 14px;
    background: #f8f9fa;
    border-left: 4px solid #3498db;
    border-radius: 8px;
    color: #333;
    line-height: 1.55;
    font-style: italic;
  }
  @media (max-width: 480px) {
    .endorse-header { grid-template-columns: 64px 1fr; }
    .endorse-avatar { width: 64px; height: 64px; }
  }

  /* Vertical Endorsements */
  .endorsements { display: grid; gap: 16px; margin: 12px 0 8px; }
  .endorse-card {
    background: #fff;
    border: 1px solid #e9ecef;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0,0,0,.05);
    padding: 14px;
  }
  .endorse-header {
    display: grid;
    grid-template-columns: 76px 1fr;
    gap: 12px;
    align-items: center;
  }
  .endorse-avatar {
    width: 76px; height: 76px;
    border-radius: 50%;
    overflow: hidden;
    border: 2px solid #ecf0f1;
    background: #fff;
  }
  .endorse-avatar img { width: 100%; height: 100%; object-fit: cover; }
  .endorse-name { margin: 0; font-weight: 800; color: #2c3e50; font-size: 1.02rem; }
  .endorse-affil { color: #666; font-size: .93rem; margin-top: 2px; }
  .endorse-links { display: flex; gap: 8px; margin-top: 6px; flex-wrap: wrap; }
  .endorse-links a {
    display: inline-flex; align-items: center; justify-content: center;
    width: 34px; height: 34px; border-radius: 8px;
    background: #f0f4f8; border: 1px solid #e1e8f0; text-decoration: none;
    transition: background .18s ease, border-color .18s ease, transform .18s ease, box-shadow .18s ease;
  }
  .endorse-links svg { width: 18px; height: 18px; fill: #2c3e50; }
  .endorse-quote {
    margin: 12px 2px 2px 2px;
    padding: 12px 14px;
    background: #f8f9fa;
    border-left: 4px solid #3498db;
    border-radius: 8px;
    color: #333;
    line-height: 1.55;
    font-style: italic;
  }
  @media (max-width: 480px) {
    .endorse-header { grid-template-columns: 64px 1fr; }
    .endorse-avatar { width: 64px; height: 64px; }
  }

  /* Remove underlines for button-like links, keep them clean on hover */
  .pub-actions a,
  .pub-actions a:visited,
  .pub-chip,
  .pub-chip:visited,
  .project-gh,
  .project-gh:visited,
  .endorse-links a,
  .endorse-links a:visited {
    text-decoration: none !important;
    box-shadow: none !important;
    background-image: none !important;
  }
  .pub-actions a:hover,
  .pub-chip:hover,
  .project-gh:hover,
  .endorse-links a:hover,
  .endorse-links a:focus {
    text-decoration: none !important;
    box-shadow: none !important;
    background-image: none !important;
  }

  /* Pop hover for endorsement buttons to match other buttons */
  .endorse-links a:hover,
  .endorse-links a:focus {
    background: #eaf4ff;
    border-color: #9fb9d6;
    transform: translateY(-1px);
    box-shadow: 0 2px 8px rgba(0,0,0,.08);
  }

  /* Accessible focus ring */
  .endorse-links a:focus-visible,
  .project-gh:focus-visible,
  .pub-chip:focus-visible,
  .pub-actions a:focus-visible {
    outline: 2px solid #9fb9d6;
    outline-offset: 2px;
  }


/* Make project cards feel clickable */
.project-card.is-clickable { cursor: pointer; }
.project-card.is-clickable:focus {
  outline: 2px solid #9fb9d6;
  outline-offset: 3px;
}

  /* Education metrics chips */
  .edu-metrics {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 10px;
  }
  .chip, .chip-button {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 10px;
    border-radius: 999px;
    border: 1px solid #e1e8f0;
    background: #f7f9fc;
    color: #2c3e50;
    font-weight: 700;
    font-size: .9rem;
    cursor: default;
    user-select: none;
  }
  .chip-button {
    cursor: pointer;
    transition: background .15s ease, border-color .15s ease, transform .15s ease;
  }
  .chip-button:hover, .chip-button:focus {
    background: #eaf4ff;
    border-color: #9fb9d6;
    transform: translateY(-1px);
    outline: none;
  }

  /* 4.0 courses list */
  .course-list {
    margin: 10px 0 0 0;
    padding: 12px 14px;
    background: #ffffff;
    border: 1px solid #e9ecef;
    border-radius: 10px;
    box-shadow: 0 2px 6px rgba(0,0,0,.05);
    list-style: none;
  }
  .course-list li {
    padding: 6px 2px;
    border-bottom: 1px dashed #e9ecef;
  }
  .course-list li:last-child { border-bottom: 0; }
  .is-hidden { display: none !important; }

  .course-list-inline {
    margin: 10px 0 0 0;
    padding: 12px 14px;
    background: #ffffff;
    border: 1px solid #e9ecef;
    border-radius: 10px;
    box-shadow: 0 2px 6px rgba(0,0,0,.05);
    line-height: 1.6;
    font-size: 0; /* prevent HTML whitespace between items */
  }
  .course-list-inline .course-item {
    display: inline;
    font-size: 1rem; /* restore readable size */
  }
  .course-list-inline .course-item + .course-item::before {
    content: ", ";
  }

  .course-list-inline {
  font-size: 0; /* prevent HTML whitespace */
  }
  .course-list-inline .course-item {
    display: inline;
    font-size: 1rem;
  }

</style>

<!-- {% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %} -->

<span class='anchor' id='about-me'></span>


# About Me  
I’m **Mahdis Sepahvand**, a **Computer Engineering** undergraduate at **Shahid Beheshti University**.
My academic and research interests lie at the intersection of **computer vision**, **deep learning**, **medical imaging**, and **generative & diffusion models**. I am also passionate about exploring **multimodal learning and data-driven applications** in **science** and **healthcare**.

For my Bachelor’s project, I worked on **fine-tuning large multimodal models** for **medical image** analysis — an experience that deepened my interest in integrating AI techniques with real-world medical challenges.
I’m eager to pursue **Master’s or direct PhD opportunities** where I can continue researching in these fields and contribute to meaningful, interdisciplinary AI projects.

Outside of academia, I enjoy writing, reading books, and listening to music, which help me stay creative and inspired.

You can reach me via:
- [Email](mailto:Mahdissep18@gmail.com)
- [Telegram](https://t.me/mahdissep)



# Education

<div class="education-card">
  <div class="education-info">
    <div class="education-title">
      <strong>Sep 2021 - Jan 2026</strong><br/>
      Bachelor, Computer Engineering, Shahid Beheshti Univeristy, Tehran, Iran
    </div>

    <div class="edu-metrics" aria-label="Education metrics">
      <span class="chip" title="Cumulative">Cumulative: 18.09/20 (3.77/4.00)</span>
      <span class="chip" title="Last two academic years GPA">Last two years: 19.07/20 (4.00/4.00)</span>
    </div>

    <!-- Courses, names only, continuous with commas -->
    <div id="fourPointCourses" class="course-list-inline" role="list">
      <span style="font-size:1rem;"><strong>Relevant 4/4 Courses: </strong></span> 
      <span class="course-item" role="listitem">Computer Vision</span>
      <span class="course-item" role="listitem">Machine Learning</span>
      <span class="course-item" role="listitem">
      Bachelor Thesis (Multimodal-AI-Odontogenic-Cyst-Diagnosis | <a href="https://github.com/MahdisSep/Multimodal-AI-Odontogenic-Cyst-Diagnosis.git">My Bachelor Thesis</a>)</span>
      <span class="course-item" role="listitem">Graph Theory and Algorithms</span>
      <span class="course-item" role="listitem">Algorithms Design</span>
      <span class="course-item" role="listitem">Data Structures</span>
      <span class="course-item" role="listitem">Linear Algebra</span>
      <span class="course-item" role="listitem">Probability &amp; Statistics</span>
      <span class="course-item" role="listitem">Data Base</span>
    </div>



  </div>

  <div class="education-logo">
    <img src="../images/Sbu-logo.png" alt="SBU logo" />
  </div>
</div>

<div class="education-card" aria-label="Education entry: Sampad Diploma in Mathematics and Physics">
  <div class="education-info">
    <div class="education-title">
      <strong>Sep 2019 – Jan 2021</strong><br/>
      Diploma, Mathematics & Physics, National Organization for Development of Exceptional Talents (Sampad), Iran
    </div>

    <div class="edu-metrics" aria-label="Education metrics">
      <span class="chip" title="Cumulative GPA">GPA: 4.00/4.00</span>
      <span class="chip" title="Ranked 1st in the school">Ranked 1st in the school</span>
    </div>
  </div>

  <div class="education-logo">
    <img src="../images/sampad.jfif" alt="National Organization for Development of Exceptional Talents (Sampad) logo" />
  </div>
</div>


## Languages
<div class="lang-chips">
  <span class="chip">Persian — Native</span>
  <span class="chip">English — IELTS 6.5</span>
</div>


# Publications

## Bachelor Thesis

<div class="pub-card">
  <div class="pub-media">
    <span class="pub-badge is-progress">In Progress</span>
    <img src="images/bsc-thesis.png" alt="Multimodal-AI-Odontogenic-Cyst-Diagnosis">
  </div>

  <div class="pub-body">
    <h3 class="pub-title"> A multimodal AI framework for the diagnosis of Odontogenic Cysts</h3>

    <!-- (Text unchanged) -->
    <p class="pub-abstract">
      This ongoing research project focuses on developing a multimodal deep learning framework for the diagnosis of odontogenic cysts.Our approach integrates data from panoramic radiography (radiomics), histopathology (digital pathology), and clinical/demographic records, enabling the model to learn complementary features from each modality.We fine-tuned the Qwen2.5-7B large multimodal model using the QLoRA optimization technique, achieving a diagnostic accuracy of up to 92%, significantly outperforming unimodal baselines.This work is still in progress and will be further expanded into a research paper in the near future. More updates coming soon!
    </p>
  </div>
</div>


# Experience
For additional details about each experience, please see my CV or contact me.

<!-- Teaching Assistant (full list, shown by default) -->
  <article class="exp-card">
    <img class="exp-card__logo" src="/images/Sbu-logo.png" alt="Shahid Beheshti University">
    <div class="exp-card__body">
      <header class="exp-card__header">
        <h3 class="exp-card__role">Undergraduate Research and Teaching Assistant (Part-time)</h3>
        <div class="exp-card__dates">Tehran, Iran</div>
      </header>

      <div class="exp-card__org">Shahid Beheshti University — Computer Science Faculty</div>

      <p class="exp-card__summary">
        Managed assignments, ran recitations, mentored projects, and managed teams as a head teaching assistant.
      </p>

      <ul class="exp-card__badges">
        <li class="badge"><i class="fas fa-chalkboard-teacher"></i> Teaching</li>
        <li class="badge"><i class="fas fa-brain"></i> RL/ML/AI</li>
      </ul>

      <details class="exp-card__details" open>
        <summary>Course list</summary>
        <ul class="exp-card__bullets">
          <li><strong>Computer Vision (A collaborative project with the Faculty of Medicine, University of Tehran)</strong> — Fall 2025, Dr. Hamed Malek, Dr. Mahdavi</li>
          <li><strong>Compiler Design (Head Teaching Assistant)</strong> — Fall 2024, Dr. Mehran Alidoost Nia</li>
          <li><strong>Algorithm Design</strong> — Fall 2024, Dr. Farokh Legha Moazemi</li>
          <li><strong>Formal Languages & Automata Theory Course (Head Teaching Assistant)</strong> — Spring 2024, Dr. Ramak Ghavami Zadeh</li>
          <li><strong>Algorithm Design</strong> — Spring 2024, Dr. Ramak Ghavami Zadeh</li>
          <li><strong>Advanced Programming</strong> — Spring 2023, Dr. Sadegh Ali Akbari</li>
          <li><strong>Formal Languages & Automata Theory Course</strong> — Spring 2023, Dr. Ramak Ghavami Zadeh</li>
          <li><strong>Introduction to Programming</strong> — Fall 2022, Dr. Sadegh Ali Akbari</li>
        </ul>
      </details>
    </div>
  </article>

# Courses

<section class="cert-grid">

  <!-- IELTS -->
  <article class="cert-card">
    <img class="cert-card__logo" src="/images/ielts.jpg" alt="IELTS">
    <div class="cert-card__body">
      <h3 class="cert-card__title">IELTS Academic</h3>
      <div class="cert-card__org">IELTS Official</div>
      <div class="cert-card__meta">Issued Sep 2025</div>
    </div>
  </article>

  <article class="cert-card">
    <img class="cert-card__logo" src="/images/deeplearningai.jpg" alt="DeepLearning.AI">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Unsupervised Learning, Recommenders, Reinforcement Learning</h3>
      <div class="cert-card__org">DeepLearning.AI</div>
      <div class="cert-card__meta">Issued Mar 2025</div>
      <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/5HQYM7PKHX4Z">View credential</a>
    </div>
  </article>

  <article class="cert-card">
    <img class="cert-card__logo" src="/images/deeplearningai.jpg" alt="DeepLearning.AI">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Advanced Learning Algorithms</h3>
      <div class="cert-card__org">DeepLearning.AI</div>
      <div class="cert-card__meta">Issued Oct 2024</div>
      <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/LYD09SFN7KK8">View credential</a>
    </div>
  </article>

  <article class="cert-card">
    <img class="cert-card__logo" src="/images/deeplearningai.jpg" alt="DeepLearning.AI">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Supervised Machine Learning: Regression and Classification</h3>
      <div class="cert-card__org">DeepLearning.AI</div>
      <div class="cert-card__meta">Issued Apr 2024</div>
      <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/9M7SBTAHATYA">View credential</a>
    </div>
  </article>
 
  <article class="cert-card">
    <img class="cert-card__logo" src="/images/meta.jpg" alt="meta">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Introduction to Databases</h3>
      <div class="cert-card__org">Meta</div>
      <div class="cert-card__meta">Issued Sep 2023</div>
      <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/BBKN8JZBC2P5">View credential</a>
    </div>
  </article>

  <article class="cert-card">
    <img class="cert-card__logo" src="/images/Tehran.png" alt="UT">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Deep Learning Course </h3>
      <div class="cert-card__org">University of Tehran, ACM</div>
      <div class="cert-card__meta">Issued Summer 2024</div>
      <a class="cert-link" href="https://drive.google.com/file/d/1yM4jr7wKAeMP3Gsu9m0jof2VCjKjWLAb/view?usp=sharing">View credential</a>
    </div>
  </article>

  
  <article class="cert-card">
    <img class="cert-card__logo" src="/images/irans.jpg" alt="IUST">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Machine Learning and Data Science</h3>
      <div class="cert-card__org">Iran University of science and technology, Computernic</div>
      <div class="cert-card__meta">Issued Summer 2023</div>
      <a class="cert-link" href="https://drive.google.com/file/d/1gukQEzuG4HfpNKtIw4E7LIabVlXEetH9/view?usp=sharing">View credential</a>
    </div>
  </article>

   <article class="cert-card">
    <img class="cert-card__logo" src="/images/Sbu-logo.png" alt="sbu">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Introduction to linux</h3>
      <div class="cert-card__org">Shahid Beheshti University</div>
      <div class="cert-card__meta">Issued Summer 2022</div>
      <a class="cert-link" href="https://drive.google.com/file/d/1Uc0ZVzI_57kB7DJfhhPUF26RCZf9XE-r/view?usp=sharing">View credential</a>
    </div>
  </article>

   <article class="cert-card">
    <img class="cert-card__logo" src="/images/Sbu-logo.png" alt="sbu">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Fundamentals of Python</h3>
      <div class="cert-card__org">Shahid Beheshti University</div>
      <div class="cert-card__meta">Issued Summer 2022</div>
      <a class="cert-link" href="https://drive.google.com/file/d/1zhIBX-m2hb-LuaCxnPBB0B6O9MrOv_Pr/view?usp=sharing">View credential</a>
    </div>
  </article>

   <article class="cert-card">
    <img class="cert-card__logo" src="/images/Sbu-logo.png" alt="sbu">
    <div class="cert-card__body">
      <h3 class="cert-card__title">Computer vision</h3>
      <div class="cert-card__org">Shahid Beheshti University</div>
      <div class="cert-card__meta">Issued Winter 2023</div>
      <a class="cert-link" href="https://drive.google.com/file/d/1CHhlvweQD3QqxTDmC95tLj4Jf80qj20-/view?usp=sharing">View credential</a>
    </div>
  </article>

</section>


<!-- <script type="text/javascript" id="mmvst_globe" src="//mapmyvisitors.com/globe.js?d=HVZ1dytXl71ZnJux6Lqi9u_XgGZap1uRgqVjt2_TcTc"></script> -->

<br>
<br>
<br>
<br>