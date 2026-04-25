# Exposé

## Problemfeld und Kontext
Im Kontext zunehmender Digitalisierung individueller Lebensbereiche gewinnt die visuelle Selbstbeobachtung, etwa durch Fotos oder Videos, stetig an Bedeutung. Plattformen wie soziale Netzwerke bieten zwar vielfältige Möglichkeiten zur Darstellung des Selbst, sind jedoch primär auf Außenwirkung und Bewertung ausgerichtet. Es fehlt an niedrigschwelligen, nutzerzentrierten Anwendungen, die eine strukturierte und persönliche Form der Dokumentation ermöglichen. Insbesondere fehlt es an einer fokussierten, datenschutzfreundlichen Möglichkeit zur täglichen, persönlichen Dokumentation über visuelle Selbstbeobachtung, die nicht auf Selbstdarstellung abzielt, sondern auf Reflexion und Motivation. Eine gezielte, visuell unterstützte Selbstbeobachtung über einen längeren Zeitraum kann sowohl reflektierende als auch motivierende Funktionen erfüllen. Die Herausforderung besteht darin, eine Anwendung zu gestalten, die diesen Prozess technisch zuverlässig und gestalterisch ansprechend unterstützt, ohne soziale Vergleichsdynamiken oder technische Barrieren.

## Zielsetzung
Ziel dieses Praxisprojekts ist die Konzeption und prototypische Entwicklung einer browserbasierten Web-Anwendung, die es Nutzer:innen ermöglicht, täglich ein Selfie aufzunehmen und ihren individuellen Verlauf über eine visuelle Timeline zu verfolgen. Nach einer festgelegten Anzahl an Einträgen wird aus den aufgenommenen Bildern automatisch ein animiertes Video generiert, welches die persönliche Veränderung über Zeit sichtbar macht. Die Anwendung verbindet dabei Elemente aus dem Bereich des digitalen Self-Tracking mit einer klaren, motivierenden Benutzeroberfläche.

## Aufgabenstellung
Im Zentrum steht die schrittweise Entwicklung eines funktionsfähigen Prototyps. Die Teilaufgaben umfassen:
- Anbindung der Kamera über den Browser zur Aufnahme von Selfies
- Verwaltung, Speicherung und Anzeige der Bilddaten innerhalb einer Timeline
- Implementierung eines Reminder-Systems zur Förderung der Regelmäßigkeit
- Automatisierte Erstellung eines Videos aus den erfassten Bildern
- Bereitstellung eines teilbaren Links zur Ansicht des Videos
- Berücksichtigung nutzerzentrierter Interaktions- und Gestaltungsprinzipien
Die Entwicklung erfolgt iterativ und orientiert sich an vorab definierten Erfolgskriterien für Funktionalität und Benutzerfreundlichkeit.

## Lösungsansätze
Der Lösungsansatz basiert auf einer modularen Umsetzung mit begleitender Konzeptentwicklung und gestalterischer Validierung. Einzelne technische Fragestellungen werden zunächst im Rahmen von Proof of Concepts (PoCs) erprobt, etwa zur Kameraanbindung mittels `getUserMedia()`, zur clientseitigen Verarbeitung und Vorschau von Bildern, zur Videoerstellung über FFmpeg oder zur Umsetzung des Reminder-Systems mit Node.js. <br>
Begleitend werden gestalterische Aspekte der Benutzeroberfläche mithilfe gängiger UX-Prinzipien konzipiert und getestet. Im Fokus steht eine klare, verständliche und visuell reduzierte Gestaltung, die zur täglichen Nutzung motiviert.

## Chancen und Risiken
### Chancen:
- Entwicklung eines praxistauglichen, reflexionsorientierten Tools für den Alltag
- Förderung von Motivation und Routinen durch visuelles Feedback
- Technologisch vielseitig nutzbar (Browser, mobil, offlinefähig)
- Grundlage für weiterführende Forschung im Bereich Self-Tracking und Interfacegestaltung
### Risiken:
- Unterschiedliches Verhalten von Kamera-APIs auf mobilen und Desktopgeräten
- Komplexität bei der serverseitigen Videogenerierung
- Abhängigkeit von stabiler Netzverbindung bei serverbasierten Prozessen

## Ressourcen
- **Technologien**: HTML5, JavaScript, Node.js, FFmpeg, SQLite, Docker
- **Fachliteratur & Theorie**: UX-Design, Self-Tracking, Habit-Building, visuelle Selbstwahrnehmung
- **Tools**: Figma (UI-Prototyping), GitHub (Versionierung), Markdown (Dokumentation), Docker
Rahmenbedingungen: Durchführung im Rahmen des Entwicklungsprojekts unter Betreuung von Prof. Christian Noss

