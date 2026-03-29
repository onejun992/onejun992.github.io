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

<!-- ===== RIGHT MAIN CONTENT (Academic Positioning Statement / revised full version) ===== -->
<main class="ap-main" markdown="1">

<h2 style="font-weight:800; letter-spacing:-0.025em; margin-bottom:0.4rem;">
  Academic Positioning Statement
</h2>

<div style="margin: -0.15rem 0 1rem 0;">
  <span style="display:inline-block; padding:0.28rem 0.72rem; border:1px solid rgba(0,0,0,0.12); border-radius:999px; font-size:0.92rem; font-weight:600; opacity:0.9;">
    ※ Important academic clarification
  </span>
</div>

  <p class="ap-updates-main">
    <strong>Research-oriented doctoral positioning in Cultural Content Studies</strong><br>
    <span class="ap-degree-note-en">
      Although the degree was formally conferred as <strong>Doctor of Arts (D.A.)</strong>,
      my actual academic formation was a <strong>full-time</strong>, <strong>humanities-based</strong>,
      <strong>theory-driven research pathway</strong> in <strong>Cultural Content Studies</strong>.
      From earning a <strong>Bachelor of Arts in Cultural Content Studies</strong> with a major in
      <strong>Korea-Japan Cultural Content</strong> in <strong>2016</strong> through doctoral
      degree completion in <strong>2026</strong>, I have pursued a continuous
      <strong>ten-year academic trajectory</strong> in the field, distinct from
      <strong>practice-based</strong>, <strong>performance-oriented</strong>, or
      <strong>mid-career professional tracks</strong>.
      In this sense, the academic training, research requirements, and scholarly orientation
      of my doctorate were equivalent to those of a <strong>Ph.D.-level research doctorate</strong>.
    </span>
  </p>

  <div class="ap-updates-sub">
  <details>
    <summary>Multilingual</summary>

    <div class="ml-grid">
      <div class="ml-tag">EN</div>
      <div class="ml-text">
        <strong>Academic Positioning Statement</strong><br>
        Since entering Sangmyung University in <strong>2016</strong>, I have continuously pursued the field of <strong>Cultural Content Studies</strong> through the completion of my doctoral degree in <strong>2026</strong>, forming a continuous <strong>ten-year academic trajectory</strong>.<br><br>

        Sangmyung University has, since around <strong>2016</strong>, increasingly developed into a Seoul-based university with a strong emphasis on <strong>comprehensive culture- and arts-related education</strong>, with notable programs in fields such as <strong>games, animation, music, dance, film and visual media, and cultural content</strong>. My own academic pathway was formed within this broader institutional environment, but remained consistently oriented toward the <strong>humanities-based and theory-driven study of Cultural Content</strong>.<br><br>

        At the undergraduate level, I earned a <strong>Bachelor of Arts in Cultural Content Studies</strong>, with a <strong>major in Korea-Japan Cultural Content</strong>. At the graduate level, I was affiliated with the <strong>Department of Global Culture Contents</strong>. Across my undergraduate, master’s, and doctoral training, my academic foundation consistently remained within <strong>Cultural Content Studies</strong>.<br><br>

        The academic lineage of the graduate field to which I belonged can be traced to the earlier <strong>Creative Contents</strong> program structure under Sangmyung University’s former <strong>professional graduate school</strong> system (Korean: <strong>특수대학원 창의콘텐츠학과</strong>). This point is crucial for understanding the formal designation and institutional particularity of my degree. The former professional graduate school system primarily served <strong>in-service, working adult, and often older students</strong>, was generally <strong>not organized as a full-time academic training system</strong>, and in principle granted <strong>master’s degrees as its highest academic qualification</strong>.<br><br>

        Because my graduate field inherited part of that earlier institutional framework, it retained certain <strong>structural limitations and residual features of the old system</strong>, while also enrolling a substantial number of students from <strong>arts- and practice-oriented backgrounds</strong>. As a result, the degree designation in my case reflects not the actual nature of my own academic training, but the <strong>historical constraints and transitional legacy of the older departmental and degree-granting system</strong>.<br><br>

        Within that institutional setting, however, my own pathway belonged clearly to the <strong>Cultural Content Studies</strong> direction, characterized by a <strong>humanities-based</strong>, <strong>theory-driven</strong>, and <strong>research-oriented</strong> formation. It should therefore be distinguished both from historically common <strong>professional, in-service, and older mid-career study patterns</strong> and from the more <strong>arts- or practice-led doctoral profiles</strong> that were associated with other directions in the broader field.<br><br>

        During my doctoral training, I completed rigorous scholarly work including academic writing and publication, conference presentations, and participation in research projects. Therefore, although the diploma formally designates the degree as <strong>Doctor of Arts (D.A.)</strong>, the actual training pathway, academic standards, and research outcomes should be understood as those of a <strong>Ph.D.-level research doctorate</strong> in the humanities. In this sense, the doctoral title conferred upon me should be regarded as <strong>academically equivalent in standing and function to a Ph.D.</strong>, rather than as a professional, arts-based, or practice-led doctorate.
      </div>

      <div class="ml-tag">KR</div>
      <div class="ml-text">
        <strong>학문적 정체성 및 설명</strong><br>
        본인은 <strong>2016년</strong> 상명대학교 학부 입학 이후 <strong>2026년</strong> 박사학위 취득에 이르기까지, <strong>10년간</strong> 문화콘텐츠학 분야를 지속적으로 연구해 왔다.<br><br>

        상명대학교는 <strong>2016년 이후</strong> 서울권에서 <strong>문화예술 중심의 종합대학</strong>으로서의 성격을 점차 강화해 왔으며, <strong>게임, 애니메이션, 음악, 무용, 영화·영상, 문화콘텐츠</strong> 등 문화예술 계열의 특성화된 전공 및 학과들을 폭넓게 운영해 왔다. 그러나 이러한 대학의 전반적 문화예술 지향성과는 별도로, 본인의 학문 경로는 일관되게 <strong>인문학 기반</strong>, <strong>이론 중심</strong>, <strong>연구 중심</strong>의 문화콘텐츠학에 놓여 있었다.<br><br>

        학부에서는 <strong>문화콘텐츠학사</strong> 학위를 취득하였고, <strong>한일문화콘텐츠학</strong>을 전공하였다. 대학원에서는 <strong>글로벌문화콘텐츠학과 (Department of Global Culture Contents)</strong>에 소속되어 수학하였다. 학부, 석사, 박사 전 과정을 관통하는 본인의 학문적 기반은 일관되게 <strong>문화콘텐츠학</strong>에 있었다.<br><br>

        본인이 석사·박사 과정에서 소속되었던 학문 영역의 제도적 계보는, 상명대학교의 과거 <strong>특수대학원 창의콘텐츠학과</strong> 체계에까지 소급될 수 있다. 이 점은 본인의 학위 명칭과 제도적 특수성을 이해하는 데 매우 중요하다. 당시 <strong>특수대학원</strong>은 대체로 <strong>재직자 및 사회인, 즉 사실상 재직자 중심의 대학원생과 비교적 연령대가 높은 학습자들</strong>을 주된 대상으로 운영되었으며, 일반적으로 <strong>전일제 학술연구 체계가 아니었고</strong>, 제도상 최고 학위 역시 <strong>석사학위에 한정</strong>되어 있었다.<br><br>

        본인이 속한 석·박사 단계의 학과는 이러한 과거 체계의 연장선상에 있었기 때문에, <strong>구 제도의 잔존적 한계와 구조적 문제</strong>를 일정 부분 그대로 안고 있었으며, 동시에 <strong>예술·실기 계열 학생들</strong>이 다수 유입된 배경도 함께 존재하였다. 그 결과, 본인의 학위 표기는 본인의 실제 연구 훈련의 성격이라기보다, <strong>기존 학과 제도와 학위 수여 체계의 역사적 제한성과 과도기적 잔재</strong>를 반영한 측면이 크다.<br><br>

        그러나 그러한 제도적 배경 속에서도 본인의 경로는 명확히 <strong>문화콘텐츠학</strong>을 중심으로 한 <strong>인문학 기반</strong>, <strong>이론 중심</strong>, <strong>연구 중심</strong>의 학술 경로에 속하였다. 따라서 이는 역사적으로 비교적 많이 존재하였던 <strong>재직자·실무자·비교적 연령대가 높은 학습자 중심의 수학 형태</strong>와도 구별되며, 보다 <strong>예술 중심</strong> 또는 <strong>실천 중심</strong>의 박사 경로와도 분명히 다르다.<br><br>

        본인은 박사과정 동안 학술논문 작성 및 발표, 학술대회 발표, 학술 프로젝트 참여 등 연구형 박사 수준의 엄격한 학문 훈련을 수행하였다. 따라서 학위명은 형식상 <strong>Doctor of Arts (D.A.)</strong>로 표기되어 있으나, 실제 양성과정과 학문적 요구 수준, 연구 성과의 측면에서 본 학위는 <strong>인문학 기반의 Ph.D. 상응 연구형 박사학위</strong>로 이해되어야 한다. 즉, 본인에게 수여된 D.A. 학위는 <strong>학문적 위상과 기능에 있어 Ph.D.와 동등한 효력을 갖는 박사학위</strong>로 보아야 하며, 전문실천형 또는 예술실천형 박사와 동일시되어서는 안 된다.
      </div>

      <div class="ml-tag">JA</div>
      <div class="ml-text">
        <strong>学術的立場および説明</strong><br>
        私は <strong>2016年</strong> に祥明大学学部へ入学して以来、<strong>2026年</strong> に博士学位を取得するまで、<strong>10年間</strong> にわたり文化コンテンツ学の領域を継続して研究してきた。<br><br>

        祥明大学は <strong>2016年以降</strong>、ソウル圏において <strong>文化芸術中心の総合大学</strong> としての性格を次第に強めており、<strong>ゲーム、アニメーション、音楽、舞踊、映画・映像、文化コンテンツ</strong> などの文化芸術系分野に特色を有してきた。しかし、そのような大学全体の傾向とは別に、私自身の学問的経路は一貫して <strong>人文学基盤</strong>・<strong>理論中心</strong>・<strong>研究中心</strong> の文化コンテンツ学に属していた。<br><br>

        学部では <strong>文化コンテンツ学学士</strong> の学位を取得し、<strong>韓日文化コンテンツ学</strong> を専攻した。大学院では <strong>グローバル文化コンテンツ学科 (Department of Global Culture Contents)</strong> に所属して研鑽を積んだ。学部・修士・博士の全過程を通じて、私の学問的基盤は一貫して <strong>文化コンテンツ学</strong> に置かれていた。<br><br>

        私が所属した大学院分野の制度的系譜は、祥明大学の旧 <strong>特殊大学院・創意コンテンツ学科</strong>（韓国語原表記：<strong>특수대학원 창의콘텐츠학과</strong>）の段階にまでさかのぼることができる。この点は、私の学位名称と制度的特殊性を理解する上で極めて重要である。もともと <strong>特殊大学院</strong> は、主として <strong>在職者・社会人、すなわち実務と並行して学ぶ大学院生や比較的年齢層の高い学習者</strong> を対象とする制度であり、一般に <strong>全日制の学術研究養成システムではなく</strong>、制度上の最高学位も <strong>修士まで</strong> に限定されていた。<br><br>

        私が所属した修士・博士段階の学科は、その旧制度の延長線上にあったため、<strong>旧学科制度の残存的制約と構造的問題</strong> を一定程度引き継いでおり、同時に <strong>芸術系・実技系の学生</strong> も多く受け入れていた。このため、私に対する学位表記は、私自身の実際の研究訓練の性格そのものというより、<strong>旧制度と学位授与体系に由来する歴史的制約および過渡的残存</strong> を反映したものと理解されるべきである。<br><br>

        しかし、そのような制度的背景の中にあっても、私自身の経路は明確に <strong>文化コンテンツ学</strong> を中心とする <strong>人文学基盤</strong>・<strong>理論中心</strong>・<strong>研究中心</strong> の学術的養成過程に属していた。したがって、それは歴史的に比較的多く見られた <strong>在職者・実務家・比較的年齢層の高い学習者中心の履修形態</strong> とも区別され、また <strong>芸術実践中心</strong> あるいは <strong>専門実践中心</strong> の博士課程とも明確に異なる。<br><br>

        博士課程において私は、学術論文の執筆・発表、学会発表、学術プロジェクトへの参加など、研究型博士に相応する厳格な学術訓練を経て学位を取得した。したがって、学位名称は制度上形式的に <strong>Doctor of Arts (D.A.)</strong> と表記されているものの、実際の養成経路、学術的要求水準、および研究成果の観点から見れば、本学位は <strong>人文学基盤の Ph.D. 相当研究型博士学位</strong> と理解されるべきである。すなわち、私に授与された D.A. 学位は、<strong>学問的位階と機能において Ph.D. と同等の効力を有する博士学位</strong> と見なされるべきであり、専門職学位または芸術実践型博士学位として理解されるべきではない。
      </div>

      <div class="ml-tag">ZH</div>
      <div class="ml-text">
        <strong>学术定位与说明</strong><br>
        本人自 <strong>2016年</strong> 进入祥明大学本科起，至 <strong>2026年</strong> 博士学位取得为止，已在 <strong>文化内容学领域持续学习与研究整整10年</strong>。<br><br>

        祥明大学自 <strong>2016年以后</strong>，逐步发展为首尔圈内以 <strong>文化艺术</strong> 为鲜明特色的重要综合性高校之一，拥有 <strong>游戏、动漫、音乐、舞蹈、电影影像、文化内容</strong> 等文化艺术类优势专业与学科。然而，在这一整体文化艺术导向的学校背景之中，本人的学术路径始终明确属于以 <strong>文化内容学</strong> 为核心的 <strong>纯文科基础</strong>、<strong>理论主导</strong>、<strong>研究导向</strong> 路线。<br><br>

        本科阶段，本人取得 <strong>文化内容学学士</strong> 学位，专业为 <strong>韩日文化内容学</strong>；研究生阶段所属学科为 <strong>全球文化内容学科（Department of Global Culture Contents）</strong>。贯穿本科、硕士与博士全过程的学术基础，始终是 <strong>文化内容学（Cultural Content Studies）</strong>。<br><br>

        本人研究生阶段所属学科具有明确的制度沿革与学科历史，其更早阶段可追溯至祥明大学原 <strong>特殊大学院创意内容学科</strong>（韩文原称：<strong>특수대학원 창의콘텐츠학과</strong>）。这一点对于理解本人学位名称及其制度性特殊背景尤为关键。原有的 <strong>特殊大学院</strong> 主要面向 <strong>在职学习者，即在职研究生，以及相对大龄学习者</strong> 群体，通常 <strong>并非全日制学制</strong>，且其制度上可授予的最高学位一般仅为 <strong>硕士学位</strong>。<br><br>

        正因如此，本人硕博阶段所属的学科在转入一般研究生院体系后，仍然保留了相当程度的 <strong>旧学科制度的残存限制与结构性问题</strong>，并同时吸纳了大量 <strong>艺术类、实践类背景学生</strong>。因此，本人所获学位在名称与授予形式上的特殊性，并不应被简单理解为本人培养路径本身的性质，而应理解为 <strong>旧制度、旧学科体系以及学位授予限制所遗留下来的历史性与过渡性结果</strong>。<br><br>

        然而，即便处于这样的制度背景之下，本人自身的培养路径依然明确属于以 <strong>文化内容学</strong> 为核心的 <strong>纯文科基础</strong>、<strong>理论主导</strong>、<strong>研究导向</strong> 的学术培养路线。这一路径不仅区别于该领域历史上较为常见的 <strong>在职、实务型以及相对大龄修学模式</strong>，也与 <strong>艺术主导</strong> 或 <strong>实践主导</strong> 的博士路径有本质不同。<br><br>

        在博士培养过程中，本人完成了严格的学术论文撰写与发表、学术会议发表、学术项目参与等系统性研究训练。尽管由于学科整体设置与学位授予体制的历史性原因，学位证书形式上标注为 <strong>Doctor of Arts (D.A.)</strong>，但就实际培养路径、学术要求与研究成果而言，本人所获学位应被理解为 <strong>以人文学训练为基础、等同于 Ph.D. 层级的学术研究型博士学位</strong>。也就是说，本人所获 D.A. 学位在 <strong>学术层级、制度功能与博士资格效力</strong> 上，应视作与 <strong>Ph.D. 具有同等效力</strong> 的博士学位，而不应被视为专业实践型或艺术实践型博士学位。
      </div>
    </div>
  </details>
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

- **Doctor of Arts in Cultural Content Studies**  
  Graduate School (Humanities and Social Sciences), Sangmyung University, Seoul, South Korea  
  Department of Global Culture Contents  
  *(Initially admitted to the master's program and transferred to an integrated master's–doctoral track in March 2022)*  
  (Mar 2022 – Feb 2026)

- **Master of Arts coursework completed in Global Culture Contents**  
  Graduate School (Humanities and Social Sciences), Sangmyung University, Seoul, South Korea  
  (Sep 2020 – Feb 2022)

- **Bachelor of Arts in Cultural Content Studies**  
  College of Humanities and Social Sciences, Sangmyung University, Seoul, South Korea  
  *Major in Korea-Japan Cultural Content*  
  (Sep 2016 – Aug 2020)

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

- **Practice-based Research and Creative Activity through Digital Media.**  
  Continuously engaged in practice-based research centered on Japanese subculture and ACG-related media practice. Through sustained creative activity on the Chinese video platform Bilibili, cultural production is approached not as a supplementary interest, but as a methodological site where cultural meaning, identity, and affective experience are explored through virtual performance, anime-song covers, and media production.  
  *(Bilibili: https://space.bilibili.com/103596519)*

- **Public Cultural Communication through Digital Media (Overseas Perspective).**  
  Operated a China-oriented overseas cultural communication account on Sina Weibo with official *Orange V* verification, with follower count peaking at approximately **129,000** during its active period (September 2014 – December 2022). The account primarily introduced everyday life in Korea to China-based audiences, including food culture, lifestyle practices, and local social trends. Following shifts in platform dynamics and the discontinuation of account operation, content dissemination gradually expanded to emerging platforms such as Rednote, while the account’s follower count later declined significantly.  
  *(Weibo profile: https://weibo.com/u/1202236810)*

- **Editorial Experience in Public Digital Media.**  
  Served as an editorial contributor for a WeChat public account specializing in Korean food culture (August 2017 – December 2017).

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
