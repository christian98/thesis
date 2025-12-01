# Titel und Forschungsfrage

## 10 Titel-Vorschläge

1. **Multi-Channel Web-Integration für föderiertes Adressmanagement: Design und Implementierung einer Self-Sovereign Address Platform**

2. **Web-basierte Architekturen für föderiertes Adressmanagement: Konzeption und Evaluation eines Multi-Channel-Ansatzes für Self-Sovereign Identity**

3. **Zwischen Automatisierung und Nutzerkontrolle: Entwicklung webbasierter Interaktionsmuster für föderiertes Personal Data Management am Beispiel Adressänderungen**

4. **Föderierte API-Architekturen für Self-Sovereign Identity: Design, Implementierung und Evaluation eines Adressmanagement-Service mit abgestuften Integrationsmechanismen**

5. **Von statischen zu dynamischen Integrationsmustern: Eine webbasierte Plattform für nutzergesteuertes Adressmanagement in heterogenen Service-Ökosystemen**

6. **Praktikable Self-Sovereign Identity im Web: Architektur, Implementierung und Evaluation einer Multi-Level-Integrationsplattform für Adressmanagement**

7. **Architekturen für föderiertes Adressmanagement in API-losen Umgebungen: Eine Design Science Studie zu Browser-basierten Integrationstechniken für Self-Sovereign Identity**

8. **Von gescheiterten SSI-Netzwerken zu praktikablen Lösungen: Design einer webbasierten Adressmanagement-Plattform mit föderierter Datenhaltung und zentraler Orchestrierung**

9. **Abgestufte Integration für Self-Sovereign Address Services: Von manuellen Benachrichtigungen bis zur automatisierten Browser-Orchestrierung in heterogenen Web-Ökosystemen**

10. **Praktische Föderationsarchitekturen für Personal Data Management: Design, Implementierung und Evaluation eines unabhängig funktionierenden Adressänderungsdienstes**

---

## 5 Forschungsfragen

### Frage 1: Multi-Channel Web-Integration

**Hauptfrage:**
Welche webbasierten Integrationsmuster und Frontend-Architekturen eignen sich für föderiertes Adressmanagement, um unabhängig vom Digitalisierungsgrad externer Dienste nutzbar zu sein?

**Teilfragen:**
- Welche Web-Technologien (Browser-Extensions, REST APIs, WebHooks, Progressive Web Apps) können für verschiedene Integrationslevel genutzt werden?
- Wie muss eine Frontend-Architektur gestaltet sein, um sowohl manuelle als auch vollautomatische Workflows zu unterstützen?
- Welche Trade-offs existieren zwischen Client-seitiger und Server-seitiger Datenhaltung im Kontext von Self-Sovereign Identity?
- Wie können moderne Web-Standards (OAuth 2.0, OpenID Connect) für sichere, föderierte Authentifizierung genutzt werden?
- Welche Usability-Herausforderungen entstehen bei mehrstufigen Integrationssystemen, und wie können diese durch gezieltes Interaktionsdesign gelöst werden?

---

### Frage 2: Browser-Extensions & Client-Side Architecture

**Hauptfrage:**
Wie können Browser-Extensions als Semi-Automatic-Layer für föderiertes Adressmanagement dienen, um die Lücke zwischen manuellen und API-basierten Integrationen zu schließen?

**Teilfragen:**
- Welche Architekturpattern eignen sich für Browser-Extensions im Kontext von Personal Data Management?
- Wie können Content Scripts Adressformulare auf heterogenen Websites zuverlässig erkennen und befüllen?
- Welche Sicherheitsrisiken entstehen durch Browser-Extensions mit Zugriff auf persönliche Daten, und wie können diese mitigiert werden?
- Wie muss die Datensynchronisation zwischen Extension, lokalem Storage und Backend gestaltet sein?
- Welche User Experience Patterns erhöhen die Akzeptanz von Semi-Automatic-Workflows?

---

### Frage 3 (vorher Frage 4): Adoption & Transition in heterogenen Ökosystemen

**Hauptfrage:**
Wie kann ein föderiertes Adressmanagement-System inkrementell in ein Ökosystem eingeführt werden, in dem externe Dienste (Banken, Versicherungen, Behörden) unterschiedliche Digitalisierungsgrade aufweisen?

**Teilfragen:**
- Welche Transitionspfade ermöglichen Nutzern einen schrittweisen Wechsel von vollständig manueller zu teilautomatisierter Adressaktualisierung?
- Wie kann ein Hybrid-System gestaltet werden, das sowohl API-fähige als auch nicht-integrierte Dienste abdeckt?
- Welches Value Proposition motiviert Early Adopters zur Nutzung, wenn nur 20% ihrer Dienste initial automatisiert werden können?
- Wie können Netzwerkeffekte genutzt werden, um externe Dienste zur API-Integration zu motivieren?
- Welche Metriken zeigen Nutzern den inkrementellen Mehrwert (Zeitersparnis, reduzierte Fehler)?
