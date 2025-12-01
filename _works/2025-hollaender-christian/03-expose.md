# Exposé für eine Masterarbeit

## Multi-Channel Web-Integration für föderiertes Adressmanagement: Design und Implementierung einer Self-Sovereign Address Lösung

---

## Problemstellung

Jeder von uns gibt seine Postadresse dutzende Male weiter – an Online-Shops, Lieferdienste, Behörden, Banken und Versicherungen. Bei einem Umzug wird das zum Problem: Jeder einzelne Dienst muss manuell über die neue Adresse informiert werden. Dabei vergisst man unweigerlich wichtige Stellen, was zu Zustellproblemen führt oder dazu, dass wichtige Dokumente an der alten Adresse landen. Gleichzeitig hat man als Nutzer kaum Überblick darüber, wer eigentlich die eigene Adresse gespeichert hat.

Technisch betrachtet zeigt sich hier ein größeres Problem: Persönliche Daten liegen verstreut in hunderten verschiedenen Systemen, über die Nutzer praktisch keine Kontrolle haben. Das widerspricht den Prinzipien von Data Privacy und Self-Sovereign Identity, die auch in der DSGVO verankert sind. Eine föderierte Lösung könnte hier Abhilfe schaffen – Nutzer verwalten ihre Daten zentral und geben einzelnen Diensten gezielt Zugriff.

Die zentrale technische Herausforderung liegt dabei woanders als zunächst vermutet: Die überwältigende Mehrheit der relevanten Services bietet keine APIs für Adressänderungen an. Nach meiner Einschätzung betrifft das über 95% der Dienste. Stattdessen müssen Nutzer Webformulare manuell ausfüllen, sich in Kundenportale einloggen oder sogar Papierformulare verschicken. Ob Online-Händler, Banken, Versicherungen oder Behörden – bei fast allen läuft die Adressänderung über klassische Web-Interfaces ohne maschinelle Schnittstellen.

Das bedeutet: Ein System zur Unterstützung von Adressänderungen kann sich nicht auf REST-APIs oder Webhooks verlassen. Es muss mit der Realität umgehen, dass die meisten Dienste nur über webbasierte Formulare erreichbar sind. Ein rein API-zentrierter Ansatz würde von Anfang an ins Leere laufen, weil er auf Partner-Kooperation angewiesen wäre, die in der Praxis schlicht nicht gegeben ist.

Die Lösung liegt in einem mehrstufigen Ansatz: Ein System, das auf der untersten Ebene komplett ohne externe Kooperation funktioniert, auf der mittleren Ebene Browser-basierte Automatisierung nutzt, und auf der obersten Ebene vollständige API-Integration für kooperative Partner ermöglicht. So entsteht ein System, das vom ersten Tag an Mehrwert bietet – und mit jedem neuen Partner besser wird, ohne von ihnen abhängig zu sein.

## Forschungsfrage

Die zentrale Forschungsfrage dieser Arbeit lautet:

*Wie lässt sich eine Multi-Channel-Integrationsarchitektur für föderiertes Adressmanagement gestalten, die unabhängig vom Digitalisierungsgrad externer Dienste funktioniert?*

Diese Frage adressiert den Kern des Problems: Eine Architektur zu entwickeln, die *immer* funktioniert – egal ob der externe Dienst eine moderne API anbietet, nur ein Webformular hat, oder ausschließlich per E-Mail erreichbar ist.

Zur Beantwortung dieser Frage werden folgende Teilfragen untersucht:

**Teilfrage 1 – Multi-Channel Web-Integration:**
Welche webbasierten Integrationsmuster und Frontend-Architekturen eignen sich, um Adressaktualisierungen über verschiedene Kanäle (manuell, semi-automatisch, vollautomatisch) zu ermöglichen?

**Teilfrage 2 – Browser-Extensions als Brückentechnologie:**
Wie können Browser-Extensions als semi-automatische Integrationsschicht dienen, um die Lücke zwischen rein manuellen Prozessen und API-basierten Lösungen zu schließen?

**Teilfrage 3 – Inkrementelle Adoption:**
Wie muss ein solches System gestaltet sein, damit Nutzer sofort profitieren – auch wenn zunächst nur ein Bruchteil ihrer Dienste automatisiert integriert ist?

## Vorgehen

Methodisch folge ich einem Design-Science-Research-Ansatz, bei dem die Entwicklung eines funktionsfähigen Artefakts im Mittelpunkt steht. Die Arbeit gliedert sich in fünf Phasen:

### Phase 1: Problemverständnis und Anforderungsanalyse

In dieser Phase schärfe ich das Problemverständnis und definiere die Anforderungen an das zu entwickelnde System. Als Ausgangspunkt nutze ich die Requirements-Analyse, die ich bereits in einem vorherigen Kurs erarbeitet habe. Diese umfasst eine Stakeholder-Analyse, Personas, funktionale Anforderungen sowie Use Cases.

Ergänzend analysiere ich eine repräsentative Auswahl realer Services aus verschiedenen Bereichen – E-Commerce, Banken, Versicherungen, Behörden – und dokumentiere systematisch, welche Integrationsmöglichkeiten sie tatsächlich anbieten. Diese empirische Bestandsaufnahme bildet die Grundlage für die Architekturentscheidungen in Phase 2.

Parallel dazu sichte ich den aktuellen Stand im Bereich Self-Sovereign Identity und föderiertes Datenmanagement. Der Fokus liegt dabei auf Standards und Konzepten, die für meine Architektur relevant sind – etwa OAuth 2.0, OpenID Connect und W3C Decentralized Identifiers.

### Phase 2: Architekturentwurf

Aufbauend auf den Erkenntnissen aus Phase 1 entwerfe ich eine Multi-Channel-Integrationsarchitektur mit drei Ebenen:

**Ebene 1 – Manuelle Unterstützung:** Das System generiert strukturierte Checklisten, Deep-Links zu Kundenportalen, vorausgefüllte E-Mail-Vorlagen und exportierbare PDF-Dokumente. Diese Ebene funktioniert komplett ohne Partner-Kooperation und bietet sofortigen Nutzen.

**Ebene 2 – Semi-automatisch:** Eine Browser-Extension erkennt Adressfelder auf Webseiten und ermöglicht automatisches Ausfüllen. Diese Ebene schließt die Lücke zwischen manueller Arbeit und vollständiger Automatisierung, ohne dass der externe Dienst aktiv kooperieren muss.

**Ebene 3 – Vollautomatisch:** Für Services, die APIs bereitstellen oder aktiv kooperieren möchten, wird eine Webhook-basierte Integration ermöglicht. Diese Ebene ist optional und erweitert das System, sobald Partner hinzukommen.

Die Architektur setzt auf ein Adapter-Pattern, bei dem jeder Service über einen spezifischen Adapter angebunden wird. Eine zentrale Service-Registry verwaltet, welcher Service welche Integrationsebene unterstützt. Bei Änderungen propagiert das System die neuen Daten je nach verfügbarem Kanal.

Ein wesentlicher Aspekt des Architekturentwurfs ist die Datenhaltungsstrategie. Ich untersuche verschiedene Ansätze – zentrale Datenhaltung mit Verschlüsselung, Client-seitige Datenhaltung in der Browser-Extension, sowie Hybrid-Ansätze – und bewerte sie hinsichtlich Sicherheit, Benutzerfreundlichkeit und DSGVO-Compliance.

### Phase 3: Implementierung

Ich implementiere einen funktionsfähigen Prototyp, der die Kernkonzepte der Architektur demonstriert. Der Prototyp umfasst:

Eine Web-Anwendung als zentrale Oberfläche zur Adressverwaltung, mit Service-Verzeichnis und Status-Dashboard. Ein Backend mit Service-Registry, Adapter-Management und Unterstützung für E-Mail-basierte Benachrichtigungen. Eine Browser-Extension mit Formular-Erkennung und Auto-Fill-Funktionalität.

Als Proof-of-Concept implementiere ich Service-Integrationen auf allen drei Ebenen: rein manuelle Anleitungen für Services ohne digitale Schnittstellen, E-Mail-Automation für Services mit Kontaktformularen, Browser-Extension-basiertes Ausfüllen für gängige Online-Portale, sowie exemplarisch eine vollständige API-Integration.

Der Umfang der Implementierung orientiert sich am Ziel, die Machbarkeit und das Zusammenspiel der verschiedenen Integrationsebenen zu demonstrieren – nicht daran, ein produktionsreifes System zu bauen.

### Phase 4: Evaluation

Den Prototyp evaluiere ich anhand mehrerer Kriterien. Zunächst prüfe ich die funktionale Korrektheit: Funktionieren die verschiedenen Integrationsebenen wie konzipiert? Werden Adressänderungen zuverlässig über die jeweiligen Kanäle propagiert?

Dann betrachte ich die Architekturqualität: Wie gut lässt sich das System um neue Services erweitern? Wie verhält sich das Adapter-Pattern in der Praxis? Wo liegen die Grenzen des gewählten Ansatzes?

Ein Schwerpunkt liegt auf der Sicherheitsanalyse: Welche Angriffsvektoren existieren, insbesondere im Zusammenspiel zwischen Browser-Extension und Backend? Wie robust ist die gewählte Datenhaltungsstrategie?

Schließlich reflektiere ich die Benutzbarkeit: Ist der Workflow für Nutzer nachvollziehbar? Wie wird der inkrementelle Mehrwert wahrgenommen, wenn anfangs nur wenige Services automatisiert sind?

### Phase 5: Diskussion und Ausblick

Abschließend ordne ich die Ergebnisse ein: Was hat gut funktioniert, welche Trade-offs mussten eingegangen werden, und wo stößt der gewählte Ansatz an Grenzen?

Im Ausblick skizziere ich, wie sich das Konzept über Adressdaten hinaus erweitern ließe – etwa auf Kontaktdaten, Zahlungsinformationen oder Präferenzen. Dabei diskutiere ich, welche zusätzlichen Herausforderungen bei einer Generalisierung zu einer umfassenderen Self-Sovereign Personal Data Platform entstehen würden.

---

## Formales

**Geplantes Startdatum:** Ende November / Anfang Dezember 2025

**Bearbeitungsdauer:** 4 Monate

**Sperrvermerk geplant:** nein

**Externer Kooperationspartner:** nein
