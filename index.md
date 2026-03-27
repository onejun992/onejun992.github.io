<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
  :root{
    --sidebar-w: 265px;
    --gap: 38px;
    --text: #111;
    --muted: #666;
    --line: #e9e9e9;
  }
  
  /* ===== Research Focus tags ===== */
.ap-tags{
  display:flex;
  flex-wrap:wrap;
  gap:6px;
}

.ap-tag{
  font-size:.85em;
  padding:3px 8px;
  border:1px solid #ddd;
  border-radius:999px;
  background:#fafafa;
  line-height:1.2;
}

.ap-tag-main{
  border-color:#111;
  font-weight:600;
}

  /* ===== Academic Pages-like layout ===== */
  .ap-wrap{
    max-width: 1080px;
    margin: 0 auto;
    padding: 28px 18px;
    display: grid;
    grid-template-columns: var(--sidebar-w) minmax(0, 1fr);
    column-gap: var(--gap);
    align-items: start;
  }

  /* Sidebar */
  .ap-sidebar{ position: sticky; top: 22px; }

  .ap-card{
    border-right: 1px solid var(--line);
    padding-right: 22px;
  }

  .ap-avatar{
  width: 210px;
  height: auto;              /* ✅ 关键：高度自适应，完整显示照片 */
  border-radius: 12px;       /* 轻微圆角，学术主页常用 */
  object-fit: contain;       /* ✅ 不裁切，完整显示 */
  background: #f4f4f4;       /* 如果照片比例不同，有个干净背景 */
  display: block;
  margin: 6px 0 14px 0;
}

  .ap-name{
    font-size: 1.28rem;
    font-weight: 800;
    color: var(--text);
    margin: 0 0 6px 0;
    line-height: 1.22;
  }

  .ap-sub{
    color: var(--muted);
    margin: 0 0 14px 0;
    line-height: 1.55;
    font-size: 0.95rem;
  }

  .ap-sub strong{ color: var(--text); font-weight: 750; }

  /* Contact list (icon + text) */
  .ap-contacts{
    list-style: none;
    padding: 0;
    margin: 14px 0 0 0;
  }

  .ap-contacts li{ margin: 10px 0; }

  .ap-contacts a{
    display: flex;
    align-items: center;
    gap: 10px;
    text-decoration: none;
    color: var(--text);
    line-height: 1.45;
    font-size: 0.95rem;
    word-break: break-word;
  }

  .ap-contacts a:hover{ text-decoration: underline; }

  .ap-contacts i{
    width: 18px;
    text-align: center;
    color: #444 !important;
    font-size: 0.98rem;
    flex: 0 0 18px;
  }
  
.ap-contacts a{
  color: var(--text) !important;
}

.ap-contacts a:visited{
  color: var(--text) !important;
}

.ap-contacts a:hover{
  text-decoration: none;
}
  
.ap-contacts a:hover i{
  color: #111 !important;
}

  .ap-contacts .muted{ color: var(--muted); font-size: 0.92rem; }

  /* Main content */
  .ap-main{ min-width: 0; }

  /* Divider (match your previous section-sep) */
  .section-sep{
    margin: 18px 0;
    height: 1px;
    background: var(--line);
  }

  /* ===== Responsive ===== */
  @media (max-width: 860px){
    .ap-wrap{
      grid-template-columns: 1fr;
      row-gap: 18px;
    }
    .ap-sidebar{ position: static; top: auto; }
    .ap-card{
      border-right: none;
      padding-right: 0;
      border-bottom: 1px solid var(--line);
      padding-bottom: 16px;
    }
    .ap-avatar{ width: 132px; height: 132px; }
  }
  
/* ===== Profile card: 3 key blocks ===== */
aside.ap-sidebar .ap-section{
  padding: 10px 0;
  border-top: 1px solid rgba(0,0,0,0.08);
}

aside.ap-sidebar .ap-section:first-child{
  border-top: 0;
  padding-top: 6px;
}

aside.ap-sidebar .ap-label{
  font-size: 0.78rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #777;
  margin-bottom: 6px;
}

aside.ap-sidebar .ap-value{
  font-size: 1.02rem;
  line-height: 1.45;
  color: #222;
}

/* make Research Focus feel most important */
aside.ap-sidebar .ap-focus .ap-value{
  font-weight: 600;
}

aside.ap-sidebar .ap-focus .ap-value br + *{
  font-weight: 400;
  color: #444;
}
  
/* 最后一个 section 下面也加分割线 */
aside.ap-sidebar .ap-section:last-of-type{
  border-bottom: 1.5px solid var(--line);
  padding-bottom: 14px;
  margin-bottom: 14px;
}

/* ===== FINAL FINAL: force sidebar list + links ===== */

/* 1) 黑点：不管是 marker 还是 before，都干掉 */
aside.ap-sidebar ul,
aside.ap-sidebar ol{
  list-style: none !important;
  padding-left: 0 !important;
  margin-left: 0 !important;
}

aside.ap-sidebar li{
  list-style: none !important;
}

/* 主题常用的“伪黑点”来源 */
aside.ap-sidebar li::marker{ content: "" !important; }
aside.ap-sidebar li::before{ content: none !important; display: none !important; }
aside.ap-sidebar li::after{  content: none !important; }

/* 2) 彻底锁定左栏链接颜色 */
aside.ap-sidebar a,
aside.ap-sidebar a:link,
aside.ap-sidebar a:visited,
aside.ap-sidebar a:hover,
aside.ap-sidebar a:active{
  color: #111 !important;
  text-decoration: none !important;
}

aside.ap-sidebar a *{
  color: inherit !important;
}

/* SVG 图标 */
aside.ap-sidebar svg,
aside.ap-sidebar svg *{
  fill: #444 !important;
  stroke: #444 !important;
}

/* Font Awesome 图标 */
aside.ap-sidebar i{
  color: #444 !important;
}

/* 间距 */
aside.ap-sidebar{
  line-height: 1.55 !important;
}

aside.ap-sidebar .ap-profile-block{
  margin-bottom: 16px !important;
}
  
/* ===== Name block (final aligned version) ===== */
aside.ap-sidebar .ap-name-block{
  text-align: left;               /* 关键：左对齐 */
  margin: 10px 0 18px;
  padding-bottom: 14px;
  border-bottom: 2px solid rgba(0,0,0,0.15);
}

/* English name: academic scale */
aside.ap-sidebar .ap-name{
  margin: 4px 0 6px !important;
  font-size: 1.8rem;
  font-weight: 700;
  letter-spacing: 0.2px;
  line-height: 1.15;
  border-bottom: none !important; /* 关键：杀掉默认细线 */
}

/* Chinese / KR-JP names */
aside.ap-sidebar .ap-name-zh,
aside.ap-sidebar .ap-name-krjp{
  font-size: 1.02rem;
  font-weight: 400;
  color: #555;
  line-height: 1.25;
}

aside.ap-sidebar .ap-name-zh{ margin: 0 0 2px; }
aside.ap-sidebar .ap-name-krjp{ margin: 0; }

/* spacing before profile text */
aside.ap-sidebar .ap-profile-block{
  margin-top: 16px !important;
}

/* ===== Multilingual Research (CJK only, academic style) ===== */

.ap-main details.research-multilang {
  margin-top: 2rem;
}

/* 通用：仅作用于多语言折叠区 */
.ap-main details.research-multilang .lang-ko,
.ap-main details.research-multilang .lang-ja,
.ap-main details.research-multilang .lang-zh {
  font-size: 0.96rem;          /* 比英文略小 */
  line-height: 1.85;           /* 学术论文常用 */
  color: #333;
  margin-top: 1.4rem;
}

/* 韩文：行距略大，字距极小 */
.ap-main details.research-multilang .lang-ko {
  letter-spacing: 0.005em;
}

/* 日文：几乎不加字距 */
.ap-main details.research-multilang .lang-ja {
  letter-spacing: 0.01em;
}

/* 中文：绝对不要大字距 */
.ap-main details.research-multilang .lang-zh {
  letter-spacing: 0;
}

/* 段落间距（很关键） */
.ap-main details.research-multilang .lang-ko p,
.ap-main details.research-multilang .lang-ja p,
.ap-main details.research-multilang .lang-zh p {
  margin-bottom: 1.2rem;
}

/* ===== ONLY summary toggle style (keep body layout unchanged) ===== */

/* 1) summary 变成“学术按钮” */
main.ap-main details > summary{
  list-style: none !important;
  cursor: pointer !important;
  user-select: none !important;

  display: inline-flex !important;
  align-items: center !important;
  gap: 10px !important;

  padding: 10px 12px !important;
  margin: 10px 0 !important;

  border: 1px solid var(--line) !important;
  border-radius: 10px !important;

  background: #fafafa !important;
  color: #222 !important;

  font-size: 0.95rem !important;
  font-weight: 700 !important;
  letter-spacing: 0.02em !important;
}

/* 2) 干掉浏览器默认小三角 */
main.ap-main details > summary::-webkit-details-marker{ display:none !important; }
main.ap-main details > summary::marker{ content:"" !important; }

/* 3) 自己画一个更显眼的小箭头（左侧） */
main.ap-main details > summary::before{
  content: "▸" !important;
  font-size: 1.05rem !important;
  color: #111 !important;
  transform: translateY(-0.5px);
}
main.ap-main details[open] > summary::before{
  content: "▾" !important;
}

/* 4) hover / open 状态更“高级”一点 */
main.ap-main details > summary:hover{
  background: #f3f3f3 !important;
}

main.ap-main details[open] > summary{
  background: #fff !important;
  box-shadow: 0 1px 0 rgba(0,0,0,0.06) !important;
}

/* 5) summary 里的 strong 不要变成超粗黑块 */
main.ap-main details > summary strong{
  font-weight: 700 !important;
  color: inherit !important;
}
  
/* ===== Publications: KO main + EN/JA/ZH secondary ===== */

.pub-alt-title{
  margin-top: 0.45rem;
  margin-left: 0.15rem;
}

.pub-alt-title > div{
  font-size: 0.88rem;
  line-height: 1.65;
  color: #666;
}

.pub-alt-title .pub-en{ letter-spacing: 0.01em; }
.pub-alt-title .pub-ja{ letter-spacing: 0.02em; }
.pub-alt-title .pub-zh{ letter-spacing: 0.04em; }

/* ===== Research Focus tags (square, academic) ===== */

.ap-tags{
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.ap-tag{
  font-size: 0.85em;
  padding: 6px 10px;
  border: 1px solid #ddd;
  border-radius: 6px;   /* 方角 */
  background: #fff;
  line-height: 1.2;
  font-weight: 400;
  color: #111;
}

.ap-tag-main{
  border-color: #ddd;   /* 不再突出边框 */
  font-weight: 500;     /* 轻微强调即可 */
}

/* =========================
   Academic Updates Card
   ========================= */
.ap-updates-card{
  border: 1px solid var(--line);
  border-radius: 14px;
  background: #fff;
  padding: 14px 16px;
  margin: 6px 0 18px 0;
  box-shadow: 0 2px 10px rgba(0,0,0,0.04);
}

.ap-updates-meta{
  display:flex;
  align-items:center;
  gap:10px;
  margin-bottom: 8px;
  color:#222;
}

.ap-updates-meta .ap-badge{
  display:inline-flex;
  align-items:center;
  gap:8px;
  font-size: 0.82rem;
  font-weight: 750;
  padding: 4px 10px;
  border: 1px solid rgba(0,0,0,0.12);
  border-radius: 999px;
  background:#fafafa;
}

.ap-updates-main{
  font-size: 1.02rem;
  line-height: 1.65;
  color:#111;
  margin: 0;
}

.ap-updates-main strong{
  font-weight: 800;
}

.ap-updates-sub{
  margin-top: 10px;
  padding-top: 10px;
  border-top: 1px dashed rgba(0,0,0,0.10);
  color:#333;
  font-size: 0.95rem;
  line-height: 1.75;
}

.ap-updates-sub .u-line{
  margin: 0.25rem 0;
}

.ap-updates-sub .u-label{
  font-size: 0.78rem;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color:#777;
  margin-bottom: 6px;
}

/* ===== News multilingual: premium details ===== */
.ap-updates-sub{
  margin-top: 10px;
  padding-top: 10px;
  border-top: 1px dashed rgba(0,0,0,0.10);
}

.ap-updates-sub details{
  margin: 0;
}

.ap-updates-sub summary{
  list-style: none !important;
  cursor: pointer;
  user-select: none;

  display: inline-flex;
  align-items: center;
  gap: 10px;

  padding: 6px 10px;
  border: 1px solid rgba(0,0,0,0.10);
  border-radius: 999px;
  background: #fafafa;

  color: #222;
  font-size: 0.86rem;
  font-weight: 650;
}

.ap-updates-sub summary::-webkit-details-marker{ display:none; }
.ap-updates-sub summary::marker{ content:""; }

.ap-updates-sub summary::before{
  content: "▸";
  font-size: 0.95rem;
  color: #111;
}
.ap-updates-sub details[open] summary::before{
  content: "▾";
}

.ap-updates-sub .ml-grid{
  margin-top: 10px;
  display: grid;
  grid-template-columns: 76px 1fr;
  row-gap: 10px;
  column-gap: 12px;
}

.ap-updates-sub .ml-tag{
  font-size: 0.72rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #777;
  padding-top: 2px;
}

.ap-updates-sub .ml-text{
  color: #222;
  font-size: 0.95rem;
  line-height: 1.65;
}

.ap-updates-sub .ml-text strong{
  font-weight: 750;
}

/* ===== Academic Positioning / Degree Context ===== */
.ap-degree-note-card .ap-updates-main{
  line-height: 1.7;
}

.ap-degree-note-card .ap-degree-note-en{
  display:block;
  margin-top: 4px;
  font-size: 0.98rem;
  font-weight: 400;
  color:#222;
}

.ap-degree-note-card .ml-grid{
  grid-template-columns: 76px 1fr;
}

.ap-degree-note-card .ml-text{
  line-height: 1.78;
}

.ap-degree-note-card .ml-text strong{
  font-weight: 750;
}
  
</style>

<div class="ap-wrap">

  <!-- ===== LEFT SIDEBAR (Academic Pages style) ===== -->
  <aside class="ap-sidebar">
    <div class="ap-card">

      <img class="ap-avatar" src="{{ '/assets/img/profile.png' | relative_url }}" alt="Profile photo">

     <div class="ap-name-block">
  <div class="ap-name-zh">彭塬钧</div>
  <h1 class="ap-name">Peng Yuanjun</h1>
  <div class="ap-name-krjp">팽원균 · ほうげんきん(彭塬鈞)</div>
</div>
<div class="ap-links" style="max-width:100%;">

 <!-- CV & Publications -->
<div style="display:flex; gap:10px; flex-wrap:wrap;">

  <a href="/cv/" style="
    display:inline-block;
    font-size:0.88em;
    font-weight:600;
    padding:4px 10px;
    border:1px solid #ccc;
    border-radius:8px;
    background:#fff;
    color:#000;
    text-decoration:none;
    line-height:1.2;
    box-shadow:0 2px 6px rgba(0,0,0,0.05);
    white-space:nowrap;
  ">CV</a>

  <a href="/publications/" style="
    display:inline-block;
    font-size:0.88em;
    font-weight:600;
    padding:4px 10px;
    border:1px solid #ccc;
    border-radius:8px;
    background:#fff;
    color:#000;
    text-decoration:none;
    line-height:1.2;
    box-shadow:0 2px 6px rgba(0,0,0,0.05);
    white-space:nowrap;
  ">Publications</a>

</div>

<!-- Practice-based Research -->
<div style="margin-top:10px;">
  <a href="/practice/" style="
    display:inline-block;
    white-space:nowrap;
    font-size:0.9em;
    font-weight:600;
    padding:5px 12px;
    border:1.5px solid #111;
    border-radius:999px;
    background:#fff;
    color:#111;
    text-decoration:none;
    line-height:1.2;
    transition:all .25s ease;
  "
  onmouseover="this.style.background='#111';this.style.color='#fff';"
  onmouseout="this.style.background='#fff';this.style.color='#111';"
  >
    Practice-based Research →
  </a>
</div>

<!-- Profile block (make sure it's CLOSED) -->
<div class="ap-profile-block">
  <!-- 你的 Research Profile 正文放这里 -->
</div>

  <!-- 1) Research focus -->
  <div class="ap-section ap-focus">
    <div class="ap-label">Research Focus</div>
   <div class="ap-value ap-tags">
  <span class="ap-tag">Cultural Content</span>
  <span class="ap-tag">Cultural Hybridity</span>
  <span class="ap-tag">Japanese Subculture · ACG Culture</span>
</div>
  </div>

  <!-- 2) Academic Background -->
<div class="ap-section ap-academic-bg">
  <div class="ap-label">ACADEMIC BACKGROUND</div>
  <div class="ap-value">
   Cultural Content Studies
  </div>
</div>

  <!-- 3) Degree -->
  <div class="ap-section ap-degree">
    <div class="ap-label">Degree</div>
    <div class="ap-value">
      Doctor of Arts (D.A.)<br>
      <span style="font-size:0.92rem; color:#666; font-style:italic;">
        Ph.D.-equivalent research doctorate
      </span>
    </div>
  </div>

</div>

     <li>
  <a href="https://www.google.com/maps/search/?api=1&query=Seoul%2C%20South%20Korea"
     target="_blank" rel="noopener noreferrer">
    <i class="fa-solid fa-location-dot"></i>
    <span>Seoul, South Korea</span>
  </a>
</li>

<li>
  <span>
    <i class="fa-solid fa-building-columns"></i>
    Sangmyung University
  </span>
</li>

<li>
  <a href="mailto:onejun992@163.com">
    <i class="fa-solid fa-envelope"></i>
    <span>Email (CN)</span>
  </a>
</li>

<li>
  <a href="mailto:shadowpyj007@gmail.com">
    <i class="fa-solid fa-at"></i>
    <span>Email</span>
  </a>
</li>

<li>
  <a href="https://scholar.google.com/citations?user=OCK6mWAAAAAJ&hl=en"
     target="_blank" rel="noopener noreferrer">
    <i class="fa-solid fa-graduation-cap"></i>
    <span>Google Scholar</span>
  </a>
</li>

<li>
  <a href="https://orcid.org/0009-0003-4920-1890"
     target="_blank" rel="noopener noreferrer">
    <i class="fa-brands fa-orcid"></i>
    <span>ORCID</span>
  </a>
</li>

    </div>
  </aside>

  <!-- ===== RIGHT MAIN CONTENT (原文一字不漏) ===== -->
<main class="ap-main" markdown="1">

## Academic Positioning

<div class="ap-updates-card ap-degree-note-card">
  <div class="ap-updates-meta">
    <span class="ap-badge">Academic Positioning</span>
  </div>

  <p class="ap-updates-main">
    <strong>Ph.D.-equivalent research doctorate in Cultural Content</strong><br>
    <span class="ap-degree-note-en">
      Although the degree title is formally designated as <strong>Doctor of Arts (D.A.)</strong>,
      the actual doctoral training, academic requirements, and research pathway were
      equivalent to those of a <strong>Ph.D.-level research doctorate</strong>.
    </span>
  </p>

  <div class="ap-updates-sub">
    <details>
      <summary>Multilingual</summary>

      <div class="ml-grid">
        <div class="ml-tag">EN</div>
        <div class="ml-text">
          <strong>Academic Positioning</strong><br>
          The academic unit in which I pursued my doctoral training was centered on the field of Cultural Content and consisted of three subfields: <strong>Major in Cultural Content</strong>, <strong>Major in Cultural Arts Management</strong>, and <strong>Major in Convergent Arts Content</strong>. Its overall educational framework combined both cultural theory and artistic practice, aiming to cultivate internationally oriented and interdisciplinary scholars in the broader field of cultural content.<br><br>
          My own specialization was the <strong>Major in Cultural Content</strong>, which followed a theory-based and research-oriented academic track designed primarily for the training of scholars. Its educational objectives and training methods were distinct from, and not directly related to, the more practice- or arts-oriented subfields of Cultural Arts Management and Convergent Arts Content.<br><br>
          During my doctoral training, I completed rigorous academic requirements including scholarly writing and publication, conference presentations, and participation in academic projects. Therefore, although the degree title on the diploma is formally designated as <strong>Doctor of Arts (D.A.)</strong> due to the historical structure of the academic unit and degree-awarding system, in terms of its actual training pathway, academic standards, and research outcomes, my degree should be understood as a <strong>Ph.D.-equivalent research doctorate</strong>, rather than a professional or practice-based doctorate.
        </div>

        <div class="ml-tag">KR</div>
        <div class="ml-text">
          <strong>학문적 정체성</strong><br>
          본인 박사과정 수학 당시 소속 학과는 문화콘텐츠 분야를 핵심 양성 방향으로 삼고 있었으며, <strong>문화콘텐츠전공</strong>, <strong>문화예술경영전공</strong>, <strong>융합예술콘텐츠전공</strong>의 세부 전공으로 구성되어 있었다. 해당 학과의 전체 교육 체계는 문화이론 연구와 예술실천 응용을 아우르는 복합적 성격을 지니고 있었으며, 국제적 시야를 갖춘 융복합형 문화콘텐츠 연구 인재 양성을 지향하였다.<br><br>
          본인이 소속되었던 전공은 <strong>문화콘텐츠전공</strong>으로, 이는 이론 연구를 중심으로 하는 학술형·연구형 박사 양성 경로에 해당한다. 따라서 그 교육 목표와 훈련 방식은 문화예술경영전공 및 융합예술콘텐츠전공과 같은 실천적·예술적 성격의 세부 전공과는 분명히 구별되며, 직접적인 연관성이 없다.<br><br>
          본인은 박사과정 동안 연구형 박사 기준에 따라 엄격한 학술논문 작성 및 발표, 학술대회 발표, 학술 프로젝트 참여 등 체계적인 학문 훈련을 거쳐 학위를 취득하였다. 따라서 학과의 역사적 구조와 학위 수여 체계의 특성으로 인해 학위명은 형식상 <strong>Doctor of Arts (D.A.)</strong>로 표기되었으나, 실제 양성과정, 학문적 요구 수준 및 연구 성과의 측면에서 본 학위는 <strong>Ph.D.와 동등한 연구형 박사학위</strong>로 이해되어야 하며, 전문실천형 또는 예술실천형 박사학위로 보아서는 안 된다.
        </div>

        <div class="ml-tag">JA</div>
        <div class="ml-text">
          <strong>学術的立場</strong><br>
          私が博士課程在籍中に所属していた学科は、文化コンテンツ分野を中核的な養成領域とし、<strong>文化コンテンツ学専攻</strong>、<strong>文化芸術経営専攻</strong>、<strong>融合芸術コンテンツ専攻</strong>の三つの細分専攻によって構成されていた。学科全体の教育体系は、文化理論研究と芸術実践応用の双方を含む複合的性格を有しており、国際的視野を備えた複合型の文化コンテンツ研究人材の育成を目的としていた。<br><br>
          そのうち、私の所属専攻は <strong>文化コンテンツ学専攻</strong> であり、理論研究を中核とする学術型・研究型の博士養成課程に属していた。したがって、その教育目標および訓練方法は、文化芸術経営専攻や融合芸術コンテンツ専攻といった、より実践的・芸術的性格をもつ専攻とは明確に異なり、直接的な関連を有しない。<br><br>
          私は博士課程において、研究型博士の基準に基づき、厳格な学術論文の執筆・発表、学会発表、学術プロジェクトへの参加など、体系的な学術訓練を経て学位を取得した。したがって、学科全体の歴史的構造および学位授与制度上の事情により、学位名称は形式上 <strong>Doctor of Arts (D.A.)</strong> と表記されているものの、実際の養成経路、学術的要求水準、および研究成果の観点から見れば、本学位は <strong>Ph.D. に相当する研究型博士学位</strong> と理解されるべきであり、専門職学位または実践型博士学位として解されるべきではない。
        </div>

        <div class="ml-tag">ZH</div>
        <div class="ml-text">
          <strong>学术定位说明</strong><br>
          本人博士培养期间所属学科以文化内容领域为核心培养方向，下设<strong>文化内容学、文化艺术经营、融合艺术内容</strong>三个细分专业领域，整体培养体系兼具文化理论研究与艺术实践应用两种导向，旨在培养具有国际化视野的复合型文化内容人才。<br><br>
          本人所属的<strong>文化内容学方向</strong>属于以理论研究为核心的学术型培养路径，主要面向研究者养成；其培养目标、训练方式与文化艺术经营、融合艺术内容等偏实践或艺术类导向的细分专业并不相同，亦无直接关联。<br><br>
          在博士培养过程中，本人依照研究型博士标准，完成了严格的学术论文撰写与发表、学术会议发表、学术项目参与等系统性研究训练，并在持续的学术研究基础上取得博士学位。尽管由于学科整体设置及学位授予体制的历史性原因，学位证书标注为 <strong>Doctor of Arts (D.A.)</strong>，但就其实际培养路径、学术要求与研究成果而言，本人所获学位应被理解为<strong>等同于 Ph.D. 的学术研究型博士学位</strong>，而非专业实践型或艺术实践型博士学位。
        </div>
      </div>
    </details>
  </div>
</div>

<hr />

## News

<div class="ap-updates-card">
  <div class="ap-updates-meta">
    <span class="ap-badge">Feb 2026</span>
  </div>

  <p class="ap-updates-main">
    <strong>Postdoctoral Researcher(Non-full-time，Affiliated)</strong><br>
    <strong>K-Culture Creative Content Research Institute</strong><br>
    <strong>Sangmyung University, Seoul, South Korea</strong>
  </p>

  <div class="ap-updates-sub">
    <details>
      <summary>Multilingual</summary>

      <div class="ml-grid">
        <div class="ml-tag">KR</div>
        <div class="ml-text">
          상명대학교 <strong>K-Culture창의콘텐츠연구소</strong><br>
          <strong>박사후 연구원(비전임 · 연구 협력)</strong>
        </div>

        <div class="ml-tag">JA</div>
        <div class="ml-text">
          祥明大学（サンミョン大学） <strong>K-Culture創意コンテンツ研究所</strong><br>
          <strong>ポストドクトラル研究員(非常勤・研究協力)</strong>
        </div>

        <div class="ml-tag">ZH</div>
        <div class="ml-text">
          韩国祥明大学 <strong>K-文化创意内容研究所</strong><br>
          <strong>博士后研究员(非全职 · 合作研究)</strong>
        </div>
      </div>
    </details>
  </div>

</div>  <!-- ✅ 关键：补上 ap-updates-card 的关闭标签 -->

<hr />

## Research Profile

I received my Doctor of Arts (D.A.) in Cultural Content from the Department of Global Culture Contents at Sangmyung University, Korea.

My primary field of research is Cultural Content Studies, with cultural hybridity theory and its perspectives forming the core theoretical framework of my research.
I focus in particular on Japanese subculture, otaku culture, and two-dimensional · ACG (animation, comics, and games) cultural contents.

Within the socio-cultural context of East Asia and the contemporary new media environment, my research pays close attention to the relationships of integration between subculture and mainstream culture,
as well as to phenomena of cultural export and reversed cultural flows of cultural contents,
and analyzes processes of cultural transition and transformation such as globalization, glocalization, and hybridization.

From the perspective of cultural content re-creation and the reconstruction of meaning,
I conduct in-depth analysis and interpretation of cultural commodities and media contents.

---

<details>
  <summary><strong>연구 분야</strong></summary>

  <div class="lang-ko">
    <p>
      본인은 한국 상명대학교 글로벌문화콘텐츠학과 문화콘텐츠 전공에서 박사학위를 취득하였다.
      주요 연구분야는 문화콘텐츠학이며, 문화혼종 이론 및 그 관점을 연구의 핵심 이론적 프레임으로 설정한다.
      연구방향은 일본 서브컬쳐, 오타쿠 문화 및 2차원 · ACG(애니메이션·만화·게임)의 문화 콘텐츠에 집중된다.
    </p>

    <p>
      동아시아 사회적 맥락과 뉴미디어 시대의 환경 속에서,
      서브컬쳐와 주류문화 간의 융합 관계에 주목하고,
      문화콘텐츠의 문화적 수출과 역수출 현상을 분석한다.
      또한 글로벌화, 글로컬라이제이션, 혼종화 등 문화의 이행과 전환 과정을 분석한다.
    </p>

    <p>
      문화혼종 이론 및 그 관점에 기반하여,
      문화콘텐츠 재창조와 의미 재구성의 관점에서
      문화상품 및 미디어 콘텐츠를 심층적으로 분석하고 해석한다.
    </p>
  </div>
</details>

---

<details>
  <summary><strong>研究分野</strong></summary>

  <div class="lang-ja">
    <p>
      本人は韓国・祥明大学グローバル文化コンテンツ学科文化コンテンツ学専攻にて博士号を取得した。
      主な研究分野は文化コンテンツ学であり、文化的な混種に関する理論およびその見解を研究の中核的な理論枠組として位置づける。
      研究方向は日本のサブカルチャー、御宅文化、ならびに二次元 · ACG（动画·漫画·游戏）の文化内容に集中する。
    </p>

    <p>
      東アジアの社会的文脈およびニューメディア時代の背景のもとで、
      亜文化と主流文化のあいだの融合関係に注目し、
      文化内容の文化的輸出および文化的逆輸出の現象を分析する。
      さらに、グローバル化、グローカリゼーション、混種化など、文化の移行と転化の過程を分析する。
    </p>

    <p>
      文化的な混種に関する理論およびその見解に基づき、
      文化内容の再創造と意味重構の観点から、
      文化商品および媒体内容を深層的に分析・解釈する。
    </p>
  </div>
</details>

---

<details>
  <summary><strong>研究领域</strong></summary>

  <div class="lang-zh">
    <p>
      本人毕业于韩国祥明大学全球文化内容学科文化内容学专业，并取得博士学位。
      主要研究领域为文化内容学，并以文化混种理论及其观点作为研究的核心理论框架，
      研究方向集中于日本亚文化、御宅文化以及二次元 · ACG（动画·漫画·游戏）的文化内容。
    </p>

    <p>
      在东亚社会语境与新媒体时代背景下，
      重点关注亚文化与主流文化之间的融合关系，
      以及文化内容的文化输出与文化逆输出现象，
      并分析全球化、全球本土化与混种化等文化迁移与转化过程。
    </p>

    <p>
      基于文化混种理论，
      从文化内容再创造与意义重构的角度出发，
      对文化商品及媒体内容进行深入的分析与诠释。
    </p>
  </div>
</details>

---

## Research Background

My academic interest lies in cultural content studies, with a particular focus on ACG (Animation, Comics, and Games) cultures and cultural hybridity in East Asia. My research is grounded in long-term engagement with Japanese popular culture and its transnational circulation, especially within contemporary Chinese digital media environments.

I conceptualize culture as a dynamic and bidirectional process rather than a one-way flow from dominant to peripheral regions. Cultural exchange often involves reciprocal influence, conflict, negotiation, and eventual hybridization, producing new cultural forms and meanings. This perspective has guided my interest in cultural hybridity as a key analytical framework.

My recent research has focused on the Chinese video-sharing platform Bilibili as a representative site of cultural hybridity, where Japanese subcultural elements, local youth cultures, and platform-based participatory practices intersect. In parallel, I examine the development of China’s cultural industries in the context of global cultural circulation, including the international expansion of digital games and animation since 2020.

More broadly, my research aims to explore how cultural contents are produced, transformed, and circulated under conditions of globalization, and how platformization and transnational media practices contribute to the reconfiguration of cultural industries and cultural identities in contemporary East Asia.

---

## Publications

### Journal Articles

- **Peng, Yuanjun(팽원균)**, & Cho, Kyuheon(조규헌).  
  (2024).  
  문화혼종성 관점에서 본 중국 동영상 플랫폼 비리비리(bilibili)에 관한 고찰: 세배기(拜年紀)를 중심으로.  

  > *A Study of the Chinese Video Platform Bilibili from the Perspective of Cultural Hybridity: Focusing on “Pay New Year's call period” (Lunar New Year Gala)*  

  > *文化的な混種性の観点からみた中国動画プラットフォームBilibiliに関する考察――  
  > 「拜年紀（Bainianji）」を中心に――*  

  > *文化混种性观点下的中国视频平台哔哩哔哩（bilibili）考察——以“拜年纪”为中心*  

  *The Journal of Foreign Studies*, Foreign Studies Institute.  
  DOI: https://doi.org/10.15755/jfs.2024..70.613

---

### Conference Proceedings

- **Peng, Yuanjun(팽원균)**.  
  (2024).  
  문화혼종성 관점에서 본 중국 동영상 플랫폼 비리비리(bilibili)에 관한 고찰: 세배기(拜年紀)를 중심으로.  

  > *A Study of the Chinese Video Platform Bilibili from the Perspective of Cultural Hybridity: Focusing on “Pay New Year's call period” (Lunar New Year Gala)*  

  > *文化的な混種性の観点からみた中国動画プラットフォームBilibiliに関する考察――  
  > 「拜年紀（Bainianji）」を中心に――*  

  > *文化混种性观点下的中国视频平台哔哩哔哩（bilibili）考察——以“拜年纪”为中心*  

  *Proceedings of the Global Cultural Contents Conference*,  
  Global Cultural Contents Society, Vol. 2024, No. 8.  
  Available at: https://www.riss.kr/link?id=A109225174

- **Peng, Yuanjun(팽원균)**.  
  (2022).  
  중국 동영상 플랫폼 비리비리(bilibili)와 ACG/2차원 문화의 관계성 고찰.  

  > *A Study on the Relationship between the Chinese Video Platform Bilibili and  
  > ACG / SubCulture*  

  > *中国動画プラットフォームBilibiliとACG／二次元文化の関係性に関する考察*  

  > *中国视频平台哔哩哔哩（bilibili）与 ACG／二次元文化关系的考察*  

  *Proceedings of the Korean Cultural Contents Joint Academic Conference*.

- **Doctoral Dissertation**  
  (2026).  
  Sangmyung University, Graduate School, Seoul, South Korea.  

  중국 동영상 플랫폼 비리비리(bilibili) 세배기(拜年紀) 형성의 문화적 함의에 대한 연구  
  – 일본 서브컬쳐의 수용에서 중국 주류문화로의 이행까지 –

  > *A Study on the Cultural Implications of the Formation of the Bilibili's Lunar New Year Gala on Chinese Video Platform*  
  > *– From the acceptance of Japanese subculture to the transition into Chinese mainstream culture –*

  > *中国動画プラットフォームBilibiliにおける「拜年紀（Lunar New Year Gala）」形成の文化的含意に関する研究*  
  > *— 日本サブカルチャーの受容から中国主流文化への移行まで —*

  > *中国视频平台哔哩哔哩（bilibili）“拜年纪”形成的文化含意研究*  
  > *—— 从日本亚文化的受容到中国主流文化的移行 ——*
 
---

## Education

- **Doctor of Arts (D.A.) in Global Culture Contents** 
  Graduate School of Humanities and Social Sciences,  
  Sangmyung University, Seoul, South Korea  
  *(Originally enrolled in the M.A. program; formally transferred to the integrated M.A.–D.A.track)*  
  (Mar 2022 – Feb 2026)

- **M.A. coursework in Global Culture Contents** 
  Graduate School of Humanities and Social Sciences,  
  Sangmyung University, Seoul, South Korea (Sep 2020 – Feb 2022)

- **B.A. in Korea-Japan Cultural Content** 
  College of Humanities and Social Sciences,  
  Sangmyung University, Seoul, South Korea (Sep 2016 – Aug 2020)

---

## Language Proficiency

- **Chinese (Mandarin)**: Native speaker.

- **Korean**: Near-native professional proficiency.  
  TOPIK Level 6; over 12 years of academic study and daily life experience in Korea,  
  with extensive use in academic research, conference presentations, and institutional communication.

- **Japanese**: Advanced listening comprehension with over 20 years of continuous exposure  
  to Japanese ACG and popular culture.  
  Formal proficiency certification currently at JLPT N5; continuing systematic language training.
  
---

## Academic Service & Leadership

- **Teaching Assistant**,  
  Office of External Affairs – International Student Services Team,  
  Sangmyung University (Sep 2020 – Feb 2021)

- **Teaching Assistant**,  
  Graduate School Academic Affairs Division,  
  Sangmyung University (Mar 2021 – Feb 2023)

- **International Student Representative**,  
  Department of Korean–Japanese Cultural Contents,  
  Sangmyung University (Mar 2018 – Feb 2019)

- **Chinese International Student Representative**,  
  Department of Korean–Japanese Cultural Contents,  
  Sangmyung University (Mar 2019 – Aug 2020)

- **Team Leader & Chief Coordinator**,  
  International Student Representative Group,  
  Creative Convergence Success Conference,  
  Sangmyung University (March 2019 – June 2019).  
  Led and coordinated a representative team participating in the university-wide  
  creative contents exhibition competition on behalf of the department.

- **Director**,  
  Sangmyung University Chinese Students and Scholars Association (SMUCSSA),  
  affiliated with the Education Section, 
  of the Embassy of the People’s Republic of China in the Republic of Korea
  (Mar 2021 – Jun 2021)

- **President (6th Term)**,  
  Sangmyung University Chinese Students and Scholars Association (SMUCSSA),  
  affiliated with the Education Section, 
  of the Embassy of the People’s Republic of China in the Republic of Korea  
  (Jul 2021 – May 2022)  
  *(Official election announcement: https://mp.weixin.qq.com/s/Ym-ubGgLLlgHEIrR4BSEDQ)*

\*Following the transition into doctoral studies in March 2022 and increasing academic commitments, voluntarily stepped down from the presidential role. Subsequently facilitated a structured leadership transition by formally endorsing the Secretary-General—whom I had previously mentored—as the succeeding President, while continuing to support the association in a Vice Presidential and advisory capacity until mid-2025, fully concluding involvement upon the graduation of the 7th-term President.*<br>
*(Official election announcement(7th-term)：https://mp.weixin.qq.com/s/AtlP3RDXTQEWRYuK_CGzxg)*.  

**Summary:** Demonstrated progressive leadership development, academic service experience, organizational management, and cross-cultural coordination within university and official educational frameworks.

---

## Awards & Honors

- **Conference Presentation Award**,  
  Academic Festival, Department of Korean-Japanese Cultural Contents,  
  Sangmyung University (December 2019).

- **Conference Presentation Award**,  
  Korean Cultural Contents Joint Academic Conference  
  (June 2022).

- **Conference Presentation Award**,  
  Summer Conference of the Global Cultural Contents Society  
  (August 2024).

## Projects & Research Activities

- **Book Chapter Contributor**.  
  *코로나 체인지* (Corona Change).  
  Lettre Publishing, January 15, 2021.  
  ISBN: 9791197230219.  
  https://www.yes24.com/Product/Goods/96836878

- **Book Chapter Contributor**.  
  *문화, 콘텐츠에 빠지다* (Immersed in Culture and Contents).  
  Lettre Publishing, December 30, 2021.  
  ISBN: 9791197230233.  
  https://www.yes24.com/Product/Goods/105894052

- **Book Chapter Contributor**.  
  *한류와 문화콘텐츠: 한류를 보는 다양한 시선들*  
  (Hallyu and Cultural Contents: Diverse Perspectives on Hallyu).  
  Lettre Publishing, February 6, 2023.  
  ISBN: 9791197230264.  
  https://www.yes24.com/Product/Goods/117303953

- **Practice-based Research in Japanese Subculture and ACG Media**.  
  Conducted sustained digital cultural practice on Bilibili as a virtual streamer (V-Tuber),  
  producing content centered on Japanese ACG (Anime, Comics, and Games) culture,  
  including virtual performances and Japanese anime song covers.  
  This practice functioned as research-in-action, enabling in-depth, experiential analysis of  
  Japanese subcultural aesthetics, virtual identity construction, audience participation,  
  and platform-mediated cultural interaction within contemporary East Asian digital subcultures.  
  *(Bilibili channel: https://space.bilibili.com/103596519)*

---

## Public Engagement & Media

- **Public Cultural Communication through Digital Media (Overseas Perspective)**.  
  Operated a China-oriented overseas cultural information account on Sina Weibo with official *Orange V* verification,  
  reaching approximately **128,000 followers** (September 2014 – December 2022).  
  The platform primarily targeted China-based audiences interested in Korean culture,  
  providing first-hand introductions to everyday life in Korea, including food culture, lifestyle practices,  
  and local social trends.  
  Following shifts in platform dynamics and audience engagement, content dissemination gradually transitioned  
  to emerging social media platforms such as Rednot.  
  *(Weibo profile: https://weibo.com/u/1202236810)*

- **Editorial Experience in Public Digital Media**.  
  Served as an editorial contributor for a WeChat public account specializing in Korean food culture  
  (August 2017 – December 2017).

---

## Personal Values & Academic Disposition

Through more than twelve years of academic study and everyday life in Korea,  
I have cultivated strong perseverance, ethical self-discipline, and a respectful attitude  
toward others. I value kindness, patience, and integrity as fundamental principles  
guiding both my academic work and interpersonal relationships.  
Careful attention to detail, a cautious yet forward-looking mindset, and a strong sense  
of responsibility constitute the foundation of my academic disposition.

A defining feature of my academic life has been a long-standing commitment to discipline  
and reliability. From early education through doctoral training, I have consistently  
maintained rigorous personal standards regarding time management and task completion,  
approaching academic responsibilities with punctuality, preparedness, and respect  
for institutional schedules. I regard timely engagement and conscientious execution  
not as exceptional qualities, but as essential conditions for sustaining trust  
within academic and organizational environments.

An important formative experience occurred during my late adolescence.  
At the age of seventeen, I successfully achieved a substantial and sustained physical  
transformation, reducing my body weight from approximately 100 kilograms to 70 kilograms  
within a limited period, and maintaining regular physical training, healthy routines,  
and disciplined daily habits thereafter. This experience reinforced my understanding of  
long-term commitment, self-regulation, and consistency as foundational principles applicable  
not only to personal well-being, but also to academic research and professional life.

In addition, my experience of more than two years as a trainee within the Korean  
entertainment industry has shaped my sensitivity to cultural production systems,  
aesthetic standards, and the operational dynamics of the creative industries.  
This background has contributed to my sustained interest in popular culture, fashion,  
and entertainment as structured cultural fields rather than purely expressive domains.

Extended periods of independent living abroad have strengthened my capacity to confront  
challenges autonomously and to respond to uncertainty with composure and resilience.  
Combined with a reflective, inward-oriented, and meaning-driven personal disposition—  
often associated with the INFJ personality profile—I approach problems by seeking  
their underlying structures rather than surface phenomena. This orientation has fostered  
a habit of analytical depth, anticipatory thinking, and long-term planning.

Overall, I consider academic work to be grounded not only in intellectual ability,  
but also in character, consistency, and responsibility. These values shape my approach  
to research, collaboration, and engagement within both academic and cultural contexts.

  </main>
</div>
