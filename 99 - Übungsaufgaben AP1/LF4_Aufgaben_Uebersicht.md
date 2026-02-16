# LF4-Aufgaben in IHK AP1-Prüfungen (Fachinformatiker)

## Themengebiete LF4

- Datenschutz (DSGVO, BDSG)
- IT-Grundschutz (BSI IT-Grundschutz-Kompendium)
- Schutzbedarfsfeststellung / Schutzbedarfsanalyse
- Schutzziele (Vertraulichkeit, Integrität, Verfügbarkeit)
- Verschlüsselung, Passwortsicherheit, Datensicherung
- Phishing, IT-Sicherheitsmaßnahmen

---

## Herbst 2021 (29.09.2021)

### Aufgabe 4 - Datenschutz und Datensicherheit (24 Punkte)

**Kontext:** Arztpraxis Care - IT.SYS GmbH soll Datenschutz und Datensicherheit gewährleisten.

#### 4a) Schutzziele zuordnen (6 Punkte)

Schutzziele Vertraulichkeit, Integrität und Verfügbarkeit sollen Sicherheitsmaßnahmen zugeordnet werden (pro Zeile ein Kreuz + Begründung):
| Sicherheitsmaßnahme                                 | V   | I   | VF  | Begründung                                               |
| --------------------------------------------------- | --- | --- | --- | -------------------------------------------------------- |
| Sichere Passwörter wählen                         | X   |     |     | Zugriff Fremder auf Benutzerdaten wird besser geschützt |
| Regelmäßige Datensicherung der Patientendaten     |     |     |     | (zu ergänzen)                                           |
| Verschlüsselung der Festplatten                   |     |     |     | (zu ergänzen)                                           |
| Zentrale Bearbeitung wichtiger Dokumente auf Server |     |     |     | (zu ergänzen)                                           |
| Hashwertüberprüfung bei Softwareinstallation      |     |     |     | (zu ergänzen)                                           |

#### 4b) BSI IT-Grundschutz-Kompendium: Basis-Anforderungen PC-Client (2 Punkte)

Je eine Maßnahme nennen für:

- Aktivieren von Autoupdate-Mechanismen
- Differenzieren von Benutzerrollen (Rollentrennung)

#### 4c) Schutzbedarfsanalyse (6 Punkte)

Schutzbedarfskategorien:

- Niedrig bis mittel: Schadensauswirkungen begrenzt und überschaubar
- Hoch: Schadensauswirkungen können beträchtlich sein
- Sehr hoch: Schadensauswirkungen können existenziell bedrohliches Ausmaß erreichen
Begründung für gewählten Schutzbedarf ergänzen:
| IT-Anwendung                                                           | Schutzziel      | Kategorie | Begründung                                                           |
| ---------------------------------------------------------------------- | --------------- | --------- | --------------------------------------------------------------------- |
| Prüfziffernverfahren bei Übermittlung der Krankenversicherungsnummer | Integrität      | hoch      | z.B.: Verfälschte Daten können zu fehlerhaften Abrechnungen führen |
| Textverarbeitung                                                       | Verfügbarkeit   | mittel    | (zu ergänzen)                                                        |
| Software zur telemedizinischen Beratung über Videokonferenz           | Vertraulichkeit | hoch      | (zu ergänzen)                                                        |
| Patientendatenverarbeitung                                             | Integrität      | sehr hoch | (zu ergänzen)                                                        |

#### 4d) Besonderer Schutz personenbezogener Daten (2 Punkte)

Für welche Art von Daten ist ein besonderer Schutz gesetzlich vorgeschrieben? Rechtliche Grundlage benennen.
#### 4e) Kriterien für sichere Passwörter (4 Punkte)
Zwei Kriterien angeben, die ein sicheres Passwort erfüllen sollte. Beschreiben, warum diese Kriterien für höhere Sicherheit sorgen.

#### 4f) Risiken der Datensicherung auf gleicher Festplatte (4 Punkte)

Gebührenabrechnungssoftware sichert freitags auf separater Partition derselben Festplatte.

- **4fa)** Zwei Risiken beschreiben (2 Punkte)
- **4fb)** Konkreten Verbesserungsvorschlag unterbreiten (2 Punkte)

---

## Frühjahr 2022 (30.03.2022)

### Aufgabe 3b - WLAN-Authentifizierung (3 Punkte) - tangential LF4

**Kontext:** AllRound AG - Netzwerkzugriff für Notebook ins Firmen-WLAN.
WPA-PSK vs. EAP/WPA-Enterprise-RADIUS: Vor-/Nachteil und Empfehlung für Unternehmensgröße.
| Verfahren                 | Vorteil            | Nachteil                                    | Unternehmensgröße |
| ------------------------- | ------------------ | ------------------------------------------- | ------------------- |
| WPA-PSK                   | Einfach umzusetzen | Unsicher, da PW schnell bekannt werden kann | Kleine Unternehmen  |
| EAP/WPA-Enterprise-RADIUS | (zu ergänzen)     | (zu ergänzen)                              | (zu ergänzen)      |

> **Hinweis:** Diese Aufgabe ist nur tangential LF4-relevant (Netzwerksicherheit/Authentifizierung). Der Schwerpunkt liegt auf Netzwerktechnik.

---

## Frühjahr 2023 (01.03.2023)

### Aufgabe 3 - Datenschutz und Datensicherheit (24 Punkte)

**Kontext:** SecuRita AG (Finanzsektor) - Neustrukturierung der Arbeitsplätze unter Beachtung von Datensicherheit und Datenschutz.

#### 3a) Schalenmodell Betriebssystem (4 Punkte)

Funktionsebenen eines PCs: Schichten-/Schalenmodell. Eine Schicht oberhalb und eine unterhalb des Betriebssystems benennen. Funktion der benannten Schichten beschreiben.

#### 3b) BSI - Sicherheit auf Betriebssystemebene (12 Punkte)

Bezug auf BSI-Information zu Angriffen auf Windows 10 und SiSyPHuS-Studie.

- **3ba)** Zwei allgemeine Aufgaben des BSI nennen (2 Punkte)
- **3bb)** Begriff „Härung“ eines Betriebssystems erläutern (2 Punkte)
- **3bc)** Zwei Beispiele für eine Härung eines Betriebssystems nennen (2 Punkte)
- **3bd)** Zwei Systemwerkzeuge („Bordmittel“) des Betriebssystems nennen, mit denen IT-Sicherheit erhöht werden kann (2 Punkte)
- **3be)** Beschreiben, wozu Gruppenrichtlinien auf einem Arbeitsplatzrechner eingesetzt werden können (4 Punkte)

#### 3c) Protokollierung und Datenschutz (8 Punkte)

BSI-Empfehlungen zur Konfiguration der Protokollierung von Aktivitäten.
- **3ca)** Beschreiben, inwiefern Protokollierung (Logging) zur Erhöhung der IT-Sicherheit beitragen kann (4 Punkte)
- **3cb)** Besondere Anforderungen an den Datenschutz bei der Protokollierung beschreiben (4 Punkte)

---

## Herbst 2023 (19.09.2023)

### Aufgabe 3 - Datenschutz und IT-Sicherheit (22 Punkte)

**Kontext:** OptiSoft-XXL GmbH - Firmeneigener Laptop als Telearbeitsplatz, Schutz der Kundendaten.

#### 3a) Gesetzliche Grundlagen Datenschutz (2 Punkte)

Zwei in Deutschland für den Datenschutz relevante gesetzliche Grundlagen nennen.

#### 3b) BSI-Anforderungen Telearbeit (4 Punkte)

BSI gibt Anforderungen zum Schutz von Informationen für Telearbeit vor. Je ein Beispiel für technisch-organisatorische Maßnahme:

| Bereich                               | Maßnahme |
| ------------------------------------- | -------- |
| Zugriffsschutz auf mobile Datenträger |          |
| Verschlüsselung der lokalen SSD       |          |
| Zutrittsschutz Telearbeitsplatz       |          |
| Sichere Anmeldung am Laptop           |          |
| Sichere Datenkommunikation            |          |
| Transport von Datenträgern            |          |

#### 3c) Verschlüsselung mit TPM (11 Punkte)
Lokale SSD verschlüsseln mit Trusted Platform Module (TPM). Passwort beim Start, Wiederherstellungsschlüssel getrennt aufbewahrt.
- **3ca)** Zwei Kriterien für ein sicheres Passwort nennen (2 Punkte)
- **3cb)** Sicherung des Wiederherstellungsschlüssels - Vorteile/Nachteile verschiedener Verfahren beurteilen (3 Punkte):
  - Auf PC in Textdatei speichern
  - In Cloud-Speicher hochladen
  - Auf USB-Stick speichern
  - Wiederherstellungsschlüssel ausdrucken
- **3cc)** Schutzziele Vertraulichkeit und Integrität: Was bedeutet dies bezogen auf Daten der SSD? (4 Punkte)
- **3cd)** Verschlüsselungssystem bei Diebstahl des Laptops beurteilen (2 Punkte)

#### 3d) VPN und digitales Zertifikat (5 Punkte)

Sichere Verbindung vom Telearbeitsplatz zum Firmennetz.

- **3da)** Sicherheitstechnischen Vorteil eines VPN beschreiben (2 Punkte)
- **3db)** Identifizierung mithilfe des digitalen Zertifikats beschreiben (3 Punkte)

---

## Frühjahr 2024 (Februar 2024)

### Aufgabe 4 - IT-Sicherheit und Datenschutz (26 Punkte)

**Kontext:** KustoFlex GmbH - Neuer Mitarbeiter Herr Mueller arbeitet mit hauseigenem CAD-Programm, ist beim Kunden vor Ort tätig, leistungsfaehiger Laptop mit lokaler Festplatte. Grosse Rechenleistung und hoher Speicherbedarf fuer Konstruktionszeichnungen.
#### 4a) Maßnahmen zur Gewährleistung der Geheimhaltung (6 Punkte)
Herr Mueller ist mit Bus/Bahn und an öffentlichen Plätzen unterwegs. Maßnahmen/Verhaltensweisen zur Gewährleistung der Geheimhaltung nennen, besondere Vorsichtsmaßnahmen erforderlich.

| Maßnahmen oder Verhaltensweisen         | Folge der Nichtbeachtung                                |
| ---------------------------------------- | ------------------------------------------------------- |
| Beispiel: Nutzung einer Blickschutzfolie | Bildschirminhalt kann von Unberechtigten gelesen werden |
| (zu ergänzen)                           | (zu ergänzen)                                          |
#### 4b) VPN-Funktionalität (2 Punkte)
Herr Mueller sichert seine Daten möglichst auf dem Server der KustoFlex GmbH über VPN.
Funktionalität des Begriffs VPN erläutern.

#### 4c) Datensicherung auf externen Festplatten (3 Punkte)

Herr Mueller kritisiert, dass im Aussendienst nicht immer eine stabile Internetverbindung zur Verfügung steht. Nach den Sicherheitsrichtlinien der KustoFlex GmbH sind für lokal gespeicherte Daten Tagessicherungen auf mehreren (nummerierten) externen Festplatten vorgesehen.
Drei Punkte nennen, die bei lokal gespeicherten Daten mithilfe von externen Festplatten zu beachten sind, wenn die Daten möglichst zuverlässig gesichert werden sollen. Datensicherheitsaspekte berücksichtigen.

#### 4d) Malware (6 Punkte)

- **4da)** Drei Arten von Malware nennen (3 Punkte)
- **4db)** Den in Aufgabe 4da) genannten Arten jeweils ein spezifisches Merkmal zuweisen (3 Punkte)

#### 4e) Schutz vor Malware (3 Punkte)

Eine Antivirensoftware ist bereits auf dem Laptop installiert.
Drei weitere organisatorische oder technische Empfehlungen erläutern, wie man sich vor Malware schützen kann.
#### 4f) Übertragungsdauer berechnen (6 Punkte)

Speedtest-Ergebnis: Download 75,78 Mbps, Upload 50,02 Mbps.
Übertragungsdauer für 1 GiB Datenumfang berechnen (auf volle Sekunden runden, Ergebnis in Minuten und Sekunden).

> **Hinweis:** Aufgabe 4f ist nicht LF4-relevant (Netzwerktechnik/Berechnung), aber Teil der Gesamtaufgabe 4.

---

## Herbst 2024 (17.09.2024)

### Aufgabe 1 - BSI IT-Grundschutz Besprechungsraum (teilweise LF4, 10 Punkte)

**Kontext:** Identify OHG - Herstellung elektronischer Schlüsselsysteme und Ausweise, höchste Sicherheitsanforderungen.

#### 1a) Zutrittskontrolle (3 Punkte)

Absicherung eines Besprechungsraums: Automatische Zutrittskontrolle an der Eingangstür.
Drei technische Möglichkeiten nennen, um eine automatische Zutrittskontrolle zu gewährleisten.

#### 1b) Sicherheitsrisiken (3 Punkte)

Sicherheitsrisiken folgender Situationen beschreiben:

| Situation                                                          | Sicherheitsrisiko                                                                      |
| ------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| Geöffnete Fenster und Türen nach Verlassen des Besprechungsraums | (Beispiel: Informationen/IT-Geräte können durch Diebstahl in falsche Hände geraten) |
| Nutzung durch externe Personen                                     | (zu ergänzen)                                                                         |
| Lose verlegte Kabel                                                | (zu ergänzen)                                                                         |
| Nutzung von BYOD (Bring Your Own Device)                           | (zu ergänzen)                                                                         |

#### 1c) BSI-Grundschutz Praesentationsrechner (4 Punkte)

PC für Präsentationen mit Anzeigegerät. BSI-Grundschutz empfiehlt sichere Konfiguration.
Vorgeschlagene Maßnahmen begründen:

- Nutzung einer Minimalkonfiguration mit festgelegter Anwendungssoftware
- Anschluss an ein vom LAN der Institution getrenntes Datennetz

### Aufgabe 3c - Phishing-Mails (9 Punkte)

**Kontext:** Korrespondenz mit Hardwarelieferanten, Warnung vor Phishingmails.

- **3ca)** Eine Gefahr durch Phishingmails beschreiben (2 Punkte)
- **3cb)** Drei Anzeichen nennen, an denen man Phishingmails erkennen kann (3 Punkte)
- **3cc)** Zwei Maßnahmen, die dem **Unternehmen** zum Schutz vor Phishingmails empfohlen werden (2 Punkte)
- **3cd)** Zwei Maßnahmen, die das Unternehmen den **Mitarbeitern** beim Empfang von Mails vorgibt (2 Punkte)

---

## Frühjahr 2025 (25.03.2025)
### Aufgabe 1e - Sicherheitsmaßnahmen (7 Punkte)

**Kontext:** Innova DVTech 2000 OHG - IT-Betreuung einer Rechtsanwaltskanzlei.

Englischer Text des Herstellers zu Sicherheitsmaßnahmen (Security Baseline, Firewall, Updates, Memory Integrity).
- **1ea)** Vier Sicherheitsmaßnahmen nennen, die im Text beschrieben werden (4 Punkte)
- **1eb)** Begründen, warum es aus Sicherheitsgründen nicht zu empfehlen ist, allen Benutzern Adminrechte zu geben (3 Punkte)

### Aufgabe 2 - Datensicherheit im E-Mail-Verkehr (20 Punkte)

**Kontext:** Rechtsanwälte wünschen verschlüsselte Kommunikation mit Mandanten.

#### 2a) Rechtliche Grundlage E-Mail-Sicherheit (3 Punkte)

- **2aa)** Rechtliche Grundlage für erhöhte Sicherheitsanforderungen bei E-Mail-Kommunikation zwischen Rechtsanwalt und Mandant nennen (1 Punkt)
- **2ab)** Zweck dieser rechtlichen Grundlage beschreiben (2 Punkte)

#### 2b) Asymmetrische Verschlüsselung (7 Punkte)
- **2ba)** Vorgehensweise bei asymmetrischer Verschlüsselung und Entschlüsselung anhand einer Skizze (Anwalt -> Mandant) beschreiben (4 Punkte)
- **2bb)** IT-Schutzziel nennen, das durch Verwendung der Schlüssel erreicht wird (1 Punkt)
- **2bc)** Einen Vorteil und einen Nachteil der asymmetrischen Verschlüsselung im Vergleich zur symmetrischen Verschlüsselung nennen (2 Punkte)

#### 2c) Lizenzmodelle (4 Punkte)

Open-Source-Lizenz vs. proprietäre Software: Je zwei Vorteile nennen.
> Hinweis: Nur teilweise LF4-relevant, primär Softwarelizenzierung.

#### 2d) Hashwert bei Softwaredownload (4 Punkte)

Auf der Website des Software-Anbieters wird neben der Installationsdatei ein SHA-256-Hashwert angeboten.
Zweck der Verwendung eines Hashwerts beim Softwaredownload erläutern.

---

## Zusammenfassung: LF4-Punkte pro Prüfung
| Prüfung       | Aufgabe(n)              | Punkte | Schwerpunkte                                                                                             |
| -------------- | ----------------------- | ------ | -------------------------------------------------------------------------------------------------------- |
| Herbst 2021    | Aufgabe 4 komplett      | 24     | Schutzziele, BSI-Grundschutz, Schutzbedarfsanalyse, Datenschutzrecht, Passwortsicherheit, Datensicherung |
| Frühjahr 2022 | Aufgabe 3b (tangential) | ~3     | WLAN-Authentifizierung (WPA-PSK vs. EAP)                                                                 |
| Frühjahr 2023 | Aufgabe 3 komplett      | 24     | BSI, Härung, Gruppenrichtlinien, Protokollierung, Datenschutz                                          |
| Herbst 2023    | Aufgabe 3 komplett      | 22     | Datenschutzgesetze, BSI-Telearbeit, Verschlüsselung (TPM), VPN, Zertifikate                             |
| Frühjahr 2024 | Aufgabe 4 komplett      | 26     | Geheimhaltung unterwegs, VPN, Datensicherung, Malware, Schutz vor Malware                                |
| Herbst 2024    | Aufgabe 1a-c + 3c       | 19     | BSI-Grundschutz Besprechungsraum, Zutrittskontrolle, Phishing                                            |
| Frühjahr 2025 | Aufgabe 1e + 2          | 27     | Sicherheitsmaßnahmen, E-Mail-Verschlüsselung, Hashwert, Adminrechte                                    |
## Häufig abgefragte Themen
1. **BSI IT-Grundschutz-Kompendium** - in fast jeder Prüfung
2. **Schutzziele (CIA)** - Vertraulichkeit, Integrität, Verfügbarkeit
3. **Verschlüsselung** - symmetrisch vs. asymmetrisch, TPM, VPN
4. **Datenschutzgesetze** - DSGVO, BDSG
5. **Passwortsicherheit** - Kriterien für sichere Passwörter
6. **Schutzbedarfsfeststellung** - Kategorien und Begründungen
7. **Härung** von Betriebssystemen
8. **Phishing** - Erkennung und Schutzmaßnahmen
9. **Hashwerte** - Integritätsprüfung
10. **Zutrittskontrolle** - physische Sicherheit
11. **Malware** - Arten, Merkmale und Schutzmaßnahmen
12. **Datensicherung** - Strategien, Risiken, externe Medien