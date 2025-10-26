# aarzoogupta3.github.io
!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Aarzoo (Ajay) Gupta — Portfolio</title>
  <meta name="description" content="Aarzoo Gupta — Graphic Designer, Illustrator, 3D modeller" />
  <style>
    /* ====== LIGHT THEME PORTFOLIO (single-file) ====== */
    :root{
      --bg:#ffffff; --fg:#0b0b0b; --muted:#6b6b6b; --accent:#1f6feb; --card:#fbfbfb;
      --radius:14px; --maxw:1000px; --shadow: 0 6px 20px rgba(11,11,11,0.06);
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, 'Roboto Mono', monospace;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      background:var(--bg); color:var(--fg); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
      display:flex; align-items:center; justify-content:center; padding:32px;
    }
    .wrap{width:100%; max-width:var(--maxw)}
    header{display:flex; gap:24px; align-items:center; justify-content:space-between}
    .brand{display:flex; gap:16px; align-items:center}
    .avatar{width:84px; height:84px; border-radius:12px; background:linear-gradient(135deg,var(--accent),#00c2ff); display:flex; align-items:center; justify-content:center; color:white; font-weight:700; font-size:22px; box-shadow:var(--shadow)}
    h1{margin:0;font-size:28px}
    h2{margin:6px 0 0;font-size:14px;color:var(--muted);font-weight:600}
    .intro{margin-top:28px; display:grid; grid-template-columns:1fr 320px; gap:28px; align-items:start}
    .card{background:var(--card); border-radius:var(--radius); padding:22px; box-shadow:var(--shadow)}
    p.lead{margin:0; color:var(--fg); line-height:1.6}
    .links{display:flex; gap:12px; margin-top:18px}
    a.btn{display:inline-flex; gap:10px; align-items:center; text-decoration:none; padding:10px 14px; border-radius:10px; font-weight:600; background:transparent; border:1px solid rgba(11,11,11,0.06)}
    .contact{display:flex; flex-direction:column; gap:8px}
    .projects{margin-top:24px; display:grid; gap:16px}
    .project{display:flex; gap:16px; align-items:center}
    .thumb{width:120px; height:80px; border-radius:10px; background:linear-gradient(90deg,#eee,#ddd); flex-shrink:0}
    footer{margin-top:34px; text-align:center; color:var(--muted); font-size:13px}
    .top-actions{display:flex; gap:8px; align-items:center}
    .theme-toggle{background:transparent;border:1px solid rgba(11,11,11,0.06); padding:8px 10px;border-radius:10px; cursor:pointer}
    /* responsive */
    @media (max-width:880px){
      .intro{grid-template-columns:1fr}
      .avatar{width:68px;height:68px}
    }
    /* small helper */
    .muted{color:var(--muted)}
    .mono{font-family:var(--mono); font-size:13px}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="avatar">AG</div>
        <div>
          <h1>Aarzoo (Ajay) Gupta</h1>
          <h2>Graphic Designer • Illustrator • 3D modeller</h2>
        </div>
      </div>
      <div class="top-actions">
        <button class="theme-toggle" id="switchToDark">Open Dark Theme</button>
      </div>
    </header>

    <main class="intro">
      <section class="card">
        <p class="lead">I am the person who likes new things, challenges, art and targets for a goal with the result of learning and practice that have been traversed in earnest — the result will be maximised. Maybe a lot of people are more than good than me, but with perseverance and strong approach, will can defeat all.</p>

        <div class="links">
          <a class="btn" href="https://www.instagram.com/__arrzz?igsh=aXB2dmxveDJjY240" target="_blank">Instagram</a>
          <a class="btn" href="https://www.linkedin.com/in/ajay-gupta-8b91892a3?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">LinkedIn</a>
          <a class="btn" href="mailto:aarzoogupta124@gmail.com">Email</a>
        </div>

        <section class="projects">
          <!-- Projects are editable: copy or replace .project blocks -->
          <div class="project card">
            <div class="thumb" aria-hidden></div>
            <div>
              <div style="font-weight:700">Project Title — Editable</div>
              <div class="muted">Short description of the project. Replace this with your work summary or case study intro.</div>
            </div>
          </div>

          <div class="project card">
            <div class="thumb" aria-hidden></div>
            <div>
              <div style="font-weight:700">Project Title — Editable</div>
              <div class="muted">Short description of the project. Replace this with your work summary or case study intro.</div>
            </div>
          </div>

        </section>
      </section>

      <aside class="card contact">
        <div style="font-weight:700">Contact</div>
        <div class="muted mono">Email</div>
        <a href="mailto:aarzoogupta124@gmail.com">aarzoogupta124@gmail.com</a>

        <div class="muted mono">Quick Links</div>
        <a href="https://www.instagram.com/__arrzz?igsh=aXB2dmxveDJjY240" target="_blank">Instagram</a>
        <a href="https://www.linkedin.com/in/ajay-gupta-8b91892a3?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">LinkedIn</a>

        <div style="margin-top:12px">
          <div class="muted">Theme</div>
          <div>Light — Minimal • Modern • Professional</div>
        </div>
      </aside>
    </main>

    <footer class="mono">Made by Aarzoo Gupta • Edit the projects in the HTML to add your work • <span id="buildInfo">Light</span></footer>
  </div>

  <script>
    // Simple redirect to the dark-theme file if requested
    document.getElementById('switchToDark').addEventListener('click', function(){
      // if deploying as separate files, this will point to the dark file
      window.location.href = 'dark-theme.html';
    });
  </script>
</body>
</html>
