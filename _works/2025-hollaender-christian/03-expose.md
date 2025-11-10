# Exposé für eine Masterarbeit

## Multi-Channel Web-Integration für föderiertes Adressmanagement: Design und Implementierung einer Self-Sovereign Address Platform

---

## Problemstellung

Jeder von uns gibt seine Postadresse dutzende Male weiter -- an Online-Shops, Lieferdienste, Behörden, Banken und Versicherungen. Bei einem Umzug wird das zum Problem: Jeder einzelne Dienst muss manuell über die neue Adresse informiert werden. Dabei vergisst man unweigerlich wichtige Stellen, was zu Problemen bei der Zustellung führt oder dazu, dass wichtige Dokumente an der alten Adresse landen. Gleichzeitig hat man als Nutzer kaum Überblick darüber, wer eigentlich die eigene Adresse gespeichert hat.

Technisch betrachtet zeigt sich hier ein größeres Problem: Persönliche Daten liegen verstreut in hunderten verschiedenen Systemen, über die Nutzer praktisch keine Kontrolle haben. Das widerspricht den Prinzipien von Data Privacy und Self-Sovereign Identity, die auch in der DSGVO verankert sind. Eine föderierte Lösung könnte hier Abhilfe schaffen -- Nutzer verwalten ihre Daten zentral und geben einzelnen Diensten gezielt Zugriff.

Die zentrale technische Herausforderung liegt dabei woanders als zunächst vermutet: Die überwältigende Mehrheit der relevanten Services bietet keine APIs für Adressänderungen an. Nach meiner Einschätzung betrifft das über 95% der Dienste. Stattdessen müssen Nutzer Webformulare manuell ausfüllen, sich in Kundenportale einloggen oder Papierformulare verschicken. Ob Amazon, Sparkasse, Versicherungen oder Behörden -- bei fast allen läuft die Adressänderung über klassische Web-Interfaces ohne maschinelle Schnittstellen.

Das bedeutet: Ein System zur Automatisierung von Adressänderungen kann sich nicht auf REST-APIs oder Webhooks verlassen. Es muss mit der Realität umgehen, dass die meisten Dienste nur über Web-basierte Formulare erreichbar sind. Die Frage ist also, wie man trotzdem eine praktikable Lösung baut.

Gleichzeitig stellt sich die Frage nach der Datenhaltung: Braucht es eine zentrale Datenbank, oder gibt es Architekturen, die das Risiko von Daten-Leaks von vornherein minimieren? Wie baut man ein System, das gleichzeitig sicher, benutzerfreundlich, DSGVO-konform und realistisch integrierbar ist?

Das Sovrin Network zeigt, wohin rein technologiegetriebene Ansätze führen können. Sovrin setzte auf Blockchain für Self-Sovereign Identity, scheiterte aber an mangelnder Adoption und fehlender praktischer Integrierbarkeit. Das MainNet wurde im März 2025 eingestellt. Daraus folgt: Man braucht einen pragmatischeren Ansatz, der verschiedene Integrationslevel unterstützt und mit den realen Einschränkungen existierender Web-Systeme umgehen kann.

## Forschungsfrage

Die zentrale Forschungsfrage dieser Arbeit lautet:

*Wie lässt sich eine föderierte Adressmanagement-Plattform gestalten, die heterogene Web-basierte Integrationsmechanismen unterstützt und Nutzern Self-Sovereign Control über ihre Daten ermöglicht, während sie praktisch mit bestehenden Systemen ohne APIs funktioniert?*

Konkret sollen folgende Teilfragen beantwortet werden:

- Welche Web-basierten Integrationsmechanismen sind praktisch umsetzbar, wenn keine APIs verfügbar sind? In Betracht kommen Browser-Extensions für automatisches Formular-Ausfüllen, Headless Browser-Automation, E-Mail-Automation sowie Deep-Links zu Kundenportalen.
- Wie designt man eine Multi-Level-Integration-Architektur, die graceful degradation unterstützt -- von vollautomatischen API-Calls bis zu manuellen Anleitungen?
- Wie kann eine Browser-Extension sicher mit einem Backend kommunizieren, ohne Nutzerdaten zu kompromittieren?
- Wie lassen sich Headless Browser-Automations (ähnlich Cypress oder Playwright) für Audit-Zwecke aufzeichnen, ohne gegen Datenschutz-Richtlinien zu verstoßen?
- Welche Datenhaltungsstrategien existieren, und wie unterscheiden sie sich hinsichtlich Sicherheit und Daten-Leak-Risiko?
- Wie gestaltet man eine DSGVO-konforme Lösung, die Privacy-by-Design umsetzt?

## Vorgehen

Methodisch orientiere ich mich an einem Design-Science-Ansatz mit starkem Praxisbezug. Die Arbeit gliedert sich in mehrere Phasen:

### Phase 1: Analyse und Problemraum-Exploration

Zunächst recherchiere ich den aktuellen Stand im Bereich Self-Sovereign Identity und föderiertes Datenmanagement. Dabei betrachte ich bestehende Standards wie OAuth 2.0, OpenID Connect und W3C DID. Besonders aufschlussreich sind auch gescheiterte Ansätze wie Sovrin, um zu verstehen, welche Faktoren zum Scheitern führten.

Ein wesentlicher Schwerpunkt liegt auf der empirischen Analyse: Welche Integrationsmöglichkeiten bieten relevante Services tatsächlich an? Ich analysiere eine repräsentative Auswahl von Services aus verschiedenen Bereichen -- E-Commerce, Banken, Versicherungen, Behörden -- und dokumentiere systematisch, ob APIs existieren, welche Web-Interfaces verfügbar sind, und welche Automation-Ansätze technisch realisierbar sind.

Als Ausgangspunkt nutze ich die Requirements-Analyse, die ich bereits in einem vorherigen Kurs erarbeitet habe und die Stakeholder-Analyse, Personas, funktionale Anforderungen sowie Use Cases umfasst.

### Phase 2: Multi-Level Integration Architecture Design

Aufbauend auf den Erkenntnissen aus Phase 1 entwerfe ich eine flexible Architektur, die verschiedene Integrationslevel unterstützt:

**Level 0 -- Manual (Guided):** Das System generiert strukturierte Checklisten, Deep-Links zu Kundenportalen und vorausgefüllte E-Mail-Vorlagen. Dieser Ansatz funktioniert unabhängig von Partner-Kooperationen.

**Level 1 -- Semi-Automated:** Auf dieser Stufe werden automatisch vorausgefüllte PDF-Formulare generiert und E-Mails im Namen des Nutzers verschickt, inklusive Tracking-Funktionalität.

**Level 2 -- Browser-Assisted:** Eine Browser-Extension erkennt Adressfelder auf Webseiten und ermöglicht Auto-Fill. Ergänzend kommt Headless Browser-Automation (Playwright oder Cypress) für komplexe Login-Flows zum Einsatz. Die Automations werden per Video aufgezeichnet, sowohl für Audit-Zwecke als auch zur Fehleranalyse.

**Level 3 -- Full API Integration:** Für kooperative Services erfolgt die Integration über RESTful API Calls und Webhook-basierte Benachrichtigungen mit OAuth 2.0 Authentifizierung.

Die Architektur nutzt ein Adapter Pattern, bei dem jeder Service über einen spezifischen Adapter angebunden wird. Eine zentrale Service-Registry verwaltet, welcher Service welches Integrationslevel unterstützt.

### Phase 3: Sicherheitskonzept und Datenhaltungsstrategie

In dieser Phase untersuche ich verschiedene Ansätze für sichere Datenhaltung: zentrale Datenbank mit Verschlüsselung, Client-Side Encryption (bei der der Server nur verschlüsselte Daten verarbeitet) sowie Hybrid-Ansätze. Für jeden Ansatz bewerte ich Sicherheitsrisiken, Implementierungskomplexität und DSGVO-Compliance.

Besonderer Fokus liegt auf Zero-Knowledge-Ansätzen und der Frage, wie Browser-Extensions und Headless-Automations sicher mit dem Backend kommunizieren können. Dabei spielen Aspekte wie Content Security Policy und Cross-Origin Security eine zentrale Rolle.

### Phase 4: Implementierung eines funktionsfähigen Prototyps

Ich implementiere ein MVP mit folgenden Komponenten:

- **Web-Anwendung:** Zentrale Oberfläche zur Adressverwaltung mit Service-Verzeichnis und Status-Dashboard
- **Backend-API:** Service-Registry, Adapter-Management, verschlüsselte Datenhaltung und E-Mail-Automation
- **Browser-Extension:** Formular-Erkennung, Auto-Fill-Funktionalität und sichere Backend-Kommunikation
- **Headless Browser-Automation:** Integration von Playwright oder Cypress mit Video-Recording und Error Handling

Als Proof-of-Concept implementiere ich mindestens fünf Service-Integrationen auf verschiedenen Levels: manuelle Anleitung (beispielsweise für Behörden), E-Mail-Automation (für kleinere Versandhändler ohne Web-Portal), Browser-Extension (Amazon oder Zalando), Headless-Automation (Bank-Portal mit komplexem Login) sowie API-Integration mit einem Test-Service.

### Phase 5: Evaluation und kritische Reflexion

Den fertigen Prototyp evaluiere ich hinsichtlich der Erfolgsquote verschiedener Integrationslevel, Performance, Skalierbarkeit und Security. Ein Threat-Modeling identifiziert potenzielle Angriffsvektoren. Zusätzlich bewerte ich die Usability des Systems.

Die kritische Reflexion umfasst die Analyse, welche Aspekte gut funktioniert haben, welche Trade-offs eingegangen werden mussten, und wie sich der Ansatz im Vergleich zu Alternativen verhält.

### Phase 6: Ausblick und Generalisierung

Abschließend untersuche ich, wie sich das Konzept über Adressdaten hinaus erweitern ließe -- etwa auf Kontaktdaten, Präferenzen oder Zahlungsinformationen. Daraus entwickle ich eine Vision für eine umfassendere Self-Sovereign Personal Data Platform und diskutiere die damit verbundenen zusätzlichen Herausforderungen.

## Formales

**Geplantes Startdatum:** Ende November / Anfang Dezember 2025

**Bearbeitungsdauer:** 4 Monate

**Sperrvermerk geplant:** nein

**Externer Kooperationspartner:** nein
