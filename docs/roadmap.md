---
layout: page
title: Roadmap
---

# 📅 Unsere Produkt-Roadmap (HTML/CSS)

<div class="simple-roadmap">

  <div class="roadmap-item done">
    <div class="item-date">Q3 2025</div>
    <div class="item-content">
      <h3>Projektstart und Setup</h3>
      <p>Status: **Abgeschlossen**</p>
    </div>
  </div>

  <div class="roadmap-item wip">
    <div class="item-date">Q4 2025</div>
    <div class="item-content">
      <h3>Dark Mode Implementierung</h3>
      <p>Status: **In Arbeit**</p>
    </div>
  </div>

  <div class="roadmap-item planned">
    <div class="item-date">Q1 2026</div>
    <div class="item-content">
      <h3>Überarbeitung der Navigation</h3>
      <p>Status: **Geplant**</p>
    </div>
  </div>

  <div class="roadmap-item idea">
    <div class="item-date">Q2 2026</div>
    <div class="item-content">
      <h3>Integration eines neuen Tools</h3>
      <p>Status: **Idee**</p>
    </div>
  </div>

</div>

<style scoped>
/* Verwenden Sie scoped, um Konflikte zu vermeiden */

.simple-roadmap {
    position: relative;
    padding-left: 30px; /* Platz für die Linie und die Punkte */
    /* Die Hauptlinie der Zeitleiste */
    border-left: 3px solid var(--vp-c-divider-light);
}

.roadmap-item {
    position: relative;
    margin-bottom: 40px;
    padding-left: 20px;
}

/* Der Zeitleisten-Punkt wird mit ::before erzeugt */
.roadmap-item::before {
    content: '';
    position: absolute;
    left: -18.5px; /* Muss auf der Linie positioniert werden */
    top: 5px;
    width: 15px;
    height: 15px;
    border-radius: 50%;
    background-color: var(--vp-c-bg); /* Hintergrundfarbe des Punktes */
    border: 3px solid; /* Wird später von der Status-Klasse gefärbt */
    z-index: 10;
}

/* --- Status-Farbdefinitionen --- */

.roadmap-item.done::before {
    border-color: var(--vp-c-green-1); /* Grün */
    background-color: var(--vp-c-green-1);
}

.roadmap-item.wip::before {
    border-color: var(--vp-c-yellow-1); /* Gelb/Orange */
    background-color: var(--vp-c-yellow-1);
}

.roadmap-item.planned::before,
.roadmap-item.idea::before {
    border-color: var(--vp-c-brand-1); /* Primärfarbe */
    background-color: var(--vp-c-brand-1);
}

/* --- Inhalt-Styling --- */

.item-date {
    display: block;
    font-size: 0.9em;
    font-weight: 600;
    color: var(--vp-c-brand-1);
    margin-bottom: 5px;
}

.item-content h3 {
    margin-top: 0;
    margin-bottom: 5px;
    border-bottom: none;
    line-height: 1.2;
}
</style>
