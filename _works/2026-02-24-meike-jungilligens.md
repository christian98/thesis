---
layout: work-result
author: Meike Jungilligens
title: "Verbesserung der Screenreader-Unterstützung in Vuetify: Eine
  komponentenbasierte Analyse und Op- timierung der
  Accessibility-Implementierung nach WCAG 2.1"
date: 2026-02-24
result-pdf:
  - uploads/bachelorarbeit_meike_jungilligens_2026.pdf
result-repo: https://github.com/mjung2605/screenreader-a11y-in-vuetify
slideshow: false
final-presentation: Ako9qommi28
research-diary: false
type: Bachelorarbeit
status: finished
visibility: published
keywords: Digitale Barrierefreiheit, Screenreader, WCAG 2.1, Vuetify, UI-Frameworks
main-examiner: true
thumbnail: /assets/uploads/bilddoku-09-meike-jungilligens.png
---
Diese Arbeit untersucht die digitale Barrierefreiheit von UI-Komponenten in modernen Webframeworks vor dem Hintergrund des Barrierefreiheitsstärkungsgesetzes (BFSG), das ab 2025 verbindliche Anforderungen für große Teile des privaten Sektors in Deutschland schafft. Ein besonderer Fokus liegt auf der Rolle von Screenreadern, die Menschen mit Sehbehinderungen den Zugang zu Webinhalten ermöglichen.

Im Mittelpunkt der Untersuchung steht das Vue-basierte UI-Framework Vuetify (Version 3). Anhand von Accessibility-Issues im offiziellen Repository wurden vier Komponenten ausgewählt und hinsichtlich ihrer Screenreader-Kompatibilität gemäß WCAG 2.1 analysiert.
Auf Basis einer Analyse bestehender Accessibility-Patterns im Quellcode wurde ein Entscheidungsbaum entwickelt, der Entwickler dabei unterstützt, strukturierte Entscheidungen zwischen nativer HTML-Semantik und ARIA-basierten Implementierungen zu treffen. Anschließend wurden identifizierte Barrieren direkt im Quellcode behoben und mithilfe identischer Testverfahren erneut evaluiert.

Die Ergebnisse zeigen, dass sich die Screenreader-Kompatibilität der untersuchten Komponenten deutlich verbessern lässt. Alle zuvor nicht erfüllten, screenreaderrelevanten WCAG-Kriterien konnten nach der Optimierung erfüllt werden. Die entwickelten Verbesserungen wurden als Pull Requests in den Open-Source-Entwicklungsprozess von Vuetify eingebracht und zeigen, dass Barrierefreiheit in komponentenbasierten Frameworks systematische Analyse und bewusste Implementierungsentscheidungen erfordert.
