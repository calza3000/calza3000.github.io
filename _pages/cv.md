---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D. in Information Engineering (Bioengineering curriculum), University of Padova, 2024 (expected)
* M.S. in Bioengineering, University of Padova, 2024
* B.S. in Biomedical Engineering, University of Padova, 2022

Work experience
======
* Nov 2024 - Today: Ph.D. Student
  * University of Padova, Department of Information Engineering
  * Topic: “Enhancing type 1 diabetes care: A deep learning-powered clinical decision support system for proactive therapeutic interventions using explainable blood glucose forecasting”.
  * Supervisor: Prof. Andrea Facchinetti; Co-supervisor: Prof. Giacomo Cappon

* Feb 2022 - May 2022: Research Intern
  * University of Padova, Department of Information Engineering
  * Systems Biology and Bioinformatics Group (SysBioBig)
  * Supervisor: Prof. Massimo Bellato

Skills
======
* **Languages:** Italian (Mother tongue), English (C1), French (A2), Spanish (A2)
* **Digital Skills:**
  * **Advanced:** Matlab, R, Python
  * **Intermediate:** LaTeX, Microsoft Office Package, Git/GitHub, Simulink
  * **Basic:** SLURM Job Scheduler, SQL

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
