# LF4-Aufgaben in IHK AP1-Prüfungen - Musterlösungen

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

#### 4a) Schutzziele zuordnen (6 Punkte)

| Sicherheitsmaßnahme                                | V   | I   | VF  | Begründung                                                                               |
| --------------------------------------------------- | --- | --- | --- | ----------------------------------------------------------------------------------------- |
| Sichere Passwörter wählen                         | X   |     |     | Zugriff Fremder auf Benutzerdaten wird besser geschützt                                  |
| Regelmäßige Datensicherung der Patientendaten     |     |     | X   | Bei einem Datenverlust können die Daten wiederhergestellt werden                         |
| Verschlüsselung der Festplatten                    | X   |     |     | Daten können nur mit Schlüssel gelesen werden, Schutz vor unberechtigtem Zugriff        |
| Zentrale Bearbeitung wichtiger Dokumente auf Server |     | X   |     | Einheitlicher Datenbestand, keine unterschiedlichen Versionen auf verschiedenen Endgeräten |
| Hashwertüberprüfung bei Softwareinstallation      |     | X   |     | Änderungen an der Software können erkannt werden                                     |

#### 4b) BSI IT-Grundschutz-Kompendium: Basis-Anforderungen PC-Client (2 Punkte)

- **Autoupdate-Mechanismen aktivieren:** Sicherheitsupdates werden zeitnah eingespielt
- **Rollentrennung:** Keine normalen Tätigkeiten mit Administratorrechten durchführen

#### 4c) Schutzbedarfsanalyse (6 Punkte)

| IT-Anwendung                                                           | Schutzziel      | Kategorie | Begründung                                                                                           |
| ---------------------------------------------------------------------- | --------------- | --------- | ----------------------------------------------------------------------------------------------------- |
| Prüfziffernverfahren bei Übermittlung der Krankenversicherungsnummer | Integrität     | hoch      | Verfälschte Daten können zu fehlerhaften Abrechnungen führen                                       |
| Textverarbeitung                                                       | Verfügbarkeit  | mittel    | Kurzfristiger Ausfall hat begrenzte Auswirkungen, Arbeit kann nachgeholt werden                        |
| Software zur telemedizinischen Beratung über Videokonferenz           | Vertraulichkeit | hoch      | Patientendaten/-gespräche dürfen nicht von Unbefugten mitgehört/mitgelesen werden                   |
| Patientendatenverarbeitung                                             | Integrität     | sehr hoch | Verfälschte Patientendaten können zu Fehlbehandlungen führen, existenziell bedrohlich für Patienten |

#### 4d) Besonderer Schutz personenbezogener Daten (2 Punkte)

- **Datenart:** Personenbezogene Daten, insbesondere Patientendaten und Mitarbeiterdaten
- **Rechtliche Grundlage:** BDSG (Bundesdatenschutzgesetz) bzw. DSGVO (Datenschutz-Grundverordnung)

#### 4e) Kriterien für sichere Passwörter (4 Punkte)
1. **Ausreichende Länge:** längere Passwörter erhöhen die Anzahl möglicher Kombinationen und erschweren Brute-Force-Angriffe
2. **Verwendung von Sonderzeichen:** Vergrößerung des Zeichenraums, unsinnige Zeichenketten statt Wörterbuchwörter
3. **Unterschiedliche Passwörter** für verschiedene Dienste verwenden
4. **Keine Wörterbuchwörter** oder leicht zu erratende Begriffe

#### 4f) Risiken der Datensicherung auf gleicher Festplatte (4 Punkte)

**4fa) Zwei Risiken:**

- Keine räumliche/zeitliche Trennung: Bei Defekt der Festplatte sind Originaldaten und Sicherung gleichzeitig verloren
- Wöchentlicher Sicherungszyklus ist zu lang: Bei täglicher Arbeit können bis zu einer Woche Daten verloren gehen

**4fb) Verbesserungsvorschlag:**

- Sicherung auf externem Medium (z.B. externe Festplatte, NAS)
- Tägliche Sicherung statt wöchentlich
-Externes Sicherungsmedium an einem anderen Ort aufbewahren (räumliche Trennung)

---

## Frühjahr 2022 (30.03.2022)

### Aufgabe 3b - WLAN-Authentifizierung (3 Punkte)

| Verfahren                 | Vorteil                                                   | Nachteil                                             | Unternehmensgröße              |
| ------------------------- | --------------------------------------------------------- | ---------------------------------------------------- | ------------------------------ |
| WPA-PSK                   | Einfach umzusetzen                                        | Unsicher, da Passwort schnell bekannt werden kann   | Kleine Unternehmen             |
| EAP/WPA-Enterprise-RADIUS | Sehr viel sicherer, eigene Name/Passwort-Kombination pro Nutzer | Komplizierter einzurichten, RADIUS-Server erforderlich | Mittlere und große Unternehmen |

---

## Frühjahr 2023 (01.03.2023)

### Aufgabe 3 - Datenschutz und Datensicherheit (24 Punkte)

#### 3a) Schalenmodell Betriebssystem (4 Punkte)

| Schicht        | Beschreibung/Funktion                                                     |
| -------------- | ------------------------------------------------------------------------- |
| Anwendung      | Oberhalb des BS; Erstellung von Textdokumenten, Tabellenkalkulation usw. |
| Betriebssystem | Bereitstellung der Benutzeroberfläche, Verwaltung der Ressourcen        |
| UEFI/BIOS      | Unterhalb des BS; Schnittstelle zwischen Hardware und Betriebssystem     |
| PC-Hardware    | Verarbeitung und Speicherung von Daten                                    |

#### 3b) BSI - Sicherheit auf Betriebssystemebene (12 Punkte)

**3ba) Zwei allgemeine Aufgaben des BSI:**

- Zentrale Anlaufstelle für Fragen zur IT-Sicherheit
- Erarbeitung von Standards und Empfehlungen für IT-Sicherheit
- Schutz der IT-Systeme des Bundes

**3bb) Härung eines Betriebssystems:**
Härung bedeutet die Reduktion von Angriffsmöglichkeiten durch Entfernung oder Deaktivierung nicht notwendiger Softwarebestandteile und Dienste.
**3bc) Zwei Beispiele für Härung:**

- Entfernung nicht erforderlicher Softwarekomponenten
- Reduzierung von Benutzerrechten auf das notwendige Minimum
- Verschlüsselung von Datenträgern
- Nicht benötigte Benutzerkonten löschen/deaktivieren
- Nicht benötigte Ports schließen

**3bd) Zwei Systemwerkzeuge (Bordmittel):**

- Firewall (Windows-Firewall)
- Virenschutz (Windows Defender)
- Datensicherung (Windows-Sicherung)
- Benutzerverwaltung

**3be) Gruppenrichtlinien:**

Gruppenrichtlinien erlauben die zentrale Vorgabe von Einstellungen für Arbeitsplatzrechner. Die Einstellungen können nicht durch den Anwender geändert werden. Beispiele:
- Passworteinstellungen (Mindestlänge, Komplexität, Änderungsintervall)
- Sperrung von Konfigurationsmöglichkeiten
- Einschränkung der Softwareinstallation
- Bildschirmsperre nach Inaktivität

#### 3c) Protokollierung und Datenschutz (8 Punkte)

**3ca) Beitrag der Protokollierung zur IT-Sicherheit:**

- Identifikation von Fehlern und Fehlfunktionen
- Erkennung von unerlaubten Aktivitäten und Angriffsversuchen
- Zuordnung von Ereignissen zu bestimmten Zeiten und Benutzern
- Nachvollziehbarkeit von Änderungen (Revisionssicherheit)

**3cb) Anforderungen an den Datenschutz bei Protokollierung:**

- Protokolldaten dürfen nur begrenzt gespeichert und ausgewertet werden
- Grundsatz der Datensparsamkeit ist zu beachten
- Protokolldaten enthalten ggf. personenbezogene Daten (wer hat wann was getan)
- Auswertung nur zu definierten Zwecken, nicht zur Leistungsüberwachung

---

## Herbst 2023 (19.09.2023)

### Aufgabe 3 - Datenschutz und IT-Sicherheit (22 Punkte)

#### 3a) Gesetzliche Grundlagen Datenschutz (2 Punkte)

- DSGVO (Datenschutz-Grundverordnung)
- BDSG (Bundesdatenschutzgesetz)
- Weitere möglich: Strafgesetzbuch, Grundgesetz (Art. 10), Landesdatenschutzgesetze

#### 3b) BSI-Anforderungen Telearbeit (4 Punkte)

| Bereich                                | Maßnahme                                                                      |
| -------------------------------------- | ----------------------------------------------------------------------------- |
| Zugriffsschutz auf mobile Datenträger | Verschlüsselung der SSD/Festplatte                                            |
| Zutrittsschutz Telearbeitsplatz        | Türen und Fenster schließen, abschließbarer Schrank für Laptop               |
| Sichere Anmeldung am Laptop            | Sichere Passwörter verwenden, Zweifaktor-Authentifizierung                    |
| Sichere Datenkommunikation             | VPN-Verbindung nutzen, sichere Protokolle (HTTPS, SFTP)                       |
| Transport von Datenträgern             | Sicherheitsschulung der Mitarbeiter, Einsatz von Kurieren, Transportkoffer    |
#### 3c) Verschlüsselung mit TPM (11 Punkte)
**3ca) Zwei Kriterien für ein sicheres Passwort:**
- Mindestlänge von 8 Zeichen
- Verwendung von Groß- und Kleinbuchstaben, Ziffern und Sonderzeichen
- Kein Wort, das in einem Wörterbuch steht
**3cb) Sicherung des Wiederherstellungsschlüssels - Vor-/Nachteile:**

| Verfahren                  | Vorteil                                       | Nachteil                                                      |
| -------------------------- | --------------------------------------------- | ------------------------------------------------------------- |
| PC in Textdatei speichern  | Kein zusätzlicher Speicher nötig              | Ggf. nicht erreichbar wenn PC nicht startet                    |
| Cloud-Speicher             | Von verschiedenen Geräten erreichbar          | Datenschutzrichtlinien müssen beachtet werden                 |
| USB-Stick                  | Mobil, kann an verschiedenen Orten genutzt werden | Kann verloren gehen oder gestohlen werden                    |
| Ausdrucken                 | Kein IT-Endgerät erforderlich                 | Drucker und sicherer Ablageort erforderlich                    |

**3cc) Schutzziele bezogen auf Daten der SSD:**

- **Vertraulichkeit:** Nur berechtigte Personen können die Daten auf der SSD einsehen. Durch die Verschlüsselung wird verhindert, dass Unbefugte die Daten lesen können.
- **Integrität:** Änderungen an den Daten können bemerkt werden. Die Verschlüsselung schützt vor unbemerkter Manipulation der gespeicherten Daten.
**3cd) Verschlüsselungssystem bei Diebstahl:**
Die Daten sind nicht zugänglich, da das Passwort zum Entsperren des TPM-Moduls nicht vorliegt. Der Dieb kann die verschlüsselte SSD nicht auslesen, selbst wenn er sie in einen anderen Rechner einbaut.

#### 3d) VPN und digitales Zertifikat (5 Punkte)

**3da) Sicherheitstechnischer Vorteil eines VPN:**

VPN ermöglicht eine sichere Datenübertragung auch über ein unsicheres Netzwerk (z.B. öffentliches WLAN oder Internet). Die Daten werden verschlüsselt übertragen und sind vor dem Mitlesen durch Dritte geschützt.

**3db) Identifizierung mithilfe des digitalen Zertifikats:**

Das digitale Zertifikat dient der Authentifizierung des Mitarbeiters gegenüber dem VPN-Server des Unternehmens. Es stellt sicher, dass sich nur autorisierte Personen mit dem Firmennetzwerk verbinden können. Das Zertifikat wird von einer vertrauenswürdigen Stelle ausgestellt und enthält den öffentlichen Schlüssel des Inhabers.

---

## Frühjahr 2024 (Februar 2024)

### Aufgabe 4 - IT-Sicherheit und Datenschutz (26 Punkte)

#### 4a) Maßnahmen zur Gewährleistung der Geheimhaltung (6 Punkte)
| Maßnahmen oder Verhaltensweisen                          | Folge der Nichtbeachtung                                       |
| -------------------------------------------------------- | -------------------------------------------------------------- |
| Nutzung einer Blickschutzfolie                            | Bildschirminhalt kann von Unberechtigten gelesen werden        |
| Zugangs-/Zugriffskontrolle (sicheres Passwort verwenden) | Unberechtigter Zugriff auf Geräte und Daten                   |
| Verschlüsselung der Daten/Datenträger                    | Unberechtigter Zugriff auf Daten bei Verlust/Diebstahl         |
| Sicherung lokal gespeicherter Daten (Backup)             | Verfügbarkeit der Daten ist nicht mehr gegeben                |
| VPN-Verbindung nutzen                                     | Datenübertragung könnte abgegriffen/mitgelesen werden        |
#### 4b) VPN-Funktionalität (2 Punkte)
VPN (Virtual Private Network) ist eine Netzwerkverbindung, die ohne eigene physische Verbindung betrieben wird und von Unberechtigten nicht einsehbar ist. Es handelt sich um eine verschlüsselte Verbindung über ein öffentliches Netz (z.B. Internet), die einen sicheren Tunnel zwischen zwei Endpunkten herstellt.

#### 4c) Datensicherung auf externen Festplatten (3 Punkte)

- Datenträger müssen verschlüsselt sein (Passwort erforderlich), damit bei Verlust kein Zugriff möglich ist
- Feste Reihenfolge der Datenträger einhalten: Bei Ausfall eines Datenträgers stehen weitere Sicherungsstände zur Verfügung
- Nach Nutzung aller Datenträger wird wieder mit dem ersten begonnen (Generationsprinzip / Rotationsprinzip)

#### 4d) Malware (6 Punkte)

| Malware-Art           | Spezifisches Merkmal                                                             |
| --------------------- | -------------------------------------------------------------------------------- |
| Virus                 | Befällt bestehenden Programmcode und verbreitet sich bei Ausführung selbst      |
| Wurm                  | Wird nach Infektion selbstständig aktiv und breitet sich eigenständig im Netz aus |
| Trojaner              | Tarnt sich als nützliche Software, enthält aber Schadcode                       |
| Spyware               | Spioniert Inhalte und Aktivitäten des Benutzers aus                              |
| Adware                | Platziert gezielt unerwünschte Werbung                                           |
| Hintertuer/Backdoor   | Ermöglicht unbefugten Zugang unter Umgehung der Sicherheitsmechanismen           |
| Scareware             | Verunsichert den Benutzer durch gefälschte Warnmeldungen                         |
| Ransomware            | Verschlüsselt oder blockiert Daten und fordert Lösegeld                          |
| Keylogger             | Protokolliert Tastatureingaben (z.B. Passwörter)                                 |

#### 4e) Schutz vor Malware (3 Punkte)

- Keine unbekannten Datenträger (z.B. USB-Sticks) anschließen
- Kein Download von Software aus unsicheren/unbekannten Quellen
- Keine Ausführung aktiver Inhalte (Makros in Dokumenten, unbekannte E-Mail-Anhänge)
- AdBlocker verwenden
- Regelmäßige Updates des Betriebssystems und der Software
- Mitarbeiter sensibilisieren und schulen

#### 4f) Übertragungsdauer berechnen (6 Punkte)

**Gegeben:** Upload = 50,02 Mbps; Datenvolumen = 1 GiB

**Berechnung:**

1. 1 GiB = 1 x 1.024 x 1.024 x 1.024 Byte = 1.073.741.824 Byte
2. In Bit: 1.073.741.824 x 8 = 8.589.934.592 Bit
3. Upload: 50,02 Mbps = 50.020.000 Bit/s
4. Zeit = 8.589.934.592 / 50.020.000 = 171,73 s
5. Gerundet: **172 s = 2 Minuten 52 Sekunden**

---

## Herbst 2024 (17.09.2024)

### Aufgabe 1 - BSI IT-Grundschutz Besprechungsraum (10 Punkte)

#### 1a) Zutrittskontrolle (3 Punkte)

Drei technische Möglichkeiten für automatische Zutrittskontrolle:

- Fingerabdrucksensor (biometrisch)
- Stimmenerkennung (biometrisch)
- Zahlencode/PIN-Eingabe
- Kartenscanner (Chipkarte/RFID)

#### 1b) Sicherheitsrisiken (3 Punkte)

| Situation                                                          | Sicherheitsrisiko                                                                                    |
| ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| Geöffnete Fenster und Türen nach Verlassen des Besprechungsraums | Informationen/IT-Geräte können durch Diebstahl in falsche Hände geraten                           |
| Nutzung durch externe Personen                                     | Vertrauliche Informationen können an externe/unberechtigte Personen gelangen                         |
| Lose verlegte Kabel                                                | Unterbrechung von Netzwerkverbindungen, Stolpergefahr, Beschädigung von Geräten                     |
| Nutzung von BYOD (Bring Your Own Device)                           | Malware kann ins Firmennetz gelangen, Ausspähung von Firmendaten über ungesicherte/private Geräte |

#### 1c) BSI-Grundschutz Praesentationsrechner (4 Punkte)

- **Minimalkonfiguration:** Einfacher zu pflegen und zu warten, weniger fehleranfällig, bietet weniger Angriffsmöglichkeiten da nur benötigte Software installiert ist
- **Getrenntes Datennetz:** Nutzer des Praesentationsrechners können nicht auf Firmendaten im LAN zugreifen, Isolation schützt das interne Netzwerk vor Angriffen über den Praesentationsrechner

### Aufgabe 3c - Phishing-Mails (9 Punkte)

**3ca) Gefahr durch Phishingmails:**

Zugangsdaten (Benutzername/Passwort) können gestohlen werden. Angreifer können dadurch an sicherheitskritische Informationen gelangen und sich Zugang zu Systemen verschaffen.
**3cb) Drei Anzeichen für Phishingmails:**

- Fehlerhafte Rechtschreibung/Grammatik in der E-Mail
- Keine persönliche Anrede (z.B. "Sehr geehrter Kunde" statt Name)
- Zeitdruck und Fristsetzungen ("Ihr Konto wird in 24 Stunden gesperrt")
- Aufforderung zur Eingabe persönlicher Daten oder Zugangsdaten
**3cc) Zwei Maßnahmen für das Unternehmen:**
- Gute Spamfilter einsetzen und regelmäßig aktualisieren
- Phishing-Angriffe simulieren, um die Aufmerksamkeit der Mitarbeiter zu testen
- Regelmäßige Schulung der Mitarbeiter zum Thema Phishing
**3cd) Zwei Maßnahmen für Mitarbeiter:**
- Keine Übermittlung von Benutzername/Passwort per E-Mail
- Keine Links aus verdächtigen E-Mails anklicken
- Keine Anhänge aus unbekannten Quellen öffnen
- Verdachtsfälle umgehend an die IT-Abteilung melden

---

## Frühjahr 2025 (25.03.2025)
### Aufgabe 1e - Sicherheitsmaßnahmen (7 Punkte)
**1ea) Vier Sicherheitsmaßnahmen aus dem englischen Text:**

- Security Compliance Toolkit (Sicherheitsbasiskonfiguration)
- Komplexe Passwörter erzwingen
- Betriebssystem-interne Firewall aktivieren
- Regelmäßige Updates installieren
- Memory Integrity Features aktivieren

**1eb) Begründung gegen Adminrechte für alle Benutzer:**
- Rechner und Netzwerk werden anfälliger gegen Malware, da Schadsoftware mit Administratorrechten ausgeführt werden kann und tiefgreifende Systemänderungen vornehmen kann
- Anwender könnten die Rechte missbrauchlich nutzen (z.B. unautorisierte Software installieren, Sicherheitseinstellungen ändern)

### Aufgabe 2 - Datensicherheit im E-Mail-Verkehr (20 Punkte)

#### 2a) Rechtliche Grundlage E-Mail-Sicherheit (3 Punkte)

**2aa) Rechtliche Grundlage:**

- DSGVO (Datenschutz-Grundverordnung)
- Bundesdatenschutzgesetz (BDSG)

**2ab) Zweck:**

Schutz personenbezogener Daten. Die Kommunikation zwischen Rechtsanwalt und Mandant enthält besonders schützenswerte personenbezogene Daten, die vor unbefugtem Zugriff geschützt werden müssen.
#### 2b) Asymmetrische Verschlüsselung (7 Punkte)

**2ba) Vorgehensweise:**

1. Der Rechtsanwalt verschlüsselt die Nachricht mit dem öffentlichen Schlüssel des Mandanten
2. Die verschlüsselte Nachricht wird über das Internet übertragen
3. Der Mandant entschlüsselt die Nachricht mit seinem privaten Schlüssel
4. Nur der Besitzer des privaten Schlüssels kann die Nachricht lesen

**2bb) IT-Schutzziel:**

**Vertraulichkeit** - Nur der berechtigte Empfänger kann die Nachricht entschlüsseln und lesen.
**2bc) Vorteil und Nachteil gegenüber symmetrischer Verschlüsselung:**
- **Vorteil:** Keine gesicherte Übertragung eines geheimen Schlüssels nötig. Der öffentliche Schlüssel kann frei verteilt werden, ohne die Sicherheit zu gefährden.
- **Nachteil:** Höherer Rechenaufwand, dadurch langsamere Ver-/Entschlüsselung im Vergleich zur symmetrischen Verschlüsselung.

#### 2c) Lizenzmodelle (4 Punkte)

| Lizenzmodell | Vorteil 1                                                   | Vorteil 2                                                            |
| ------------ | ----------------------------------------------------------- | -------------------------------------------------------------------- |
| Open-Source  | Ggf. kostenlos nutzbar                                      | Quellcode ist öffentlich einsehbar und überprüfbar (Transparenz)  |
| Proprietaer  | Bessere Zusammenarbeit/Kompatibilität mit Hersteller-Software | Gesicherter Service und Support durch den Hersteller                |

#### 2d) Hashwert bei Softwaredownload (4 Punkte)

Nach dem Download wird der Hashwert der heruntergeladenen Datei erneut berechnet und mit dem auf der Website angebotenen Hashwert verglichen. Stimmen beide Hashwerte überein, wurde die Datei korrekt und vollständig übertragen und nicht manipuliert. So können Übertragungsfehler und Manipulationen identifiziert werden.
**Schutziel:** Integrität - Die Unversehrtheit der Daten wird sichergestellt.

---

## Zusammenfassung: LF4-Punkte pro Prüfung
| Prüfung       | Aufgabe(n)              | Punkte | Schwerpunkte                                                                                             |
| -------------- | ----------------------- | ------ | -------------------------------------------------------------------------------------------------------- |
| Herbst 2021    | Aufgabe 4 komplett      | 24     | Schutzziele, BSI-Grundschutz, Schutzbedarfsanalyse, Datenschutzrecht, Passwortsicherheit, Datensicherung |
| Frühjahr 2022  | Aufgabe 3b (tangential) | ~3     | WLAN-Authentifizierung (WPA-PSK vs. EAP)                                                                 |
| Frühjahr 2023  | Aufgabe 3 komplett      | 24     | BSI, Härung, Gruppenrichtlinien, Protokollierung, Datenschutz                                          |
| Herbst 2023    | Aufgabe 3 komplett      | 22     | Datenschutzgesetze, BSI-Telearbeit, Verschlüsselung (TPM), VPN, Zertifikate                             |
| Frühjahr 2024  | Aufgabe 4 komplett      | 26     | Geheimhaltung unterwegs, VPN, Datensicherung, Malware, Schutz vor Malware                                |
| Herbst 2024    | Aufgabe 1a-c + 3c       | 19     | BSI-Grundschutz Besprechungsraum, Zutrittskontrolle, Phishing                                            |
| Frühjahr 2025  | Aufgabe 1e + 2          | 27     | Sicherheitsmaßnahmen, E-Mail-Verschlüsselung, Hashwert, Adminrechte                                    |