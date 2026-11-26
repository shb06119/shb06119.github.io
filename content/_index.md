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
