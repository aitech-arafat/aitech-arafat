<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>rahul-jha98 (Rahul Jha) · GitHub</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif; font-size: 14px; background: #ffffff; color: #1f2328; line-height: 1.5; }

  /* TOPBAR */
  .topbar { background: #24292f; display: flex; align-items: center; padding: 0 16px; height: 48px; gap: 16px; }
  .topbar-logo { color: #fff; font-size: 24px; }
  .topbar-logo svg { fill: white; width: 32px; height: 32px; }
  .topbar-user { color: #e6edf3; font-size: 14px; font-weight: 600; }
  .topbar-search { background: #2d333b; border: 1px solid #444c56; border-radius: 6px; padding: 4px 12px; color: #8b949e; font-size: 14px; width: 260px; display: flex; align-items: center; gap: 8px; }
  .topbar-search span { font-size: 12px; }
  .topbar-right { margin-left: auto; display: flex; align-items: center; gap: 12px; }
  .topbar-icon { color: #e6edf3; font-size: 20px; cursor: pointer; }
  .avatar-sm { width: 32px; height: 32px; border-radius: 50%; overflow: hidden; }
  .avatar-sm img { width: 100%; height: 100%; object-fit: cover; }

  /* NAV TABS */
  .subnav { background: #fff; border-bottom: 1px solid #d0d7de; padding: 0 16px; display: flex; align-items: center; gap: 0; }
  .subnav a { display: flex; align-items: center; gap: 6px; padding: 12px 16px; font-size: 14px; font-weight: 600; color: #1f2328; text-decoration: none; border-bottom: 2px solid transparent; white-space: nowrap; }
  .subnav a.active { border-bottom-color: #fd8c73; color: #1f2328; }
  .subnav a:hover { color: #1f2328; }
  .subnav .count { background: #afb8c133; border-radius: 20px; padding: 2px 8px; font-size: 12px; font-weight: 500; color: #1f2328; }

  /* MAIN LAYOUT */
  .main { max-width: 1280px; margin: 0 auto; padding: 24px 16px; display: grid; grid-template-columns: 296px 1fr; gap: 24px; align-items: start; }

  /* SIDEBAR */
  .sidebar {}
  .avatar-lg { width: 260px; height: 260px; border-radius: 50%; overflow: hidden; border: 1px solid #d0d7de; margin-bottom: 16px; }
  .avatar-lg img { width: 100%; height: 100%; object-fit: cover; }
  .profile-name { font-size: 20px; font-weight: 600; line-height: 1.25; margin-bottom: 4px; }
  .profile-username { font-size: 20px; font-weight: 300; color: #57606a; margin-bottom: 16px; }
  .btn-follow { width: 100%; padding: 5px 16px; background: #f6f8fa; border: 1px solid rgba(31,35,40,.15); border-radius: 6px; font-size: 14px; font-weight: 500; cursor: pointer; color: #24292f; margin-bottom: 16px; }
  .btn-follow:hover { background: #eef1f4; }
  .followers { font-size: 14px; color: #1f2328; margin-bottom: 16px; display: flex; gap: 8px; }
  .followers span { font-weight: 600; }
  .followers a { color: #57606a; text-decoration: none; }
  .followers a:hover { color: #0969da; }
  .profile-meta { list-style: none; margin-bottom: 16px; }
  .profile-meta li { display: flex; align-items: center; gap: 8px; padding: 4px 0; font-size: 14px; color: #57606a; }
  .profile-meta li svg { fill: #57606a; width: 16px; height: 16px; flex-shrink: 0; }
  .profile-meta li a { color: #0969da; text-decoration: none; }
  .profile-meta li a:hover { text-decoration: underline; }

  /* ACHIEVEMENTS */
  .achievements-title { font-size: 14px; font-weight: 600; color: #1f2328; margin-bottom: 8px; }
  .achievements-grid { display: flex; flex-wrap: wrap; gap: 6px; }
  .achievement-badge { position: relative; width: 42px; height: 42px; border-radius: 50%; overflow: hidden; border: 1px solid #d0d7de; }
  .achievement-badge img { width: 100%; height: 100%; object-fit: cover; }
  .achievement-badge .badge-count { position: absolute; bottom: 0; right: -2px; background: #fff; border: 1px solid #d0d7de; border-radius: 10px; font-size: 10px; font-weight: 600; padding: 0px 3px; color: #57606a; }

  /* RIGHT CONTENT */
  .content {}

  /* README CARD */
  .readme-card { border: 1px solid #d0d7de; border-radius: 6px; margin-bottom: 24px; overflow: hidden; }
  .readme-header { background: #f6f8fa; border-bottom: 1px solid #d0d7de; padding: 8px 16px; font-size: 12px; color: #57606a; }
  .readme-header a { color: #57606a; text-decoration: none; }
  .readme-header a:hover { color: #0969da; }
  .readme-body { padding: 24px 32px; }

  .readme-body h1 { font-size: 24px; font-weight: 600; border-bottom: 1px solid #d0d7de; padding-bottom: 8px; margin-bottom: 16px; }
  .readme-body h3 { font-size: 18px; font-weight: 600; margin: 24px 0 12px; }
  .readme-body p { margin-bottom: 16px; line-height: 1.6; }
  .readme-body ul { padding-left: 24px; margin-bottom: 16px; }
  .readme-body ul li { padding: 3px 0; line-height: 1.6; }
  .readme-body a { color: #0969da; text-decoration: none; }
  .readme-body a:hover { text-decoration: underline; }

  /* Social badges */
  .social-badges { display: flex; gap: 6px; margin-bottom: 16px; }
  .social-badges img { height: 28px; }

  /* About me section layout */
  .about-layout { display: grid; grid-template-columns: 1fr 260px; gap: 16px; }
  .about-layout ul { padding-left: 0; list-style: none; }
  .about-layout ul li { padding: 4px 0; display: flex; align-items: flex-start; gap: 6px; }
  .about-layout ul li::before { content: "•"; color: #57606a; flex-shrink: 0; margin-top: 1px; }

  /* Illustration image */
  .illustration { width: 100%; border-radius: 6px; }

  /* Tools icons */
  .tools-row { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 8px; }
  .tools-row a img { width: 38px; height: 38px; }

  /* GitHub Stats */
  .stats-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 8px; }
  .stats-card { border: 1px solid #d0d7de; border-radius: 6px; padding: 16px; }
  .stats-card-title { font-size: 14px; font-weight: 600; color: #0969da; margin-bottom: 12px; }
  .stats-row { display: flex; justify-content: space-between; padding: 4px 0; font-size: 13px; color: #57606a; border-bottom: 1px solid #f0f0f0; }
  .stats-row:last-child { border-bottom: none; }
  .stats-row span:last-child { font-weight: 600; color: #1f2328; }

  .langs-card { border: 1px solid #d0d7de; border-radius: 6px; padding: 16px; }
  .langs-title { font-size: 14px; font-weight: 600; color: #0969da; margin-bottom: 12px; }
  .lang-bar { height: 8px; border-radius: 4px; display: flex; overflow: hidden; margin-bottom: 12px; }
  .lang-dot { display: flex; align-items: center; gap: 6px; font-size: 12px; color: #57606a; padding: 2px 0; }
  .lang-dot-color { width: 10px; height: 10px; border-radius: 50%; }
  .langs-list { display: flex; flex-wrap: wrap; gap: 8px 16px; }

  /* Projects */
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .project-card { border: 1px solid #d0d7de; border-radius: 8px; padding: 16px; transition: box-shadow .2s; cursor: pointer; }
  .project-card:hover { box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
  .project-name { font-size: 16px; font-weight: 700; color: #0969da; margin-bottom: 4px; }
  .project-name.artistify { color: #4b6ce1; }
  .project-name.sheets { color: #2da44e; }
  .project-name.readme { color: #1f2328; }
  .project-name.password { color: #e04040; }
  .project-name.oxy { color: #e05c2a; }
  .project-name.wavelength { color: #c27c2c; }

  /* PINNED */
  .section-title { font-size: 16px; font-weight: 600; margin-bottom: 12px; color: #1f2328; }
  .pinned-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 24px; }
  .pinned-card { border: 1px solid #d0d7de; border-radius: 6px; padding: 16px; }
  .pinned-card-header { display: flex; align-items: center; gap: 6px; margin-bottom: 6px; }
  .pinned-card-header svg { fill: #57606a; width: 16px; height: 16px; }
  .pinned-card-name { font-size: 14px; font-weight: 600; color: #0969da; }
  .pinned-card-badge { font-size: 12px; color: #57606a; border: 1px solid #d0d7de; border-radius: 20px; padding: 2px 8px; }
  .pinned-card-desc { font-size: 13px; color: #57606a; margin-bottom: 12px; line-height: 1.5; }
  .pinned-card-meta { display: flex; align-items: center; gap: 12px; font-size: 12px; color: #57606a; }
  .lang-dot-small { width: 12px; height: 12px; border-radius: 50%; display: inline-block; }
  .star-count { display: flex; align-items: center; gap: 3px; }

  /* CONTRIBUTION */
  .contrib-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; }
  .contrib-title { font-size: 14px; color: #1f2328; font-weight: 400; }
  .contrib-year { background: #0969da; color: white; font-size: 12px; padding: 4px 12px; border-radius: 6px; font-weight: 500; }
  .contrib-graph { border: 1px solid #d0d7de; border-radius: 6px; padding: 16px; margin-bottom: 4px; }
  .contrib-graph-inner { overflow-x: auto; }
  .contrib-grid { display: flex; gap: 3px; }
  .contrib-col { display: flex; flex-direction: column; gap: 3px; }
  .contrib-cell { width: 10px; height: 10px; border-radius: 2px; background: #ebedf0; }
  .contrib-cell.l1 { background: #9be9a8; }
  .contrib-cell.l2 { background: #40c463; }
  .contrib-cell.l3 { background: #30a14e; }
  .contrib-cell.l4 { background: #216e39; }

  .year-list { display: flex; flex-direction: column; gap: 4px; }
  .year-item { font-size: 13px; color: #0969da; cursor: pointer; text-align: right; }
  .year-item.active { font-weight: 600; color: #1f2328; }

  .contrib-layout { display: grid; grid-template-columns: 1fr auto; gap: 16px; align-items: start; }

  /* FOOTER */
  footer { background: #f6f8fa; border-top: 1px solid #d0d7de; padding: 40px 16px 20px; margin-top: 40px; }
  .footer-inner { max-width: 1280px; margin: 0 auto; display: flex; align-items: center; gap: 24px; flex-wrap: wrap; font-size: 12px; color: #57606a; }
  .footer-inner svg { fill: #57606a; width: 24px; height: 24px; }
  .footer-links { display: flex; flex-wrap: wrap; gap: 16px; }
  .footer-links a { color: #57606a; text-decoration: none; }
  .footer-links a:hover { color: #0969da; }

  /* Contrib activity */
  .activity-section { margin-top: 16px; }
  .activity-month { font-size: 14px; font-weight: 600; margin-bottom: 8px; color: #1f2328; }
  .activity-empty { font-size: 13px; color: #57606a; border: 1px solid #d0d7de; border-radius: 6px; padding: 12px 16px; }

  .emoji { font-style: normal; }
</style>
</head>
<body>

<!-- TOP NAV -->
<nav class="topbar">
  <div class="topbar-logo">
    <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
  </div>
  <div class="topbar-user" style="color:#e6edf3">rahul-jha98</div>
  <div class="topbar-search">
    <span>🔍</span><span style="color:#8b949e">Type / to search</span>
  </div>
  <div class="topbar-right">
    <span class="topbar-icon">⊞</span>
    <span class="topbar-icon">+</span>
    <div class="avatar-sm"><img src="https://avatars.githubusercontent.com/u/29267275?v=4" alt="avatar"></div>
  </div>
</nav>

<!-- SUB NAV -->
<div class="subnav">
  <a href="#" class="active">Overview</a>
  <a href="#">Repositories <span class="count">38</span></a>
  <a href="#">Projects</a>
  <a href="#">Packages</a>
  <a href="#">Stars <span class="count">24</span></a>
</div>

<!-- MAIN -->
<div class="main">

  <!-- SIDEBAR -->
  <aside class="sidebar">
    <div class="avatar-lg">
      <img src="https://avatars.githubusercontent.com/u/29267275?v=4" alt="Rahul Jha">
    </div>
    <div class="profile-name">Rahul Jha</div>
    <div class="profile-username">rahul-jha98</div>
    <button class="btn-follow">Follow</button>
    <div class="followers">
      <span>173</span><a href="#">followers</a>
      <span style="color:#57606a">·</span>
      <span>4</span><a href="#">following</a>
    </div>
    <ul class="profile-meta">
      <li>
        <svg viewBox="0 0 16 16"><path d="M10.5 5a2.5 2.5 0 1 1-5 0 2.5 2.5 0 0 1 5 0zm.061 3.073a4 4 0 1 0-5.123 0 6.004 6.004 0 0 0-3.431 5.142.75.75 0 0 0 1.498.07 4.5 4.5 0 0 1 8.99 0 .75.75 0 1 0 1.498-.07 6.005 6.005 0 0 0-3.432-5.142z"/></svg>
        <a href="#">@atlassian</a>
      </li>
      <li>
        <svg viewBox="0 0 16 16"><path d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10zm0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6z"/></svg>
        Kalyan, Maharashtra
      </li>
      <li>
        <svg viewBox="0 0 16 16"><path d="M1.75 2h12.5c.966 0 1.75.784 1.75 1.75v8.5A1.75 1.75 0 0 1 14.25 14H1.75A1.75 1.75 0 0 1 0 12.25v-8.5C0 2.784.784 2 1.75 2zM1.5 12.251c0 .138.112.25.25.25h12.5a.25.25 0 0 0 .25-.25V5.809L8.38 8.966a.75.75 0 0 1-.76 0L1.5 5.809v6.442zm13-8.181v-.32a.25.25 0 0 0-.25-.25H1.75a.25.25 0 0 0-.25.25v.32L8 7.88z"/></svg>
        jharahul1998@gmail.com
      </li>
      <li>
        <svg viewBox="0 0 24 24" style="fill:none;stroke:#57606a;stroke-width:2"><path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"/></svg>
        <a href="https://twitter.com/jharahul98">@jharahul98</a>
      </li>
      <li>
        <svg viewBox="0 0 24 24" style="fill:#57606a"><path d="M20.5 2h-17A1.5 1.5 0 002 3.5v17A1.5 1.5 0 003.5 22h17a1.5 1.5 0 001.5-1.5v-17A1.5 1.5 0 0020.5 2zM8 19H5v-9h3zM6.5 8.25A1.75 1.75 0 118.3 6.5a1.78 1.78 0 01-1.8 1.75zM19 19h-3v-4.74c0-1.42-.6-1.93-1.38-1.93A1.74 1.74 0 0013 14.19a.66.66 0 000 .14V19h-3v-9h2.9v1.3a3.11 3.11 0 012.7-1.4c1.55 0 3.36.86 3.36 3.66z"/></svg>
        <a href="https://www.linkedin.com/in/rahul-jha-84a204178/">in/rahul-jha-84a204178</a>
      </li>
    </ul>

    <div class="achievements-title">Achievements</div>
    <div class="achievements-grid">
      <div class="achievement-badge">
        <img src="https://github.githubassets.com/assets/pair-extraordinaire-default-579438a20e01.png" alt="Pair Extraordinaire">
      </div>
      <div class="achievement-badge">
        <img src="https://github.githubassets.com/assets/starstruck-default-b6610abad518.png" alt="Starstruck">
        <span class="badge-count">x2</span>
      </div>
      <div class="achievement-badge">
        <img src="https://github.githubassets.com/assets/arctic-code-vault-contributor-default-df8d74122a06.png" alt="Arctic Code Vault">
      </div>
      <div class="achievement-badge">
        <img src="https://github.githubassets.com/assets/pull-shark-default-498c279a747d.png" alt="Pull Shark">
        <span class="badge-count">x2</span>
      </div>
    </div>
  </aside>

  <!-- MAIN CONTENT -->
  <main class="content">

    <!-- README CARD -->
    <div class="readme-card">
      <div class="readme-header">
        <a href="#">rahul-jha98</a> / <strong>README.md</strong>
      </div>
      <div class="readme-body">
        <h1>Hey 👋, I'm Rahul Jha!</h1>

        <div class="social-badges">
          <a href="https://www.linkedin.com/in/rahul-jha98/" target="_blank">
            <img src="https://raw.githubusercontent.com/rahul-jha98/rahul-jha98/561d474902b59c7429ec22bb73e225696c27b202/assets/linkedin.svg" alt="LinkedIn">
          </a>
          <a href="https://twitter.com/jharahul98/" target="_blank">
            <img src="https://raw.githubusercontent.com/rahul-jha98/rahul-jha98/561d474902b59c7429ec22bb73e225696c27b202/assets/twitter.svg" alt="Twitter">
          </a>
          <a href="https://www.kaggle.com/rahuljha98/" target="_blank">
            <img src="https://raw.githubusercontent.com/rahul-jha98/rahul-jha98/561d474902b59c7429ec22bb73e225696c27b202/assets/kaggle.svg" alt="Kaggle">
          </a>
        </div>

        <p>I am a versatilist and easily adapt to different hats (Full Stack Web Developer 🌐, App Developer 📱, ML Engineer 🤖 or beginner level Designer 🎨) depending on what the project requires. I love exploring new tech stack 💻 and leveraging them to build cool stuffs 🛠️.</p>

        <h3>🧐 More About Me:</h3>
        <div class="about-layout">
          <ul>
            <li>🔭 I'm currently working on <strong>youtube-audio-player</strong></li>
            <li>🤝 I'm looking to collaborate on <a href="https://github.com/rahul-jha98/sheets-database">sheets-database</a></li>
            <li>🌱 I'm currently learning Typescript;</li>
            <li>👨🏻‍💻 Most of my projects are available on <a href="https://github.com/rahul-jha98?tab=repositories">Github</a></li>
            <li>🎨 Using <a href="https://storyset.com/illustration/javascript-frameworks/amico">this svg</a> and Figma I made 👉</li>
            <li>💬 Ask me about anything tech related, I am happy to help;</li>
            <li>📫 Feel free to ping me on <a href="https://www.linkedin.com/in/rahul-jha98/">LinkedIn</a></li>
            <li>📝 Checkout my <a href="#">resume</a></li>
            <li>📚 When I am free, I read fantasy and fiction novels. Checkout my <a href="#">Goodreads</a> to see the book I have read</li>
          </ul>
          <img class="illustration" src="https://storyset.com/image/javascript-frameworks/amico" 
            onerror="this.src='https://cdn.dribbble.com/users/1162077/screenshots/3848914/programmer.gif'; this.onerror=null;"
            alt="illustration" style="border-radius:8px; max-height:200px; object-fit:contain; background:#f6f8fa; border:1px solid #e1e4e8; padding:8px;">
        </div>

        <h3>🔨 Languages and Tools:</h3>
        <div class="tools-row">
          <a href="https://pytorch.org/" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/pytorch/pytorch.svg" alt="pytorch" width="38" height="38"></a>
          <a href="https://www.tensorflow.org" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/tensorflow/tensorflow.svg" alt="tensorflow" width="38" height="38"></a>
          <a href="https://www.python.org" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/python/python.svg" alt="python" width="38" height="38"></a>
          <a href="https://developer.android.com" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/android/android.svg" alt="android" width="38" height="38"></a>
          <a href="https://kotlinlang.org" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/kotlin/kotlin.svg" alt="kotlin" width="38" height="38"></a>
          <a href="https://www.java.com" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/java/java.svg" alt="java" width="38" height="38"></a>
          <a href="https://firebase.google.com/" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/firebase/firebase.svg" alt="firebase" width="38" height="38"></a>
          <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/javascript/javascript.svg" alt="javascript" width="38" height="38"></a>
          <a href="https://www.typescriptlang.org/" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/typescript/typescript.svg" alt="typescript" width="38" height="38"></a>
          <a href="https://reactjs.org/" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/react/react.svg" alt="react" width="38" height="38"></a>
          <a href="https://nodejs.org" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/node/node.svg" alt="nodejs" width="38" height="38"></a>
          <a href="https://git-scm.com/" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/git-scm/git-scm.svg" alt="git" width="38" height="38"></a>
          <a href="https://www.figma.com/" target="_blank"><img src="https://raw.githubusercontent.com/rahul-jha98/github_readme_icons/main/language_and_tools/square/figma/figma.svg" alt="figma" width="38" height="38"></a>
        </div>

        <h3>📊 Github Stats</h3>
        <div class="stats-grid">
          <div class="stats-card">
            <div class="stats-card-title">Rahul Jha's GitHub Statistics</div>
            <div class="stats-row"><span>⭐ Stars</span><span>833</span></div>
            <div class="stats-row"><span>🍴 Forks</span><span>1,412</span></div>
            <div class="stats-row"><span>📊 All-time contributions</span><span>879</span></div>
            <div class="stats-row"><span>📝 Lines of code changed</span><span>964,654</span></div>
            <div class="stats-row"><span>👁️ Repository views (past two weeks)</span><span>476</span></div>
            <div class="stats-row"><span>📁 Repositories with contributions</span><span>52</span></div>
          </div>
          <div class="langs-card">
            <div class="langs-title">Most Used Languages</div>
            <div class="lang-bar">
              <div style="width:30.15%;background:#f1e05a"></div>
              <div style="width:27.72%;background:#f1e05a;filter:hue-rotate(10deg)"></div>
              <div style="width:19.86%;background:#e34c26"></div>
              <div style="width:9.44%;background:#563d7c"></div>
              <div style="width:7.43%;background:#2b7489"></div>
              <div style="width:3.11%;background:#A97BFF"></div>
              <div style="flex:1;background:#3572A5"></div>
            </div>
            <div class="langs-list">
              <div class="lang-dot"><div class="lang-dot-color" style="background:#f1e05a"></div>Jupyter Notebook 30.15%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#f7df1e"></div>JavaScript 27.72%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#e34c26"></div>HTML 19.86%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#563d7c"></div>CSS 9.44%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#2b7489"></div>TypeScript 7.43%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#A97BFF"></div>Kotlin 3.11%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#3572A5"></div>Python 1.75%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#b07219"></div>Java 0.32%</div>
              <div class="lang-dot"><div class="lang-dot-color" style="background:#4fc08d"></div>Vue 0.20%</div>
            </div>
          </div>
        </div>

        <h3>🛠️ My Projects</h3>
        <div class="projects-grid">
          <a href="https://rahul-jha98.github.io/Artistify.ai/" target="_blank" style="text-decoration:none;">
            <img src="https://github.com/rahul-jha98/rahul-jha98/raw/main/projects/artistify.svg" alt="Artistify" style="width:100%;height:60px;object-fit:contain;" onerror="this.style.display='none';this.nextElementSibling.style.display='flex'">
            <div style="display:none;align-items:center;gap:10px;padding:12px 16px;border:1px solid #d0d7de;border-radius:8px;font-size:18px;font-weight:700;color:#4b6ce1;">🎨 <span style="color:#4b6ce1">Artistify</span><span style="color:#1f2328">.ai</span></div>
          </a>
          <a href="https://rahul-jha98.github.io/sheets-database/" target="_blank" style="text-decoration:none;">
            <img src="https://github.com/rahul-jha98/rahul-jha98/raw/main/projects/sheetsdatabase.svg" alt="Sheets Database" style="width:100%;height:60px;object-fit:contain;" onerror="this.style.display='none';this.nextElementSibling.style.display='flex'">
            <div style="display:none;align-items:center;gap:10px;padding:12px 16px;border:1px solid #d0d7de;border-radius:8px;font-size:18px;font-weight:700;"><span style="color:#2da44e">sheets</span>-database</div>
          </a>
          <a href="https://github.com/rahul-jha98/README_icons" target="_blank" style="text-decoration:none;">
            <img src="https://github.com/rahul-jha98/rahul-jha98/raw/main/projects/readmeicons.svg" alt="README Icons" style="width:100%;height:60px;object-fit:contain;" onerror="this.style.display='none';this.nextElementSibling.style.display='flex'">
            <div style="display:none;align-items:center;gap:10px;padding:12px 16px;border:1px solid #d0d7de;border-radius:8px;font-size:18px;font-weight:700;">README Icons</div>
          </a>
          <a href="https://thepasswordkeeper.netlify.app/" target="_blank" style="text-decoration:none;">
            <img src="https://github.com/rahul-jha98/rahul-jha98/raw/main/projects/passwordkeeper.svg" alt="Password Keeper" style="width:100%;height:60px;object-fit:contain;" onerror="this.style.display='none';this.nextElementSibling.style.display='flex'">
            <div style="display:none;align-items:center;gap:10px;padding:12px 16px;border:1px solid #d0d7de;border-radius:8px;font-size:18px;font-weight:700;"><span style="color:#e04040">Password</span> Keeper</div>
          </a>
          <a href="#" target="_blank" style="text-decoration:none;">
            <img src="https://github.com/rahul-jha98/rahul-jha98/raw/main/projects/oxytracker.svg" alt="OxyTracker" style="width:100%;height:60px;object-fit:contain;" onerror="this.style.display='none';this.nextElementSibling.style.display='flex'">
            <div style="display:none;align-items:center;gap:10px;padding:12px 16px;border:1px solid #d0d7de;border-radius:8px;font-size:18px;font-weight:700;color:#e05c2a;">🔴 OxyTracker</div>
          </a>
          <a href="https://wavelengths.netlify.app/" target="_blank" style="text-decoration:none;">
            <img src="https://github.com/rahul-jha98/rahul-jha98/raw/main/projects/wavelength.svg" alt="Wavelength" style="width:100%;height:60px;object-fit:contain;" onerror="this.style.display='none';this.nextElementSibling.style.display='flex'">
            <div style="display:none;align-items:center;gap:10px;padding:12px 16px;border:1px solid #d0d7de;border-radius:8px;font-size:18px;font-weight:700;color:#c27c2c;">〰️ WAVELENGTH</div>
          </a>
        </div>
      </div>
    </div>

    <!-- PINNED -->
    <div class="section-title">Pinned</div>
    <div class="pinned-grid">
      <div class="pinned-card">
        <div class="pinned-card-header">
          <svg viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9zm10.5-1V9h-8c-.356 0-.694.074-1 .208V2.5a1 1 0 011-1h8zM5 12.25v3.25a.25.25 0 00.4.2l1.45-1.087a.25.25 0 01.3 0L8.6 15.7a.25.25 0 00.4-.2v-3.25a.25.25 0 00-.25-.25h-3.5a.25.25 0 00-.25.25z"/></svg>
          <span class="pinned-card-name">Artistify.ai</span>
          <span class="pinned-card-badge">Public</span>
        </div>
        <div class="pinned-card-desc">Web-app to generate artistically styled images generated using Style Transfer Model running in the browser.</div>
        <div class="pinned-card-meta">
          <span><span class="lang-dot-small" style="background:#f7df1e"></span> JavaScript</span>
          <span class="star-count">⭐ 55</span>
          <span>🍴 13</span>
        </div>
      </div>
      <div class="pinned-card">
        <div class="pinned-card-header">
          <svg viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9zm10.5-1V9h-8c-.356 0-.694.074-1 .208V2.5a1 1 0 011-1h8zM5 12.25v3.25a.25.25 0 00.4.2l1.45-1.087a.25.25 0 01.3 0L8.6 15.7a.25.25 0 00.4-.2v-3.25a.25.25 0 00-.25-.25h-3.5a.25.25 0 00-.25.25z"/></svg>
          <span class="pinned-card-name">PasswordKeeper</span>
          <span class="pinned-card-badge">Public</span>
        </div>
        <div class="pinned-card-desc">Web-app to help you securely store your encrypted passwords in your Google Drive.</div>
        <div class="pinned-card-meta">
          <span><span class="lang-dot-small" style="background:#f7df1e"></span> JavaScript</span>
          <span class="star-count">⭐ 55</span>
          <span>🍴 5</span>
        </div>
      </div>
      <div class="pinned-card">
        <div class="pinned-card-header">
          <svg viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9zm10.5-1V9h-8c-.356 0-.694.074-1 .208V2.5a1 1 0 011-1h8zM5 12.25v3.25a.25.25 0 00.4.2l1.45-1.087a.25.25 0 01.3 0L8.6 15.7a.25.25 0 00.4-.2v-3.25a.25.25 0 00-.25-.25h-3.5a.25.25 0 00-.25.25z"/></svg>
          <span class="pinned-card-name">sheets-database</span>
          <span class="pinned-card-badge">Public</span>
        </div>
        <div class="pinned-card-desc">Library to help use a Google Sheet as a database</div>
        <div class="pinned-card-meta">
          <span><span class="lang-dot-small" style="background:#2b7489"></span> TypeScript</span>
          <span class="star-count">⭐ 76</span>
          <span>🍴 6</span>
        </div>
      </div>
      <div class="pinned-card">
        <div class="pinned-card-header">
          <svg viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9zm10.5-1V9h-8c-.356 0-.694.074-1 .208V2.5a1 1 0 011-1h8zM5 12.25v3.25a.25.25 0 00.4.2l1.45-1.087a.25.25 0 01.3 0L8.6 15.7a.25.25 0 00.4-.2v-3.25a.25.25 0 00-.25-.25h-3.5a.25.25 0 00-.25.25z"/></svg>
          <span class="pinned-card-name">JustJoking.ai</span>
          <span class="pinned-card-badge">Public</span>
        </div>
        <div class="pinned-card-desc">Using a Transformer for learning the Language Model and Generate Short Jokes</div>
        <div class="pinned-card-meta">
          <span><span class="lang-dot-small" style="background:#f1e05a"></span> Jupyter Notebook</span>
          <span class="star-count">⭐ 13</span>
          <span>🍴 2</span>
        </div>
      </div>
      <div class="pinned-card">
        <div class="pinned-card-header">
          <svg viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9zm10.5-1V9h-8c-.356 0-.694.074-1 .208V2.5a1 1 0 011-1h8zM5 12.25v3.25a.25.25 0 00.4.2l1.45-1.087a.25.25 0 01.3 0L8.6 15.7a.25.25 0 00.4-.2v-3.25a.25.25 0 00-.25-.25h-3.5a.25.25 0 00-.25.25z"/></svg>
          <span class="pinned-card-name">RestaurantTrends.stats</span>
          <span class="pinned-card-badge">Public</span>
        </div>
        <div class="pinned-card-desc">Visualise the trends in food and restaurant choices of customers in a city by scraping data from Zomato.</div>
        <div class="pinned-card-meta">
          <span><span class="lang-dot-small" style="background:#4fc08d"></span> Vue</span>
          <span class="star-count">⭐ 5</span>
          <span>🍴 1</span>
        </div>
      </div>
      <div class="pinned-card">
        <div class="pinned-card-header">
          <svg viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 014.5 0h8.75a.75.75 0 01.75.75v12.5a.75.75 0 01-.75.75h-2.5a.75.75 0 110-1.5h1.75v-2h-8a1 1 0 00-.714 1.7.75.75 0 01-1.072 1.05A2.495 2.495 0 012 11.5v-9zm10.5-1V9h-8c-.356 0-.694.074-1 .208V2.5a1 1 0 011-1h8zM5 12.25v3.25a.25.25 0 00.4.2l1.45-1.087a.25.25 0 01.3 0L8.6 15.7a.25.25 0 00.4-.2v-3.25a.25.25 0 00-.25-.25h-3.5a.25.25 0 00-.25.25z"/></svg>
          <span class="pinned-card-name">Hope</span>
          <span class="pinned-card-badge">Public</span>
        </div>
        <div class="pinned-card-desc">The android app hosts chat rooms that facilitate group therapy sessions for people suffering from depression moderated by a chatbot.</div>
        <div class="pinned-card-meta">
          <span><span class="lang-dot-small" style="background:#A97BFF"></span> Kotlin</span>
          <span class="star-count">⭐ 4</span>
          <span>🍴 1</span>
        </div>
      </div>
    </div>

    <!-- CONTRIBUTIONS -->
    <div class="contrib-layout">
      <div>
        <div class="contrib-header">
          <span class="contrib-title">0 contributions in the last year</span>
          <span class="contrib-year">2026</span>
        </div>
        <div class="contrib-graph">
          <div id="contrib-grid"></div>
          <div style="display:flex;justify-content:space-between;margin-top:8px;font-size:11px;color:#57606a;">
            <span>Aug</span><span>Sep</span><span>Oct</span><span>Nov</span><span>Dec</span><span>Jan</span><span>Feb</span><span>Mar</span><span>Apr</span><span>May</span><span>Jun</span><span>Jul</span>
          </div>
          <div style="display:flex;align-items:center;gap:6px;margin-top:12px;font-size:11px;color:#57606a;">
            <span>Learn how we count contributions</span>
            <span style="margin-left:auto">Less</span>
            <div style="width:10px;height:10px;background:#ebedf0;border-radius:2px"></div>
            <div style="width:10px;height:10px;background:#9be9a8;border-radius:2px"></div>
            <div style="width:10px;height:10px;background:#40c463;border-radius:2px"></div>
            <div style="width:10px;height:10px;background:#30a14e;border-radius:2px"></div>
            <div style="width:10px;height:10px;background:#216e39;border-radius:2px"></div>
            <span>More</span>
          </div>
        </div>
        <div class="activity-section">
          <div class="activity-month">Contribution activity</div>
          <div style="font-size:14px;font-weight:600;margin-bottom:8px;">August 2026</div>
          <div class="activity-empty">rahul-jha98 has no activity yet for this period.</div>
          <div style="text-align:center;margin-top:12px;">
            <a href="#" style="color:#0969da;font-size:13px;text-decoration:none;border:1px solid #d0d7de;padding:6px 16px;border-radius:6px;display:inline-block;">Show more activity</a>
          </div>
        </div>
      </div>
      <div class="year-list">
        <div class="year-item active">2026</div>
        <div class="year-item">2025</div>
        <div class="year-item">2024</div>
        <div class="year-item">2023</div>
        <div class="year-item">2022</div>
        <div class="year-item">2021</div>
        <div class="year-item">2020</div>
        <div class="year-item">2019</div>
        <div class="year-item">2018</div>
        <div class="year-item">2017</div>
      </div>
    </div>

  </main>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
    <span>© 2026 GitHub, Inc.</span>
    <div class="footer-links">
      <a href="#">Terms</a>
      <a href="#">Privacy</a>
      <a href="#">Security</a>
      <a href="#">Status</a>
      <a href="#">Community</a>
      <a href="#">Docs</a>
      <a href="#">Contact</a>
      <a href="#">Manage cookies</a>
      <a href="#">Do not share my personal information</a>
    </div>
  </div>
</footer>

<script>
  // Generate contribution grid
  const grid = document.getElementById('contrib-grid');
  grid.style.cssText = 'display:flex;gap:3px;';
  for(let w = 0; w < 52; w++){
    const col = document.createElement('div');
    col.style.cssText = 'display:flex;flex-direction:column;gap:3px;';
    for(let d = 0; d < 7; d++){
      const cell = document.createElement('div');
      cell.style.cssText = 'width:10px;height:10px;border-radius:2px;background:#ebedf0;';
      col.appendChild(cell);
    }
    grid.appendChild(col);
  }
</script>
</body>
</html>
