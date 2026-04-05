---
layout: default
title: home
---
<section class="hero">
  <div class="container hero-grid">
    <div class="card hero-main">
      <div class="eyebrow">Theoretical Quantum Physics · Quantum Information · Non-Hermitian Dynamics</div>
      <h1>Zengzhao Li</h1>
 
      <p style="font-size:1.08rem; line-height:1.75; margin-bottom:12px;">
        <strong>Associate Researcher, Shenzhen International Quantum Academy</strong><br>
        PhD in Theoretical Physics, Fudan University · Formerly at UC Berkeley · Max Planck Institute for the Physics of Complex Systems · Lund University
      </p>

      <p class="muted" style="margin-top:10px;">
        I am a theoretical quantum physicist working on <strong>non-Hermitian quantum systems</strong>,
        <strong>exceptional-point dynamics</strong>, <strong>open quantum systems</strong>, and
        <strong>quantum information</strong>. My research explores how spectral singularities,
        dissipation, and driven quantum dynamics enable new mechanisms for entanglement generation,
        energy transfer, quantum control, and scalable quantum technologies.
      </p>

      <div class="hero-actions">
        <a class="btn primary" href="{{ '/publications/' | relative_url }}">Selected Publications</a>
        <a class="btn" href="{{ '/files/cv.pdf' | relative_url }}" target="_blank" rel="noreferrer">Download CV</a>
        <a class="btn" href="mailto:zengzhaoli09@gmail.com">Contact</a>
      </div>
    </div>

    <aside class="card hero-side">
      <div class="profile">
        <img src="{{ '/images/photo.jpg' | relative_url }}" alt="Zengzhao Li" style="width:100%;display:block;border-radius:24px;border:1px solid rgba(0,0,0,0.08);" />
      </div>

      <div class="side-block">
        <div class="side-label">Current Affiliation</div>
        <div class="side-value">Shenzhen International Quantum Academy</div>
        <div class="muted">Shenzhen, China · Associate Researcher</div>
      </div>

      <div class="side-block">
        <div class="side-label">Background</div>
        <div class="muted">Fudan University · UC Berkeley · Max Planck · Lund University</div>
      </div>

      <div class="side-block">
        <div class="side-label">Research Focus</div>
        <div class="chips">
          <span class="chip">Exceptional Points</span>
          <span class="chip">Non-Hermitian Physics</span>
          <span class="chip">Open Quantum Systems</span>
          <span class="chip">Quantum Information</span>
        </div>
      </div>
    </aside>
  </div>
</section>

<section>
  <div class="container">
    <div class="section-head">
      <div>
        <h2 class="section-title">Research Snapshot</h2>
      </div>
      <div class="section-note">A concise view of the main themes developed across the site.</div>
    </div>

    <div class="grid-3">
      <div class="feature-card">
        <h3>Exceptional points and non-Hermitian dynamics</h3>
        <p>Understanding how exceptional points and non-Hermitian spectral structures generate new mechanisms for quantum dynamics, response, and control.</p>
      </div>

      <div class="feature-card">
        <h3>Open quantum systems and quantum information</h3>
        <p>Studying dissipative and non-Markovian dynamics with emphasis on quantum sensing, entanglement generation, and information processing.</p>
      </div>

      <div class="feature-card">
        <h3>Floquet engineering and quantum devices</h3>
        <p>Exploring driven quantum phases, Majorana-related phenomena, and theoretical routes toward silicon-based quantum computation and quantum simulation.</p>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="container">
    <div class="section-head">
      <div>
        <h2 class="section-title">Selected Highlights</h2>
      </div>
      <div class="section-note">Signals of background, impact, and scientific direction.</div>
    </div>

    <div class="grid-3">
      <div class="feature-card">
        <h3>International research background</h3>
        <p>Academic training and research experience across <strong>Fudan University</strong>, <strong>UC Berkeley</strong>, the <strong>Max Planck Institute for the Physics of Complex Systems</strong>, and <strong>Lund University</strong>.</p>
      </div>

      <div class="feature-card">
        <h3>High-impact research</h3>
        <p>24 papers as first or corresponding author, including work in <em>Physical Review Letters</em>, <em>Physical Review Research</em>, <em>Physical Review A</em>, <em>Physical Review B</em>, and <em>New Journal of Physics</em>.</p>
      </div>

      <div class="feature-card">
        <h3>Recognized contributions</h3>
        <p>The proposed multijunction phase-slip flux qubit was highlighted in <em>Nature Reviews Materials</em>, and recent work has clarified the role of exceptional points in entanglement generation and energy transfer.</p>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="container">
    <div class="section-head">
      <div>
        <h2 class="section-title">Featured Publications</h2>
      </div>
      <div class="section-note">A short selection on the front page, with the full list on the publications page.</div>
    </div>

    <div class="card panel">
      {% assign featured = site.publications | sort: 'year' | reverse | slice: 0, 5 %}
      {% for pub in featured %}
      <div class="pub-item">
        <div class="pub-title"><a href="{{ pub.url | relative_url }}">{{ pub.title }}</a></div>
        <div class="pub-meta">{{ pub.authors }} · <em>{{ pub.venue }}</em> {% if pub.volume %}{{ pub.volume }},{% endif %} {% if pub.pages %}{{ pub.pages }}{% endif %} ({{ pub.year }})</div>
        <div class="pub-links">
          {% if pub.paperurl %}<a href="{{ pub.paperurl }}" target="_blank" rel="noreferrer">DOI</a>{% endif %}
          {% if pub.arxiv %}<a href="{{ pub.arxiv }}" target="_blank" rel="noreferrer">arXiv</a>{% endif %}
        </div>
      </div>
      {% endfor %}
    </div>

    <div class="hero-actions" style="margin-top:18px;">
      <a class="btn primary" href="{{ '/publications/' | relative_url }}">View All Publications</a>
      <a class="btn" href="{{ '/about/' | relative_url }}">Read Full Bio</a>
    </div>
  </div>
</section>
