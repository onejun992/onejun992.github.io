<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
  :root{
    --sidebar-w: 265px;
    --gap: 38px;
    --text: #111;
    --muted: #666;
    --line: #e9e9e9;
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
  width: 170px;
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
  
</style>

<div class="ap-wrap">

  <!-- ===== LEFT SIDEBAR (Academic Pages style) ===== -->
  <aside class="ap-sidebar">
    <div class="ap-card">

      <img class="ap-avatar" src="{{ '/assets/img/profile.jpg' | relative_url }}" alt="Profile photo">

     <div class="ap-name-block">
  <div class="ap-name-zh">彭塬钧</div>
  <h1 class="ap-name">Peng Yuanjun</h1>
  <div class="ap-name-krjp">팽원균 · ほうげんきん(彭塬鈞)</div>
</div>

<div class="ap-profile-block">

  <!-- 1) Research focus -->
  <div class="ap-section ap-focus">
    <div class="ap-label">Research Focus</div>
    <div class="ap-value">
      Cultural Contents<br>
      Cultural Hybridity · Japanese Subculture · ACG(Animation, Comics, and Games) Contents
    </div>
  </div>

  <!-- 2) Academic Background -->
<div class="ap-section ap-academic-bg">
  <div class="ap-label">ACADEMIC BACKGROUND</div>
  <div class="ap-value">
    Major in Cultural Contents
  </div>
</div>

  <!-- 3) Degree -->
  <div class="ap-section ap-degree">
    <div class="ap-label">Degree</div>
    <div class="ap-value">
      Ph.D. (Doctor of Arts)
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

<li>
  <a href="https://x.com/hibiki_v2022"
     target="_blank" rel="noopener noreferrer">
    <i class="fa-brands fa-x-twitter"></i>
    <span>X (Twitter)</span>
  </a>
</li>

    </div>
  </aside>

  <!-- ===== RIGHT MAIN CONTENT (原文一字不漏) ===== -->
  <main class="ap-main" markdown="1">

## Research Profile

I received my Ph.D. in Cultural Contents from the Department of Global Cultural Contents at Sangmyung University, Korea.

My primary field of research is Cultural Contents Studies, with cultural hybridity theory and its perspectives forming the core theoretical framework of my research.
I focus in particular on Japanese subculture, otaku culture, and two-dimensional · ACG (animation, comics, and games) cultural contents.

Within the socio-cultural context of East Asia and the contemporary new media environment, my research pays close attention to the relationships of integration between subculture and mainstream culture,
as well as to phenomena of cultural export and reversed cultural flows of cultural contents,
and analyzes processes of cultural transition and transformation such as globalization, glocalization, and hybridization.

From the perspective of cultural contents re-creation and the reconstruction of meaning,
I conduct in-depth analysis and interpretation of cultural commodities and media contents.

---

<details>
  <summary><strong>연구 분야</strong></summary>

  <div class="lang-ko">
    <p>
      본인은 한국 상명대학교 글로벌문화콘텐츠학과 문화콘텐츠 전공에서 박사학위를 취득하였다.
      주요 연구분야는 문화콘텐츠학이며, 문화혼종 이론 및 그 관점을 연구의 핵심 이론적 틀로 설정한다.
      연구방향은 일본 아문화, 오타쿠 문화, 그리고 2차원 · ACG(애니메이션·만화·게임)의 문화 콘텐츠에 집중된다.
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
      主な研究分野は文化コンテンツ学であり、文化的混種に関する理論およびその見解を研究の中核的な理論枠組として位置づける。
      研究方向は日本亜文化(subculture)、御宅文化、ならびに二次元 · ACG（动画·漫画·游戏）の文化内容に集中する。
    </p>

    <p>
      東アジアの社会的文脈およびニューメディア時代の背景のもとで、
      亜文化と主流文化のあいだの融合関係に注目し、
      文化内容の文化的輸出および文化的逆輸出の現象を分析する。
      さらに、グローバル化、グローカリゼーション、混種化など、文化の移行と転化の過程を分析する。
    </p>

    <p>
      文化的混種に関する理論およびその見解に基づき、
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

My academic interest lies in cultural contents studies, with a particular focus on ACG (Animation, Comics, and Games) cultures and cultural hybridity in East Asia. My research is grounded in long-term engagement with Japanese popular culture and its transnational circulation, especially within contemporary Chinese digital media environments.

I conceptualize culture as a dynamic and bidirectional process rather than a one-way flow from dominant to peripheral regions. Cultural exchange often involves reciprocal influence, conflict, negotiation, and eventual hybridization, producing new cultural forms and meanings. This perspective has guided my interest in cultural hybridity as a key analytical framework.

My recent research has focused on the Chinese video-sharing platform Bilibili as a representative site of cultural hybridity, where Japanese subcultural elements, local youth cultures, and platform-based participatory practices intersect. In parallel, I examine the development of China’s cultural industries in the context of global cultural circulation, including the international expansion of digital games and animation since 2020.

More broadly, my research aims to explore how cultural contents are produced, transformed, and circulated under conditions of globalization, and how platformization and transnational media practices contribute to the reconfiguration of cultural industries and cultural identities in contemporary East Asia.

---

## Publications

### Journal Articles

- **Peng, Yuanjun(팽원균)**, & Cho, Kyuheon(조규헌).  
  (2024).  
  문화혼종성 관점에서 본 중국 동영상 플랫폼 비리비리(bilibili)에 관한 고찰: 세배기(拜年紀)를 중심으로.  

  > *A Study of the Chinese Video Platform Bilibili from the Perspective of Cultural Hybridity: Focusing on the “Bainianji” (New Year Festival Program)*  

  > *文化的混種性の観点からみた中国動画プラットフォームBilibiliに関する考察――  
  > 「拜年紀（Bainianji）」を中心に――*  

  > *文化混种性观点下的中国视频平台哔哩哔哩（bilibili）考察——以“拜年纪”为中心*  

  *The Journal of Foreign Studies*, Foreign Studies Institute.  
  DOI: https://doi.org/10.15755/jfs.2024..70.613

---

### Conference Proceedings

- **Peng, Yuanjun(팽원균)**.  
  (2024).  
  문화혼종성 관점에서 본 중국 동영상 플랫폼 비리비리(bilibili)에 관한 고찰: 세배기(拜年紀)를 중심으로.  

  > *A Study of the Chinese Video Platform Bilibili from the Perspective of Cultural Hybridity: Focusing on the “Bainianji” (New Year Festival Program)*  

  > *文化的混種性の観点からみた中国動画プラットフォームBilibiliに関する考察――  
  > 「拜年紀（Bainianji）」を中心に――*  

  > *文化混种性观点下的中国视频平台哔哩哔哩（bilibili）考察——以“拜年纪”为中心*  

  *Proceedings of the Global Cultural Contents Conference*,  
  Global Cultural Contents Society, Vol. 2024, No. 8.  
  Available at: https://www.riss.kr/link?id=A109225174

- **Peng, Yuanjun(팽원균)**.  
  (2022).  
  중국 동영상 플랫폼 비리비리(bilibili)와 ACG/2차원 문화의 관계성 고찰.  

  > *Examining the Relationship between the Chinese Video Platform Bilibili and  
  > ACG / Two-Dimensional Culture*  

  > *中国動画プラットフォームBilibiliとACG／二次元文化の関係性に関する考察*  

  > *中国视频平台哔哩哔哩（bilibili）与 ACG／二次元文化关系的考察*  

  *Proceedings of the Korean Cultural Contents Joint Academic Conference*.

### Doctoral Dissertation

- **Ph.D. Dissertation**  
  Sangmyung University, Seoul, South Korea.  
  (Details forthcoming)

---

## Education

- **Ph.D. in Global Cultural Contents**,  
  Graduate School of Humanities and Social Sciences,  
  Sangmyung University, Seoul, South Korea  
  *(Originally enrolled in the M.A. program; formally transferred to the integrated M.A.–Ph.D. track)*  
  (Mar 2022 – Feb 2026)

- **M.A. coursework in Global Cultural Contents**,  
  Graduate School of Humanities and Social Sciences,  
  Sangmyung University, Seoul, South Korea (Sep 2020 – Feb 2022)

- **B.A. in Korean–Japanese Cultural Contents**,  
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
  under the guidance of the Education Section,  
  Embassy of the People’s Republic of China in the Republic of Korea  
  (Mar 2021 – Jun 2021)

- **President**,  
  Sangmyung University Chinese Students and Scholars Association (SMUCSSA),  
  under the guidance of the Education Section,  
  Embassy of the People’s Republic of China in the Republic of Korea  
  (Jul 2021 – May 2022)

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
