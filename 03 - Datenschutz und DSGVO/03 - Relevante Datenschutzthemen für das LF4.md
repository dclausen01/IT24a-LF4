### 1. Sicherheit der Verarbeitung (Technische und Organisatorische Maßnahmen)

Dies ist der zentrale Artikel für das Lernfeld 4, da er die Brücke zwischen rechtlichen Anforderungen und technischer Umsetzung schlägt.

- **Relevanter Artikel:** Artikel 32
    
- **Inhalt:** IT-Systeme müssen so gestaltet sein, dass ein dem Risiko angemessenes Schutzniveau gewährleistet ist. Dazu gehören konkrete Techniken wie **Pseudonymisierung** und **Verschlüsselung**.
    
- **Bezug zu Lernfeld 4:** Sie müssen Maßnahmen auswählen, die die klassischen Schutzziele der IT-Sicherheit sicherstellen, welche in der DSGVO explizit genannt werden:
    - **Vertraulichkeit** (Confidentiality)
    - **Integrität** (Integrity)
    - **Verfügbarkeit** (Availability)
    - **Belastbarkeit** der Systeme (Resilience).
        
- **Wichtig für die Praxis:** Die Maßnahmen müssen regelmäßig auf ihre Wirksamkeit überprüft und evaluiert werden.

### 2. Datenschutz-Folgenabschätzung (Risikoanalyse)

Das Lernfeld 4 fordert die Durchführung einer „Schutzbedarfsanalyse“. In der DSGVO entspricht dies der Datenschutz-Folgenabschätzung (DSFA) für risikoreiche Verarbeitungen.

- **Relevanter Artikel:** Artikel 35
- **Inhalt:** Wenn eine Form der Verarbeitung (insbesondere bei neuen Technologien) voraussichtlich ein hohes Risiko für die Rechte und Freiheiten natürlicher Personen zur Folge hat, muss vorab eine Abschätzung der Folgen durchgeführt werden.
- **Bezug zu Lernfeld 4:** Fachinformatiker müssen lernen, Risiken nicht nur technisch (Systemausfall), sondern auch im Hinblick auf die Folgen für die betroffenen Personen (Diskriminierung, Identitätsdiebstahl) zu bewerten. Eine solche Analyse ist zwingend erforderlich bei systematischer Überwachung oder der Verarbeitung besonderer Datenkategorien im großen Umfang.

### 3. Grundsätze der Verarbeitung (Die "Schutzziele")

Die DSGVO definiert Grundsätze, die als Leitplanken für jede IT-Architektur dienen.

- **Relevanter Artikel:** Artikel 5
    
- **Inhalt:**
    - **Integrität und Vertraulichkeit:** Daten müssen vor unbefugter oder unrechtmäßiger Verarbeitung sowie vor Verlust oder Zerstörung geschützt werden.
    - **Datenminimierung:** Es dürfen nur so viele Daten wie nötig verarbeitet werden.
    - **Speicherbegrenzung:** Daten dürfen nicht ewig gespeichert werden (Löschkonzepte).
        
- **Bezug zu Lernfeld 4:** Diese Grundsätze definieren die Anforderungen an das zu sichernde System. Eine Schutzbedarfsanalyse muss prüfen, ob das System diese Prinzipien einhält.
    

### 4. Privacy by Design & Privacy by Default

Für die Entwicklung und Konfiguration von IT-Systemen sind diese Konzepte essenziell.

- **Relevanter Artikel:** Artikel 25
    
- **Inhalt:**
    - **Datenschutz durch Technikgestaltung (Privacy by Design):** Datenschutz muss bereits bei der Entwicklung in die Systemarchitektur integriert werden (z. B. durch Pseudonymisierung).
    - **Datenschutzfreundliche Voreinstellungen (Privacy by Default):** Systeme müssen standardmäßig so eingestellt sein, dass nur notwendige Daten verarbeitet werden (z. B. Checkboxen dürfen nicht vor-ausgewählt sein).
        
- **Bezug zu Lernfeld 4:** Bei der Beurteilung von Software oder der Planung von IT-Lösungen müssen Fachinformatiker prüfen, ob diese Anforderungen erfüllt sind.

### 5. Umgang mit Datenpannen (Incident Management)

Teil der Datensicherheit ist der korrekte Umgang mit Sicherheitsvorfällen.

- **Relevante Artikel:** Artikel 33 und 34
- **Inhalt:** Verletzungen des Schutzes personenbezogener Daten (Data Breaches) müssen **binnen 72 Stunden** der Aufsichtsbehörde gemeldet werden, es sei denn, das Risiko für die betroffenen Personen ist gering. Bei hohem Risiko müssen auch die betroffenen Personen benachrichtigt werden.
- **Bezug zu Lernfeld 4:** In Betriebshandbüchern oder Notfallkonzepten müssen Prozesse definiert sein, wie bei Datenverlust oder Hacks reagiert wird, um diese Fristen einzuhalten.

### 6. Besondere Kategorien personenbezogener Daten (Hoher Schutzbedarf)

Für die Schutzbedarfsanalyse ist es entscheidend zu wissen, _welche_ Daten verarbeitet werden.

- **Relevanter Artikel:** Artikel 9
- **Inhalt:** Die Verarbeitung von besonders sensiblen Daten (z. B. Gesundheitsdaten, genetische/biometrische Daten, Religionszugehörigkeit) ist grundsätzlich untersagt, außer es liegen spezifische Ausnahmen vor.
- **Bezug zu Lernfeld 4:** Systeme, die solche Daten verarbeiten, haben automatisch einen **sehr hohen Schutzbedarf**. Hier müssen die Sicherheitsmaßnahmen (Art. 32) deutlich strenger ausfallen.
    

### Zusammenfassung für die Prüfungsvorbereitung
Für das Lernfeld 4 sollten Sie sich besonders auf **Artikel 32 (Sicherheit der Verarbeitung)** konzentrieren und verstehen, wie man technische und organisatorische Maßnahmen (TOMs) auswählt, um Risiken zu minimieren. Zudem sollten Sie die Verbindung zwischen der **Datenschutz-Folgenabschätzung (Art. 35)** und einer technischen Schutzbedarfsanalyse herstellen können.