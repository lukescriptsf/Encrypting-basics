# Encrypting-basics
Dieses Repository nutzt GPG (GNU Privacy Guard) für die asymmetrische Verschlüsselung. Hier ist der schnelle Workflow zum Ver- und Entschlüsseln von Dateien.

### GPG ist ein leistungsstarkes Werkzeug zur asymmetrischen Verschlüsselung
Es basiert auf dem PGP-Standard (Pretty Good Privacy) und wird verwendet, um digitale Kommunikation sicher und authentisch zu gestalten.
Wie funktioniert es?

Das System nutzt ein Schlüsselpaar, bestehend aus einem Public Key und einem Private Key:

 - Public Key (Öffentlich): Er ist wie deine Adresse oder ein offenes Vorhängeschloss. Jeder kann ihn nutzen, um Daten für dich zu verschlüsseln oder deine digitale Unterschrift zu prüfen.
 - Private Key (Privat): Er ist dein streng geheimer Schlüssel. Nur mit ihm kannst du Nachrichten entschlüsseln, die für dich bestimmt sind, oder Dokumente rechtssicher signieren.

Wofür wird GPG verwendet?

 - E-Mail-Verschlüsselung: Schützt den Inhalt deiner E-Mails vor neugierigen Blicken (z. B. mit PGP-Plugins).
 - Datei-Verschlüsselung: Sicheres Speichern oder Versenden von sensiblen Dokumenten auf Ubuntu/Linux.
 - Software-Integrität: Entwickler signieren ihre Programme, damit du sicher sein kannst, dass der Code nicht manipuliert wurde (z. B. bei apt-Repositories).

## Wie verschlüsseln und entschlüsseln basics

Zeigt erstelle keys
```
gpg --list-keys
```

Erstellt neue keys
```
gpg --full-generate-key
```

Public key zum teilen
```
gpg --armor --export dein@email.de > public_key.asc
```

Datei verschlüsseln
```
gpg --encrypt --recipient empfaenger@email.de vertraulich.txt
```

Datei entschlüsseln
```
gpg --decrypt /path/to/file/vertraulich.txt.asc
```

Public key entfernen
```
gpg --delete-key [ID]
```

Privaten key anzeigen (ACHTUNG! NICHT TEILEN!)
```
gpg --list-secret-keys
```

