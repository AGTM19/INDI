Hallo.

0. Allgemeine Voraussetzungen
1. Getting Started
2. Benutzung von Git
3. Was wird gepusht/gepullt?
4. Bekannte Bugs
A1. Git f�r Windows installieren
A2. Datenschutz

0. Allgemeine Voraussetzungen
  - Der Administrator (Dein Tutor Bayram) hat Deinen GitHub-Account dem Repository hinzugef�gt und Du hast die Einladung (per Mail) angenommen.
  - PowerShell-Skripte startest Du durch "Rechte Maustaste > Mit PowerShell ausf�hren"; bearbeitest Du aber durch Doppelklick
  - Stelle zun�chst sicher, dass Git installiert ist (siehe A1. Git f�r Windows installieren)

1. Getting Started
  - Zieh Dir den ganzen Ordner "SimGruppe8_GitReady" an einen geeigneten Platz auf Deinem PC
  - Starte das PowerShell-Skript "gitStorePassword.ps1"
  - Gib' bei der Abfrage Deinen GitHub User-Namen und Dein -Passwort ein (Siehe: A2. Datenschutz)
  - Du bist bereit, alles zu benutzen!

2. Benutzung von Git
  - Willst Du nur auf den neusten Stand kommen:
    - Starte das PowerShell-Skript "gitPull.ps1"
  - Willst Du Deine �nderungen hochladen:
    - Starte das PowerShell-Skript "gitPushChain.ps1"
    - Dieses Skript:
      - Pullt den aktuellen Stand
      - Committet all Deine �nderungen
      - Fragt nach einer Textnachricht f�r den Commit (bitte immer ausf�llen)
      - Pusht schlie�lich den erstellten Commit

3. Was wird gepusht/gepullt?
  - .gitignore
  - gnc/controller_INDI.slx
  - gnc/INDI/*
  - (siehe .gitignore)
  - HINWEIS:
    Wie aus den genannten Files ersichtlich, ist es nicht vorgesehen, dass die Schnittstellen von den gepushten/gepullten Files ver�ndert werden.
    Sollte das dennoch notwendig sein, sprich das bitte mit den anderen Teilnehmern des Projektes ab.

4. Bekannte Bugs
  - Matlab Path nicht vollst�ndig
    - Es kann sein, dass der Ordner ~/gnc/INDI/ nicht automatisch dem Pfad hinzugef�gt ist und die Files nicht gefunden werden
    - Fix:
      - In der Matlab Konsole "pathtool" eingeben
      - Oben Links unter "Add Folder..." den Ordner "~/gnc/INDI/" hinzuf�gen

A1. Git f�r Windows installieren
  - Pr�fen ob Git installiert ist
    - Dr�cke die Windowstaste, schreibe "powershell" und dr�cke "Enter"
    - Schreibe "git" und dr�cke Enter
    - Wenn rote Schrift erscheint, ist Git nicht installiert, andernfalls schon
  - Git installieren
    - Downloade dir den GitInsaller unter http://git-scm.com/download/win
    - Folge den Installationsanweisungen
    - Starte Deinen Computer ggf. neu

A2. Datenschutz
  Sein Passwort speichern zu lassen ist optional. Man kann es alternativ auch jedes mal bei Skriptausf�hrung eingeben.
  Zum Speichern Deines Passworts wird der git-credential.helper verwendet.
  Dieser speichert dein Passwort in (mehr oder weniger) lesbarem Text standardm��ig unter "~/.git-credentials"
  Dies ist definitiv nicht die sicherste Variante, aber vermutlich die einfachste.
  Mit L�schen der "~/.git-credentials" Datei, wird Dein Passwort wieder sicher.