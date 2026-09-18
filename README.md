Now updating the About section and adding a dedicated Academics section before Football:Now let's view the football section area to insert a new Academics section right before it, and move coursework there:Now inserting a full Academics section before Football, moving coursework there, and trimming the Business section:Now trim the Business section since coursework and some honors moved to Academics, and swap its accolades list to avoid duplication:Now let's touch up the closing quote to reflect an academics-first framing, then republish:Now republish the updated artifact:Updated. Here's what changed to shift the focus more academic:

- **Name** is now Yashasvi Chauhan throughout.
- **Hero** now leads with GPA and National Honor Society instead of the football stat line; the headline puts "Rigorous in the classroom" first.
- **New dedicated Academics section** (before Football) with GPA, class rank, AP/Honors course count, Honor Roll years, academic accolades, and the coursework list moved here.
- **About section** now opens with academics as the priority, football as secondary discipline-builder — and the two-column block puts "The Classroom" before "The Field."
- **Business section** trimmed down to just the ventures/activities, since the academic credentials now live in their own section.

Here's the full updated code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Yashasvi Chauhan — #22</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Source+Serif+4:ital,opsz,wght@0,8..60,400;0,8..60,500;0,8..60,600;0,8..60,700;1,8..60,400&display=swap" rel="stylesheet">
<style>
  :root {
    --field:   #10221A;
    --field-2: #16301F;
    --gold:    #C9A227;
    --gold-2:  #E4C55A;
    --paper:   #F1ECDD;
    --ink:     #17190F;
    --ink-soft: #4A4A3E;
    --line:    rgba(23,25,15,0.16);
    --bg: var(--paper);
    --bg-panel: #ffffff;
    --text: var(--ink);
    --text-soft: var(--ink-soft);
    --hairline: var(--line);
    --accent: var(--gold);
    --field-bg: var(--field);
    --field-bg-2: var(--field-2);
    --field-text: var(--paper);
  }

  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
      --bg: #0D0F0A;
      --bg-panel: #15170F;
      --text: #EDE8D8;
      --text-soft: #A9A594;
      --hairline: rgba(237,232,216,0.14);
      --field-bg: #0B1712;
      --field-bg-2: #112417;
    }
  }
  :root[data-theme="dark"] {
    --bg: #0D0F0A;
    --bg-panel: #15170F;
    --text: #EDE8D8;
    --text-soft: #A9A594;
    --hairline: rgba(237,232,216,0.14);
    --field-bg: #0B1712;
    --field-bg-2: #112417;
  }

  * { box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    margin: 0;
    background: var(--bg);
    color: var(--text);
    font-family: "Source Serif 4", Georgia, "Times New Roman", serif;
    font-size: 17px;
    line-height: 1.65;
    -webkit-font-smoothing: antialiased;
  }
  h1, h2, h3, .display {
    font-family: "Anton", "Arial Narrow", sans-serif;
    font-weight: 400;
    letter-spacing: 0.01em;
    line-height: 0.95;
    margin: 0;
  }
  a { color: inherit; }
  img { max-width: 100%; display: block; }
  .wrap {
    max-width: 1080px;
    margin: 0 auto;
    padding: 0 28px;
  }
  .rule {
    border: none;
    border-top: 1px solid var(--hairline);
    margin: 0;
  }

  /* ---------- NAV ---------- */
  nav {
    position: sticky;
    top: 0;
    z-index: 50;
    background: var(--bg);
    border-bottom: 1px solid var(--hairline);
  }
  .nav-inner {
    max-width: 1080px;
    margin: 0 auto;
    padding: 16px 28px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
  }
  .nav-mark {
    font-family: "Anton", sans-serif;
    font-size: 22px;
    letter-spacing: 0.02em;
    white-space: nowrap;
  }
  .nav-links {
    display: flex;
    gap: 26px;
    font-size: 14px;
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .nav-links a {
    text-decoration: none;
    color: var(--text-soft);
    border-bottom: 1px solid transparent;
    padding-bottom: 2px;
    transition: color .15s ease, border-color .15s ease;
  }
  .nav-links a:hover { color: var(--text); border-color: var(--accent); }
  .nav-toggle { display: none; }

  /* ---------- HERO ---------- */
  .hero {
    position: relative;
    background: var(--field-bg);
    color: var(--field-text, var(--paper));
    overflow: hidden;
  }
  .hero-inner {
    max-width: 1080px;
    margin: 0 auto;
    padding: 88px 28px 64px;
    position: relative;
    z-index: 2;
  }
  .hero-number {
    position: absolute;
    right: -0.06em;
    top: 50%;
    transform: translateY(-46%);
    font-family: "Anton", sans-serif;
    font-size: min(46vw, 560px);
    line-height: 1;
    color: rgba(228, 197, 90, 0.09);
    z-index: 1;
    user-select: none;
    pointer-events: none;
  }
  .hero-eyebrow-row {
    display: flex;
    align-items: baseline;
    gap: 14px;
    color: var(--gold-2);
    font-size: 15px;
    margin-bottom: 22px;
    flex-wrap: wrap;
  }
  .hero-eyebrow-row span:not(:last-child)::after {
    content: "";
    display: inline-block;
    width: 5px; height: 5px;
    border-radius: 50%;
    background: currentColor;
    margin-left: 14px;
    vertical-align: middle;
    opacity: .7;
  }
  .hero h1 {
    font-size: clamp(52px, 9vw, 108px);
    color: var(--paper);
  }
  .hero h1 em {
    font-style: normal;
    color: var(--gold-2);
  }
  .hero-tag {
    max-width: 540px;
    margin-top: 26px;
    font-size: 19px;
    color: rgba(241,236,221,0.82);
  }
  .hero-cta {
    display: flex;
    gap: 14px;
    margin-top: 38px;
    flex-wrap: wrap;
  }
  .btn {
    font-family: "Source Serif 4", serif;
    font-size: 15px;
    padding: 12px 22px;
    border-radius: 3px;
    text-decoration: none;
    display: inline-block;
    border: 1px solid transparent;
    cursor: pointer;
  }
  .btn-solid {
    background: var(--gold);
    color: #17190F;
  }
  .btn-outline {
    border-color: rgba(241,236,221,0.4);
    color: var(--paper);
  }

  /* scoreline strip under hero */
  .scoreline {
    position: relative;
    z-index: 2;
    border-top: 1px solid rgba(241,236,221,0.14);
    background: rgba(0,0,0,0.14);
  }
  .scoreline-inner {
    max-width: 1080px;
    margin: 0 auto;
    padding: 0 28px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
  }
  .score-cell {
    padding: 22px 18px;
    border-left: 1px solid rgba(241,236,221,0.14);
    text-align: left;
  }
  .score-cell:first-child { border-left: none; }
  .score-num {
    font-family: "Anton", sans-serif;
    font-size: 34px;
    color: var(--gold-2);
  }
  .score-label {
    font-size: 12.5px;
    color: rgba(241,236,221,0.65);
    margin-top: 4px;
  }

  /* ---------- SECTION SHELL ---------- */
  section { padding: 84px 0; }
  .section-head {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    gap: 24px;
    margin-bottom: 44px;
    border-bottom: 1px solid var(--hairline);
    padding-bottom: 18px;
  }
  .section-head h2 {
    font-size: clamp(30px, 4vw, 44px);
  }
  .section-head .index {
    font-family: "Anton", sans-serif;
    font-size: 15px;
    color: var(--text-soft);
    white-space: nowrap;
  }

  /* ---------- ABOUT / DUAL IDENTITY ---------- */
  .dual {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0;
    border: 1px solid var(--hairline);
  }
  .dual > div {
    padding: 40px;
  }
  .dual > div:first-child {
    border-right: 1px solid var(--hairline);
  }
  .dual h3 {
    font-size: 26px;
    margin-bottom: 16px;
  }
  .dual p { color: var(--text-soft); margin: 0 0 14px; }
  .dual .tag {
    display: inline-block;
    font-size: 13px;
    color: var(--accent);
    margin-bottom: 14px;
  }
  .about-copy {
    max-width: 680px;
    font-size: 18px;
    color: var(--text-soft);
    margin-bottom: 48px;
  }
  .about-copy strong { color: var(--text); font-weight: 600; }

  /* ---------- STATS TABLE ---------- */
  table.stat-table {
    width: 100%;
    border-collapse: collapse;
    font-family: "Source Serif 4", serif;
  }
  table.stat-table caption {
    text-align: left;
    font-size: 14px;
    color: var(--text-soft);
    margin-bottom: 14px;
  }
  table.stat-table th, table.stat-table td {
    text-align: left;
    padding: 13px 10px;
    border-bottom: 1px solid var(--hairline);
    font-size: 15px;
  }
  table.stat-table th {
    font-size: 12.5px;
    color: var(--text-soft);
    font-weight: 600;
  }
  table.stat-table td.num, table.stat-table th.num {
    text-align: right;
    font-family: "Anton", sans-serif;
    font-size: 17px;
    letter-spacing: 0.02em;
  }
  .stats-grid {
    display: grid;
    grid-template-columns: 1.3fr 1fr;
    gap: 48px;
    align-items: start;
  }
  .accolades { list-style: none; padding: 0; margin: 0; }
  .accolades li {
    display: flex;
    gap: 14px;
    padding: 12px 0;
    border-bottom: 1px solid var(--hairline);
    font-size: 15.5px;
  }
  .accolades li:last-child { border-bottom: none; }
  .accolades .yr {
    font-family: "Anton", sans-serif;
    color: var(--accent);
    min-width: 48px;
  }

  /* ---------- VENTURES ---------- */
  .ventures {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--hairline);
    border: 1px solid var(--hairline);
  }
  .venture {
    background: var(--bg);
    padding: 32px 28px;
  }
  .venture .role {
    font-size: 12.5px;
    color: var(--accent);
    margin-bottom: 10px;
  }
  .venture h3 {
    font-family: "Source Serif 4", serif;
    font-weight: 600;
    font-size: 20px;
    margin-bottom: 10px;
    line-height: 1.25;
  }
  .venture p {
    color: var(--text-soft);
    font-size: 15px;
    margin: 0;
  }

  /* ---------- COURSEWORK ---------- */
  .course-list {
    columns: 2;
    column-gap: 40px;
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .course-list li {
    break-inside: avoid;
    padding: 10px 0;
    border-bottom: 1px solid var(--hairline);
    font-size: 15px;
    display: flex;
    justify-content: space-between;
    gap: 10px;
  }
  .course-list li .grade {
    color: var(--text-soft);
    font-family: "Anton", sans-serif;
    font-size: 13px;
  }

  /* ---------- QUOTE ---------- */
  .quote {
    background: var(--field-bg);
    color: var(--paper);
    padding: 76px 0;
  }
  .quote blockquote {
    max-width: 760px;
    margin: 0 auto;
    padding: 0 28px;
    font-family: "Source Serif 4", serif;
    font-style: italic;
    font-size: clamp(22px, 3vw, 30px);
    line-height: 1.5;
  }
  .quote cite {
    display: block;
    font-style: normal;
    margin-top: 24px;
    font-size: 14px;
    color: var(--gold-2);
  }

  /* ---------- CONTACT ---------- */
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 48px;
  }
  .contact-list { list-style: none; padding: 0; margin: 0; }
  .contact-list li {
    padding: 16px 0;
    border-bottom: 1px solid var(--hairline);
    display: flex;
    justify-content: space-between;
    font-size: 15.5px;
  }
  .contact-list li span:first-child { color: var(--text-soft); }
  .contact-list li a { text-decoration: none; }
  .contact-list li a:hover { color: var(--accent); }

  footer {
    border-top: 1px solid var(--hairline);
    padding: 28px 0;
    font-size: 13px;
    color: var(--text-soft);
  }
  .footer-row {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
  }

  /* ---------- RESPONSIVE ---------- */
  @media (max-width: 760px) {
    .nav-links { display: none; }
    .dual { grid-template-columns: 1fr; }
    .dual > div:first-child { border-right: none; border-bottom: 1px solid var(--hairline); }
    .stats-grid { grid-template-columns: 1fr; }
    .ventures { grid-template-columns: 1fr; }
    .course-list { columns: 1; }
    .scoreline-inner { grid-template-columns: repeat(2, 1fr); }
    .score-cell:nth-child(3) { border-left: none; }
    .contact-grid { grid-template-columns: 1fr; }
    .hero-number { font-size: 62vw; opacity: 0.7; }
    section { padding: 56px 0; }
  }

  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-inner">
    <div class="nav-mark">Y. CHAUHAN <span style="color:var(--accent)">22</span></div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#academics">Academics</a></li>
      <li><a href="#football">Football</a></li>
      <li><a href="#business">Business</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<header class="hero">
  <div class="hero-number">22</div>
  <div class="hero-inner">
    <div class="hero-eyebrow-row">
      <span>3.9 GPA · National Honor Society</span>
      <span>Entrepreneurship &amp; Business</span>
      <span>Class of 2027</span>
    </div>
    <h1>Rigorous in the<br>classroom. Relentless<br><em>on the field.</em></h1>
    <p class="hero-tag">Yashasvi Chauhan — a scholar-athlete pursuing a demanding entrepreneurship and business course load, with three years as a varsity running back sharpening the discipline that carries over to the classroom.</p>
    <div class="hero-cta">
      <a class="btn btn-solid" href="#academics">See academics</a>
      <a class="btn btn-outline" href="#contact">Get in touch</a>
    </div>
  </div>
  <div class="scoreline">
    <div class="scoreline-inner">
      <div class="score-cell">
        <div class="score-num">3.9</div>
        <div class="score-label">Weighted GPA</div>
      </div>
      <div class="score-cell">
        <div class="score-num">Top 8%</div>
        <div class="score-label">Class rank, of 340</div>
      </div>
      <div class="score-cell">
        <div class="score-num">6</div>
        <div class="score-label">AP &amp; Honors courses</div>
      </div>
      <div class="score-cell">
        <div class="score-num">1,240</div>
        <div class="score-label">Rushing yards, senior season</div>
      </div>
    </div>
  </div>
</header>

<main>

  <section id="about">
    <div class="wrap">
      <div class="section-head">
        <h2>Two playbooks, one player</h2>
        <div class="index">About</div>
      </div>
      <p class="about-copy">Academics come first for me: <strong>a demanding course load, a 3.9 GPA, and a genuine interest in how businesses actually work.</strong> Football is where I test that same discipline under pressure — three years as a varsity running back for the Lincoln High Wolves have taught me to prepare like the film session matters as much as the game. Between the two, I've built a habit of showing up ready, whether that's for a case study or a fourth-and-one.</p>

      <div class="dual">
        <div>
          <span class="tag">The Classroom</span>
          <h3>Entrepreneurship &amp; Business Major (Intended)</h3>
          <p>Consistent honor roll student carrying six AP and Honors courses this year. Drawn to the operational side of business — finance, marketing, and how small companies actually get built and run.</p>
          <p>3.9 Weighted GPA · Top 8% of Class · National Honor Society</p>
        </div>
        <div>
          <span class="tag">The Field</span>
          <h3>Running Back / Kick Returner</h3>
          <p>Three-year varsity starter known for patience behind the line and a second gear after contact. Team captain, senior year. Treats film study as seriously as classwork.</p>
          <p>5'11" · 195 lbs · 4.58s 40-yard dash</p>
        </div>
      </div>
    </div>
  </section>

  <section id="academics" style="background:var(--bg-panel);">
    <div class="wrap">
      <div class="section-head">
        <h2>In the classroom</h2>
        <div class="index">Academics</div>
      </div>
      <div class="stats-grid">
        <div>
          <table class="stat-table">
            <caption>Academic record</caption>
            <tbody>
              <tr>
                <td>Weighted GPA</td>
                <td class="num">3.9</td>
              </tr>
              <tr>
                <td>Class rank</td>
                <td class="num">Top 8% of 340</td>
              </tr>
              <tr>
                <td>AP &amp; Honors courses (current)</td>
                <td class="num">6</td>
              </tr>
              <tr>
                <td>Years on Honor Roll</td>
                <td class="num">4</td>
              </tr>
            </tbody>
          </table>

          <div style="margin-top:44px;">
            <h3 style="font-family:'Source Serif 4',serif; font-weight:600; font-size:20px; margin-bottom:18px;">Relevant coursework</h3>
            <ul class="course-list">
              <li><span>Intro to Entrepreneurship</span><span class="grade">A</span></li>
              <li><span>Principles of Marketing</span><span class="grade">A</span></li>
              <li><span>Business Finance</span><span class="grade">A-</span></li>
              <li><span>AP Microeconomics</span><span class="grade">A</span></li>
              <li><span>Financial Accounting</span><span class="grade">B+</span></li>
              <li><span>Public Speaking</span><span class="grade">A</span></li>
            </ul>
          </div>
        </div>
        <div>
          <ul class="accolades">
            <li><span class="yr">2026</span> National Honor Society, Inductee</li>
            <li><span class="yr">2026</span> AP Scholar with Honor</li>
            <li><span class="yr">2025</span> Principal's Honor Roll (all four years)</li>
            <li><span class="yr">2025</span> DECA Regional Finalist, Entrepreneurship Series</li>
            <li><span class="yr">2024</span> Student Business Club, President</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <div class="wrap"><hr class="rule"></div>

  <section id="football">
    <div class="wrap">
      <div class="section-head">
        <h2>On the field</h2>
        <div class="index">Football</div>
      </div>
      <div class="stats-grid">
        <div>
          <table class="stat-table">
            <caption>Career rushing &amp; receiving, by season</caption>
            <thead>
              <tr>
                <th>Season</th>
                <th class="num">Carries</th>
                <th class="num">Yards</th>
                <th class="num">TDs</th>
                <th class="num">Rec.</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Sophomore</td>
                <td class="num">98</td>
                <td class="num">612</td>
                <td class="num">6</td>
                <td class="num">14</td>
              </tr>
              <tr>
                <td>Junior</td>
                <td class="num">151</td>
                <td class="num">968</td>
                <td class="num">11</td>
                <td class="num">22</td>
              </tr>
              <tr>
                <td>Senior</td>
                <td class="num">184</td>
                <td class="num">1,240</td>
                <td class="num">17</td>
                <td class="num">26</td>
              </tr>
            </tbody>
          </table>
        </div>
        <div>
          <ul class="accolades">
            <li><span class="yr">2026</span> Team Captain</li>
            <li><span class="yr">2026</span> All-Conference First Team</li>
            <li><span class="yr">2025</span> All-Conference Second Team</li>
            <li><span class="yr">2025</span> Regional Offensive Player of the Week (×3)</li>
            <li><span class="yr">2024</span> Varsity Call-Up, Sophomore Year</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <div class="wrap"><hr class="rule"></div>

  <section id="business">
    <div class="wrap">
      <div class="section-head">
        <h2>Applying it</h2>
        <div class="index">Business</div>
      </div>
      <p class="about-copy" style="margin-bottom:36px;">Coursework is where the concepts get taught; these are where I've tried to put them into practice.</p>

      <div class="ventures">
        <div class="venture">
          <div class="role">Founder, 2025 – Present</div>
          <h3>Chauhan Athletics Co.</h3>
          <p>A small direct-to-consumer apparel brand making training gear for youth football players, run out of a home studio with a local print partner. Manages sourcing, pricing, and Instagram-based sales.</p>
        </div>
        <div class="venture">
          <div class="role">President, 2025 – Present</div>
          <h3>Lincoln High Student Business Club</h3>
          <p>Leads a 30-member club that runs a campus pop-up shop each semester and mentors underclassmen entering DECA competitions.</p>
        </div>
        <div class="venture">
          <div class="role">Regional Finalist, 2026</div>
          <h3>DECA — Entrepreneurship Series</h3>
          <p>Placed in the top eight teams regionally for a business plan built around athlete-founded small brands, presented to a panel of local business owners.</p>
        </div>
      </div>
    </div>
  </section>

  <div class="quote">
    <blockquote>
      "Football taught me how to prepare for something before it happens. That habit is the same one I use to stay ahead in the classroom — the game just makes the stakes easier to feel."
      — Yashasvi Chauhan
    </blockquote>
  </div>

  <section id="contact">
    <div class="wrap">
      <div class="section-head">
        <h2>Let's talk</h2>
        <div class="index">Contact</div>
      </div>
      <div class="contact-grid">
        <div>
          <p style="color:var(--text-soft); max-width:440px; margin-top:0;">Open to conversations with college coaches and admissions, business mentors, or anyone curious about the training apparel brand. Highlight reel and transcript available on request.</p>
        </div>
        <ul class="contact-list">
          <li><span>Email</span><a href="mailto:yashasvi.chauhan@example.com">yashasvi.chauhan@example.com</a></li>
          <li><span>Phone</span><a href="tel:+15555550122">(555) 555-0122</a></li>
          <li><span>Highlight reel</span><a href="#">Hudl profile ↗</a></li>
          <li><span>Business</span><a href="#">@chauhanathletics ↗</a></li>
        </ul>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap footer-row">
    <span>Yashasvi Chauhan · Lincoln High Wolves · Class of 2027</span>
    <span>Portfolio last updated September 2026</span>
  </div>
</footer>

</body>
</html>
```
