# IT-Sicherheit bei der "Muster-Apotheke GmbH"

## Szenario
Eine mittelständische Apothekenkette mit 5 Filialen und einer Zentrale. 50 Mitarbeiter, davon 5 in der IT. Patienten- und Lieferantendaten müssen geschützt werden.

---

## 1. Sicherheitsrichtlinie der Muster-Apotheke GmbH

**1.1 Sicherheitsziele**
- Schutz aller Patientendaten vor unbefugtem Zugriff (Vertraulichkeit)
- Gewährleistung der Korrektheit von Bestell- und Abrechnungsdaten (Integrität)
- Sicherstellung der Verfügbarkeit der Apotheken-Software während der Öffnungszeiten (Verfügbarkeit)

**1.2 Geltungsbereich**
- Alle 5 Filialen und die Zentrale
- Alle IT-Systeme (Kassensysteme, Bestandsverwaltung, Netzwerke)
- Alle Mitarbeiter mit Zugang zu IT-Systemen

**1.3 Verantwortlichkeiten**
- Geschäftsführung: Ressourcenbereitstellung, strategische Entscheidungen
- IT-Leiter (Herr Müller): Umsetzung und Überwachung
- Datenschutzbeauftragter: Kontrolle der DSGVO-Compliance
- Filialleiter: Umsetzung vor Ort

**1.4 Grundsätze**
- Need-to-know-Prinzip: Zugang nur bei betrieblicher Notwendigkeit
- Mitarbeiterschulungen: Mindestens 1x jährlich
- Meldung von Sicherheitsvorfällen innerhalb 24 Stunden

---

## 2. Sicherheitskonzept

**2.1 Geltungsbereich konkretisiert**

| Standort | Systeme | Verantwortlicher |
|----------|---------|------------------|
| Zentrale | Serverraum, Hauptserver, Firewall | Herr Müller |
| Filiale 1-5 | Je 2 Kassensysteme, 1 Büro-PC | Jeweils Filialleiter |

**2.2 Bestandsaufnahme (Auszug)**

| Asset | Typ | Standort | Nutzer |
|-------|-----|----------|--------|
| Server "APOTHEKE-MAIN" | physisch | Zentrale | IT-Admin |
| Patientenverwaltung "PharmaSoft" | Software | Server | Apotheker |
| Kassensysteme (10x) | Hardware | Filialen | Apothekenpersonal |
| VPN-Verbindungen | Netzwerk | Zentrale↔Filialen | Alle |

**2.3 Risikoanalyse (Beispiel)**

| Bedrohung | Schwachstelle | Wahrscheinlichkeit | Schadenspotenzial | Risiko |
|-----------|---------------|-------------------|-------------------|--------|
| Ransomware-Befall | Fehlende Schulung, veraltete Software | mittel | hoch | **hoch** |
| Serverausfall | Kein Backup, keine Redundanz | niedrig | sehr hoch | **hoch** |
| DatenDiebstahl | Schwache Passwörter | mittel | hoch | **hoch** |

**2.4 Maßnahmenplan**

| Maßnahme | Typ | Priorität | Verantwortlich | Frist |
|----------|-----|-----------|----------------|-------|
| Einführung MFA für alle Systeme | technisch | hoch | Herr Müller | Q1 |
| Tägliches Backup (extern) | technisch | hoch | Herr Müller | Q1 |
| Mitarbeiterschulung Phishing | organisatorisch | hoch | HR | Q1 |
| Patchmanagement automatisieren | technisch | mittel | Herr Müller | Q2 |
| Notfallhandbuch erstellen | organisatorisch | mittel | Herr Müller | Q2 |

---

## 3. Strukturanalyse

**3.1 Geschäftsprozesse**
```
[Patientenaufnahme] → [Medikamentenausgabe] → [Abrechnung]
         ↓                    ↓                   ↓
    PharmaSoft           PharmaSoft           Kassensystem
```

**3.2 Netzplan (vereinfacht)**
```
                    ┌─────────────────┐
                    │   Internet      │
                    └────────┬────────┘
                             │
                    ┌────────▼────────┐
                    │   Firewall      │
                    │   (Zentrale)    │
                    └────────┬────────┘
                             │
         ┌───────────────────┼───────────────────┐
         │                   │                   │
    ┌────▼────┐        ┌─────▼─────┐       ┌─────▼─────┐
    │ Server  │        │ Switch    │       │ VPN-Gateway│
    │ (Main)  │        │ (Zentrale)│       │           │
    └─────────┘        └─────┬─────┘       └─────┬─────┘
                             │                   │
         ┌───────────┬───────┴───────┬───────────┘
         │           │               │
    ┌────▼───┐  ┌────▼───┐     ┌────▼───┐
    │Filiale1│  │Filiale2│ ... │Filiale5│
    └────────┘  └────────┘     └────────┘
```

**3.3 IT-Systeme (Auszug)**

| System | Funktion | OS | Standort |
|--------|----------|----|----------|
| APOTHEKE-MAIN | Patientenverwaltung, Bestellwesen | Windows Server 2022 | Zentrale |
| APOTHEKE-BACKUP | Backup-Server | Linux | Zentrale (externer Standort) |
| KASSE-01 bis 10 | Kassensysteme | Windows 10 | Filialen |
| FW-MAIN | Firewall | pfSense | Zentrale |

**3.4 Räumlichkeiten**

| Raum | Standort | Systeme | Zugangskontrolle |
|------|----------|---------|------------------|
| Serverraum | Zentrale | Server, Switch, Firewall | Chipkarte + PIN |
| Büroräume | Zentrale | 5 Arbeitsplätze | Schlüssel |
| Apotheken | Filialen | Kassensysteme | Schlüssel (Personal) |

**3.5 Kommunikationsverbindungen**

| Verbindung | Typ | Verschlüsselt | Genutzt von |
|------------|-----|---------------|-------------|
| Zentrale ↔ Internet | DSL 100 Mbit | TLS | Alle |
| Zentrale ↔ Filialen | VPN (IPsec) | Ja | Apothekenpersonal |
| Server ↔ Backup-Server | LAN/WAN | Ja | IT-Admin |

---

## 4. Schutzbedarfsfeststellung

**4.1 Bewertungskriterien**

| Stufe | Vertraulichkeit | Integrität | Verfügbarkeit |
|-------|-----------------|------------|---------------|
| **Normal** | Interne Daten, keine sensiblen Infos | Fehler korrigierbar | Ausfall < 24h akzeptabel |
| **Hoch** | Betriebsinterne Daten, personenbezogene Daten | Fehler verursacht finanziellen Schaden | Ausfall < 4h akzeptabel |
| **Sehr hoch** | Hochsensible Daten, Gesundheitsdaten | Fehler gefährdet Leben/Existenz | Ausfall > 1h kritisch |

**4.2 Bewertung der Assets**


| Asset | Vertraulichkeit | Integrität | Verfügbarkeit | Gesamt |
|-------|-----------------|------------|---------------|--------|
| **Server APOTHEKE-MAIN** | **hoch** (Patientendaten) | **hoch** (Abrechnung) | **sehr hoch** (Öffnungszeiten) | **sehr hoch** |
| **PharmaSoft-Datenbank** | **hoch** (Patientendaten) | **hoch** | **hoch** | **hoch** |
| **Kassensysteme** | normal | **hoch** | **hoch** | **hoch** |
| **Backup-Server** | **hoch** | **hoch** | normal | **hoch** |
| **VPN-Verbindungen** | **hoch** | **hoch** | **hoch** | **hoch** |
| **Büro-PCs** | normal | normal | normal | **normal** |

**4.3 Ableitung spezifischer Maßnahmen**

| Asset | Schutzbedarf | Konkrete Maßnahmen |
|-------|--------------|-------------------|
| Server APOTHEKE-MAIN | sehr hoch | Redundante Stromversorgung (USV), Failover-Server, 24/7-Monitoring, verschlüsseltes Backup |
| PharmaSoft-Datenbank | hoch | Tägliche Backups, Zugriffskontrolle, Protokollierung |
| Kassensysteme | hoch | Regelmäßige Updates, geschultes Personal, Ausfallersatzgeräte |
| VPN-Verbindungen | hoch | Starke Authentifizierung (Zertifikate), regelmäßige Überprüfung |

---

## Zusammenfassung der Zusammenhänge

```
┌─────────────────────────────────────────────────────────────┐
│  1. SICHERHEITSRICHTLINIE                                   │
│  "Patientendaten müssen geschützt werden"                   │
│  "Verfügbarkeit während Öffnungszeiten gewährleisten"       │
└──────────────────────────┬──────────────────────────────────┘
                           │ Strategische Vorgaben
                           ▼
┌─────────────────────────────────────────────────────────────┐
│  2. SICHERHEITSKONZEPT                                      │
│  Maßnahmen: MFA, Backup, Schulung, Patchmanagement          │
│  Verantwortliche: Herr Müller (IT), Filialleiter            │
└──────────────────────────┬──────────────────────────────────┘
                           │ Rahmen für Umsetzung
                           ▼
┌─────────────────────────────────────────────────────────────┐
│  3. STRUKTURANALYSE                                         │
│  Erfasst: Server, 10 Kassensysteme, VPN-Verbindungen        │
│  Netzplan: Zentrale mit 5 Filialen                          │
└──────────────────────────┬──────────────────────────────────┘
                           │ Liste aller zu schützenden Objekte
                           ▼
┌─────────────────────────────────────────────────────────────┐
│  4. SCHUTZBEDARFSFESTSTELLUNG                               │
│  Server = sehr hoch → USV, Failover, Monitoring             │
│  Kassensysteme = hoch → Updates, Schulung, Ersatzgeräte     │
│  Büro-PCs = normal → Standard-Maßnahmen                     │
└─────────────────────────────────────────────────────────────┘
```

