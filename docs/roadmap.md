---
layout: page
title: Roadmap
---

# 🛣️ Offizielle Entwicklungs-Roadmap

Dies ist der aktuelle Stand unserer geplanten und abgeschlossenen Features.

<script setup>
// 1. Die zentrale Datenstruktur für die Timeline
const timelineEvents = ref([
    { title: 'Projektstart und Basis-Setup', date: 'Q3 2025', status: 'Abgeschlossen' },
    { title: 'Dark Mode Implementierung', date: 'Q4 2025', status: 'In Arbeit' },
    { title: 'Überarbeitung der Navigation', date: 'Q1 2026', status: 'Geplant' },
    { title: 'Integration eines neuen Tools', date: 'Q2 2026', status: 'Geplant' },
    { title: 'Feature-Idee X', date: 'Zukunft', status: 'Idee' },
])

// 2. Hilfsfunktion zur Zuweisung einer CSS-Klasse basierend auf dem Status
const getClass = (status) => {
    switch (status) {
        case 'Abgeschlossen': return 'status-done';
        case 'In Arbeit': return 'status-wip';
        default: return 'status-planned';
    }
}
</script>

<div class="simple-timeline">
    <div v-for="event in timelineEvents" :key="event.title" class="timeline-event">
        <div class="timeline-dot" :class="getClass(event.status)"></div>
        
        <div class="timeline-content">
            <span class="timeline-date">{{ event.date }}</span>
            <h3 class="event-title">{{ event.title }}</h3>
            <p class="event-status">Status: **{{ event.status }}**</p>
        </div>
    </div>
</div>

<style scoped>
/* Scoped CSS sorgt dafür, dass diese Stile nur die Timeline in dieser Datei betreffen */

.simple-timeline {
    position: relative;
    padding-left: 20px; 
    /* Vertikale Linie: Die Hauptlinie der Zeitleiste */
    border-left: 3px solid var(--vp-c-divider-light);
}

.timeline-event {
    position: relative;
    margin-bottom: 30px;
    padding-bottom: 10px;
}

.timeline-dot {
    position: absolute;
    left: -11px; /* Positioniert den Punkt auf der Linie */
    top: 5px;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    /* Der Punkt wird durch die Status-Klassen gefärbt */
    background-color: var(--vp-c-bg-alt); 
    border: 3px solid var(--vp-c-bg); /* Rand, der den Punkt vom Inhalt abhebt */
    z-index: 10;
}

/* Zustandsfarben (verwenden VitePress Farb-Variablen) */
.status-done {
    background-color: var(--vp-c-green-1); /* Grün für abgeschlossen */
    border-color: var(--vp-c-green-1);
}
.status-wip {
    background-color: var(--vp-c-yellow-1); /* Gelb für in Arbeit */
    border-color: var(--vp-c-yellow-1);
}
.status-planned {
    background-color: var(--vp-c-brand-1); /* Primärfarbe für geplant/Idee */
    border-color: var(--vp-c-brand-1);
}

.timeline-content {
    padding-left: 10px;
}

.timeline-date {
    display: block;
    font-size: 0.85em;
    color: var(--vp-c-text-2);
    margin-bottom: 5px;
}

.event-title {
    margin: 0;
    line-height: 1.2;
    font-size: 1.1em;
    border-bottom: none;
}
.event-status {
    font-size: 0.9em;
    color: var(--vp-c-text-3);
}
</style>
