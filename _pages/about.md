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

  :root {
    /* brand blues used in your cards */
    --blue-light: #e0f7ff;
    --blue-base:  #0095dd;
    --blue-dark:  #006f9a;
  
    /* publications sizing */
    --pub-left-col-basis: 40%;
    --pub-left-col-max: 300px;
    --pub-img-col-h: 340px;
    --pub-img-gap: 8px;
  
    /* experience & certs vars */
    --exp-bg: #f8fbff;
    --exp-border: #e4eef8;
    --exp-accent: #0f7bdc;
    --badge-bg: #eaf3ff;
    --badge-text: #0f4573;
  
    --card-bg:#f8fbff; --card-b:#e4eef8; --card-ac:#070bf5;
    --chip-bg:#eef6ff; --chip-b:#d9e8fb; --chip-text:#0f4573;
  
    --p-bg:#f7fbff; --p-br:#e2eefb; --p-ac:#0f7bdc; --p-ac-2:#084a9a;
    --p-text:#143a52; --p-ratio: 16/7; --pub-img-eps: 6px; --rb-h: 42px; --rb-gap: 6px;

    /* Glow / gradient border for Experience cards */
    --exp-radius: 14px;
    --exp-bw: 1.6px;                 /* border width */
    --exp-glow: 0 16px 36px rgba(106, 183, 255, 0.48);   /* outer glow */
    --exp-glow-hover: 0 24px 54px rgba(215, 255, 252, 0.95);

    /* warm blue gradient edge */
    --exp-grad-1: #01f6f29a;           /* light cyan-blue */
    --exp-grad-2: #0c56ebcd;           /* vivid royal blue */
    --exp-grad-3: #000808b9;           /* deeper blue for angle mix */

    /* logo sizes */
    --exp-logo: 100px;                /* default single logo square */
    --exp-lab-logo: 80px;            /* stacked lab logos */
    --exp-lab-gap: 25px;              /* gap between stacked logos */
  }
  

  :root{
    /* Projects (gradient edge + glow) */
    --proj-radius: 14px;
    --proj-bw: 1.6px;
    --proj-bg: #f8fbff;
    --proj-glow: 0 16px 36px rgba(15,105,189,.22);
    --proj-glow-hover: 0 22px 48px rgba(7,246,242,.28);
  
    /* gradient edge (harmonized with Experience) */
    --proj-grad-1: #9bf8ff;   /* light cyan */
    --proj-grad-2: #2f7cf0;   /* royal blue */
    --proj-grad-3: #0a2038cc; /* deep blue */
  
    /* media sizing for project cards */
    --proj-media-w: 300px;
    --proj-media-ratio: 16/10;
  }
  
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
  /* ===== Experience & Education Cards (gradient + soft glow) ===== */
.experience-card,
.education-card {
  display: flex;
  align-items: flex-start;
  gap: 1.25rem;
  margin-bottom: 1rem;
  padding: 1.25rem 1.5rem;

  border-radius: var(--exp-radius, 12px);
  border: var(--exp-bw, 2px) solid transparent;
  background:
    linear-gradient(var(--exp-bg, #fff), var(--exp-bg, #fff)) padding-box,
    linear-gradient(135deg, var(--exp-grad-1, #d1e5f8), var(--exp-grad-2, #a7d8f5) 55%, var(--exp-grad-3, #cde4fa)) border-box;

  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.04), var(--exp-glow, 0 0 8px rgba(33, 150, 243, 0.08));
  transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
  box-sizing: border-box;
}

.experience-card:hover,
.education-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.08), var(--exp-glow-hover, 0 0 14px rgba(33, 150, 243, 0.15));
}

/* Logo section */
.experience-logo,
.education-logo {
  flex-shrink: 0;
  width: var(--exp-logo, 80px);
  height: var(--exp-logo, 80px);
  display: flex;
  align-items: center;
  justify-content: center;
  background: #fff;
  border-radius: 12px;
  border: 1px solid var(--exp-border, #e2e8f0);
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
  overflow: hidden;
}

.experience-logo img,
.education-logo img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

/* Info section */
.experience-info,
.education-info {
  flex: 1;
  display: grid;
  gap: 0.25rem;
}

/* Titles */
.experience-title,
.education-title {
  font-size: 1.05rem;
  font-weight: 700;
  color: #143a52;
  margin: 0;
}

.experience-title a,
.education-title a {
  color: inherit;
  text-decoration: none;
  transition: color 0.3s ease;
}

.experience-title a:hover,
.education-title a:hover {
  color: var(--exp-accent, #9bcef7ff);
}

/* Role / Subtitle */
.experience-role,
.education-role {
  color: #5b6b7a;
  font-style: italic;
  font-size: 0.9rem;
}

/* Topics or description */
.experience-topics,
.education-topics {
  color: #384b5a;
  font-size: 0.95rem;
  line-height: 1.5;
}

/* Responsive (mobile layout) */
@media (max-width: 640px) {
  .experience-card,
  .education-card {
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 1rem;
  }

  .experience-logo,
  .education-logo {
    width: 70px;
    height: 70px;
    border-radius: 10px;
  }
}


  .section-title {
    font-size: 1.8em;
    color: #2c3e50;
    margin: 40px 0 20px;
    padding-bottom: 10px;
    border-bottom: 2px solid #ecf0f1;
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
    color: #9bcef7ff;
  }

/* Force horizontal images into one row */
.wide-row {
  grid-column: 1 / -1; /* span full width of grid */
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 15px;
}


/* ===== Publications (fixed + light) ===== */
/* ===== Publications (styled like Experience) ===== */
.pub-card {
  display: grid;
  grid-template-columns: minmax(240px, 30%) 1fr; 
  align-items: start;        
  gap: 1.25rem;              
  padding: 1rem 1.25rem;

  border-radius: var(--exp-radius, 12px);
  border: var(--exp-bw, 2px) solid transparent;
  background:
    linear-gradient(var(--exp-bg, #fff), var(--exp-bg, #fff)) padding-box,
    linear-gradient(135deg, var(--exp-grad-1, #d1e5f8), var(--exp-grad-2, #a7d8f5) 55%, var(--exp-grad-3, #cde4fa)) border-box;
  box-shadow: 0 8px 16px rgba(0,0,0,.04), var(--exp-glow, 0 0 8px rgba(33,150,243,0.08));
  overflow: hidden;
}


.pub-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 24px rgba(0,0,0,.08), var(--exp-glow-hover, 0 0 14px rgba(33,150,243,0.15));
}

.pub-media {
  position: relative;
  border-radius: 12px;
  border: 1px solid var(--exp-border, #e2e8f0);
  background: #fff;
  overflow: hidden;
  aspect-ratio: 16/10;
  box-shadow: 0 1px 4px rgba(0,0,0,.05);
}

.pub-media img,
.pub-media video {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: center;
}

.pub-badge {
  position: absolute;
  top: 10px;
  left: 10px;
  background: #edf5ff;
  color: #1d4ed8;
  border: 1px solid #d6e6ff;
  font-size: .78rem;
  font-weight: 700;
  padding: 6px 10px;
  border-radius: 999px;
  box-shadow: 0 1px 3px rgba(0,0,0,.06);
}

/* Content Section */
.pub-body {
  display: grid;
  gap: 10px;
  align-content: start;
}

.pub-title {
  font-size: 1.05rem;
  font-weight: 700;
  margin: 0;
  color: #143a52;
}

.pub-authors {
  font-size: .95rem;
  color: #384b5a;
}

.pub-affils {
  font-size: .9rem;
  color: #5b6b7a;
}

/* Action chips هماهنگ با exp badges */
.pub-actions {
  display: flex;
  flex-wrap: wrap;
  gap: .5rem;
  margin-top: .25rem;
}

.pub-chip {
  display: inline-flex;
  align-items: center;
  gap: .35rem;
  padding: .28rem .55rem;
  background: var(--badge-bg, #edf5ff);
  color: var(--badge-text, #143a52);
  border: 1px solid rgba(15,123,220,.12);
  border-radius: 999px;
  font-size: .82rem;
  font-weight: 600;
  white-space: nowrap;
  transition: background .15s ease, transform .15s ease;
}

.pub-chip:hover {
  transform: translateY(-1px);
  background: #eaf4ff;
}

/* Responsive */
@media (max-width: 820px) {
  .pub-card {
    grid-template-columns: 1fr;
    padding: 1rem;
  }
  .pub-media {
    aspect-ratio: 16/9;
  }
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
  /* ===== Chips & Chip Buttons (modern unified look) ===== */
.chip,
.chip-button {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  padding: 0.35rem 0.75rem;
  border-radius: 999px;
  font-weight: 700;
  font-size: 0.9rem;
  line-height: 1.2;
  white-space: nowrap;

  
  background: linear-gradient(
    135deg,
    #f8fcff,    
    #eaf6ff    
  );
  color: #1e4a70; 
  border: 1px solid rgba(15, 123, 220, 0.08); 
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.03);

  user-select: none;
  cursor: default;
  transition: all 0.2s ease;
}

.chip i,
.chip-button i {
  font-size: 0.95em;
  opacity: 0.8;
}

.chip-button {
  cursor: pointer;
}

.chip-button:hover,
.chip-button:focus {
  background: linear-gradient(
    135deg,
    #edf8ff,
    #dff2ff
  );
  transform: translateY(-1px);
  box-shadow: 0 4px 10px rgba(0, 123, 255, 0.08);
  border-color: rgba(15, 123, 220, 0.18);
  outline: none;
}

.chip--muted {
  background: #f9fbfd;
  color: #6b7c8a;
  border-color: #e7edf3;
  box-shadow: none;
}

.chip-group {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
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

  /* ===== Experience list ===== */
.experience-list{ display:grid; gap:1.25rem; }

/* Card with gradient edge + soft glow */
.exp-card{
  display:grid;
  grid-template-columns:var(--exp-logo) 1fr;
  gap:1rem; align-items:start;
  padding:1rem 1.25rem;
  border-radius:var(--exp-radius);

  /* gradient border trick */
  background:
    linear-gradient(var(--exp-bg), var(--exp-bg)) padding-box,
    linear-gradient(135deg, var(--exp-grad-1), var(--exp-grad-2) 55%, var(--exp-grad-3)) border-box;
  border: var(--exp-bw) solid transparent;

  /* subtle elevation */
  box-shadow: 0 8px 16px rgba(0,0,0,.04), var(--exp-glow);
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.exp-card:hover{ transform:translateY(-2px); box-shadow:0 12px 24px rgba(0,0,0,.08), var(--exp-glow-hover); }

/* default single logo */
.exp-card__logo{
  width:var(--exp-logo); height:var(--exp-logo);
  border-radius:12px; object-fit:cover; background:#fff;
  border:1px solid var(--exp-border);
}

/* header + text */
.exp-card__header{ display:flex; flex-wrap:wrap; justify-content:space-between; gap:.25rem .75rem; margin-bottom:.25rem; }
.exp-card__role{ font-size:1.05rem; margin:0; color:#143a52; }
.exp-card__dates{ font-size:.9rem; color:#5b6b7a; }
.exp-card__org{ font-weight:600; color:#254b6b; margin-bottom:.25rem; }
.exp-card__summary{ margin:.25rem 0 .5rem; color:#384b5a; }

/* badges */
.exp-card__badges{ display:flex; flex-wrap:wrap; gap:.5rem; list-style:none; padding:0; margin:.25rem 0 0; }
.badge{
  display:inline-flex; align-items:center; gap:.35rem; padding:.28rem .55rem;
  background:var(--badge-bg); color:var(--badge-text);
  border:1px solid rgba(15,123,220,.12); border-radius:999px; font-size:.82rem; font-weight:600; white-space:nowrap;
}
.badge i{ font-size:.9em; opacity:.9; }

/* details */
.exp-card__details summary{ cursor:pointer; margin-top:.35rem; color:var(--exp-accent); font-weight:600; }
.exp-card__bullets{ margin:.5rem 0 0 .9rem; }
.exp-card__bullets li{ margin:.15rem 0; }

.exp-card__logos{
  display:grid; align-content:start;
  grid-template-rows: var(--exp-lab-logo) var(--exp-lab-logo);
  gap: var(--exp-lab-gap);
  width:var(--exp-logo);           /* reserve column width */
}
.exp-card__logos img{
  width:100%; height:var(--exp-lab-logo);
  object-fit:cover; background:#fff; border-radius:12px;
  border:1px solid var(--exp-border);
}

/* responsive */
@media (max-width:640px){
  .exp-card{ grid-template-columns:60px 1fr; padding:.9rem; }
  .exp-card__logo{ width:60px; height:60px; border-radius:8px; }
  .exp-card__logos{ width:60px; grid-template-rows: 44px 44px; gap:4px; }
  .exp-card__logos img{ height:44px; border-radius:8px; }
}


/* ===== Recommendations (compact, blue-warm) ===== */

/* the tiny trigger pill that sits with your badges */
.rec-chip{
  display:inline-flex; align-items:center; gap:.45rem;
  padding:.34rem .68rem; border-radius:999px;
  background:var(--rec-pill-bg);
  border:1.2px solid var(--rec-pill-br);
  color:var(--rec-pill-fg); font-weight:800; font-size:.88rem;
  text-decoration:none; cursor:pointer; user-select:none;
  transition:transform .15s ease, box-shadow .15s ease;
}
.rec-chip i{ font-size:.95em; opacity:.95; }
.rec-chip:hover{ transform:translateY(-1px); box-shadow:0 10px 22px rgba(15, 91, 184, .15); }

/* the collapsible drawer */
.rec-drawer{ margin-top:.55rem; }
.rec-drawer > summary{
  list-style:none; cursor:pointer; user-select:none;
  display:inline-flex; align-items:center; gap:.45rem;
  padding:.4rem .75rem; border-radius:999px;
  background:var(--rec-pill-bg); border:1px solid var(--rec-pill-br);
  color:var(--rec-pill-fg); font-weight:800; font-size:.9rem;
  box-shadow:0 3px 8px rgba(0,0,0,.06);
}
.rec-drawer > summary::-webkit-details-marker{ display:none; }
.rec-drawer > summary::after{ content:"▾"; transition:transform .15s ease; }
.rec-drawer[open] > summary::after{ transform:rotate(180deg); }

/* drawer body */
.rec{
  margin-top:.6rem;
  padding:.75rem .9rem .9rem;
  background:var(--rec-bg);
  border:1px solid var(--rec-br);
  border-radius:12px;
  color:var(--rec-ink);
}

/* compact header: avatar + name + role + LinkedIn button */
.rec__head{
  display:flex; align-items:center; justify-content:space-between; gap:.75rem; margin-bottom:.4rem;
}
.rec__who{
  display:flex; align-items:center; gap:.6rem; min-width:0;
}
.rec__avatar{
  width:var(--rec-avatar); height:var(--rec-avatar);
  border-radius:50%; background:#fff; border:1px solid var(--rec-br);
  display:grid; place-items:center; font-weight:900; color:var(--rec-pill-fg);
}
.rec__txt{ min-width:0; }
.rec__name{ margin:0; font-weight:900; line-height:1.1; }
.rec__meta{ margin:.1rem 0 0; font-size:.9rem; color:#375a86; opacity:.95; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }

/* “View on LinkedIn” small button */
.rec__cta{
  display:inline-flex; align-items:center; gap:.4rem;
  padding:.36rem .6rem; border-radius:10px; text-decoration:none;
  background:#eef6ff; border:1px solid var(--rec-pill-br); color:var(--rec-pill-fg); font-weight:800;
  transition:transform .12s ease, box-shadow .12s ease;
}
.rec__cta:hover{ transform:translateY(-1px); box-shadow:0 6px 14px rgba(15,91,184,.18); }
.rec__cta i{ font-size:1rem; }

/* quote text */
.rec__body{
  margin-top:.4rem;
  padding-left:.9rem;
  border-left:4px solid var(--rec-quote);
  color:var(--rec-ink);
  line-height:1.55;
}
.rec__body p{ margin:.45rem 0; }


:root{
  --rec-avatar: 90px;        /* change this to resize Navid’s photo */
  --rec-org-logo: 45px;      /* change this to resize the Huawei logo */
}

/* use only the details control (we removed the extra chip) */
.rec-drawer{ margin-top:.55rem; }

/* pill look for the summary; NO TRIANGLE; add a circle on the left */
.rec-drawer > summary{
  list-style:none; cursor:pointer; user-select:none;
  display:inline-flex; align-items:center; gap:.55rem;
  padding:.46rem .85rem; border-radius:999px;
  background:var(--rec-pill-bg); border:1px solid var(--rec-pill-br);
  color:var(--rec-pill-fg); font-weight:800; font-size:.92rem;
  box-shadow:0 3px 8px rgba(0,0,0,.06);
}
.rec-drawer > summary::-webkit-details-marker{ display:none; }
.rec-drawer > summary::after{ content:none; }                /* removes triangle */
.rec-drawer > summary::before{                               /* the circle cue */
  content:""; display:inline-block; width:.55rem; height:.55rem;
  border-radius:50%; background:var(--rec-pill-fg);
  box-shadow:0 0 0 3px rgba(255,255,255,.65) inset;
}

/* drawer body (unchanged look, just here for completeness) */
.rec{
  margin-top:.6rem; padding:.75rem .9rem .9rem;
  background:var(--rec-bg); border:1px solid var(--rec-br);
  border-radius:12px; color:var(--rec-ink);
}

/* header (avatar + text + button) */
.rec__head{ display:flex; align-items:center; justify-content:space-between; gap:.75rem; margin-bottom:.4rem; }
.rec__who{ display:flex; align-items:center; gap:.6rem; min-width:0; }

.rec__avatar{
  width:var(--rec-avatar); height:var(--rec-avatar);
  border-radius:50%; object-fit:cover; background:#fff;
  border:1px solid var(--rec-br);
}

.rec__txt{ min-width:0; }
.rec__name{ margin:0; font-weight:900; line-height:1.15; }
.rec__meta{
  margin:.12rem 0 0; font-size:.92rem; color:#0970ed; opacity:.98;
  display:flex; align-items:center; gap:.4rem;
}

/* tiny round Huawei logo */
.rec__org-logo{
  width:var(--rec-org-logo); height:var(--rec-org-logo);
  border-radius:30%; object-fit:cover; border:1px solid var(--rec-br);
}

/* “View on [in]” button */
.rec__cta{
  display:inline-flex; align-items:center; gap:.45rem;
  padding:.4rem .7rem; border-radius:10px; text-decoration:none;
  background:#eef6ff; border:1px solid var(--rec-pill-br); color:var(--rec-pill-fg); font-weight:800;
  transition:transform .12s ease, box-shadow .12s ease;
}
.rec__cta:hover{ transform:translateY(-1px); box-shadow:0 6px 14px rgba(15,91,184,.18); }
.rec__cta i{ font-size:1rem; line-height:0; }



/* remove any native disclosure marker (all browsers) */
.rec-drawer > summary::marker { content: none; }
.rec-drawer > summary::-webkit-details-marker { display: none; }

/* hide the FA icon inside the summary */
.rec-drawer > summary i { display: none; }

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

<section class="experience-list">

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


      <details class="exp-card__details" open>
        <summary>Course list</summary>
        <ul class="exp-card__bullets">
          <li><strong>Computer Vision (A collaborative project with the Faculty of Medicine, University of Tehran)</strong> — Fall 2025, Dr. Hamed Malek, Dr. Nazanin Mahdavi</li>
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
</section>

# Courses

<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      IELTS Academic
    </div>
    <div class="experience-role">IELTS Official, Issued Sep 2025</div>
  </div>
  <div class="experience-logo">
    <img src="../images/ielts.jpg" alt="Logo" />
  </div>
</div>

<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Unsupervised Learning, Recommenders, Reinforcement Learning
    </div>
    <div class="experience-role">DeepLearning.AI, Issued Mar 2025</div>
    <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/5HQYM7PKHX4Z">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/deeplearningai.jpg" alt="DeepLearning.AI" />
  </div>
</div>

<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Advanced Learning Algorithms
    </div>
    <div class="experience-role">DeepLearning.AI, Issued Oct 2024</div>
    <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/LYD09SFN7KK8">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/deeplearningai.jpg" alt="DeepLearning.AI" />
  </div>
</div>


<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Supervised Machine Learning: Regression and Classification
    </div>
    <div class="experience-role">DeepLearning.AI, Issued Apr 2024</div>
    <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/9M7SBTAHATYA">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/deeplearningai.jpg" alt="DeepLearning.AI" />
  </div>
</div>


<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Introduction to Databases
    </div>
    <div class="experience-role">Meta, Issued Sep 2023</div>
    <a class="cert-link" href="https://www.coursera.org/account/accomplishments/records/BBKN8JZBC2P5">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/meta.jpg" alt="meta" />
  </div>
</div>

<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Deep Learning Course
    </div>
    <div class="experience-role">University of Tehran, ACM, Issued Summer 2024</div>
    <a class="cert-link" href="https://drive.google.com/file/d/1yM4jr7wKAeMP3Gsu9m0jof2VCjKjWLAb/view?usp=sharing">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/Tehran.png" alt="UT" />
  </div>
</div>
  


<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Machine Learning and Data Science
    </div>
    <div class="experience-role">Iran University of science and technology, Computernic, Issued Summer 2023</div>
    <a class="cert-link" href="https://drive.google.com/file/d/1gukQEzuG4HfpNKtIw4E7LIabVlXEetH9/view?usp=sharing">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/iran.png" alt="Logo" />
  </div>
</div>

<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Introduction to linux
    </div>
    <div class="experience-role">Shahid Beheshti University, Issued Summer 2022</div>
    <a class="cert-link" href="https://drive.google.com/file/d/1Uc0ZVzI_57kB7DJfhhPUF26RCZf9XE-r/view?usp=sharing">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/Sbu-logo.png" alt="sbu" />
  </div>
</div>

<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Fundamentals of Python
    </div>
    <div class="experience-role">Shahid Beheshti University, Issued Summer 2022</div>
     <a class="cert-link" href="https://drive.google.com/file/d/1zhIBX-m2hb-LuaCxnPBB0B6O9MrOv_Pr/view?usp=sharing">View credential</a>
  </div>   
  <div class="experience-logo">
    <img src="../images/Sbu-logo.png" alt="sbu" />
  </div>
</div>

<div class="experience-card">
  <div class="experience-info">
    <div class="experience-title">
      Computer vision
    </div>
    <div class="experience-role">Shahid Beheshti University, Issued Winter 2023</div>
    <a class="cert-link" href="https://drive.google.com/file/d/1CHhlvweQD3QqxTDmC95tLj4Jf80qj20-/view?usp=sharing">View credential</a>
  </div>
  <div class="experience-logo">
    <img src="../images/Sbu-logo.png" alt="sbu" />
  </div>
</div>


<!-- <script type="text/javascript" id="mmvst_globe" src="//mapmyvisitors.com/globe.js?d=HVZ1dytXl71ZnJux6Lqi9u_XgGZap1uRgqVjt2_TcTc"></script> -->

<br>
<br>
<br>
<br>