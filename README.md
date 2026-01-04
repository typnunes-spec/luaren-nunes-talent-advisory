# luaren-nunes-talent-advisory
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Luaren Nunes Talent Advisory — Executive coaching, fractional Chief People Officer, and HR/Org advisory services." />
  <title>Luaren Nunes Talent Advisory</title>
  <style>
    :root{
      --bg:#0b0d10;
      --card:#11151b;
      --text:#e8eef7;
      --muted:#a9b4c4;
      --line:rgba(232,238,247,.12);
      --accent:#7dd3fc; /* subtle sky */
      --accent2:#a7f3d0; /* subtle mint */
      --shadow: 0 12px 40px rgba(0,0,0,.45);
      --radius:16px;
      --max:1100px;
      --pad: clamp(18px, 2.5vw, 28px);
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      background:
        radial-gradient(900px 500px at 10% -10%, rgba(125,211,252,.18), transparent 60%),
        radial-gradient(800px 500px at 110% 0%, rgba(167,243,208,.10), transparent 55%),
        linear-gradient(180deg, #07090c, var(--bg));
      color:var(--text);
    }
    a{color:inherit}
    .wrap{max-width:var(--max); margin:0 auto; padding:0 var(--pad);}
    .skip{
      position:absolute; left:-999px; top:auto; width:1px; height:1px; overflow:hidden;
    }
    .skip:focus{left:var(--pad); top:var(--pad); width:auto; height:auto; padding:10px 14px; background:#fff; color:#000; border-radius:10px; z-index:9999;}
    header{
      position:sticky; top:0; z-index:50;
      backdrop-filter:saturate(140%) blur(10px);
      background: rgba(11,13,16,.75);
      border-bottom: 1px solid var(--line);
    }
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      padding:14px 0;
      gap:12px;
    }
    .brand{
      display:flex; flex-direction:column; gap:2px; text-decoration:none;
      line-height:1.1;
    }
    .brand strong{font-size:14px; letter-spacing:.12em; text-transform:uppercase}
    .brand span{font-size:12px; color:var(--muted)}
    nav ul{
      list-style:none; margin:0; padding:0;
      display:flex; align-items:center; gap:18px;
    }
    nav a{
      text-decoration:none;
      font-size:13px;
      color:var(--muted);
      padding:8px 10px;
      border-radius:10px;
      transition: background .2s ease, color .2s ease;
    }
    nav a:hover, nav a:focus{
      background: rgba(232,238,247,.06);
      color: var(--text);
      outline:none;
    }
    .cta{
      display:flex; gap:10px; align-items:center;
    }
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      gap:10px;
      border-radius: 12px;
      padding:10px 14px;
      font-size:13px;
      text-decoration:none;
      border:1px solid var(--line);
      background: rgba(232,238,247,.04);
      color: var(--text);
      transition: transform .08s ease, background .2s ease, border-color .2s ease;
      white-space:nowrap;
    }
    .btn:hover{background: rgba(232,238,247,.07); transform: translateY(-1px);}
    .btn.primary{
      border-color: rgba(125,211,252,.35);
      background: linear-gradient(180deg, rgba(125,211,252,.18), rgba(232,238,247,.04));
    }
    .btn.primary:hover{border-color: rgba(125,211,252,.55);}
    .hamburger{
      display:none;
      border:1px solid var(--line);
      background: rgba(232,238,247,.04);
      color:var(--text);
      border-radius:12px;
      padding:10px 12px;
      cursor:pointer;
    }
    .hamburger:focus{outline:2px solid rgba(125,211,252,.35); outline-offset:2px;}
    .mobile{
      display:none;
      padding:0 0 14px 0;
    }
    .mobile a{
      display:block;
      padding:12px 12px;
      border:1px solid var(--line);
      border-radius:12px;
      margin-top:10px;
      text-decoration:none;
      color:var(--muted);
      background: rgba(232,238,247,.03);
    }
    .mobile a:hover{color:var(--text); background: rgba(232,238,247,.06);}
    main{padding: 44px 0 80px;}
    .hero{
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap: 28px;
      align-items:start;
      padding: 30px 0 12px;
    }
    .kicker{
      display:inline-flex; gap:10px; align-items:center;
      padding:8px 12px;
      border-radius:999px;
      border:1px solid var(--line);
      background: rgba(232,238,247,.03);
      color: var(--muted);
      font-size:12px;
      width:fit-content;
    }
    .dot{
      width:8px; height:8px; border-radius:50%;
      background: linear-gradient(180deg, var(--accent), var(--accent2));
      box-shadow: 0 0 18px rgba(125,211,252,.25);
    }
    h1{
      margin:14px 0 10px;
      font-size: clamp(30px, 4.2vw, 46px);
      letter-spacing:-.02em;
      line-height:1.1;
    }
    .lead{
      color: var(--muted);
      font-size: 15px;
      line-height:1.7;
      max-width: 62ch;
      margin: 0 0 18px;
    }
    .hero-actions{display:flex; gap:10px; flex-wrap:wrap; margin-top:16px;}
    .panel{
      border:1px solid var(--line);
      background: linear-gradient(180deg, rgba(232,238,247,.04), rgba(232,238,247,.02));
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 18px;
    }
    .panel h3{margin:0 0 10px; font-size:13px; letter-spacing:.12em; text-transform:uppercase; color:var(--muted);}
    .stats{display:grid; gap:10px; margin-top:10px;}
    .stat{
      border:1px solid var(--line);
      border-radius: 14px;
      padding:12px 12px;
      background: rgba(232,238,247,.02);
    }
    .stat strong{display:block; font-size:14px; margin-bottom:4px;}
    .stat span{color:var(--muted); font-size:13px; line-height:1.4;}
    section{padding: 44px 0;}
    .section-title{
      display:flex; align-items:baseline; justify-content:space-between; gap:16px;
      margin-bottom: 18px;
    }
    .section-title h2{
      margin:0;
      font-size: 18px;
      letter-spacing:.12em;
      text-transform:uppercase;
      color: var(--muted);
    }
    .section-title p{margin:0; color:var(--muted); font-size:13px; max-width: 70ch;}
    .grid{
      display:grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 14px;
    }
    .card{
      grid-column: span 4;
      border:1px solid var(--line);
      background: rgba(232,238,247,.03);
      border-radius: var(--radius);
      padding: 18px;
      transition: transform .12s ease, background .2s ease, border-color .2s ease;
      min-height: 170px;
    }
    .card:hover{transform: translateY(-2px); background: rgba(232,238,247,.05); border-color: rgba(125,211,252,.25);}
    .card h3{margin:0 0 8px; font-size:16px;}
    .card p{margin:0 0 12px; color:var(--muted); font-size:13.5px; line-height:1.7;}
    .bullets{margin:0; padding-left: 18px; color: var(--muted); font-size:13px; line-height:1.7;}
    .bullets li{margin:6px 0;}
    .split{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
    }
    .steps{
      display:grid; gap:10px;
    }
    .step{
      display:flex; gap:12px;
      border:1px solid var(--line);
      border-radius: 14px;
      padding: 14px;
      background: rgba(232,238,247,.02);
    }
    .step .num{
      width:28px; height:28px; border-radius:10px;
      display:flex; align-items:center; justify-content:center;
      border:1px solid rgba(125,211,252,.25);
      background: rgba(125,211,252,.10);
      color: var(--text);
      font-size:13px;
      flex: 0 0 auto;
    }
    .step strong{display:block; margin-bottom:4px;}
    .step span{color:var(--muted); font-size:13px; line-height:1.6;}
    .quote{
      border:1px solid var(--line);
      border-radius: var(--radius);
      padding: 18px;
      background: linear-gradient(180deg, rgba(167,243,208,.06), rgba(232,238,247,.02));
    }
    blockquote{margin:0; color:var(--text); font-size:14px; line-height:1.8;}
    .quote footer{margin-top:10px; color:var(--muted); font-size:13px;}
    form{
      display:grid; gap:10px;
    }
    label{font-size:12px; color:var(--muted);}
    input, textarea{
      width:100%;
      border-radius:12px;
      border:1px solid var(--line);
      background: rgba(232,238,247,.03);
      color: var(--text);
      padding: 12px 12px;
      font-size: 14px;
      outline:none;
    }
    input:focus, textarea:focus{border-color: rgba(125,211,252,.35); box-shadow: 0 0 0 3px rgba(125,211,252,.10);}
    textarea{min-height:110px; resize:vertical;}
    .form-row{display:grid; grid-template-columns: 1fr 1fr; gap:10px;}
    .note{color:var(--muted); font-size:12px; line-height:1.6; margin: 8px 0 0;}
    footer{
      border-top:1px solid var(--line);
      padding: 22px 0;
      color: var(--muted);
      font-size: 12px;
    }
    .foot{
      display:flex; justify-content:space-between; align-items:center; gap:12px; flex-wrap:wrap;
    }
    .pill{
      border:1px solid var(--line);
      border-radius:999px;
      padding:8px 12px;
      background: rgba(232,238,247,.02);
      color:var(--muted);
      text-decoration:none;
    }
    /* Responsive */
    @media (max-width: 900px){
      .hero{grid-template-columns:1fr; }
      .card{grid-column: span 6;}
      .split{grid-template-columns:1fr;}
    }
    @media (max-width: 650px){
      nav ul{display:none;}
      .hamburger{display:inline-flex;}
      .mobile{display:block;}
      .card{grid-column: span 12;}
      .form-row{grid-template-columns:1fr;}
    }
  </style>
</head>

<body>
  <a class="skip" href="#main">Skip to content</a>

  <header>
    <div class="wrap">
      <div class="nav">
        <a class="brand" href="#top" aria-label="Luaren Nunes Talent Advisory Home">
          <strong>Luaren Nunes</strong>
          <span>Talent Advisory</span>
        </a>

        <nav aria-label="Primary">
          <ul>
            <li><a href="#services">Services</a></li>
            <li><a href="#approach">Approach</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </nav>

        <div class="cta">
          <a class="btn" href="#contact">Book a consult</a>
          <a class="btn primary" href="#services">Explore services</a>
          <button class="hamburger" id="menuBtn" aria-expanded="false" aria-controls="mobileMenu" aria-label="Open menu">
            Menu
          </button>
        </div>
      </div>

      <div class="mobile" id="mobileMenu" hidden>
        <a href="#services">Services</a>
        <a href="#approach">Approach</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </header>

  <main id="main">
    <div class="wrap" id="top">
      <section class="hero" aria-label="Hero">
        <div>
          <div class="kicker"><span class="dot" aria-hidden="true"></span> Executive coaching • Fractional CPO • HR/Org advisory</div>
          <h1>People strategy that scales leadership, culture, and performance.</h1>
          <p class="lead">
            Luaren Nunes Talent Advisory partners with founders and leadership teams to build clear org design,
            stronger managers, and the operating rhythm that helps teams execute—without losing what makes your company you.
          </p>

          <div class="hero-actions">
            <a class="btn primary" href="#contact">Schedule a discovery call</a>
            <a class="btn" href="#approach">See how we work</a>
          </div>

          <p class="note">
            Serving growth-stage teams and established organizations looking to sharpen leadership effectiveness and HR foundations.
          </p>
        </div>

        <aside class="panel" aria-label="At-a-glance">
          <h3>Focus areas</h3>
          <div class="stats">
            <div class="stat">
              <strong>Executive Coaching</strong>
              <span>Clarity, presence, decision-making, and stakeholder influence.</span>
            </div>
            <div class="stat">
              <strong>Fractional Chief People Officer</strong>
              <span>Hands-on people leadership to stabilize, scale, and align the org.</span>
            </div>
            <div class="stat">
              <strong>HR & Org Advisory</strong>
              <span>Structure, systems, and policies that support performance and growth.</span>
            </div>
          </div>
        </aside>
      </section>

      <section id="services" aria-label="Services">
        <div class="section-title">
          <h2>Services</h2>
          <p>Choose a focused engagement or combine offerings into a single advisory partnership.</p>
        </div>

        <div class="grid">
          <article class="card" aria-label="Executive Coaching">
            <h3>Executive Coaching</h3>
            <p>For leaders navigating complexity, growth, and high-stakes decisions.</p>
            <ul class="bullets">
              <li>Leadership presence & communication</li>
              <li>Executive decision-making & prioritization</li>
              <li>Stakeholder management & influence</li>
              <li>Performance conversations & accountability</li>
            </ul>
          </article>

          <article class="card" aria-label="Fractional Chief People Officer">
            <h3>Fractional Chief People Officer</h3>
            <p>Strategic + operational people leadership, right-sized for your stage.</p>
            <ul class="bullets">
              <li>People strategy, planning, and cadence</li>
              <li>Org design, leveling, and manager enablement</li>
              <li>Talent processes (hiring → performance)</li>
              <li>Culture, engagement, retention levers</li>
            </ul>
          </article>

          <article class="card" aria-label="HR and Organizational Advisory">
            <h3>HR / Org Advisory</h3>
            <p>Build reliable HR infrastructure that supports growth and reduces risk.</p>
            <ul class="bullets">
              <li>HR foundations, policies, and compliance hygiene</li>
              <li>Comp, role clarity, and performance frameworks</li>
              <li>Change management & team effectiveness</li>
              <li>Employee relations & leadership alignment</li>
            </ul>
          </article>
        </div>
      </section>

      <section id="approach" aria-label="Approach">
        <div class="section-title">
          <h2>Approach</h2>
          <p>A simple, repeatable process that creates momentum and measurable progress.</p>
        </div>

        <div class="split">
          <div class="steps" aria-label="Process steps">
            <div class="step">
              <div class="num">1</div>
              <div>
                <strong>Diagnose</strong>
                <span>Clarify goals, constraints, and what “better” looks like for leadership and the org.</span>
              </div>
            </div>
            <div class="step">
              <div class="num">2</div>
              <div>
                <strong>Design</strong>
                <span>Align on a focused plan: outcomes, scope, timeline, and success metrics.</span>
              </div>
            </div>
            <div class="step">
              <div class="num">3</div>
              <div>
                <strong>Implement</strong>
                <span>Build the rhythm: coaching, operating cadences, tools, and leadership enablement.</span>
              </div>
            </div>
            <div class="step">
              <div class="num">4</div>
              <div>
                <strong>Sustain</strong>
                <span>Measure, iterate, and hand off systems so progress continues without dependency.</span>
              </div>
            </div>
          </div>

          <aside class="quote" aria-label="Value proposition">
            <blockquote>
              “Minimalism isn’t less work—it’s less noise. We focus on the few changes that unlock the most leverage:
              clearer roles, stronger managers, and a people system that matches your pace of growth.”
            </blockquote>
            <footer>— Luaren Nunes Talent Advisory</footer>

            <div style="height:14px"></div>

            <a class="btn primary" href="#contact">Let’s talk about your goals</a>
          </aside>
        </div>
      </section>

      <section id="about" aria-label="About">
        <div class="section-title">
          <h2>About</h2>
          <p>Keep this section concise. Add a short bio, credibility markers, and the types of teams you support.</p>
        </div>

        <div class="grid">
          <article class="card" style="grid-column: span 7;">
            <h3>Trusted people leadership, tailored to your stage</h3>
            <p>
              Luaren partners with leaders to translate business goals into practical people strategy—without overbuilding.
              Expect a calm, structured approach: clear priorities, direct feedback, and systems that your team can actually run.
            </p>
            <ul class="bullets">
              <li>Works well with founders, exec teams, and first-time managers</li>
              <li>Balances high performance with sustainable culture</li>
              <li>Creates clarity: roles, expectations, and operating rhythm</li>
            </ul>
          </article>

          <article class="card" style="grid-column: span 5;">
            <h3>Engagement options</h3>
            <p>Common ways clients partner:</p>
            <ul class="bullets">
              <li><strong>Coaching:</strong> weekly/biweekly sessions</li>
              <li><strong>Fractional CPO:</strong> 1–3 days/week</li>
              <li><strong>Advisory:</strong> project-based or retainer</li>
            </ul>
            <p class="note">Tip: Add logos, industries, or results once you have approvals.</p>
          </article>
        </div>
      </section>

      <section id="contact" aria-label="Contact">
        <div class="section-title">
          <h2>Contact</h2>
          <p>Send a note. This form opens your email client (no backend needed). Replace the email placeholder below.</p>
        </div>

        <div class="grid">
          <div class="card" style="grid-column: span 7;">
            <h3>Schedule a discovery call</h3>
            <p>Share a little context and we’ll respond with next steps.</p>

            <form id="contactForm">
              <div class="form-row">
                <div>
                  <label for="name">Name</label>
                  <input id="name" name="name" autocomplete="name" required />
                </div>
                <div>
                  <label for="company">Company</label>
                  <input id="company" name="company" autocomplete="organization" />
                </div>
              </div>

              <div class="form-row">
                <div>
                  <label for="email">Email</label>
                  <input id="email" name="email" type="email" autocomplete="email" required />
                </div>
                <div>
                  <label for="service">Interested in</label>
                  <input id="service" name="service" placeholder="Coaching / Fractional CPO / Advisory" />
                </div>
              </div>

              <div>
                <label for="message">Message</label>
                <textarea id="message" name="message" required placeholder="What are you trying to improve right now?"></textarea>
              </div>

              <button class="btn primary" type="submit">Send message</button>
              <p class="note">No spam. If you prefer, email directly: <span id="directEmail">(set your email below)</span>.</p>
            </form>
          </div>

          <aside class="card" style="grid-column: span 5;">
            <h3>Quick details</h3>
            <p class="note" style="margin-top:0;">
              Add your preferred locations, time zone, and any scheduling link.
            </p>
            <ul class="bullets">
              <li><strong>Typical response:</strong> 1–2 business days</li>
              <li><strong>Engagements:</strong> remote / hybrid (customize)</li>
              <li><strong>Focus:</strong> leadership, org design, HR strategy</li>
            </ul>

            <div style="height:14px"></div>
            <a class="pill" href="#services">View services</a>
            <a class="pill" href="#approach" style="margin-left:8px;">How we work</a>
          </aside>
        </div>
      </section>
    </div>
  </main>

  <footer>
    <div class="wrap">
      <div class="foot">
        <div>© <span id="year"></span> Luaren Nunes Talent Advisory. All rights reserved.</div>
        <div style="display:flex; gap:10px; flex-wrap:wrap;">
          <a class="pill" href="#top">Back to top</a>
          <a class="pill" href="#contact">Contact</a>
        </div>
      </div>
    </div>
  </footer>

  <script>
    // ====== Customize this email address ======
    const BUSINESS_EMAIL = "hello@yourdomain.com"; // <-- replace with real email

    // Footer year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Mobile menu toggle
    const menuBtn = document.getElementById("menuBtn");
    const mobileMenu = document.getElementById("mobileMenu");
    menuBtn?.addEventListener("click", () => {
      const isOpen = menuBtn.getAttribute("aria-expanded") === "true";
      menuBtn.setAttribute("aria-expanded", String(!isOpen));
      mobileMenu.hidden = isOpen;
    });

    // Close mobile menu after clicking a link
    mobileMenu?.querySelectorAll("a").forEach(a => {
      a.addEventListener("click", () => {
        menuBtn.setAttribute("aria-expanded", "false");
        mobileMenu.hidden = true;
      });
    });

    // Contact form -> mailto (no backend)
    const directEmail = document.getElementById("directEmail");
    directEmail.textContent = BUSINESS_EMAIL;

    document.getElementById("contactForm").addEventListener("submit", (e) => {
      e.preventDefault();
      const name = document.getElementById("name").value.trim();
      const company = document.getElementById("company").value.trim();
      const email = document.getElementById("email").value.trim();
      const service = document.getElementById("service").value.trim();
      const message = document.getElementById("message").value.trim();

      const subject = encodeURIComponent(`Inquiry — ${service || "Talent Advisory"} (${name})`);
      const bodyLines = [
        `Name: ${name}`,
        `Company: ${company || "-"}`,
        `Email: ${email}`,
        `Interested in: ${service || "-"}`,
        ``,
        `Message:`,
        message
      ];
      const body = encodeURIComponent(bodyLines.join("\n"));

      window.location.href = `mailto:${BUSINESS_EMAIL}?subject=${subject}&body=${body}`;
    });
  </script>
</body>
</html>
```
