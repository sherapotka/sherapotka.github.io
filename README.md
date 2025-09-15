# sherapotka.github.io

index.html
research.html
styles.css
cv.pdf          (your optimized CV)
headshot.jpg    (your photo)

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Shera Potka</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <nav class="nav">
    <a href="/">Shera Potka</a>
    <div class="nav-links">
      <a href="cv.pdf">CV</a>
      <a href="research.html">Research</a>
      <a href="https://github.com/sherapotka">GitHub</a>
      <a href="https://linkedin.com/in/shera-potka">LinkedIn</a>
    </div>
  </nav>

  <header class="hero">
    <img class="avatar" src="headshot.jpg" alt="Shera Potka portrait">
    <div>
      <h1>Shera Potka</h1>
      <p>PhD Candidate in Computer Science, University of Victoria</p>
      <ul class="social">
        <li><a href="mailto:spotka@uvic.ca">Email</a></li>
        <li><a href="https://scholar.google.com/">Google Scholar</a></li>
      </ul>
    </div>
  </header>

  <main class="content">
    <section>
      <h2>Education</h2>
      <ul>
        <li><b>Ph.D., Computer Science</b> — University of Victoria (2023–Present)</li>
        <li><b>M.A., Media & Computer Science</b> — University of Cologne (2021–2023)</li>
        <li><b>B.A., Media & Computer Science</b> — University of Cologne (2019–2021)</li>
      </ul>
    </section>

    <section>
      <h2>Experience</h2>
      <ul>
        <li><b>Instructor</b>, Data Models & Algorithms — UVic (2025)</li>
        <li><b>Teaching Assistant</b>, Data Mining & Web Design — UVic (2023–2024)</li>
        <li><b>Software Developer</b>, CCEH Cologne (2022–2023)</li>
        <li><b>Research Assistant</b>, ETCL UVic (2022–2023)</li>
        <li><b>Web Designer</b>, Junger Anleger (2021–2022)</li>
      </ul>
    </section>

    <section>
      <h2>Selected Publications</h2>
      <ul class="pubs">
        <li><b>Community Structure and Coherence in Digital Humanities Works</b> — IISA 2023 <em>(Best Paper Award)</em></li>
        <li><b>Enhancing Structural Minority Visibility in Link Recommendations</b> — MEDES 2024 <em>(Best Paper Award)</em></li>
        <li><b>Word Embedding Bias in Large Language Models</b> — I-SPAN 2025</li>
        <li><b>Gender & Race Bias in Consumer Product Recommendations</b> — AINA 2025</li>
        <li><b>CluSanT: Differentially Private Text Sanitization</b> — NAACL 2025</li>
      </ul>
    </section>

    <section>
      <h2>Technologies</h2>
      <p><b>Languages:</b> Java, Python, C/C++, SQL, JavaScript, HTML, PHP</p>
      <p><b>Tools:</b> React, WordPress, Elementor, Node.js, .NET, MySQL, Postgres</p>
    </section>
  </main>
</body>
</html>

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Research — Shera Potka</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <nav class="nav">
    <a href="/">Shera Potka</a>
    <div class="nav-links">
      <a href="cv.pdf">CV</a>
      <a class="active" href="research.html">Research</a>
    </div>
  </nav>

  <main class="content">
    <h1>Research</h1>
    <p>My research focuses on three ethical dimensions of AI:</p>
    <h2>Fairness in Social Recommenders</h2>
    <p>Developing algorithms to improve minority visibility and reduce popularity bias.</p>
    <h2>Bias Detection in Large Language Models</h2>
    <p>Analyzing gender and race bias in word embeddings and contextual models.</p>
    <h2>Privacy in NLP</h2>
    <p>Exploring differentially private text sanitization techniques (e.g., CluSanT).</p>
  </main>
</body>
</html>

:root { --max: 880px; --pad: 20px; --fg: #111; --muted: #666; }
* { box-sizing: border-box; }
body { margin: 0; font: 16px/1.6 system-ui, sans-serif; color: var(--fg); }
a { color: inherit; text-decoration: underline; }
.nav { display:flex; justify-content:space-between; align-items:center; padding:12px var(--pad); border-bottom:1px solid #eee; position:sticky; top:0; background:#fff; }
.nav > a { font-weight:600; text-decoration:none; }
.nav-links a { margin-left:16px; text-decoration:none; }
.nav-links a.active { text-decoration:underline; }
.hero { display:flex; gap:20px; align-items:center; max-width:var(--max); margin:30px auto; padding:0 var(--pad); }
.avatar { width:120px; height:120px; border-radius:50%; object-fit:cover; }
.social { display:flex; gap:16px; list-style:none; padding:0; margin:10px 0 0; color:var(--muted); }
.content { max-width:var(--max); margin:0 auto 60px; padding:0 var(--pad); }
h1,h2 { line-height:1.2; }
h2 { margin-top:34px; }
.pubs li { margin-bottom:10px; }
@media (max-width:640px){ .hero { flex-direction:column; align-items:flex-start; } .avatar { width:96px; height:96px; } }
