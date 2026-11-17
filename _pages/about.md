---
layout: about
title: about
permalink: /
subtitle: Scientist I, <a href="https://alleninstitute.org/" target="_blank">Allen Institute</a>

profile:
  align: right
  image:
  image_circular: false
  more_info:

selected_papers: false
social: false

announcements:
  enabled: false

latest_posts:
  enabled: false
---

<section id="about" class="home-section">
  <h2>about</h2>
  <p>Hi! I'm Maedeh, I'm a scientist at the Allen Institute in the optical physiology group.</p>
  <p>
    I'm broadly interested in how the brain processes and transforms information, from large-scale network dynamics to computations
    within individual neurons. My current research focuses on understanding how single neurons integrate and transform thousands of
    synaptic inputs into spiking outputs, using two-photon imaging and combinations of voltage, calcium, and glutamate indicators.
  </p>
  <p>
    During my doctoral research, I designed and developed microfluidic devices and combined them with in vivo calcium imaging and
    confocal microscopy to study brain-wide neural dynamics underlying decision-making and sexually dimorphic behaviors in
    <em>C. elegans</em>.
  </p>
</section>

<section id="publications" class="home-section">
  <h2>publications</h2>
  <div class="publications">
{% bibliography %}
  </div>
</section>

<section id="projects" class="home-section">
  <h2>projects</h2>
  <p><em>Placeholder: project descriptions will go here.</em></p>
</section>

<section id="cv" class="home-section">
  <h2>cv</h2>
  {% assign cv = site.data.cv.cv %}
  {% assign n = 0 %}

  <h3 class="cv-group cv-group-experience">Experience</h3>
  <div class="cv-list">
    {% for e in cv.sections.Experience %}
    <div class="cv-entry c{{ n | modulo: 10 }}">
      <div class="cv-when">{{ e.start_date }} – {{ e.end_date }}</div>
      <div class="cv-what">
        <div class="cv-title">{{ e.position }}</div>
        <div class="cv-sub">{{ e.company }}</div>
      </div>
    </div>
    {% assign n = n | plus: 1 %}
    {% endfor %}
  </div>

  <h3 class="cv-group cv-group-education">Education</h3>
  <div class="cv-list">
    {% for e in cv.sections.Education %}
    <div class="cv-entry c{{ n | modulo: 10 }}">
      <div class="cv-when">{{ e.start_date }} – {{ e.end_date }}</div>
      <div class="cv-what">
        <div class="cv-title">{{ e.studyType }}</div>
        <div class="cv-sub">{{ e.institution }}</div>
      </div>
    </div>
    {% assign n = n | plus: 1 %}
    {% endfor %}
  </div>

  <h3 class="cv-group cv-group-conferences">Conferences</h3>
  <div class="cv-list">
    {% for e in cv.sections.Conferences %}
    <div class="cv-entry c{{ n | modulo: 10 }}">
      <div class="cv-when">{{ e.label }}</div>
      <div class="cv-what">
        <div class="cv-sub cv-sub-strong">{{ e.details }}</div>
      </div>
    </div>
    {% assign n = n | plus: 1 %}
    {% endfor %}
  </div>
</section>
