# PROTOCOL.md: Skill-Driven Development Ökosystem

**Languages:** [English](PROTOCOL.md) · [Русский](PROTOCOL_ru.md) · [العربية](PROTOCOL_ar.md) · [中文](PROTOCOL_zh.md) · **Deutsch** · [Español](PROTOCOL_es.md) · [Français](PROTOCOL_fr.md) · [日本語](PROTOCOL_ja.md) · [한국어](PROTOCOL_ko.md) · [Português](PROTOCOL_pt.md)

## 1. Konzept und Philosophie

Dieses Dokument beschreibt die Entwicklungsmethodik innerhalb des Portfolios, angepasst an ein hybrides Agenten-Ökosystem. Das Protokoll deckt den gesamten Produktlebenszyklus ab — vom ersten Architekturentwurf bis zur finalen Generierung von Präsentationsartefakten.

Kernprinzip: **Architekturentscheidungen müssen explizit, reproduzierbar und vertretbar sein.** Wir haben uns vom reinen Schreiben von Code hin zu **Skill-Driven Development** (kompetenzbasierter Entwicklung) entwickelt, bei dem Routineaufgaben, Design, Tests und Analysen an spezialisierte Skills bestimmter Agenten delegiert werden.

---

## 2. Rollen und Skill-Verteilung

Drei Hauptakteure und die einheitliche Agentenumgebung sind an diesem Prozess beteiligt. Ihre Rollen sind streng voneinander getrennt und überschneiden sich nicht.

### 2.1. Developer (Mensch)
Der Product Owner. Hat das letzte Wort bei jeder Architekturentscheidung, genehmigt den Scope, legt die Entwicklungsrichtung fest und nimmt die Lieferergebnisse der Agenten ab.

### 2.2. OpenCode (Autonomer Umsetzer)
Der ausführende Agent, der im Terminal mit einem Kontextfenster von bis zu 1 Mio. Token arbeitet. Verantwortlich für das Schreiben von Code, den Aufbau von Benutzeroberflächen sowie die Erstellung von Dokumenten und Medienartefakten.
Verfügt über folgendes Skill-Arsenal:
*   **Engineering und Code:** `code-review-skill`, `webapp-testing`, `mcp-builder`, `skill-creator`, `claude-api`.
*   **Design und Frontend:** `frontend-design`, `web-artifacts-builder`, `theme-factory`, `canvas-design`, `algorithmic-art`, `brand-guidelines`.
*   **Dokumentation und Office:** `build-project-docs`, `doc-coauthoring`, `docx`, `pdf`, `pptx`, `xlsx`.
*   **Kommunikation und Schulung:** `academy-guide`, `internal-comms`, `slack-gif-creator`, `discernment-nudge`.

### 2.3. Claude Desktop (Architekt und Analyst)
Agiert als Rechenzentrum und Architekturprüfer. Schreibt keinen produktiven Code direkt, sondern verifiziert Logik, analysiert Datenbankdaten und formuliert Aufgaben für OpenCode.
Skill-Arsenal:
*   **Kontextverwaltung:** `morning`, `Import-memory`, `skill-creator`, `doc-coauthoring`.
*   **Analytik und Validierung:** `analyze`, `data-context-extractor`, `explore-data`, `validate-data`, `statistical-analysis`.
*   **Datenbank und Datenvisualisierung:** `sql-queries`, `write-query`, `build-dashboard`, `create-viz`, `data-visualization`.

### 2.4. Antigravity (Einheitliche Agentenumgebung)
Eine vollautonome Umgebung, die das gesamte Set aus 33 Skills integriert.
*   **Schlüsselregel:** Alle Projektdokumentationen müssen ab sofort ausschließlich über Antigravity erstellt und gepflegt werden, unter Verwendung der Gemini- und Claude-Modelle (als den führenden Dokumentationswerkzeugen mit uneingeschränktem Zugriff auf Skills).

---

## 3. Protokollphasen (Projektlebenszyklus)

### Phase 1: Initialisierung und ARCHITECTURE.md
Die Architektur wird formuliert, bevor eine einzige Zeile Code geschrieben wird.
1.  **Claude Desktop** aktiviert die Skills `morning` und `Import-memory`, um den Kontext und frühere Arbeiten zu laden. Anschließend wendet er `analyze` an, um die Anforderungen zu zerlegen.
2.  **OpenCode** verwendet `build-project-docs`, um einen Entwurf von `ARCHITECTURE.md` zu erstellen.
3.  Das Dokument verfestigt sich: Datenstrukturen, Speicherformate, Tech-Stack und Modulaufteilung.

### Phase 2: Grill-me (Architektur-Stresstest)
Architektur wird nicht auf Glauben übernommen. Sie muss angegriffen und hinterfragt werden.
1.  **Claude Desktop** wendet `data-context-extractor` an, um „blinde Flecken“ in den Daten zu identifizieren, und `doc-coauthoring`, um unbequeme Fragen zu generieren.
2.  **OpenCode** kann `discernment-nudge` für eine kritische Selbsteinschätzung der vorgeschlagenen technischen Lösungen nutzen.
3.  Jeder strittige Entscheidungspunkt wird durch eine Triade abgeschlossen: **gewählte Lösung -> Grund für die Ablehnung der Alternative -> Ausschlüsse aus dem Scope**.

### Phase 3: Deliberate Deviations (Bewusste Abweichungen)
Ein Abschnitt in `ARCHITECTURE.md`, in dem wir alle Features und Fähigkeiten festhalten, die wir **bewusst nicht bauen**. Die Grenzen der Fähigkeiten eines Projekts sind ein vollwertiger Teil seiner Architektur. Wenn sich eine Entscheidung während der Entwicklung ändert, wird die alte Entscheidung zusammen mit der Begründung hierher verschoben.

### Phase 4: Modul-für-Modul-Implementierung
Die Entwicklung erfolgt von unten nach oben entlang des Abhängigkeitsgraphen.
1.  **OpenCode** implementiert den Projektkern. Für Integrationen und Protokolle werden `mcp-builder` und `claude-api` genutzt.
2.  Bei der Arbeit an der visuellen Seite aktiviert **OpenCode** die Kette: `brand-guidelines` -> `theme-factory` -> `frontend-design` -> `web-artifacts-builder`.
3.  Für die prozedurale Grafikgenerierung oder komplexe Canvas-Elemente werden `algorithmic-art` und `canvas-design` angewendet.

### Phase 5: Code-Review & Tests
Die Verifizierung ist immer vom Schreiben des Codes getrennt.
1.  **OpenCode** führt einen separaten Durchgang mit `code-review-skill` durch, um Fehler und Kompromisse zu identifizieren.
2.  UI- und Integrationstests werden über den Skill `webapp-testing` durchgeführt. Die Testausgabe (stdout/stderr) wird ohne Änderungen gespeichert.
3.  **Claude Desktop** schaltet sich ein, um die Datenverarbeitung zu überprüfen: Er verwendet `sql-queries` und `write-query`, um die Datenbankintegrität zu prüfen, sowie `validate-data` und `statistical-analysis`, um die Geschäftslogik zu verifizieren.

### Phase 6: Artefakt- und Analysengenerierung
Das Projekt muss dem Benutzer oder den Stakeholdern präsentiert werden.
1.  **Claude Desktop** erstellt mithilfe von `build-dashboard`, `create-viz` und `data-visualization` Berichte basierend auf den Anwendungsergebnissen oder Metriken.
2.  **OpenCode** verpackt diese Daten in fertige geschäftliche Artefakte:
    *   Berichte und Spezifikationen: Skills `pdf`, `docx`, `xlsx`.
    *   Architekturpräsentationen: Skill `pptx`.
    *   Schulungs- und interne Materialien: `academy-guide`, `internal-comms`.
    *   Dynamische Inhalte für Ankündigungen: `slack-gif-creator`.

### Phase 7: Finale Checkliste
Vor dem Release wird Folgendes überprüft:
*   Synchronisation des finalen Codes mit `ARCHITECTURE.md`.
*   Vorhandensein tatsächlicher Testprotokolle.
*   Fehlen temporärer Dateien, Caches und geheimer Schlüssel.

---

## 4. Richtlinie zur Modellauswahl (Model Selection Policy)

OpenCode läuft auf kostenlosen Modellen, deren Auswahl durch die Aufgabe bestimmt wird:

| Modell | Rolle | Zweck | Datenschutzstatus |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.2 Free** | Autonomer Agent (Core) | Ausführung der Haupt-Skill-Matrix, 1 Mio. Token Kontext, mehrstufige Logik im Terminal. | Dauerhaft kostenloser Tarif |
| **Nemotron 3 Ultra Free** | Tiefer Analyst | Komplexe Mathematik, anspruchsvolle Algorithmen, groß angelegtes System-Refactoring. | **NVIDIA Trial** — Daten werden protokolliert, um das Produkt zu verbessern. |
| **Nemotron 3.5 Lightning Free** | Hintergrund-Executor | Schnelle Validierung, utilitäre Funktionsaufrufe, Massenverarbeitung. | **NVIDIA Trial** — wie Ultra. |
| **MiMo V2.5 Free** | UI/UX Assistent | Screenshot-Debugging, spontanes `frontend-design`. | Temporärer kostenloser Zeitraum. |

Für **Antigravity** wird **Gemini 3.5 Flash (Medium)** als primäre Engine verwendet, um einen minimalen Verbrauch von Limits/Quoten zu gewährleisten und ein kontinuierliches Arbeiten an Aufgaben und Dokumentationen zu ermöglichen.

**Sicherheitsbeschränkung:** Es ist **strengstens verboten**, private Schlüssel, Token, echte Datenbanken und private Repositories an Trial-Endpunkte (Nemotron, MiMo) zu übergeben. Für sensible Daten wird ausschließlich eine lokale oder vertrauenswürdige Umgebung verwendet.

---

## 5. Kernprinzipien des Ökosystems

1. **Eine explizite Entscheidung ist besser als ein bequemer Standard.** Wenn ein Agent an eine Weggabelung stößt, rät er nicht, sondern formuliert Optionen und wartet auf die Genehmigung (oder protokolliert einen Kompromiss).
2. **Skills werden für ihren beabsichtigten Zweck verwendet.** Es ist nicht erforderlich, Markdown-Tabellen zu erstellen, wenn ein Excel-Bericht benötigt wird (nutzen Sie `xlsx`). Ein Dashboard muss nicht in Text beschrieben werden (nutzen Sie `build-dashboard` + `create-viz`).
3. **Ein im Review gefundener Fehler bedeutet ein funktionierendes System.** Ein Fund in der Review-Phase über `code-review-skill` ist der Beweis, dass der zweistufige Filter funktioniert.
4. **Projektgrenzen sind unantastbar.** Ein halbfertiges Alleskönner-Werkzeug ist schlechter als ein hochspezialisiertes Werkzeug mit einem klar dokumentierten Abschnitt für bewusste Abweichungen (Deliberate Deviations).
