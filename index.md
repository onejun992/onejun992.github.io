<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
/* ===== Mobile-only fixes (<=700px). Desktop unaffected ===== */
@media (max-width: 700px){

  /* 1) 整个 hero 区块改为上下结构 + 居中 */
  .hero-wrap{
    display: flex !important;
    flex-direction: column !important;
    align-items: center !important;
    gap: 1.2rem !important;
  }

  /* 2) 左侧列（头像+联系方式）整体居中，并限制宽度 */
  .left-col{
    width: 100% !important;
    max-width: 420px !important;
    margin: 0 auto !important;
    text-align: center !important;
  }

  /* 头像居中 + 稍微小一点更精致 */
  .left-col img{
    width: 160px !important;
    display: block !important;
    margin: 0 auto !important;
  }

  /* 3) 右侧信息也居中放置（块居中，文字仍可左对齐） */
  .right-col{
    width: 100% !important;
    max-width: 420px !important;
    margin: 0 auto !important;
  }

  /* 4) 联系方式块：整块居中，但内部文字左对齐（更学术、更干净） */
  .contact-box{
    display: inline-block !important;   /* 关键：让它变成“可居中”的块 */
    text-align: left !important;        /* 内部仍左对齐 */
    margin: 0.9rem auto 0 auto !important;
  }

  /* 5) 让名字别被拆成 PENG / YUANJUN */
  .right-col h2{
    white-space: nowrap !important;
    font-size: 1.6rem !important; /* 小一点，减少断行概率 */
    margin-top: 0 !important;
  }
}
</style>

<div class="hero-wrap" style="display: flex; gap: 2rem;">

<!-- 左侧：头像 + 联系方式 -->
<div class="left-col" style="flex: 0 0 200px;">

  <!-- 头像区域 -->
  <div style="text-align: center;">
    <img
      src="{{ '/assets/img/profile.jpg' | relative_url }}"
      alt="Profile photo"
      style="width: 180px; border-radius: 8px;"
    >
  </div>

<!-- ===================== -->
<!-- Academic Contact Info -->
<!-- ===================== -->
<div class="contact-box academic-contacts">

  <div class="contact-item">
    <i class="fa-solid fa-location-dot"></i>
    <span>Seoul, South Korea</span>
  </div>

  <div class="contact-item">
    <i class="fa-regular fa-envelope"></i>
    <a href="mailto:onejun992@163.com">onejun992@163.com</a>
  </div>

  <div class="contact-item">
    <i class="fa-regular fa-envelope"></i>
    <a href="mailto:shadowpyj007@gmail.com">shadowpyj007@gmail.com</a>
  </div>

  <div class="contact-item">
    <i class="fa-solid fa-graduation-cap"></i>
    <a href="https://scholar.google.com/citations?user=OCK6mWAAAAAJ&hl=en"
       target="_blank" rel="noopener noreferrer">
      Google Scholar
    </a>
  </div>

  <div class="contact-item">
    <i class="fa-brands fa-orcid"></i>
    <a href="https://orcid.org/0009-0003-4920-1890"
       target="_blank" rel="noopener noreferrer">
      ORCID
    </a>
  </div>

  <div class="contact-item">
    <i class="fa-brands fa-x-twitter"></i>
    <a href="https://x.com/hibiki_v2022"
       target="_blank" rel="noopener noreferrer">
      X (Twitter)
    </a>
  </div>

</div>

  <!-- 右侧：基本信息 -->
  <div class="right-col" style="flex: 1;">

    <h2 style="margin-top: 0;">Peng Yuanjun</h2>

    <!-- 一句话研究定位（Tagline） -->
    <p style="margin: 0.25em 0 0.5em 0; font-size: 1em; line-height: 1.35;">
      Researcher in Cultural Contents Studies<br>
      Cultural Hybridity, Japanese Subculture (ACG cultural contents)
    </p>

    <!-- 多语言姓名 -->
    <p style="margin: 0.6em 0;">
      팽원균 / ほうげんきん(彭塬鈞) / 彭塬钧
    </p>

    <!-- 学位 -->
    <p style="margin: 0.6em 0; color: #555;">
      Ph.D. (Doctor of Arts)
    </p>

    <!-- 所属信息 -->
    <p style="margin: 0.6em 0;">
      Department of Global Cultural Contents<br>
      Major in Cultural Contents<br>
      Sangmyung University, Seoul, South Korea
    </p>

  </div>
</div>

<div class="section-sep"></div>

## Research Profile

I received my Ph.D. in Cultural Contents from the Department of Global Cultural Contents at Sangmyung University, Korea.

My primary field of research is Cultural Contents Studies, with cultural hybridity as a central conceptual framework.
I focus in particular on Japanese subculture, otaku culture, and two-dimensional (ACG: animation, comics, and games) contents and cultures.

Within the East Asian socio-cultural context, my research pays close attention to cultural export and reversed cultural flows,
as well as processes of globalization, glocalization, and hybridization as forms of cultural transition.

From the perspective of cultural contents re-creation and the reconstruction of meaning,
I conduct in-depth analysis and interpretation of cultural commodities and media contents.

---

<details>
<summary><strong>연구 분야</strong></summary>

<br/>

본인은 한국 상명대학교 글로벌문화콘텐츠학과 문화콘텐츠 전공에서 박사학위를 취득하였다.
주요 연구 분야는 문화콘텐츠학이며 문화적 혼종성(cultural hybridity)을 핵심 개념으로 삼아 연구를 수행하고 있다.
특히 일본 서브컬처, 오타쿠 문화, 및 이차원·ACG(애니메이션·만화·게임)의 콘텐츠 및 문화에 관심을 두고 있다.

동아시아 사회적 맥락에서 문화콘텐츠의 문화적 수출과 문화적 역류(reversed cultural flows),
그리고 글로벌화(globalization), 글로컬라이제이션(glocalization), 혼종화(hybridization) 등
문화 이행(cultural transition)의 다양한 양상에 주목한다.

또한 문화콘텐츠의 재창조와 의미 재구성이라는 관점에서
문화상품 및 미디어 콘텐츠를 심층적으로 분석하고 해석한다.

</details>

---

<details>
<summary><strong>研究分野</strong></summary>

<br/>

韓国・祥明大学グローバル文化コンテンツ学科（文化コンテンツ学専攻）にて博士号を取得。
主な研究分野は文化コンテンツ学であり、文化的混種性（cultural hybridity）を中心的な概念として研究を行っている。
特に日本のサブカルチャー、オタク文化、および二次元・ACG（アニメ・マンガ・ゲーム）のコンテンツおよび文化に強い関心を持っている。

東アジアの社会的文脈において、文化コンテンツの文化的輸出および文化的逆流（reversed cultural flows）、
ならびにグローバル化、グローカル化、混種化といった文化の移行（cultural transition）の諸過程に注目している。

また、文化コンテンツの再創造と意味の再構築という観点から、
文化商品およびメディア・コンテンツを深層的に分析・解釈している。

</details>

---

<details>
<summary><strong>研究领域</strong></summary>

<br/>

本人毕业于韩国祥明大学全球文化内容学科文化内容学专业，并取得博士学位。
主要研究领域为文化内容学，以文化混种为核心研究概念，
研究方向集中于日本亚文化、御宅文化以及二次元·ACG（动画、漫画、游戏）的内容及文化。

在东亚社会语境背景下，重点关注文化内容的文化输出与文化逆流，
以及全球化、全球本土化与混种化等文化迁移与转化过程。

并从文化内容再创造与意义重构的角度出发，
对文化商品及媒体内容进行深层次的分析与诠释。

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

- **Peng, Yuanjun**, & Cho, Kyuheon.  
  (2024).  
  문화혼종성 관점에서 본 중국 동영상 플랫폼 비리비리(bilibili)에 관한 고찰: 세배기(拜年纪)를 중심으로.  
  *The Journal of Foreign Studies*, Foreign Studies Institute.  
  DOI: https://doi.org/10.15755/jfs.2024..70.613

### Conference Proceedings

- **Peng, Yuanjun**.  
  (2024).  
  문화혼종성 관점에서 본 중국 동영상 플랫폼 비리비리(bilibili)에 관한 고찰: 세배기(拜年纪)를 중심으로.  
  *Proceedings of the Global Cultural Contents Conference*,  
  Global Cultural Contents Society, Vol. 2024, No. 8.  
  Available at: https://www.riss.kr/link?id=A109225174

- **Peng, Yuanjun**.  
  (2022).  
  중국 동영상 플랫폼 비리비리(bilibili)와 ACG/2차원 문화의 관계성 고찰.  
  *Proceedings of the Korean Cultural Contents Joint Academic Conference*.

  ### Doctoral Dissertation

- **Ph.D. Dissertation**  
  Sangmyung University, Seoul, South Korea.  
  (Details forthcoming)

### Academic Profiles

- Google Scholar:  
  https://scholar.google.com/citations?user=OCK6mWAAAAAJ&hl=en

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
