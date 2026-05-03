---
layout: work-result
author: Christian Holländer
related-folder: 2025-hollaender-christian
title: "Multi-Channel Web-Integration für föderiertes Adressmanagement: Design und Implementierung einer Self-Sovereign Address Lösung"
date: 2026-05-04
result-pdf: 2025-hollaender-christian/04-results/Masterarbeit-Hollaender-Christian.pdf
result-website: https://smove.pyramine.de
result-repo: https://gitlab.com/christian98-uni/masterarbeit
slideshow: false
research-diary: true
type: Masterarbeit
status: finished
visibility: published
keywords: Adressmanagement, Multi-Channel-Integration, Browser-Extension, föderierte Datenweitergabe, Self-Sovereign Identity, Datensouveränität, inkrementelle Adoption, Graceful Degradation
main-examiner: true
---
In Deutschland ziehen jährlich rund acht Millionen Menschen um – und jeder Umzug zieht eine Kaskade manueller Adressänderungen bei dutzenden Diensten nach sich. Bestehende Lösungsansätze auf Basis dezentraler Identitäten (Self-Sovereign Identity) scheiterten nicht an technischer Unreife, sondern an einem Henne-Ei-Problem: Ohne teilnehmende Dienste kein Nutzwert, ohne Nutzwert kein Anreiz zur Teilnahme.

Der wissenschaftliche Beitrag dieser Arbeit sind drei generalisierbare Architekturprinzipien: **Partnerunabhängigkeit durch abgestufte Kanalstrategie** (die unterste Stufe liefert Mehrwert ohne externe Kooperation), **zentraler Vertrauens-Provider** (Zentralisierung ermöglicht stellvertretende Authentifizierung, die ein dezentrales Modell ausschließt) und **Graceful Degradation** (explizites Sichtbarmachen von Handlungsbedarf statt stummem Versagen). Diese Prinzipien gelten über den Adressmanagement-Kontext hinaus für jede föderierte Stammdaten-Architektur.

Zur Validierung entwirft und implementiert diese Arbeit *SMove* – eine Multi-Channel-Integrationsarchitektur mit dreistufiger Kanalstrategie: Level 1 (E-Mail-Vorlagen) deckt alle Dienste ohne jede externe Kooperation ab, Level 2 (Browser-Extension) ermöglicht semi-automatische Formular-Befüllung als Brückentechnologie, Level 3 (API-Integration) demonstriert vollautomatische Erweiterbarkeit ohne Architekturänderungen.
