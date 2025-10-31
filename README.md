<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Wilson Wandu — Tech Strategist & BI Innovator</title>
  <meta name="description" content="Wilson Wandu — Tech Strategist | BI & Automation Innovator | Storytelling That Drives Action" />

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg-1: #0f1724;
      --accent-from: #556bff;
      --accent-to: #9b5de5;
      --glass: rgba(255,255,255,0.04);
      --muted: rgba(255,255,255,0.65);
      --card-radius: 14px;
      --max-width: 1100px;
    }

    *{box-sizing:border-box}
    body{
      margin:0;
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: radial-gradient(1200px 600px at -10% -10%, rgba(86,96,255,0.12), transparent 8%),
                  linear-gradient(160deg, rgba(7,12,24,1) 0%, rgba(10,14,26,1) 20%, rgba(15,19,33,1) 100%);
      color: #eaeaef;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding-bottom:60px;
    }

    /* subtle animated gradient overlay */
    .gradient-overlay{
      position:fixed;
      inset:0;
      z-index:0;
      pointer-events:none;
      background: linear-gradient(120deg, rgba(85,107,255,0.06), rgba(155,93,229,0.05));
      mix-blend-mode: overlay;
      animation: float 10s ease-in-out infinite;
    }
    @keyframes float{
      0% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-8px) rotate(1deg); }
      100% { transform: translateY(0px) rotate(0deg); }
    }

    header{
      position:sticky;
      top:0;
      z-index:20;
      backdrop-filter: blur(8px);
      background: linear-gradient(180deg, rgba(10,14,26,0.6), rgba(10,14,26,0.45));
      border-bottom: 1px solid rgba(255,255,255,0.03);
      padding:10px 18px;
    }
    .nav-inner{
      max-width:var(--max-width);
      margin:0 auto;
      display:flex;
      gap:16px;
      align-items:center;
      justify-content:space-between;
    }
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
    }
    .brand img{
      width:44px;
      height:44px;
      border-radius:10px;
      object-fit:cover;
      box-shadow: 0 6px 18px rgba(88,80,180,0.12), 0 1px 0 rgba(255,255,255,0.02) inset;
    }
    .brand h1{
      font-size:16px;
      margin:0;
      font-weight:700;
      letter-spacing:0.2px;
    }
    nav a{
      color:var(--muted);
      text-decoration:none;
      margin-left:14px;
      font-weight:500;
      font-size:14px;
      transition: color .18s ease, transform .18s ease;
    }
    nav a:hover{ color: #fff; transform: translateY(-2px); }

    main{
      max-width:var(--max-width);
      margin:28px auto;
      position:relative;
      z-index:5;
      padding:0 18px;
    }

    .hero{
      display:flex;
      gap:28px;
      align-items:center;
      margin-bottom:22px;
    }
    .hero-left{
      flex:1;
      min-width:240px;
    }
    .hero-right{
      width:160px;
      height:160px;
      border-radius:18px;
      overflow:hidden;
      box-shadow: 0 18px 40px rgba(88,80,180,0.14);
      border: 1px solid rgba(255,255,255,0.04);
      flex-shrink:0;
    }
    .hero-right img{ width:100%; height:100%; object-fit:cover; display:block; }

    .tagline{
      color:#e9eefc;
      margin:6px 0 14px;
      font-weight:600;
      font-size:14px;
    }
    .lead{
      color:rgba(255,255,255,0.9);
      font-size:20px;
      margin:0 0 8px;
      line-height:1.25;
      font-weight:700;
    }
    .bio{
      color:var(--muted);
      margin:0;
      font-size:15px;
      line-height:1.55;
    }

    /* sections */
    section{
      margin-top:28px;
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius: var(--card-radius);
      padding:20px;
      box-shadow: 0 6px 30px rgba(11,12,20,0.35);
      border: 1px solid rgba(255,255,255,0.03);
    }
    .section-title{
      display:flex;
      align-items:center;
      gap:12px;
      margin-bottom:12px;
    }
    .section-title h2{
      margin:0;
      font-size:18px;
      letter-spacing:0.2px;
    }
    .small{ color:var(--muted); font-size:13px; }

    /* skills grid */
    .skills{
      display:flex;
      flex-wrap:wrap;
      gap:10px;
    }
    .skill{
      background: linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      padding:8px 12px;
      border-radius:10px;
      font-weight:600;
      font-size:13px;
      border:1px solid rgba(255,255,255,0.02);
    }

    /* projects */
    .projects .project{
      margin-bottom:20px;
      display:block;
    }
    .project-title{
      font-weight:700;
      margin:10px 0 8px;
    }
    .video-wrap{
      border-radius:10px;
      overflow:hidden;
      background: #000;
      max-width:100%;
      width:640px;
      height:360px;
      box-shadow: 0 10px 30px rgba(20,16,40,0.55);
      border: 1px solid rgba(255,255,255,0.03);
    }
    video{
      display:block;
      width:100%;
      height:100%;
      background:#000;
    }
    sub{ color:var(--muted); font-size:13px; }

    /* experience list */
    .exp-item{
      padding:12px 0;
      border-bottom:1px dashed rgba(255,255,255,0.03);
    }
    .exp-item:last-child{ border-bottom: none; }

    /* contact */
    .contact-grid{
      display:flex;
      gap:18px;
      flex-wrap:wrap;
    }
    .contact-card{
      flex:1 1 220px;
      padding:12px;
      border-radius:10px;
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));
      border:1px solid rgba(255,255,255,0.02);
    }

    /* footer area for github stats */
    .footer{
      max-width:var(--max-width);
      margin:22px auto 80px;
      padding:0 18px;
      display:flex;
      gap:18px;
      align-items:flex-start;
      justify-content:space-between;
      flex-wrap:wrap;
    }

    .stats-card img{
      border-radius:12px;
      border:1px solid rgba(255,255,255,0.03);
    }

    /* responsive */
    @media (max-width:900px){
      .hero{ flex-direction:column; align-items:flex-start; gap:18px; }
      .hero-right{ width:120px; height:120px; border-radius:12px; }
      .video-wrap{ width:100%; height:calc(100% * 9 / 16); } /* responsive 16:9 */
      video{ height:100%; }
    }
    @media (max-width:480px){
      nav a{ display:none; } /* keep header simple on very small screens */
      .nav-inner{ justify-content:space-between; }
    }

    /* accent underline for section titles */
    .accent-line{
      height:6px;
      width:88px;
      border-radius:8px;
      background: linear-gradient(90deg, var(--accent-from), var(--accent-to));
      margin-right:8px;
      box-shadow: 0 6px 18px rgba(89,78,220,0.12);
    }
  </style>
</head>

<body>

  <div class="gradient-overlay" aria-hidden="true"></div>

  <header>
    <div class="nav-inner">
      <div class="brand" style="gap:12px">
        <img src="https://raw.githubusercontent.com/WWWandu/Wandu.github.io/main/assets/Wilson%20Passport.png" alt="Wilson Wandu">
        <div>
          <h1 style="font-size:15px; margin:0;">Wilson Wandu</h1>
          <div style="font-size:12px; color:var(--muted)">Tech Strategist • BI & Automation</div>
        </div>
      </div>

      <nav aria-label="Main navigation">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>

    <!-- HERO -->
    <section aria-labelledby="hero">
      <div class="hero">
        <div class="hero-left">
          <div class="tagline">Tech Strategist | BI & Automation Innovator | Storytelling That Drives Action</div>
          <h2 class="lead">👋 Hi, I'm Wilson Wandu</h2>
          <p class="bio">Tech-savvy, data-driven, and curious by nature. I thrive on using BI and automation to simplify work, uncover insights, and tell data stories that inspire better decisions.</p>
          <p style="margin-top:12px;">
            <a href="#projects" style="display:inline-block;padding:10px 14px;border-radius:10px;background:linear-gradient(90deg,var(--accent-from),var(--accent-to));color:#fff;text-decoration:none;font-weight:600;">View Projects</a>
            <a href="mailto:wilsonwwandu@outlook.com" style="display:inline-block;padding:10px 14px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);color:var(--muted);text-decoration:none;margin-left:8px;">Contact</a>
          </p>
        </div>

        <div class="hero-right" aria-hidden="true">
          <img src="https://raw.githubusercontent.com/WWWandu/Wandu.github.io/main/assets/Wilson%20Passport.png" alt="Wilson Photo">
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" aria-labelledby="about-title" style="margin-top:20px;">
      <div class="section-title">
        <div class="accent-line" aria-hidden="true"></div>
        <h2 id="about-title">About</h2>
      </div>
      <p class="small">I'm a results-driven Business Analyst, BI Developer and Instructional Systems Designer with experience in banking, digital transformation, and data analytics. I specialize in Power BI development — from data modeling, DAX calculations, and ETL processes to building interactive dashboards and reports that transform raw data into actionable insights. Adept at bridging IT and business, I ensure technical solutions deliver real business value.</p>
    </section>

    <!-- SKILLS -->
    <section id="skills" aria-labelledby="skills-title" style="margin-top:18px;">
      <div class="section-title">
        <div class="accent-line" aria-hidden="true"></div>
        <h2 id="skills-title">Skills & Tools</h2>
      </div>

      <div class="skills" role="list">
        <span class="skill">Power BI</span>
        <span class="skill">Microsoft Fabric</span>
        <span class="skill">Data Modeling & DAX</span>
        <span class="skill">ETL & Data Pipelines</span>
        <span class="skill">Data Storytelling</span>
        <span class="skill">Process Optimization</span>
        <span class="skill">Instructional Design</span>
        <span class="skill">Project Management</span>
        <span class="skill">SAP (HR)</span>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects" aria-labelledby="projects-title" style="margin-top:18px;">
      <div class="section-title">
        <div class="accent-line" aria-hidden="true"></div>
        <h2 id="projects-title">Projects Showcase</h2>
      </div>

      <div class="projects">
        <!-- Project 1 -->
        <article class="project" aria-labelledby="p1">
          <div class="project-title" id="p1">Contact Centre Churn Analysis</div>
          <p class="small">Dashboard highlighting customer churn trends in the contact center with actionable insights.</p>
          <div class="video-wrap" style="margin-top:12px;">
            <video controls playsinline preload="metadata" poster="" >
              <source src="https://github.com/WWWandu/Wandu.github.io/raw/main/assets/Customer%20Churn%20Rate.mp4" type="video/mp4">
              Your browser does not support MP4 video.
            </video>
          </div>
          <br><sub>Customer Churn Rate</sub>
        </article>

        <!-- Project 2 -->
        <article class="project" aria-labelledby="p2" style="margin-top:18px;">
          <div class="project-title" id="p2">CRM Training (Instructional Design)</div>
          <p class="small">This video demonstrates system training, instructional design, and user enablement — simplifying technical processes into clear learning content.</p>
          <div class="video-wrap" style="margin-top:12px;">
            <video controls playsinline preload="metadata">
              <source src="https://github.com/WWWandu/Wandu.github.io/raw/main/assets/CRM%20Training-Cut%20Clip.mp4" type="video/mp4">
              Your browser does not support MP4 video.
            </video>
          </div>
          <br><sub>CRM Training</sub>
        </article>

        <!-- Project 3 -->
        <article class="project" aria-labelledby="p3" style="margin-top:18px;">
          <div class="project-title" id="p3">Daraja System Training</div>
          <p class="small">Explainer video for the Daraja system — used to improve onboarding and adoption.</p>
          <div class="video-wrap" style="margin-top:12px;">
            <video controls playsinline preload="metadata">
              <source src="https://github.com/WWWandu/Wandu.github.io/raw/main/assets/Daraja%20System%20Training-%20Cut%20clip.mp4" type="video/mp4">
              Your browser does not support MP4 video.
            </video>
          </div>
          <br><sub>Daraja System Training</sub>
        </article>

      </div>
    </section>

    <!-- ACHIEVEMENTS -->
    <section id="achievements" aria-labelledby="achieve-title" style="margin-top:18px;">
      <div class="section-title">
        <div class="accent-line" aria-hidden="true"></div>
        <h2 id="achieve-title">Achievements & Highlights</h2>
      </div>
      <ul class="small" style="margin:0 0 0 18px;">
        <li>Digital Transformation @ Tambulika Sacco — boosted efficiency & customer support</li>
        <li>System Training Library — built explainer videos for ITSM Daraja & CRM</li>
        <li>Executive Technical Storytelling — dashboards on uptime, SLA, and KPIs for leadership</li>
        <li>PwC Power BI Simulation — gender diversity analytics dashboards</li>
      </ul>
    </section>

    <!-- EXPERIENCE -->
    <section id="experience" aria-labelledby="exp-title" style="margin-top:18px;">
      <div class="section-title">
        <div class="accent-line" aria-hidden="true"></div>
        <h2 id="exp-title">Professional Experience</h2>
      </div>

      <div class="exp-item">
        <strong>Business Process Architect</strong> — NCBA Bank, Nairobi | <em>Oct 2025 – Present</em>
        <div class="small">Lead end-to-end optimization of Power BI dashboards and ETL workflows, championing process improvements and automation to improve reliability and scalability.</div>
      </div>

      <div class="exp-item">
        <strong>IT Business Analyst & Instructional Systems Designer</strong> — NCBA Bank, Nairobi | <em>Feb 2024 – Oct 2025</em>
        <div class="small">Bridged IT and business, delivered interactive Power BI dashboards, and produced explainer videos for systems like NCBA Daraja & Microsoft CRM D365.</div>
      </div>

      <div class="exp-item">
        <strong>Learning Analyst & Instructional Designer</strong> — NCBA Bank, Nairobi | <em>Dec 2022 – Feb 2024</em>
      </div>

      <div class="exp-item">
        <strong>Business Analyst</strong> — Tambulika Sacco, Nairobi | <em>May 2019 – Dec 2021</em>
        <div class="small">Spearheaded system documentation & workflows, revamping collections and boosting revenue by 30%.</div>
      </div>

      <div class="exp-item">
        <strong>Microsoft Dynamics NAV ERP Specialist</strong> — Tambulika Sacco | <em>May 2017 – May 2018</em>
        <div class="small">Led transformation to Dynamics NAV / Business Central, improving accuracy and efficiency.</div>
      </div>

      <div class="exp-item">
        <strong>Other Roles</strong> — Financial Consultant & Trainer (ICEA Lion Group), Freelance Brand Creative Designer.
      </div>
    </section>

    <!-- EDUCATION & CERTS -->
    <section id="education" aria-labelledby="edu-title" style="margin-top:18px;">
      <div class="section-title">
        <div class="accent-line" aria-hidden="true"></div>
        <h2 id="edu-title">Education & Certifications</h2>
      </div>

      <div class="small" style="margin-bottom:8px;">
        <strong>BA, Economics & Finance</strong> — Kenyatta University (2021)<br>
        <strong>Certificate, Basics in Chinese Language & Culture</strong> — Kenyatta University (2019)
      </div>

      <div class="small">
        <strong>Selected Certifications:</strong>
        <ul style="margin:6px 0 0 18px;">
          <li>Microsoft Azure AI Fundamentals</li>
          <li>Generative AI (Microsoft & LinkedIn)</li>
          <li>Advanced Certificate in Program & Project Management (Udemy)</li>
          <li>Six Sigma Black Belt - Analyzing Process Flows</li>
          <li>Microsoft Certified: Power BI Data Analyst Associate — Ongoing</li>
          <li>ITIL Foundation</li>
          <li>PwC Power BI Job Simulation — Sept 2024</li>
        </ul>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" aria-labelledby="contact-title" style="margin-top:18px;">
      <div class="section-title">
        <div class="accent-line" aria-hidden="true"></div>
        <h2 id="contact-title">Contact</h2>
      </div>

      <div class="contact-grid">
        <div class="contact-card">
          <strong>Email</strong>
          <div class="small"><a href="mailto:wilsonwwandu@outlook.com" style="color:var(--muted);text-decoration:none;">wilsonwwandu@outlook.com</a></div>
        </div>

        <div class="contact-card">
          <strong>Phone</strong>
          <div class="small">+254 716 277141</div>
        </div>

        <div class="contact-card">
          <strong>Location</strong>
          <div class="small">Nairobi, Kenya</div>
        </div>

        <div class="contact-card">
          <strong>Portfolio</strong>
          <div class="small"><a href="https://wwwandu.github.io/Wandu.github.io/" style="color:var(--muted);text-decoration:none;">GitHub Pages Portfolio</a></div>
        </div>
      </div>
    </section>

  </main>

  <!-- Footer / Stats -->
  <div class="footer" role="contentinfo">
    <div class="small" style="max-width:640px;">
      <div style="font-weight:700;margin-bottom:8px;">Let's connect</div>
      <div style="color:var(--muted)">Turning data into stories that inspire action.</div>
    </div>

    <div class="stats-card">
      <!-- GitHub stats card -->
      <img src="https://github-readme-stats.vercel.app/api?username=WWWandu&show_icons=true&theme=dark" alt="GitHub stats for WWWandu">
    </div>
  </div>

  <script>
    // Smooth scroll for internal anchors
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', function(e){
        const target = document.querySelector(this.getAttribute('href'));
        if(target){ e.preventDefault(); target.scrollIntoView({behavior:'smooth', block:'start'}); }
      });
    });
  </script>
</body>
</html>
