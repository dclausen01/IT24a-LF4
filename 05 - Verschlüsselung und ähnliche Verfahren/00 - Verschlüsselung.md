## Übersicht
- **Dauer:** 5 Stunden (à 45 Minuten)
- **Themen:** Grundlagen der Verschlüsselung, symmetrische/asymmetrische Verfahren, moderne Anwendungen, praktische Implementierung

## Stunde 1: Grundlagen der Verschlüsselung

### Ziele
- Verständnis der Notwendigkeit von Verschlüsselung
- Grundbegriffe: Klartext, Geheimtext, Schlüssel
- Praktische Umsetzung mit Caesar-Chiffre

### Inhalt
- **Einführung (10 Min):** Was ist Verschlüsselung? Warum ist sie wichtig für die Datensicherheit?
- **Grundbegriffe (10 Min):** Klartext, Geheimtext, Schlüssel, Verschlüsselungsalgorithmus
- **Caesar-Chiffre (15 Min):** Erklärung der Verschiebungsmethode, Beispiele
- **Praxis (10 Min):** Verschlüsseln und Entschlüsseln von Nachrichten mit Caesar-Chiffre (z.B. mit Verschiebung von 3)

### Praxisübung
- Teilen Sie den Teilnehmern eine Nachricht (z.B. "HALLO") und lassen Sie sie mit einer Verschiebung von 3 verschlüsseln.
- Diskutieren Sie die Schwächen der Caesar-Chiffre (z.B. Anfälligkeit für Brute-Force).

## Stunde 2: Symmetrische Verschlüsselung

### Ziele
- Verständnis symmetrischer Verfahren
- Implementierung mit AES in Python

### Inhalt
- **Theorie (15 Min):** Symmetrische vs. asymmetrische Verschlüsselung, Vorstellung von AES (Advanced Encryption Standard)
- **Sicherheitsaspekte (10 Min):** Schlüsselverwaltung, Blockchiffren, ECB vs. CBC-Modus
- **Praxis (20 Min):** Implementierung einer AES-Verschlüsselung mit Python

### Code-Beispiel
```python
from cryptography.fernet import Fernet

# Schlüssel generieren
key = Fernet.generate_key()
cipher = Fernet(key)

# Verschlüsseln
message = b"Meine geheime Nachricht"
encrypted = cipher.encrypt(message)
print("Verschlüsselt:", encrypted)

# Entschlüsseln
decrypted = cipher.decrypt(encrypted)
print("Entschlüsselt:", decrypted.decode())
```

## Stunde 3: Asymmetrische Verschlüsselung

### Ziele
- Verständnis von Public/Private Key-Systemen
- RSA-Algorithmus und Anwendung in SSL/TLS

### Inhalt
- - **Theorie (15 Min):** Prinzip der asymmetrischen Verschlüsselung, RSA-Algorithmus
    - **Public-Key-Prinzip:** Jeder Teilnehmer hat ein Schlüsselpaar (öffentlich und privat). Öffentlicher Schlüssel zum Verschlüsseln, privater zum Entschlüsseln.
    - **RSA-Schlüsselerzeugung:**
        - Wähle zwei große Primzahlen p und q
        - Berechne n = p * q und φ(n) = (p-1)(q-1)
        - Wähle öffentlichen Exponenten e (typisch 65537) mit ggT(e, φ(n)) = 1 (-> Primzahl)
        - Berechne privaten Exponenten d ≡ e⁻¹ mod φ(n)
    - **Verschlüsselung:** c = m^e mod n (m: Klartext, c: Geheimtext)
    - **Entschlüsselung:** m = c^d mod n
    - **Sicherheit:** Beruht auf der Schwierigkeit der Faktorisierung großer Zahlen (RSA-Problem) --> Was ist mit Post-Quantenverschlüsselung?
- **Praxis (20 Min):** Schlüsselgenerierung und Verschlüsselung mit RSA in Python
- **Anwendung (10 Min):** Wie SSL/TLS-Handshake funktioniert

### Code-Beispiel
```python
from cryptography.hazmat.primitives.asymmetric import rsa, padding
from cryptography.hazmat.primitives import hashes

# Private und Public Key generieren
private_key = rsa.generate_private_key(public_exponent=65537, key_size=2048)
public_key = private_key.public_key()

# Verschlüsseln
message = b"Geheime Nachricht"
encrypted = public_key.encrypt(
    message,
    padding.OAEP(mgf=padding.MGF1(algorithm=hashes.SHA256()), algorithm=hashes.SHA256(), label=None)
)

# Entschlüsseln
decrypted = private_key.decrypt(
    encrypted,
    padding.OAEP(mgf=padding.MGF1(algorithm=hashes.SHA256()), algorithm=hashes.SHA256(), label=None)
)
print("Entschlüsselt:", decrypted.decode())
```

## Stunde 4: Moderne Anwendungen und Sicherheitspraktiken

### Ziele
- Verständnis von TLS/SSL-Handshake
- Sicherheitslücken und Best Practices

### Inhalt
- **TLS/SSL-Handshake (15 Min):** Wie Verschlüsselung im Web (HTTPS) funktioniert
- **Digitale Signaturen (10 Min):** Authentizität und Integrität von Daten
- **Sicherheitslücken (10 Min):** Beispiele wie Heartbleed, Best Practices (Schlüsselrotation, starke Verschlüsselung)
- **Praxis (10 Min):** Analyse eines HTTPS-Handshakes mit Wireshark (optional)

## Stunde 5: Praxisprojekt und Abschluss

### Ziele
- Praktische Umsetzung eines verschlüsselten Chat-Systems
- Diskussion zu ethischen Aspekten

### Inhalt
- **Projekt (30 Min):** Aufbau eines einfachen Client-Server-Chat-Systems mit AES-Verschlüsselung (z.B. mit Python und Flask)
- **Ethik (10 Min):** Diskussion über die Rolle von Verschlüsselung in der Gesellschaft (z.B. Datenschutz vs. Sicherheit)
- **Fragen und Zusammenfassung (5 Min)**

## Quellen
- [Teach Computing: Introduction to Encryption and Cryptography](https://teachcomputing.org/courses/CO220/introduction-to-encryption-and-cryptography)
- [Scribd: Encryption Lesson](https://www.scribd.com/document/349713554/Encryption-Lesson)
- [Verizon Innovative Learning Lesson Plans](https://www.verizon.com/learning/lesson-plans/lessons/Cybersecurity-and-Cryptography/574)
- [Cryptography.io Documentation](https://cryptography.io/en/latest/)