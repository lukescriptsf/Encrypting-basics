# Encrypting-basics
How to encrypt files bascis
Dieses Repository nutzt GPG (GNU Privacy Guard) für die asymmetrische Verschlüsselung. Hier ist der schnelle Workflow zum Ver- und Entschlüsseln von Dateien.

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
gpg --decrypt vertraulich.txt.gpg > vertraulich.txt
```

Public key entfernen
```
gpg --delete-key [ID]
```

Privaten key anzeigen (ACHTUNG! NICHT TEILEN!)
```
gpg --list-secret-keys
```

