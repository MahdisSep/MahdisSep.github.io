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
  /* ========= Soft Blue Palette ========= */
  --blue-verylight: #f2f8ff;
  --blue-light: #d8eaff;
  --blue-mid: #a9d3ff;
  --blue-accent: #4a9eff;
  --blue-deep: #1f6ed4;

  /* ========= Experience & Card Variables ========= */
  --exp-bg: var(--blue-verylight);
  --exp-border: #e2edf8;
  --exp-accent: var(--blue-accent);
  --badge-bg: #eaf3ff;
  --badge-text: #123c63;

  /* gradient border for exp/pubs */
  --exp-grad-1: #cde4fa;
  --exp-grad-2: #a7d8f5;
  --exp-grad-3: #6fb7f0;
  --exp-bw: 1.6px;
  --exp-radius: 14px;
  --exp-glow: 0 16px 36px rgba(98, 160, 255, 0.16);
  --exp-glow-hover: 0 24px 54px rgba(98, 160, 255, 0.22);

  /* logo sizing */
  --exp-logo: 100px;
  --exp-lab-logo: 80px;
  --exp-lab-gap: 25px;

  /* Projects */
  --proj-grad-1: #d6e9ff;
  --proj-grad-2: #a6d2ff;
  --proj-grad-3: #72b4f5;
  --proj-bg: var(--blue-verylight);
  --proj-glow: 0 16px 36px rgba(60,140,255,0.15);
  --proj-glow-hover: 0 22px 48px rgba(60,140,255,0.25);

  /* Chips */
  --chip-bg: #f3f8ff;
  --chip-b: #d9e8fb;
  --chip-text: #143a52;
}

/* ========= Experience List ========= */
.experience-list { display: grid; gap: 1.25rem; }

.exp-card {
  display: grid;
  grid-template-columns: var(--exp-logo) 1fr;
  gap: 1rem;
  align-items: start;
  padding: 1rem 1.25rem;
  border-radius: var(--exp-radius);

  background:
    linear-gradient(var(--exp-bg), var(--exp-bg)) padding-box,
    linear-gradient(135deg, var(--exp-grad-1), var(--exp-grad-2) 55%, var(--exp-grad-3)) border-box;
  border: var(--exp-bw) solid transparent;

  box-shadow: 0 8px 16px rgba(0,0,0,.04), var(--exp-glow);
  transition: transform .2s ease, box-shadow .2s ease;
}

.exp-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 24px rgba(0,0,0,.08), var(--exp-glow-hover);
}

.exp-card__logo {
  width: var(--exp-logo);
  height: var(--exp-logo);
  border-radius: 12px;
  object-fit: contain;
  background: #fff;
  border: 1px solid var(--exp-border);
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
}

/* Text styles */
.exp-card__header { display:flex; flex-wrap:wrap; justify-content:space-between; gap:.25rem .75rem; margin-bottom:.25rem; }
.exp-card__role { font-size:1.05rem; margin:0; color:#13344e; }
.exp-card__dates { font-size:.9rem; color:#5b6b7a; }
.exp-card__org { font-weight:600; color:#234b6b; margin-bottom:.25rem; }
.exp-card__summary { margin:.25rem 0 .5rem; color:#384b5a; }

/* details section */
.exp-card__details summary { cursor:pointer; margin-top:.35rem; color:var(--exp-accent); font-weight:600; }
.exp-card__bullets { margin:.5rem 0 0 .9rem; }
.exp-card__bullets li { margin:.15rem 0; }

/* logos stacked */
.exp-card__logos {
  display: grid;
  align-content: start;
  grid-template-rows: var(--exp-lab-logo) var(--exp-lab-logo);
  gap: var(--exp-lab-gap);
  width: var(--exp-logo);
}
.exp-card__logos img {
  width: 100%;
  height: var(--exp-lab-logo);
  object-fit: contain;
  background: #fff;
  border-radius: 12px;
  border: 1px solid var(--exp-border);
}

/* responsive */
@media (max-width:640px) {
  .exp-card { grid-template-columns:60px 1fr; padding:.9rem; }
  .exp-card__logo { width:60px; height:60px; border-radius:8px; }
  .exp-card__logos { width:60px; grid-template-rows:44px 44px; gap:4px; }
  .exp-card__logos img { height:44px; border-radius:8px; }
}

/* ========= Chips (soft blue) ========= */
.chip, .chip-button {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  padding: 0.35rem 0.75rem;
  border-radius: 999px;
  font-weight: 700;
  font-size: 0.9rem;
  color: var(--chip-text);
  background: var(--chip-bg);
  border: 1px solid var(--chip-b);
  box-shadow: 0 2px 4px rgba(90,140,200,0.08);
  transition: all 0.2s ease;
}

.chip-button { cursor: pointer; }

.chip-button:hover {
  background: #e6f1ff;
  border-color: #c5defc;
  transform: translateY(-1px);
  box-shadow: 0 5px 12px rgba(85,140,220,0.15);
}

/* Muted chip */
.chip--muted {
  background: #f2f4f7;
  color: #5b6b7a;
  border-color: #e0e6eb;
  box-shadow: none;
}

/* Group of chips */
.chip-group {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
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