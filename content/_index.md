---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/resume.pdf
      headings:
        about: 'Biography'
        education: ''
        interests: ''
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: false

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: large # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: markdown
    content:
      title: 'My Research'
      subtitle: ''
      text: |-
        My academic journey began with a major in Statistics, where I explored a wide range of statistical methods. While deriving mathematical formulations of statistical models, I became increasingly interested in the mathematics underlying them. This led me to pursue a minor in Mathematics, where topology became my favorite subject. Hoping to connect my interests in statistics and topology, I chose Topological Data Analysis (TDA) as the topic of my undergraduate thesis.

        To deepen my mathematical knowledge, I pursued a master's degree in Mathematical Sciences at KAIST, where I continued studying mathematics alongside statistical research. During this time, I became interested in environmental epidemiology and explored the limitations of conventional two-stage methods for small-area estimation. This motivated me to investigate Bayesian hierarchical models as an alternative, leading to my master's thesis comparing the performance of these approaches.

        Throughout my research, I frequently encountered the computational challenges of Markov Chain Monte Carlo (MCMC) methods, particularly their high computational cost. While searching for more efficient approaches to Bayesian inference, I discovered Integrated Nested Laplace Approximation (INLA). This growing interest in scalable Bayesian inference eventually brought me to KAUST, where I am currently studying the mathematical structure of continuous-time structural equation models (CTSEM) to develop more efficient methods for likelihood computation.

        My interests have also expanded to artificial intelligence. A course I took during graduate school sparked my curiosity about how highly complex models can achieve remarkable predictive performance, while the theoretical reasons behind their success remain an active area of research. Fascinated by these questions, I hope to pursue research that advances our understanding of AI, both theoretically and practically. 
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - events
    design:
      view: card
  - block: markdown
    id: news
    content:
      title: 'Learning Beyond Borders'
      subtitle: ''
      text: |-
        <div style="max-width:680px; margin:30px auto;">
        <p style="text-align:center; font-size:16px; opacity:0.75; margin-bottom:40px;">
        A timeline of my international experiences in education and research.
        </p>
        <div style="border-left:2px solid #b5aa94; padding-left:28px;">
        <!-- 2010: West Kelowna -->
        <div style="position:relative; padding-bottom:40px;">
        <span style="position:absolute; left:-35px; top:7px; width:12px; height:12px; border-radius:50%; background:#a59b85;"></span>
        <div style="font-size:13px; letter-spacing:1.5px; opacity:0.65;">2010 · NOVEMBER (APPROX.)</div>
        <div style="font-size:23px; font-weight:600; margin-top:6px;">🇨🇦 West Kelowna, Canada</div>
        <div style="font-size:16px; font-weight:500; margin-top:4px;">Shannon Lake Elementary School</div>
        <div style="font-size:15px; opacity:0.8; margin-top:8px;">Attended a Canadian elementary school during the fifth grade.</div>
        </div>
        <!-- 2019: Toronto -->
        <div style="position:relative; padding-bottom:40px;">
        <span style="position:absolute; left:-35px; top:7px; width:12px; height:12px; border-radius:50%; background:#a59b85;"></span>
        <div style="font-size:13px; letter-spacing:1.5px; opacity:0.65;">2019 · SUMMER</div>
        <div style="font-size:23px; font-weight:600; margin-top:6px;">🇨🇦 Toronto, Canada</div>
        <div style="font-size:16px; font-weight:500; margin-top:4px;">English Language Program</div>
        <div style="font-size:15px; opacity:0.8; margin-top:8px;">Participated in a four-week English language program during my first year of university.</div>
        </div>
        <!-- 2026: Tokyo -->
        <div style="position:relative; padding-bottom:40px;">
        <span style="position:absolute; left:-35px; top:7px; width:12px; height:12px; border-radius:50%; background:#a59b85;"></span>
        <div style="font-size:13px; letter-spacing:1.5px; opacity:0.65;">2026 · SUMMER</div>
        <div style="font-size:23px; font-weight:600; margin-top:6px;">🇯🇵 Tokyo, Japan</div>
        <div style="font-size:16px; font-weight:500; margin-top:4px;">Asia Summer School · The University of Tokyo</div>
        <div style="font-size:15px; opacity:0.8; margin-top:8px;">Participated in a one-week international summer school.</div>
        </div>
        <!-- 2026: KAUST -->
        <div style="position:relative;">
        <span style="position:absolute; left:-35px; top:7px; width:12px; height:12px; border-radius:50%; background:#a59b85;"></span>
        <div style="font-size:13px; letter-spacing:1.5px; opacity:0.65;">2026 · SEPTEMBER — PRESENT</div>
        <div style="font-size:23px; font-weight:600; margin-top:6px;">🇸🇦 Thuwal, Saudi Arabia</div>
        <div style="font-size:16px; font-weight:500; margin-top:4px;">Visiting Student Research Program · KAUST</div>
        <div style="font-size:15px; opacity:0.8; margin-top:8px;">Conducting research on scalable Bayesian inference for continuous-time structural equation models.</div>
        </div>
        </div>
        <!-- Summary -->
        <div style="display:flex; justify-content:space-around; flex-wrap:wrap; gap:20px; border-top:1px solid #b5aa94; margin-top:40px; padding-top:24px; text-align:center;">
        <div>
        <div style="font-size:30px; font-weight:600;">3</div>
        <div style="font-size:13px; opacity:0.65;">Countries</div>
        </div>
        <div>
        <div style="font-size:30px; font-weight:600;">4</div>
        <div style="font-size:13px; opacity:0.65;">Cities</div>
        </div>
        <div>
        <div style="font-size:30px; font-weight:600;">4</div>
        <div style="font-size:13px; opacity:0.65;">Experiences</div>
        </div>
        </div>
        </div>
    design:
      columns: '1'
  - block: cta-card
    demo: true # Only display this section in the HugoBlox Kit demo site
    content:
      title: 👉 Build your own academic website like this
      text: |-
        This site is generated by HugoBlox Kit - the FREE, Hugo-based open source website builder trusted by 250,000+ academics like you.

        <a class="github-button" href="https://github.com/HugoBlox/kit" data-color-scheme="no-preference: light; light: light; dark: dark;" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star HugoBlox/kit on GitHub">Star</a>

        Easily build anything with blocks - no-code required!

        From landing pages, second brains, and courses to academic resumés, conferences, and tech blogs.
      button:
        text: Get Started
        url: https://hugoblox.com/templates/
    design:
      card:
        # Card background color (CSS class)
        css_class: 'bg-gradient-to-br from-primary-500 via-primary-600 to-secondary-600 text-white shadow-2xl'
        css_style: ''
---
