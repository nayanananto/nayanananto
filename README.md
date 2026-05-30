<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ananto Nayan Bala</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Source+Sans+3:wght@300;400;500;600&display=swap');

    :root {
      --bg:          #edeae3;
      --bg-card:     #e6e3db;
      --ink:         #1c1c1a;
      --ink-mid:     #46433c;
      --ink-soft:    #7a7670;
      --gold:        #b8965a;
      --gold-pale:   #e4d5b8;
      --rule:        #d6d2c8;
      --blue:        #0000CD;
      --green-bdr:   #06402b;
      --ff-sans:     'Source Sans 3', system-ui, sans-serif;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; font-size: 16px; }
    body {
      background: var(--bg);
      color: var(--ink);
      font-family: var(--ff-sans);
      font-weight: 400;
      line-height: 1.7;
      -webkit-font-smoothing: antialiased;
      min-height: 100vh;
      padding: 2.5rem 15%;
    }
    ::selection { background: var(--gold-pale); color: var(--ink); }
    ::-webkit-scrollbar { width: 3px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--rule); }

    /* ─── SECTION COMMON ─── */
    .cv-section {
      margin-bottom: 2rem;
      padding-bottom: 0;
    }

    /* ─── ABOUT ─── */
    .about-sub { margin-bottom: 1.75rem; }
    .about-sub:last-child { margin-bottom: 0; }

    .about-sub-title,
    .thesis-label,
    .pub-type { font-size: 15px; }

    .about-sub-title {
      font-weight: 600;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: var(--blue);
      margin-bottom: 0.75rem;
      border-bottom: 1.5px solid var(--blue);
      padding-bottom: 0.35rem;
    }
    .about-sub-text {
      font-size: 15px;
      color: var(--ink-mid);
      line-height: 1.85;
    }

    .about-edu-list { display: flex; flex-direction: column; gap: 0.4rem; }
    .about-edu-item {
      font-size: 0.92rem;
      color: var(--ink-mid);
      display: flex;
      flex-wrap: wrap;
      align-items: baseline;
      gap: 0.4rem;
    }
    .about-edu-degree { color: var(--ink); font-weight: 500; }
    .about-edu-sep { color: #000; }
    .about-edu-uni { color: #000; }
    .about-edu-gpa { color: #000; font-size: 0.85rem; }

    .about-interests { display: flex; flex-wrap: wrap; gap: 0.4rem; }
    .about-interests .tag { background: transparent; }

    .tag {
      font-family: var(--ff-sans);
      font-size: 14px;
      letter-spacing: 0.07em;
      padding: 0.18rem 0.5rem;
      background: var(--bg-card);
      border: 1px solid var(--rule);
      border-radius: 2px;
      color: #B31B1B;
    }

    /* ─── THESIS & PUBLICATIONS ─── */
    .thesis-sub { margin-bottom: 2rem; }
    .thesis-sub:last-child { margin-bottom: 0; }
    .thesis-sub .about-sub-title { margin-bottom: 0.85rem; }

    .pub-list { display: flex; flex-direction: column; gap: 0.75rem; }
    .pub-item {
      background: var(--bg-card);
      border: 1px solid var(--rule);
      border-radius: 2px;
      padding: 1.5rem 1.75rem;
    }
    .pub-type {
      font-family: var(--ff-sans);
      font-size: 15px;
      text-transform: uppercase;
      color: #05472A;
      margin-bottom: 0.25rem;
    }
    .pub-title {
      font-family: var(--ff-sans);
      font-size: 1rem;
      font-weight: 500;
      color: var(--ink);
      line-height: 1.45;
      margin-bottom: 0.2rem;
    }
    .pub-authors { font-size: 0.8rem; color: var(--ink-mid); margin-bottom: 0.15rem; }
    .pub-authors strong { color: var(--ink); font-weight: 500; }
    .pub-venue { font-size: 0.78rem; color: var(--ink-soft); font-style: italic; }
    .pub-desc { font-size: 0.82rem; color: var(--ink-mid); line-height: 1.7; margin-top: 0.5rem; }

    /* ─── PROJECTS ─── */
    .projects-grid { display: flex; flex-direction: column; gap: 0; }
    .proj-item {
      padding: 1.4rem 0;
      border-bottom: 1px solid var(--rule);
    }
    .proj-item:last-child { border-bottom: none; }
    .proj-name {
      font-family: var(--ff-sans);
      font-size: 1.02rem;
      font-weight: 500;
      color: #05472A;
      margin-bottom: 0.25rem;
    }
    .proj-desc {
      font-size: 0.83rem;
      color: var(--ink-mid);
      line-height: 1.75;
      margin-bottom: 0.6rem;
    }
    .proj-stack { font-size: 0.85rem; color: var(--blue); margin-top: 0.6rem; }
    .proj-stack-label { font-weight: 600; color: var(--ink); }
    .proj-stack-link { color: var(--blue); text-decoration: none; }
    .proj-stack-link:hover { text-decoration: underline; }

    /* ─── AWARDS ─── */
    .award-list { display: flex; flex-direction: column; gap: 0; }
    .award-item {
      display: grid;
      grid-template-columns: 120px 1fr;
      padding: 1.1rem 0;
      border-bottom: 1px solid var(--rule);
    }
    .award-item:last-child { border-bottom: none; }
    .award-year {
      font-family: var(--ff-sans);
      font-size: 15px;
      color: #000;
      letter-spacing: 0.06em;
      padding-top: 0.15rem;
    }
    .award-name {
      font-size: 15px;
      font-weight: 400;
      color: var(--ink);
      margin-bottom: 0.15rem;
    }
    .award-body { font-size: 0.8rem; color: var(--ink-soft); }

    /* ─── SKILLS ─── */
    .skills-bullet-list { list-style: none; display: flex; flex-direction: column; gap: 0; }
    .skills-bullet-item {
      display: flex;
      align-items: flex-start;
      gap: 0.75rem;
      padding: 0.85rem 0;
      border-bottom: 1px solid var(--rule);
    }
    .skills-bullet-item:last-child { border-bottom: none; }
    .skills-bullet-item::before {
      content: '•';
      color: var(--blue);
      font-size: 1rem;
      font-weight: 700;
      flex-shrink: 0;
      padding-top: 0.1rem;
    }
    .skills-bullet-head {
      font-size: 15px;
      font-weight: 600;
      color: var(--ink);
      flex-shrink: 0;
      min-width: 220px;
    }
    .skills-sub-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.15rem;
      flex: 1;
    }
    .skills-sub-list li {
      font-size: 14px;
      color: var(--blue);
      line-height: 1.6;
    }
    .skills-sub-list li::before {
      content: '· ';
      color: var(--ink-soft);
    }
  </style>
</head>
<body>

  <!-- ── 01 About Me ── -->
  <section id="about" class="cv-section">

    <div class="about-sub">
      <h3 class="about-sub-title">Education</h3>
      <div class="about-edu-list">
        <div class="about-edu-item">
          <span class="about-edu-degree">Bachelor of Science, Computer Science &amp; Engineering</span>
          <span class="about-edu-sep">·</span>
          <span class="about-edu-gpa">June 2022 – June 2026</span>
        </div>
        <div class="about-edu-item">
          <span class="about-edu-uni">Ahsanullah University of Science and Technology, Dhaka, Bangladesh</span>
          <span class="about-edu-sep">·</span>
          <span class="about-edu-gpa">GPA 3.8 / 4.0</span>
        </div>
      </div>
    </div>

    <div class="about-sub">
      <h3 class="about-sub-title">Research Interest</h3>
      <div class="about-interests">
        <span class="tag">RAG</span>
        <span class="tag">Vector Embeddings and Semantic Search</span>
        <span class="tag">Compression</span>
        <span class="tag">Multi-Agent Systems</span>
        <span class="tag">LLM</span>
      </div>
    </div>

  </section>

  <!-- ── 02 Thesis & Publications ── -->
  <section id="thesis" class="cv-section">

    <div class="thesis-sub">
      <h3 class="about-sub-title">Thesis</h3>
      <div class="pub-list">
        <div class="pub-item">
          <div class="pub-title">Embedding-Driven Wind Forecasting with Semantic Tokenization, Phase Prediction, and Human-in-the-Loop Review</div>
          <div class="pub-authors"><strong>Ananto Nayan Bala</strong></div>
          <p class="pub-desc">A wind forecasting system built on NOAA/METAR data that combines LSTM-based speed prediction with compressed semantic representations of wind states. Wind conditions are tokenized into discrete phases, and a GRU model learns to predict upcoming regimes from those tokens. A Human-in-the-Loop interface lets domain experts review, correct, and confirm forecasts — keeping a human in the decision loop for high-stakes outputs. The system also retrieves historically similar wind states and supports live data feeds.</p>
        </div>
      </div>
    </div>

    <div class="thesis-sub">
      <h3 class="about-sub-title">Publications Under Review</h3>
      <div class="pub-list">
        <div class="pub-item">
          <div class="pub-type">Conference Paper · Under review at ACM RecSys 2026</div>
          <div class="pub-title">Multi-Agent Routing as Set-Valued Prediction: A WildChat Benchmark and Cost-Aware Evaluation</div>
          <div class="pub-authors"><strong>Ananto Nayan Bala</strong>, et al.</div>
          <p class="pub-desc">Treats the problem of deciding which AI agents to route a query to as a set-valued prediction task rather than a single-choice classification. A benchmark is built from WildChat conversations, and five routing strategies — KNN, linear multilabel, dependency-aware, encoder-based, and zero-shot LLM — are compared on accuracy, utility, latency, and reproducibility. A cost-aware Weighted Agent Routing (WAR) layer is proposed to balance performance against compute cost.</p>
        </div>
        <div class="pub-item">
          <div class="pub-type">Survey · Under review at ACL ARR 2026</div>
          <div class="pub-title">From Retrieval to Reasoning: Retrieval-Augmented Generation Architectures, Strategies, and Deployment Realities</div>
          <div class="pub-authors"><strong>Partha Sarker, <b>Ananto Nayan Bala</b>, Bappy Chandra Debnath, Raduan Ahmed</strong></div>
          <p class="pub-desc">A survey of 40 RAG systems organized not by benchmark rankings but by the design problems each generation of work set out to solve. Six evolutionary groups are identified — covering foundational retrieval architectures, context-window optimization, self-correcting pipelines, graph-based multi-hop reasoning, agentic and domain-specific variants, and efficiency-focused designs. The paper traces a causal thread through the field: what broke in earlier approaches, what insight fixed it, and what gap that fix left open.</p>
        </div>
      </div>
    </div>

  </section>

  <!-- ── 04 Academic Projects ── -->
  <section id="projects" class="cv-section">
    <div class="projects-grid">

      <h3 class="about-sub-title">Projects</h3>

      <div class="proj-item">
        <div class="proj-name">Adversarial Forecasting with LSTM vs GAN-LSTM</div>
        <p class="proj-desc">Standard LSTMs tend to produce over-smoothed long-horizon forecasts. This work adds a lightweight discriminator that scores how realistic each prediction looks compared to actual sequences, pushing the LSTM toward outputs that better preserve the structural patterns in the data.</p>
        <div class="proj-stack"><span class="proj-stack-label">GitHub:</span> <a class="proj-stack-link" href="#">LSTM vs GAN-LSTM</a></div>
      </div>

      <div class="proj-item">
        <div class="proj-name">Customer Segmentation using PySpark</div>
        <p class="proj-desc">Applies unsupervised clustering to the Online Retail dataset at scale using PySpark. KMeans and Gaussian Mixture Model (GMM) are run and compared to surface distinct customer groups — distinguishing high-value repeat buyers from low-frequency occasional ones.</p>
        <div class="proj-stack"><span class="proj-stack-label">GitHub:</span> <a class="proj-stack-link" href="#">Customer Segmentation using PySpark</a></div>
      </div>

      <div class="proj-item">
        <div class="proj-name">Diabetes Prediction — Decision Tree vs KNN</div>
        <p class="proj-desc">Side-by-side comparison of a Decision Tree and a K-Nearest Neighbours classifier on a diabetes dataset, evaluating where each model's decision boundaries hold up and where they break down.</p>
        <div class="proj-stack"><span class="proj-stack-label">GitHub:</span> <a class="proj-stack-link" href="#">Diabetes Prediction</a></div>
      </div>

      <div class="proj-item">
        <div class="proj-name">Phishing Website Detection</div>
        <p class="proj-desc">A WEKA-based ML pipeline that takes raw URLs and decides whether they are phishing attempts or legitimate sites. Beyond classification, the pipeline uncovers hidden clusters in URL structure and generates human-readable rules that explain which patterns signal risk.</p>
        <div class="proj-stack"><span class="proj-stack-label">GitHub:</span> <a class="proj-stack-link" href="#">Phishing Detection</a></div>
      </div>

    </div>
  </section>

  <!-- ── 05 Awards & Achievements ── -->
  <section id="awards" class="cv-section">
    <div class="award-list">
      <h3 class="about-sub-title">Awards &amp; Achievements</h3>

      <div class="award-item">
        <div class="award-year">Ongoing</div>
        <div>
          <div class="award-name">Problem Solving Excellence — LeetCode</div>
          <div class="award-body">1000+ Problems Solved &nbsp;·&nbsp; Top 8% Content Rating<br/>500+ submission days &nbsp;·&nbsp; 11 batch milestones &nbsp;·&nbsp; Expert DSA mastery.</div>
        </div>
      </div>
      <div class="award-item">
        <div class="award-year">Spring 25<br/>Fall 24<br/>Spring 24<br/>Spring 23<br/>Fall 22</div>
        <div>
          <div class="award-name">Scholarship for outstanding academic performance</div>
          <div class="award-body">Tuition waiver for demonstrated academic excellence.</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── 06 Implementation Skills ── -->
  <section id="skills" class="cv-section">
    <ul class="skills-bullet-list">

      <h3 class="about-sub-title">Implementation Skills</h3>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">Programming</span>
        <ul class="skills-sub-list">
          <li>Python 3 (Anaconda), C, C#, Dart, C++, Java, PHP, JavaScript, MATLAB</li>
        </ul>
      </li>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">Deep Learning Libraries</span>
        <ul class="skills-sub-list">
          <li>PyTorch, NumPy, Scikit-learn, Pandas, TensorFlow-Keras</li>
        </ul>
      </li>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">Data Processing</span>
        <ul class="skills-sub-list">
          <li>Map-reduce computing, PySpark</li>
        </ul>
      </li>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">LLM, RAG Libraries</span>
        <ul class="skills-sub-list">
          <li>LangChain, LangGraph, LlamaIndex, Claude Agent SDK, OpenAI</li>
        </ul>
      </li>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">Embeddings</span>
        <ul class="skills-sub-list">
          <li>Sentence-transformers, Chroma vector database, FAISS</li>
        </ul>
      </li>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">LLM Agents Implementation &amp; Automation</span>
        <ul class="skills-sub-list">
          <li>Programming Agent context, skills, memory, scope, command</li>
        </ul>
      </li>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">Agents Integration API Frameworks</span>
        <ul class="skills-sub-list">
          <li>Python-Flask, FastAPI, Uvicorn, Pydantic</li>
        </ul>
      </li>

      <li class="skills-bullet-item">
        <span class="skills-bullet-head">Tools &amp; Platforms</span>
        <ul class="skills-sub-list">
          <li>Git, GPT Codex — Coding Agent, Jupyter Notebook, Docker, VS Code</li>
        </ul>
      </li>

    </ul>
  </section>

</body>
</html>
