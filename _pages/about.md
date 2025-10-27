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

/* ========== COLOR THEME: Warm Sunset ========== */
:root {
  /* Brand palette */
  --orange-light: #ffe5b4;
  --orange-base:  #ffb74d;
  --orange-dark:  #ff8f00;

  /* Experience & cards */
  --exp-bg: #fffaf5;
  --exp-border: #ffe0b2;
  --exp-accent: #ff8f00;
  --badge-bg: #fff3e0;
  --badge-text: #663c00;

  /* Gradient edge + glow (warm) */
  --exp-grad-1: #fff3c2;    /* pale yellow */
  --exp-grad-2: #ffd580;    /* warm orange */
  --exp-grad-3: #ffad42;    /* deeper amber */
  --exp-glow: 0 16px 36px rgba(255, 179, 71, 0.25);
  --exp-glow-hover: 0 24px 54px rgba(255, 128, 0, 0.35);
  --exp-radius: 14px;
  --exp-bw: 1.6px;

  /* Cards, chips, projects */
  --card-bg: #fffaf5;
  --card-b: #ffe0b2;
  --card-ac: #ff8f00;
  --chip-bg: #fff3e0;
  --chip-b: #ffd699;
  --chip-text: #663c00;

  /* Publications & projects */
  --p-bg: #fffaf5;
  --p-br: #ffe0b2;
  --p-ac: #ff8f00;
  --p-ac-2: #d96f00;
  --p-text: #4a2900;
  --p-ratio: 16/7;

  /* Glow / gradient for projects */
  --proj-radius: 14px;
  --proj-bw: 1.6px;
  --proj-bg: #fffaf5;
  --proj-grad-1: #ffebc5;
  --proj-grad-2: #ffc676;
  --proj-grad-3: #ff9f1a;
  --proj-glow: 0 16px 36px rgba(255, 157, 51, 0.22);
  --proj-glow-hover: 0 22px 48px rgba(255, 138, 0, 0.28);

  /* logos */
  --exp-logo: 100px;
  --exp-lab-logo: 80px;
  --exp-lab-gap: 25px;
}

/* Global text / body */
body {
  color: #4a2900;
  background: #fffaf5;
  background-size: cover;
  background-attachment: fixed;
}

a {
  color: var(--exp-accent);
  text-decoration: none;
}
a:hover { color: var(--orange-dark); }

strong { color: #2e1500; }
.year-title { color: #8c5200; }

/* ====================== Experience & Education Cards ====================== */
.experience-card,
.education-card {
  display: flex;
  align-items: flex-start;
  gap: 1.25rem;
  margin-bottom: 1rem;
  padding: 1.25rem 1.5rem;

  border-radius: var(--exp-radius);
  border: var(--exp-bw) solid transparent;
  background:
    linear-gradient(var(--exp-bg), var(--exp-bg)) padding-box,
    linear-gradient(135deg,var(--exp-grad-1),var(--exp-grad-2) 55%,var(--exp-grad-3)) border-box;
  box-shadow: 0 8px 16px rgba(0,0,0,0.04), var(--exp-glow);
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.experience-card:hover,
.education-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 24px rgba(0,0,0,0.08), var(--exp-glow-hover);
}

.experience-logo,
.education-logo {
  flex-shrink: 0;
  width: var(--exp-logo);
  height: var(--exp-logo);
  background: #fff;
  border-radius: 12px;
  border: 1px solid var(--exp-border);
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  overflow: hidden;
}
.experience-logo img,
.education-logo img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.experience-info,
.education-info { flex: 1; display: grid; gap: .25rem; }

.experience-title,
.education-title {
  font-size: 1.05rem;
  font-weight: 700;
  color: #663c00;
}
.experience-title a:hover,
.education-title a:hover { color: var(--orange-dark); }

.experience-role,
.education-role {
  color: #8c5200;
  font-style: italic;
  font-size: 0.9rem;
}
.experience-topics,
.education-topics {
  color: #4a2900;
  font-size: 0.95rem;
  line-height: 1.5;
}

@media (max-width:640px){
  .experience-card,.education-card {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .experience-logo,.education-logo {
    width:70px;height:70px;border-radius:10px;
  }
}

/* ====================== Publications ====================== */
.pub-card {
  display: grid;
  grid-template-columns: minmax(240px,30%) 1fr;
  align-items: start;
  gap: 1.25rem;
  padding: 1rem 1.25rem;

  border-radius: var(--exp-radius);
  border: var(--exp-bw) solid transparent;
  background:
    linear-gradient(var(--exp-bg),var(--exp-bg)) padding-box,
    linear-gradient(135deg,var(--exp-grad-1),var(--exp-grad-2) 55%,var(--exp-grad-3)) border-box;
  box-shadow: 0 8px 16px rgba(0,0,0,.04), var(--exp-glow);
}
.pub-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 24px rgba(0,0,0,.08), var(--exp-glow-hover);
}
.pub-media {
  position: relative;
  border-radius: 12px;
  border: 1px solid var(--exp-border);
  background: #fff;
  overflow: hidden;
  aspect-ratio: 16/10;
}
.pub-media img { width:100%;height:100%;object-fit:contain; }
.pub-badge {
  position:absolute;top:10px;left:10px;
  background:#fff3e0;
  color:#ff8f00;
  border:1px solid #ffd699;
  font-size:.78rem;
  font-weight:700;
  padding:6px 10px;
  border-radius:999px;
  box-shadow:0 1px 3px rgba(0,0,0,.06);
}
.pub-body { display:grid;gap:10px; }
.pub-title { font-size:1.05rem;font-weight:700;color:#663c00; }
.pub-authors { font-size:.95rem;color:#7a4b00; }
.pub-affils { font-size:.9rem;color:#a05b00; }
.pub-chip {
  display:inline-flex;align-items:center;gap:.35rem;
  padding:.28rem .55rem;
  background:var(--badge-bg);
  color:var(--badge-text);
  border:1px solid rgba(255,143,0,.2);
  border-radius:999px;
  font-size:.82rem;font-weight:600;
  transition:background .15s ease,transform .15s ease;
}
.pub-chip:hover {
  background:#fff0da;
  transform:translateY(-1px);
}

/* ====================== Chips ====================== */
.chip, .chip-button {
  display:inline-flex;align-items:center;gap:.45rem;
  padding:.35rem .75rem;
  border-radius:999px;
  font-weight:700;font-size:.9rem;
  background:linear-gradient(135deg,#fff3e0,#ffe0b2);
  color:#4a2900;
  border:1px solid #ffd699;
  box-shadow:0 2px 5px rgba(255,170,0,0.15);
  transition:all .2s ease;
}
.chip-button { cursor:pointer; }
.chip-button:hover {
  background:linear-gradient(135deg,#ffe6c0,#ffd18f);
  transform:translateY(-1px);
  box-shadow:0 5px 12px rgba(255,138,0,0.25);
}

/* ====================== Misc headings ====================== */
.section-title {
  font-size:1.8em;
  color:#663c00;
  border-bottom:2px solid #ffd699;
}

/* Service list hover */
.service-list li { background:#fffaf5; }
.service-list li:hover { transform:translateX(5px); background:#fff3e0; }

.load-more {
  border:2px solid #ff8f00;
  background:#fffaf5;
  color:#ff8f00;
}
.load-more:hover { background:#fff3e0; }

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