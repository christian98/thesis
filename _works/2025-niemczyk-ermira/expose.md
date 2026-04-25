# Expose Bachelorarbeit

Von Ermira Niemczyk
Matrikelnummer 11117335
Studiengang Medieninformatik

Konzeption und Entwicklung einer interaktiven WebApp zur Erstellung von KI generierten Bildwelten für den Studiengang Medieninformatik 

Geplanter Zeitraum: Sommersemester 2025
                    21.05.2025 - 23.07.2025
Betreuer: Prof. Christian Noss
          Prof. Hans Kornacher

## Ausgangslage und Problemstellung

Die TH Köln steht als moderne Hochschule vor der Herausforderung, ihre vielfältigen Studienangebote und Forschungsschwerpunkte verständlich, ansprechend und zeitgemäß zu kommunizieren. Insbesondere Studieninteressierte sowie neue Studierende profitieren von visuellen Darstellungen, die ihnen Einblicke in die Lernumgebung, Inhalte und Möglichkeiten eines Studiengangs geben. Klassische Fotos oder allgemeine Illustrationen stoßen dabei schnell an ihre Grenzen, wenn es darum geht, individuelle, kontextbezogene oder zukunftsorientierte Inhalte visuell zu vermitteln.

Dank generativer Künstlicher Intelligenz, insbesondere Text-to-Image-Verfahren, eröffnen sich neue Möglichkeiten für eine flexible, fotorealistische und zugleich kontextgerechte Visualisierung. Diese Technologien können gezielt eingesetzt werden, um virtuelle Einblicke in typische Szenarien aus dem Studienalltag der Medieninformatik zu geben.

Bisher fehlt es an einem interaktiven System, das es ermöglicht, KI-generierte, ortsspezifische und fotorealistische Bilder gezielt anhand von Suchbegriffen (Prompts) aufzurufen, etwa um typische Räume, Situationen oder Lehrinhalte der TH Köln visuell darzustellen. Dozierende, Studieninteressierte oder die Hochschulkommunikation haben dadurch keine einfache Möglichkeit, passende Bildmaterialien dynamisch zu generieren oder gezielt abzurufen, z. B. um Vorträge, Infoseiten oder Präsentationen visuell zu unterstützen.

Ein besonderes Problem liegt in der Zugänglichkeit: Es fehlt ein intuitives Webtool, mit dem relevante Begriffe wie "Greenscreen", "Labor" oder "Projektraum" in einer benutzerfreundlichen Oberfläche gesucht und durch KI in ein passendes, realitätsnahes Bild der TH Köln überführt werden können. Genau hier setzt der zu entwickelte Prototyp an.

## Zielsetzung / Fragestellung des Projektes

Ziel dieser Arbeit ist die Konzeption und prototypische Umsetzung eines interaktiven Webtools, das generative Künstliche Intelligenz (insbesondere Text-to-Image-Verfahren) nutzt, um die Medieninformatik an der TH Köln visuell zu repräsentieren. Mithilfe fotorealistischer KI-Bilder sollen typische Studieninhalte sowie reale Campusbereiche wie Seminarräume oder Labore verständlich und anschaulich dargestellt werden.

Zur Erzeugung der Bilder wird insbesondere Midjourney eingesetzt, wobei ein kombinierter Ansatz verfolgt wird: Zunächst werden reale Räumlichkeiten der TH Köln fotografisch dokumentiert, insbesondere solche, in denen typische Lehr- oder Studiensituationen stattfinden. Anschließend werden diese Bilddaten als Grundlage für ein Image-to-Image-Verfahren genutzt, bei dem Personen und Räume fotorealistisch von der KI generiert werden, die unter Berücksichtigung der visuellen Identität der TH Köln wiederspiegelt.

Ein besonderer Fokus liegt auf der experimentellen Erprobung verschiedener Bildperspektiven. Vergleichsweise Frontalansicht, Vogelperspektive oder diagonale Raumtiefe. Dies dient dazu herauszufinden, wie sich unterschiedliche Perspektiven auf die Verständlichkeit, Orientierung und Wirkung der KI-generierten Darstellungen auswirken. Die Auswahl und gezielte Steuerung dieser Perspektiven erfolgt sowohl durch Prompt-Formulierungen als auch durch die Nutzung von Bildvorlagen im Image-to-Image-Prozess mit Midjourney.

Ein zusätzlicher Forschungsschwerpunkt liegt auf der Prompt-Analyse: Es wird untersucht, welche Textprompts in Midjourney notwendig sind, um bestimmte räumliche oder semantische Inhalte möglichst präzise abzubilden. Auf diese Weise soll nachvollzogen werden, wie effektiv sich KI-Bildgenerierung steuern lässt und wie realitätsnahe Darstellungen durch gezielte Promptformulierung erzielt werden können.

Der letzte zentrale Aspekt dieser Arbeit, ist die Analyse der Konsistenz von KI-generierten Bildern, über verschiedene Zeitpunkte hinweg. Dazu werden identische Prompts an mehreren aufeinanderfolgenden Tagen in Midjourney eingegeben, um zu untersuchen, ob und inwieweit sich die generierten Bilder verändern. Ziel ist es, die Reproduzierbarkeit sowie die Stabilität der Text-to-Image-Ergebnisse zu bewerten – insbesondere im Hinblick auf die Einsatzmöglichkeiten im Bereich Studiengangsvisualisierung und Hochschulkommunikation.

Es stellen sich folgende Forschungsfragen:

1. Wie beeinflusst die Wahl der Bildperspektive (Frontalansicht, Vogelperspektive etc.) die Wahrnehmung, Orientierung und Verständlichkeit von KI-generierten Visualisierungen in einem digitalen Studienorientierungstool?
2. Welche Veränderungen treten bei der wiederholten Verwendung gleicher Prompts in Midjourney im zeitlichen Verlauf auf, und welche Rückschlüsse lassen sich daraus für die Reproduzierbarkeit von KI-generierten Studieninhalten ziehen?
3. Welche Vorteile und Herausforderungen ergeben sich bei der Verwendung von Prompt-basierten Suchfunktionen zur gezielten Generierung von KI-Bildern für die Studienorientierung?

## Stand der Wissenschaft / Technik und Beriffe

### Interaktive Repräsentation der Medieninformatik
Die digitale Repräsentation von Studieninhalten ist ein zentrales Element moderner Hochschulkommunikation. Interaktive Anwendungen ermöglichen es, abstrakte Themen, Vergleichsweise Programmierung, Algorithmen oder Interface Design, zugänglich zu visualisieren und explorativ zu erleben. Besonders in der Medieninformatik, einem interdisziplinären Feld zwischen Technik und Gestaltung, bieten interaktive Visualisierungen Potenzial für eine zielgruppengerechte Ansprache (Dörner et al., 2016).

### Prototyping
Prototyping bezeichnet die iterative Erstellung und Evaluation von digitalen Systemen. Es dient dazu, frühzeitig nutzbare Versionen zu entwickeln, um Ideen zu testen, Feedback einzuholen und Anforderungen anzupassen (Rogers et al., 2011). In dieser Arbeit wird ein funktionsfähiger Webtool-Prototyp erstellt, der die technische Umsetzung und Nutzbarkeit generativer KI für die Hochschulkommunikation demonstriert.

### Webtool
Ein Webtool ist eine internetbasierte Anwendung, die direkt im Browser läuft. Solche Tools sind ortsunabhängig zugänglich und eignen sich besonders für Informationsvisualisierung und Interaktion in Bildungssettings (Preece et al., 2015). Der hier entwickelte Prototyp dient dazu, KI-generierte Bilder auf Basis von Benutzereingaben bereitzustellen.

### Text-to-Image
Text-to-Image bezeichnet ein Verfahren der generativen KI, bei dem aus einem Textprompt ein Bild erzeugt wird. Aktuelle Systeme wie Midjourney, DALL·E oder Stable Diffusion nutzen neuronale Netzwerke, um semantische Textinformationen in visuelle Darstellungen zu übersetzen (Ramesh et al., 2022). In dieser Arbeit dient das Verfahren der bildlichen Darstellung von Studieninhalten und realen Campus-Szenen, mit Hilfe von Midjourney.

### Image-to-Image
Beim Image-to-Image-Verfahren wird ein Ausgangsbild als visuelle Grundlage verwendet, das mithilfe KI-basierter Modelle transformiert oder erweitert wird, etwa durch Stilübertragung, Kontextveränderung oder fotorealistische Neukomposition (Isola et al., 2017). Diese Technik erlaubt es, reale Aufnahmen von Campusräumen mit KI zu überarbeiten und dabei inhaltlich realitätsnah zu bleiben.

### Bildperspektive
Die Perspektive eines Bildes beeinflusst seine Informationswirkung stark. Frontalansichten bieten klare Strukturen, Vogelperspektiven ermöglichen Orientierung, schräge Perspektiven erzeugen räumliche Tiefe. Studien zeigen, dass Perspektivwahl sowohl emotionale als auch kognitive Reaktionen beeinflusst (McCloud, 1993). In dieser Arbeit werden gezielt verschiedene Perspektiven getestet, um ihre Eignung für Studiengangsvisualisierungen zu analysieren.

### Generative Künstliche Intelligenz (KI)
Generative KI umfasst Modelle, die eigenständig Inhalte wie Texte, Bilder oder Audio generieren können. Dazu zählen unter anderem Generative Adversarial Networks (GANs) und Diffusionsmodelle. Solche Systeme sind in der Lage, kreative Aufgaben zu übernehmen, basierend auf gelernten Mustern aus großen Datensätzen (Goodfellow et al., 2014; Saharia et al., 2022). Im Rahmen dieser Arbeit wird generative KI eingesetzt, um neue Wege der Studiengangspräsentation und Orientierung zu ermöglichen.

## Eigene Vorgehensweise / Methoden

In dieser Arbeit wird ein exploratives, praxisorientiertes Vorgehen gewählt, um den Einsatz generativer KI zur Visualisierung der Medieninformatik an der TH Köln zu untersuchen. Die Entwicklung erfolgt in mehreren Phasen:

### Recherche und Konzeptentwicklung
Zunächst werden relevante wissenschaftliche Grundlagen zum Einsatz von generativer KI im Bildungsbereich sowie bestehende Visualisierungsansätze für Studiengänge analysiert. Auf dieser Basis wird ein inhaltliches und technisches Konzept für das Webtool erstellt.

### Datenerhebung durch Fotografie realer Räume
Anschließend werden ausgewählte Räumlichkeiten der TH Köln (z. B. Labore, Seminarräume, Aufenthaltsbereiche) fotografisch dokumentiert. Ziel ist es, reale Ausgangsmaterialien für das spätere Image-to-Image-Verfahren zu sammeln.

### Experimentelle Bildgenerierung mit Midjourney
Die aufgenommenen Bilder werden durch Midjourney über ein Image-to-Image-Verfahren fotorealistisch und symbolisch überarbeitet. Parallel werden Textprompts mehrfach zu unterschiedlichen Tageszeiten und an verschiedenen Tagen verwendet, um die Konsistenz des Outputs zu analysieren.

### Analyse und Vergleich
Die generierten Bilder werden hinsichtlich Perspektive, Ästhetik, Wiedererkennbarkeit und semantischer Genauigkeit bewertet. Auch Unterschiede zwischen Text-to-Image und Image-to-Image Ergebnissen werden analysiert.

### Prototyping des Webtools
Im Rahmen eines iterativen Prototypings wird ein Webtool entwickelt, in dem ausgewählte generierte Bilder durchsuchbar und interaktiv erkundbar sind. Dozent:innen oder Studieninteressierte können durch Begriffe gezielt Inhalte aufrufen.

### Evaluation und Reflexion
Abschließend erfolgt eine qualitative Evaluation der Bildqualität und Tool-Usability, sowie eine Reflexion des kreativen und technischen Potenzials generativer KI für die Hochschulkommunikation.

## Vorläufige Gliederung und Zeitplanung

### Gliederung

1. Einleitung
1.1 Problemstellung
1.2 Zielsetzung der Arbeit
1.3 Forschungsfragen
1.4 Aufbau der Arbeit

2. Theoretische Grundlagen
2.1 Medieninformatik und Hochschulkommunikation
2.2 Interaktive Repräsentation: Definitionen und Relevanz
2.3 Prototyping und Webtools im Bildungskontext

3. Künstliche Intelligenz und Bildgenerierung
3.1 Generative KI: Grundlagen (GANs, Diffusion Models etc.)
3.2 Text-to-Image und Image-to-Image: Vergleich und Funktionsweise
3.3 Midjourney im Einsatz: Chancen und Einschränkungen
3.4 Perspektiven in der Bildkomposition (Frontal, Vogelperspektive etc.)

4. Stand der Technik
4.1 Bestehende Tools und Projekte zur KI-Visualisierung im Hochschulbereich
4.2 Analyse vergleichbarer Anwendungen (z. B. DALL·E, DreamStudio, Artbreeder etc.)
4.3 Relevante Forschungsergebnisse und wissenschaftliche Diskurse

5. Eigene Vorgehensweise und Methodik
5.1 Datengrundlage: Eigene Bildaufnahmen der TH Köln
5.2 Auswahl der Räume und Motive
5.3 Anwendung von Midjourney (Text-to-Image & Image-to-Image)
5.4 Prompt-Vergleich über mehrere Tage: Konsistenztests
5.5 Analyse der Bildperspektiven und Bildwirkung
5.6 Toolentwicklung (Konzept, Funktion, Usability)

6. Umsetzung des Prototyps
6.1 Anforderungen und Zielgruppe
6.2 Design und technische Umsetzung (Frontend/UX)
6.3 Integration der KI-generierten Visualisierungen
6.4 Suchfunktion nach Keywords (Prompts)
6.5 Evaluation und Testlauf (z. B. mit Studierenden/Dozenten)

7. Ergebnisse und Diskussion
7.1 Erkenntnisse aus den Prompt-Tests
7.2 Analyse der visuellen Unterschiede (Tage, Perspektiven, Bildqualität)
7.3 Bewertung der Praxistauglichkeit im Hochschulkontext
7.4 Chancen und Limitationen von KI-generierten Bildern in der Studienorientierung

8. Fazit und Ausblick
8.1 Zusammenfassung der zentralen Erkenntnisse
8.2 Kritische Reflexion der Methode und Umsetzung
8.3 Potenziale für Weiterentwicklung (z. B. VR-Campus, AR-Visualisierungen, barrierefreie Tools)

9. Literaturverzeichnis (APA-Stil)

### Zeitplanung

### Woche 1: Literaturrecherche und theoretische Grundlagen

Ziel: Fundierte Basis zu den Begriffen "generative KI", "Text-to-Image", "Image-to-Image", "Prototyping" und "Bildperspektiven" schaffen.

Aufgaben:
1. Recherche zu aktuellen wissenschaftlichen Quellen.
2. Auswertung und Zusammenfassung relevanter Literatur.
3. Erste Gliederung der theoretischen Kapitel.
4. Beginn der Formulierung von Problemstellung und Zielsetzung.

### Woche 2: Konzeptentwicklung und technische Planung

Ziel: Grundlegendes Konzept für das Webtool und die KI-Experimente entwickeln.

Aufgaben:
1. Festlegen der zu visualisierenden Räume und Studieninhalte.
2. Entscheidung über technische Tools (Midjourney).
3. Entwurf des UI/UX-Konzepts für das Webtool (Skizzen, Wireframes).
4. Definition der Testmethodik: Wie und wann werden die Prompts getestet?
5. Klärung datenschutzrechtlicher Fragen bei Bildaufnahmen mit Personen.

### Woche 3: Fotografie der TH Köln – Räume und Umgebung

Ziel: Eigenes Bildmaterial erzeugen, das später durch die KI verarbeitet wird.

Aufgaben:
1. Fotografieren ausgewählter Campus-Räume (z. B. Seminarräume, Labore, Aufenthaltsbereiche).
2. Fokus auf unterschiedliche Perspektiven (Frontalansicht, Vogelperspektive, schräge Winkel).
3. Auswahl der geeignetsten Fotos für die Weiterverarbeitung.
4. Dokumentation der Aufnahmesituation (Zeitpunkt, Wetter, Licht, Perspektive).

### Woche 4: Erste Midjourney-Tests (Image-to-Image + Perspektivenanalyse)
Ziel: Erste Transformationen mit KI durchführen, Bildwirkung untersuchen.

Aufgaben:
1. Auswahl einzelner Bilder für Image-to-Image-Transformation in Midjourney.
2. Einsatz verschiedener Prompts zur Erzeugung fotorealistischer Varianten.
3. Untersuchung, wie Perspektiven (z. B. frontal vs. schräg) das KI-Ergebnis beeinflussen.
4. Dokumentation der Ergebnisse inkl. Prompt, Bildquelle und Output.

### Woche 5: Text-to-Image-Generierung & Konsistenztests
Ziel: Verlässlichkeit und Bildstil der KI analysieren.

Aufgaben:
1. Anwendung identischer Prompts an verschiedenen Tagen.
2. Vergleich der Ergebnisse auf Unterschiede bei Stil, Details und Komposition.
3. Entwicklung einer Bewertungsmatrix (z. B. Realitätsnähe, Verständlichkeit, Symbolik).
4. Auswahl der besten Ergebnisse für das Webtool.

### Woche 6: Bildvergleich & Interpretation der Unterschiede
Ziel: Analytischer Vergleich aller generierten Bilder.

Aufgaben:
1. Gegenüberstellung von Image-to-Image- und Text-to-Image-Ergebnissen.
2. Identifikation von typischen Mustern, Abweichungen, Stärken und Schwächen.
3. Bewertung, welche Varianten besonders geeignet für die Studiengangsvisualisierung sind.
4. Reflexion der Perspektivenwirkung.

### Woche 7: Prototyping des Webtools
Ziel: Funktionierender Prototyp des interaktiven Tools.

Aufgaben:
1. Entwicklung eines durchsuchbaren Webtools (z. B. nach Raum, Motiv, Prompt-Stichwort).
2. Implementierung einer simplen Benutzeroberfläche (HTML/JS oder mit Figma klickbar).
3. Integration der generierten Bilder in das Tool.
4. Test des Tools im Hinblick auf einfache Bedienbarkeit und technische Funktionalität.

### Woche 8: Usability-Tests & Tool-Anpassung
Ziel: Erste Nutzertests und Optimierung des Tools.

Aufgaben:
1. Durchführung eines kleinen Nutzertests (z. B. mit Studierenden oder Dozent:innen).
2. Sammlung von Feedback zur Navigation, Bildwahl, Verständlichkeit.
3. Optimierung von Design und Funktionalität anhand der Rückmeldungen.
4. Vorbereitung der Ergebnisdokumentation.

### Woche 9: Evaluation, Analyse & Abschluss
Ziel: Abschließende Bewertung der Ergebnisse und Fertigstellung der Arbeit.

Aufgaben:
1. Zusammenfassung der Ergebnisse: Was zeigt die KI gut? Wo sind Grenzen?
2. Reflexion: Wie kann generative KI Studieninhalte visualisieren und Kommunikation verbessern?
3. Fertigstellung der schriftlichen Arbeit (Feinschliff, Formatierung, Abgabevorbereitung).
4. Erstellung einer Präsentation (optional für Verteidigung/Kolloquium).

## Grundlegene Literatur

Moser, H., & Nake, F. (2012). Medieninformatik: Eine Einführung. Springer.
Seel, N. M. (Hrsg.). (2012). Enzyklopädie der Medienpädagogik. Springer VS.
Schnotz, W. (2014). Multimedia Learning – Theory and Research. In: R. Mayer (Hrsg.), The Cambridge Handbook of Multimedia Learning. Cambridge University Press.
Goodfellow, I., Bengio, Y., & Courville, A. (2016). Deep Learning. MIT Press.
Kietzmann, J., Paschen, J., & Treen, E. (2018). Artificial intelligence in advertising: How marketers can leverage AI. Journal of Advertising Research, 58(3), 263–267.
Floridi, L. (2019). The Logic of Information: A Theory of Philosophy as Conceptual Design. Oxford University Press.
Boehm, G. (2007). Wie Bilder Sinn erzeugen. Berlin University Press.
Kepes, G. (1944). Language of Vision. Dover Publications.
Arnheim, R. (2004). Kunst und Sehen: Eine Psychologie des schöpferischen Auges. de Gruyter.
Jäger, S. (2015). Bildperspektiven – Theorie und Analyse visueller Kommunikation. UVK Verlag.
Preece, J., Rogers, Y., & Sharp, H. (2015). Interaction Design: Beyond Human-Computer Interaction. Wiley.
Garrett, J. J. (2011). The Elements of User Experience: User-Centered Design for the Web and Beyond. New Riders.
Tidwell, J. (2020). Designing Interfaces: Patterns for Effective Interaction Design. O’Reilly.
Ramesh, A. et al. (2021). Zero-Shot Text-to-Image Generation.
Saharia, C. et al. (2022). Photorealistic Text-to-Image Diffusion Models with Deep Language Understanding. 
Nichol, A. et al. (2022). GLIDE: Towards Photorealistic Image Generation and Editing with Text-Guided Diffusion Models.
Ho, J. et al. (2020). Denoising Diffusion Probabilistic Models. NeurIPS.

## Literaturverzeichnis
Dörner, R., Broll, W., Grimm, P., & Jung, B. (2016). Virtual and Augmented Reality (VR/AR). Springer.
Goodfellow, I., Pouget-Abadie, J., Mirza, M., Xu, B., Warde-Farley, D., Ozair, S., Courville, A., & Bengio, Y. (2014). Generative adversarial nets. Advances in Neural Information Processing Systems, 27, 2672–2680.
Isola, P., Zhu, J. Y., Zhou, T., & Efros, A. A. (2017). Image-to-image translation with conditional adversarial networks. In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (pp. 1125–1134).
McCloud, S. (1993). Understanding Comics: The Invisible Art. Harper Perennial.
Preece, J., Rogers, Y., & Sharp, H. (2015). Interaction Design: Beyond Human-Computer Interaction (4th ed.). Wiley.
Ramesh, A., Dhariwal, P., Nichol, A., Chu, C., & Chen, M. (2022). Hierarchical Text-Conditional Image Generation with CLIP Latents. arXiv preprint arXiv:2204.06125.
Rogers, Y., Sharp, H., & Preece, J. (2011). Interaction Design: Beyond Human-Computer Interaction (3rd ed.). Wiley.
Saharia, C., Chan, W., Saxena, S., Li, L., Salimans, T., Ho, J., & Fleet, D. J. (2022). Photorealistic Text-to-Image Diffusion Models with Deep Language Understanding. arXiv preprint arXiv:2205.11487.
