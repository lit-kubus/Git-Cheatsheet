# Github Cheatsheet

## Table of contents
- [Github Cheatsheet](#github-cheatsheet)
  - [Table of contents](#table-of-contents)
  - [Input](#input)
  - [Commands](#commands)
  - [Arbeiten im Workplace](#arbeiten-im-workplace)
  - [Arbeiten mit dem Index](#arbeiten-mit-dem-index)
  - [Inhalt des Staging ansehen](#inhalt-des-staging-ansehen)
  - [Arbeiten mit dem lokalen Repository](#arbeiten-mit-dem-lokalen-repository)
  - [Arbeiten mit dem remote Repository](#arbeiten-mit-dem-remote-repository)
  - [Arbeiten mit Tags](#arbeiten-mit-tags)


## Input
Diese Dokument dient als unterstützung für das bearbeiten von Aufträgen, die mit GIT zu tun haben


## Commands

File Änderung
>vi, nano, vsc  

Änderung staged
>git add 

Änderung versioniert
>git commit  


## Arbeiten im Workplace

File oder Verzeichnis unter Git Control löschen
> $ git rm {file} / $ git rm {dir}

File oder Verzeichnis unter Git Control verschieben
> $ git mv {file} / $ git mv {dir}


## Arbeiten mit dem Index

Zeigt den aktuellen File Status
> $ git status

Neues oder geänderte File(s) unter Git Control bringen.
> $ git add {file}

Fügt alle neuen oder geänderten Files dem Index zu
> git add . 

Ein versehentlich ge-staged File wieder aus dem Index entfernen
> $ git reset HEAD {file}


## Inhalt des Staging ansehen

Zeigt was im Worsplace geändert, aber noch nicht im Index (staged) ist.
> $ git diff

Zeigt was bereits zum Commit vorgemerkt wurde.
> $ git diff --cached  (auch -- staged)


## Arbeiten mit dem lokalen Repository

Im Index vorgemerkte Änderungen in das lokale Repository committen
> git commit {fie}

Commit Historie ansehen
> $ git log

Ein im Workplace modifiziertes File wieder auf den Stand des letzter Commit setzen
> $ git checkout -- {file}


## Arbeiten mit dem remote Repository
Remote Repository anzeigen
> $ git remote -v

Alle Änderungen vom remote Repository (origin) in den Workplace laden
> $ git pull

Änderungen vom lokalen Repository nach remote pushen. Vor einem push immer zuerst ein pull ausführen
> git push origin


## Arbeiten mit Tags
Vorhandene Tags listen
> $ git tag

Tag erstellen (Annonated)
> $ git tag -a v1.5 -m "Version 1.5"

Tag Content ansehen
> git tag show v1.5

Einen spezifischen Tag nach origin pushen
> $ git push origin v1.5

Alle Tags gleichzeitig pushen
> git push origin --tags

Lokale Tags löschen
> $ git tag -d v1.5

Remote Tags löschen
> $ git push origin --delete v1.5