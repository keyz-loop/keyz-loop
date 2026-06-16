<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>keyz-loop GitHub Profile Preview</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Fira+Code:wght@400;600&display=swap" rel="stylesheet"/>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      background: #0d1117;
      color: #e6edf3;
      font-family: 'Inter', sans-serif;
      font-size: 16px;
      line-height: 1.7;
    }
    /* GitHub-style top bar */
    .github-bar {
      background: #161b22;
      border-bottom: 1px solid #30363d;
      padding: 12px 24px;
      display: flex;
      align-items: center;
      gap: 12px;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .github-bar svg { fill: #e6edf3; }
    .github-bar span { color: #e6edf3; font-size: 14px; font-weight: 500; }
    .github-bar .repo-name { color: #58a6ff; font-weight: 600; }
    .container {
      max-width: 980px;
      margin: 0 auto;
      padding: 32px 24px;
    }
    /* README card */
    .readme-card {
      background: #0d1117;
      border: 1px solid #30363d;
      border-radius: 12px;
      overflow: hidden;
    }
    .readme-header {
      background: #161b22;
      border-bottom: 1px solid #30363d;
      padding: 10px 18px;
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 13px;
      color: #8b949e;
    }
    .readme-body {
      padding: 32px 40px;
    }
    /* Profile header section */
    .profile-banner {
      width: 100%;
      border-radius: 8px;
      overflow: hidden;
      margin-bottom: 20px;
    }
    .profile-banner img { width: 100%; display: block; }
    .center { text-align: center; }
    .typing-img { display: block; margin: 12px auto; }
    .badges { display: flex; justify-content: center; flex-wrap: wrap; gap: 8px; margin: 16px 0; }
    .badges img { height: 28px; border-radius: 4px; }
    hr {
      border: none;
      border-top: 1px solid #30363d;
      margin: 28px 0;
    }
    h2 {
      font-size: 1.35rem;
      font-weight: 700;
      color: #e6edf3;
      margin-bottom: 16px;
      padding-bottom: 8px;
      border-bottom: 2px solid #D4A017;
      display: inline-block;
    }
    /* Code block */
    .code-block {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 8px;
      padding: 20px 24px;
      font-family: 'Fira Code', monospace;
      font-size: 13.5px;
      line-height: 1.8;
      color: #e6edf3;
      margin: 16px 0;
      overflow-x: auto;
    }
    .code-block .kw { color: #ff7b72; }
    .code-block .var { color: #79c0ff; }
    .code-block .str { color: #a5d6ff; }
    .code-block .key { color: #D4A017; }
    .code-block .arr { color: #ffa657; }
    .code-block .bool { color: #79c0ff; }
    .code-block .cmt { color: #8b949e; }
    /* About me layout */
    .about-layout {
      display: flex;
      gap: 24px;
      align-items: flex-start;
      margin-top: 16px;
    }
    .about-left { flex: 1; }
    .about-right { flex-shrink: 0; }
    .about-right img { width: 280px; border-radius: 8px; }
    .bullet-list { list-style: none; padding: 0; }
    .bullet-list li {
      padding: 6px 0;
      color: #c9d1d9;
      font-size: 14.5px;
    }
    .bullet-list li a { color: #D4A017; text-decoration: none; font-weight: 600; }
    .bullet-list li a:hover { text-decoration: underline; }
    .bullet-list li strong { color: #e6edf3; }
    .bullet-list li code {
      background: #1f2937;
      padding: 2px 6px;
      border-radius: 4px;
      font-family: 'Fira Code', monospace;
      font-size: 13px;
      color: #ffa657;
    }
    /* Tech stack */
    .tech-section { text-align: center; }
    .tech-label {
      font-weight: 700;
      color: #D4A017;
      margin: 20px 0 10px;
      font-size: 15px;
      letter-spacing: 0.5px;
    }
    .badge-row { display: flex; flex-wrap: wrap; justify-content: center; gap: 8px; margin-bottom: 6px; }
    .badge-row img { height: 28px; border-radius: 4px; transition: transform 0.2s; }
    .badge-row img:hover { transform: translateY(-2px); }
    /* Projects table */
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 16px;
      font-size: 14px;
    }
    thead tr { background: #1a0a00; }
    thead th {
      padding: 12px 16px;
      color: #D4A017;
      font-weight: 700;
      text-align: center;
      border: 1px solid #30363d;
    }
    tbody tr { transition: background 0.2s; }
    tbody tr:hover { background: #1a0a0030; }
    tbody td {
      padding: 10px 16px;
      text-align: center;
      border: 1px solid #30363d;
      color: #c9d1d9;
    }
    tbody td a { color: #D4A017; text-decoration: none; font-weight: 600; }
    tbody td code {
      background: #1a0a00;
      color: #D4A017;
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 12px;
      font-family: 'Fira Code', monospace;
      margin: 0 2px;
      border: 1px solid #B8860B40;
    }
    /* Stats cards */
    .stats-row {
      display: flex;
      gap: 16px;
      justify-content: center;
      flex-wrap: wrap;
      margin: 16px 0;
    }
    .stats-row img { border-radius: 8px; height: 180px; }
    .streak-row { text-align: center; margin: 16px 0; }
    .streak-row img { width: 70%; max-width: 600px; border-radius: 8px; }
    .trophy-row { text-align: center; margin: 16px 0; }
    .trophy-row img { width: 100%; border-radius: 8px; }
    .graph-row { text-align: center; margin: 16px 0; }
    .graph-row img { width: 100%; border-radius: 8px; }
    /* Goals */
    .goals-list { list-style: none; padding: 0; }
    .goals-list li {
      padding: 8px 0;
      font-size: 15px;
      color: #c9d1d9;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .checkbox {
      width: 16px;
      height: 16px;
      border: 2px solid #D4A017;
      border-radius: 3px;
      flex-shrink: 0;
    }
    .goals-list strong { color: #e6edf3; }
    /* Connect section */
    .connect-badges {
      display: flex;
      justify-content: center;
      gap: 12px;
      flex-wrap: wrap;
      margin: 16px 0;
    }
    .connect-badges img { height: 32px; border-radius: 6px; transition: transform 0.2s; }
    .connect-badges img:hover { transform: translateY(-3px); }
    .quote {
      text-align: center;
      color: #8b949e;
      font-style: italic;
      font-size: 15px;
      margin-top: 16px;
      padding: 12px;
      border-left: 3px solid #D4A017;
      background: #1a0a0030;
      border-radius: 0 8px 8px 0;
    }
    .quote::before { content: '💡 '; }
    /* Footer wave */
    .footer-wave { width: 100%; display: block; margin-top: 8px; }
    /* Loading spinner for images */
    img { max-width: 100%; }
    @media (max-width: 640px) {
      .readme-body { padding: 20px 16px; }
      .about-layout { flex-direction: column; }
      .about-right img { width: 100%; }
      .stats-row img { height: auto; width: 100%; }
      .streak-row img { width: 100%; }
    }
  </style>
</head>
<body>
<!-- GitHub top bar simulation -->
<div class="github-bar">
  <svg height="24" width="24" viewBox="0 0 16 16">
    <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
  </svg>
  <span><span class="repo-name">keyz-loop</span> / <span class="repo-name">keyz-loop</span></span>
  <span style="margin-left:auto; background:#21262d; border:1px solid #30363d; border-radius:6px; padding:4px 12px; font-size:12px; color:#c9d1d9;">📄 README.md</span>
</div>
<div class="container">
  <div class="readme-card">
    <div class="readme-header">
      📖 &nbsp; README.md &nbsp;·&nbsp; Preview Mode
    </div>
    <div class="readme-body">
      <!-- HEADER BANNER -->
      <div class="center">
        <div class="profile-banner">
          <img src="https://capsule-render.vercel.app/api?type=waving&color=0:8B4513,50:D4A017,100:B8860B&height=210&section=header&text=Himanshu%20Singh&fontSize=58&fontColor=ffffff&fontAlignY=38&desc=Full-Stack%20Developer%20%7C%20AI%20Builder%20%7C%20Node.js%20Enthusiast&descAlignY=60&descSize=18&animation=fadeIn" alt="Header Banner"/>
        </div>
        <img class="typing-img" src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=D4A017&center=true&vCenter=true&width=650&lines=Building+AI-Powered+Applications+%F0%9F%A4%96;Node.js+%26+JavaScript+Developer+%E2%9A%A1;Turning+Ideas+Into+Reality+%F0%9F%9A%80;Always+Learning%2C+Always+Growing+%F0%9F%8C%B1" alt="Typing SVG"/>
        <div class="badges">
          <img src="https://komarev.com/ghpvc/?username=keyz-loop&label=Profile+Views&color=D4A017&style=for-the-badge&labelColor=1a0a00" alt="Profile Views"/>
          <img src="https://img.shields.io/github/followers/keyz-loop?label=Followers&style=for-the-badge&color=B8860B&labelColor=1a0a00" alt="Followers"/>
          <img src="https://img.shields.io/badge/Open%20To%20Work-✅-D4A017?style=for-the-badge&labelColor=1a0a00" alt="Open To Work"/>
        </div>
      </div>
      <hr/>
      <!-- ABOUT ME -->
      <h2>🧑‍💻 About Me</h2>
      <div class="code-block">
        <span class="kw">const</span> <span class="var">himanshu</span> = {<br/>
        &nbsp;&nbsp;<span class="key">username:</span> &nbsp;&nbsp;<span class="str">"keyz-loop"</span>,<br/>
        &nbsp;&nbsp;<span class="key">location:</span> &nbsp;&nbsp;<span class="str">"India 🇮🇳"</span>,<br/>
        &nbsp;&nbsp;<span class="key">focus:</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[<span class="arr">"Full-Stack Dev"</span>, <span class="arr">"AI Apps"</span>, <span class="arr">"Node.js"</span>],<br/>
        &nbsp;&nbsp;<span class="key">learning:</span> &nbsp;&nbsp;[<span class="arr">"Advanced Node.js"</span>, <span class="arr">"LLMs & AI Integration"</span>, <span class="arr">"System Design"</span>],<br/>
        &nbsp;&nbsp;<span class="key">building:</span> &nbsp;&nbsp;<span class="str">"Gravity Pro Escrow — UPI-based Freelance Marketplace 💸"</span>,<br/>
        &nbsp;&nbsp;<span class="key">funFact:</span> &nbsp;&nbsp;&nbsp;<span class="str">"I debug with console.log and I'm proud of it 😄"</span>,<br/>
        &nbsp;&nbsp;<span class="key">available:</span> &nbsp;<span class="bool">true</span>,<br/>
        };
      </div>
      <div class="about-layout">
        <div class="about-left">
          <ul class="bullet-list">
            <li>🔭 Currently building <a href="https://github.com/keyz-loop/gravity-pro-escrow"><strong>Gravity Pro Escrow</strong></a> — a UPI-based escrow system for freelancers</li>
            <li>🌱 Leveling up in <strong>Node.js, Express, and AI app development</strong></li>
            <li>🤖 Passionate about integrating <strong>AI into real-world products</strong></li>
            <li>🎯 Goal: Launch my first SaaS product in 2025</li>
            <li>💬 Ask me about <strong>JavaScript, Node.js, HTML/CSS, or building apps from scratch</strong></li>
            <li>📫 Reach me at: <a href="https://www.linkedin.com/in/himanshusinghofficial"><strong>LinkedIn</strong></a> | <a href="https://github.com/keyz-loop"><strong>GitHub</strong></a></li>
            <li>⚡ Fun fact: I believe every complex system starts with a simple <code>console.log("hello")</code></li>
          </ul>
        </div>
        <div class="about-right">
          <img src="https://raw.githubusercontent.com/Adam-pw/Adam-pw/main/animation_500_kxa883sd.gif" alt="Coding GIF"/>
        </div>
      </div>
      <hr/>
      <!-- TECH STACK -->
      <div class="tech-section">
        <h2>🛠️ Tech Stack</h2>
        <div class="tech-label">Languages</div>
        <div class="badge-row">
          <img src="https://img.shields.io/badge/JavaScript-D4A017?style=for-the-badge&logo=javascript&logoColor=1a0a00" alt="JavaScript"/>
          <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/>
          <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/>
          <img src="https://img.shields.io/badge/Node.js-B8860B?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"/>
        </div>
        <div class="tech-label">Frameworks & Libraries</div>
        <div class="badge-row">
          <img src="https://img.shields.io/badge/Express.js-1a0a00?style=for-the-badge&logo=express&logoColor=D4A017" alt="Express.js"/>
          <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React"/>
          <img src="https://img.shields.io/badge/Next.js-1a0a00?style=for-the-badge&logo=nextdotjs&logoColor=D4A017" alt="Next.js"/>
        </div>
        <div class="tech-label">Tools & Platforms</div>
        <div class="badge-row">
          <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>
          <img src="https://img.shields.io/badge/GitHub-D4A017?style=for-the-badge&logo=github&logoColor=1a0a00" alt="GitHub"/>
          <img src="https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white" alt="VS Code"/>
          <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman"/>
          <img src="https://img.shields.io/badge/MongoDB-B8860B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB"/>
        </div>
        <div class="tech-label">AI & Emerging Tech</div>
        <div class="badge-row">
          <img src="https://img.shields.io/badge/OpenAI-D4A017?style=for-the-badge&logo=openai&logoColor=1a0a00" alt="OpenAI"/>
          <img src="https://img.shields.io/badge/Google%20Gemini-B8860B?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini"/>
        </div>
      </div>
      <hr/>
      <!-- PROJECTS -->
      <h2>🚀 Featured Projects</h2>
      <table>
        <thead>
          <tr>
            <th>🏆 Project</th>
            <th>📝 Description</th>
            <th>🔧 Tech</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><a href="https://github.com/keyz-loop/gravity-pro-escrow">⚖️ Gravity Pro Escrow</a></td>
            <td>UPI-based escrow system for freelancers & clients with milestone payments</td>
            <td><code>JavaScript</code> <code>Node.js</code> <code>UPI</code></td>
          </tr>
          <tr>
            <td><a href="https://github.com/keyz-loop/lowkey-campus">🏫 LowKey Campus</a></td>
            <td>Campus community platform for students</td>
            <td><code>JavaScript</code></td>
          </tr>
          <tr>
            <td><a href="https://github.com/keyz-loop/campuspulse">💓 CampusPulse</a></td>
            <td>Student activity & pulse tracker</td>
            <td><code>Node.js</code></td>
          </tr>
          <tr>
            <td><a href="https://github.com/keyz-loop/code-with-himanshu">🎓 Code With Himanshu</a></td>
            <td>Personal coding tutorials & projects</td>
            <td><code>HTML</code></td>
          </tr>
          <tr>
            <td><a href="https://github.com/keyz-loop/nodejs-learning">📚 Node.js Learning</a></td>
            <td>Node.js concepts, exercises & experiments</td>
            <td><code>JavaScript</code></td>
          </tr>
        </tbody>
      </table>
      <hr/>
      <!-- GITHUB STATS -->
      <h2>📊 GitHub Stats</h2>
      <div class="stats-row">
        <img src="https://github-readme-stats.vercel.app/api?username=keyz-loop&show_icons=true&theme=gruvbox&include_all_commits=true&count_private=true&hide_border=true&bg_color=1a0a00&title_color=D4A017&icon_color=B8860B&text_color=ffffff" alt="GitHub Stats"/>
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=keyz-loop&layout=compact&theme=gruvbox&hide_border=true&bg_color=1a0a00&title_color=D4A017&text_color=ffffff" alt="Top Languages"/>
      </div>
      <div class="streak-row">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=keyz-loop&theme=dark&hide_border=true&background=1a0a00&stroke=D4A017&ring=B8860B&fire=D4A017&currStreakLabel=D4A017&sideLabels=D4A017&dates=ffffff" alt="Streak Stats"/>
      </div>
      <hr/>
      <!-- TROPHIES -->
      <h2>🏆 GitHub Trophies</h2>
      <div class="trophy-row">
        <img src="https://github-profile-trophy.vercel.app/?username=keyz-loop&theme=gruvbox&no-frame=true&no-bg=true&margin-w=8&column=6" alt="Trophies"/>
      </div>
      <hr/>
      <!-- CONTRIBUTION GRAPH -->
      <h2>📈 Contribution Graph</h2>
      <div class="graph-row">
        <img src="https://github-readme-activity-graph.vercel.app/graph?username=keyz-loop&bg_color=1a0a00&color=D4A017&line=B8860B&point=ffffff&area=true&hide_border=true" alt="Contribution Graph"/>
      </div>
      <hr/>
      <!-- GOALS -->
      <h2>🎯 Current Goals for 2025</h2>
      <ul class="goals-list">
        <li><span class="checkbox"></span> 🚀 Launch <strong>Gravity Pro Escrow</strong> as a live product</li>
        <li><span class="checkbox"></span> 🤖 Build and ship <strong>2+ AI-integrated web apps</strong></li>
        <li><span class="checkbox"></span> 📦 Publish my first <strong>npm package</strong></li>
        <li><span class="checkbox"></span> 🌐 Reach <strong>100+ GitHub followers</strong></li>
        <li><span class="checkbox"></span> 📝 Start a <strong>dev blog</strong> sharing my learning journey</li>
        <li><span class="checkbox"></span> 🏗️ Master <strong>System Design fundamentals</strong></li>
      </ul>
      <hr/>
      <!-- CONNECT -->
      <h2>🤝 Connect With Me</h2>
      <div class="connect-badges">
        <a href="https://github.com/keyz-loop">
          <img src="https://img.shields.io/badge/GitHub-keyz--loop-1a0a00?style=for-the-badge&logo=github&logoColor=D4A017" alt="GitHub"/>
        </a>
        <a href="https://www.linkedin.com/in/himanshusinghofficial">
          <img src="https://img.shields.io/badge/LinkedIn-Himanshu%20Singh-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
        </a>
      </div>
      <div class="quote">
        "Code is like poetry — every line tells a story."
      </div>
      <!-- FOOTER WAVE -->
      <img class="footer-wave" src="https://capsule-render.vercel.app/api?type=waving&color=0:B8860B,100:8B4513&height=120&section=footer" alt="Footer"/>
    </div>
  </div>
</div>
</body>
</html>
