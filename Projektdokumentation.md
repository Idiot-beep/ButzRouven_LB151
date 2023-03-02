# Projekt-Dokumentation

Rouven Butz

| Datum     | Version | Zusammenfassung                                              |
| -----     | ------- | ------------------------------------------------------------ |
|18.01.2023 | 0.0.1   | Projektdokumentation erstellt                                |
|19.01.2023 | 0.0.2   | Projektdokumentation bis und mit Punkt 4 fertig              |
|23.02.2023 | 0.0.3   | Projekt erstellt und automatische Datenbankverknüpfung erstellt|
|28.02.2023 | 0.0.3   | GUI von Login und Spiel erstellt (noch nicht funktionsfähig)|
|01.03.2023 | 0.0.4   | Angefangen Spiellogik mit Datenbank und .xhtml Seiten zu verbinden|
|02.03.2023 | 0.0.5   | Ich habe die US - 20 implementiert und die Dokumentation abgeschlossen |




# 0 Ihr Projekt

Für die LB des Moduls 151 werde ich ein Glücksrad programmieren, welches gleich funktionieren soll, wie das im Fernsehen. Man kann also das Glücksrad drehen und verschiedene Aktionen ziehen. 

# 1 Analyse

* Tier 1 (Präsentation): Eine Website mit dem Glücksrad
* Tier 2 (Webserver): Daten aus einer Datenbank lesen und überprüfen
* Tier 3 (Application Server): Übereinstimmung von Buchstaben prüfen
* Tier 4 (Dataserver): Wörterliste und High-Score-Liste

# 2 Technologie

Ich werde mit Css, xhtml und JSF arbeiten. Dieses Format wird im Unterricht verwendet, so muss ich nicht alleine etwas völlig neues lernen. 

# 3 Datenbank

MySQL:
Ich werde MySQL verwenden, da es zuverlässig und benutzerfreundlich ist. Diese Entwicklungsumgebung wird auch im Unterricht verwendet. Da MySQL recht bekannt ist, hat es auch viele Tutorials und Foren, welche behilflich sein können.

# 4.1 User Stories

| US-№  | Verbindlichkeit | Typ        | Beschreibung                                                 |
| ----  | --------------- | ---------- | ----------------------------------                           |
| US-1  | Muss | Funktional | Als Administrator möchte ich mich mit Benutzernamen und Passwort anmelden können, um auf die Admin-Funktionen zugreifen zu können. |
| US-2  | Muss | Funktional | Als Administrator möchte ich Phrasen und Rätselwörter anlegen, ändern und löschen können, um das Spiel im Nachhinein problemlos verändern zu können.|
| US-3  | Muss | Funktional | Als Administrator möchte ich Kategorien anlegen können, um die Rätsel und Phrasen zu organisieren so dass der Benutzer die Website einfach bedienen kann. |
| US-4  | Muss | Funktional | Als Administrator möchte ich einzelne Einträge der Highscore-Liste löschen können, um deren Richtigkeit zu versichern |
| US-5  | Muss | Funktional | Als Kandidat möchte ich einen Webbrowser nutzen können, so dass ich das Spiel nicht herunterladen muss. |
| US-6  | Muss | Funktional | Als Kandidat möchte ich meinen Namen eingeben können, so dass dieser auf der Highscore-Liste erscheinen kann. |
| US-7  | Muss | Funktional | Als Kandidat möchte ich jederzeit meinen Kontostand sehen können, so dass ich immer weiss, wie viel Geld ich habe. |
| US-8  | Muss | Funktional | Als Kandidat möchte ich jederzeit meine Lebenspunkte sehen können, so dass ich immer weiss, wie oft ich noch raten kann. |
| US-9  | Muss | Funktional | Als Kandidat möchte ich erfahren ob die gewählte Antwort richtig oder falsch war, so dass ich meine Antwort dementsprechend anpassen kann. |
| US-10 | Muss | Funktional | Als Kandidat oder Administrator möchte ich in der Highscore-Liste meinen Rang, meinen Namen, den Zeitpunkt des Spiels, den Geldbetrag und die Anzahl Spielrunden sehen können, so dass man alles auf einen Blick sehen kann. |
| US-11 | Muss |  Qualität  | Als Kandidat möchte ich dass die Highscore-Liste nach Rang, welcher durch die Höhe des Geldbetrags bestimmt wird, aufsteigend sortiert ist, so dass ich die besten Kandidaten auf einen Blick sehen kann. |
| US-12 | Muss |  Qualität  | Als Kandidat möchte ich , dass kein Rätsel-Wort und keine Phrase mir mehr als einmal gestellt wird, so dass das Spiel interessant bleibt. |
| US-13 | Muss | Funktional | Als Kandidat möchte ich jederzeit die Möglichkeit haben, das Spiel zu beenden und meinen Betrag in die Highscore-Liste zu übertragen, so dass ich den Highscore besser schlagen kann. |
| US-14 | Muss |  Qualität  | Als Kandidat möchte ich, dass das Spiel mit genügend Wörtern befüllt ist, so dass ich den Highscore schlagen kann. |
| US-15 | Muss |  Qualität  | Als Kandidat möchte ich, dass die Anzahl Spielrunden gezählt werden, so dass ich diese mit anderen Kandidaten vergleichen kann. |
| US-16 | Muss |    Rand    | Als Entwickler möchte ich Formulareingaben auf Client und Serverseite überprüfen, so dass ich die Daten prüfen kann.  |
| US-17 | Muss |    Rand    | Als Entwickler möchte ich eine Datenbankanbindung verwenden, die möglichst unabhängig vom tatsächlich eingesetzten Produkt ist, so dass ich Verkomplikationen vermeiden. |
| US-18 | Kann |    Rand    | Als Entwickler möchte ich Transaktionsmanagement einsetzen, so dass ich Datenintegrität gewährleisten kann. |
| US-19 | Kann |    Rand    | Als Entwickler möchte ich, dass meine Kandidaten sichere Passwörter haben, um Kontostehlungen zu vermeiden. |
| US-20 | Kann |    Rand    | Als Kandidat möchte ich den Entwickler kontaktieren können, um mir bei Problemen zu helfen. |


# 4.2 Testfälle

|  | Vorbereitung | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  | Erstellen Sie ein gültiges Konto mit dem Benutzernamen "admin" und dem Passwort "123" | Geben Sie "admin" als Benutzernamen und "123" als Passwort ein | Erfolgreiche Anmeldung und Zugriff auf die Administrationsfunktionen |
| 2.1  | Als Admin anmelden Die Funktion ein Rätselwort zu erstellen aufrufen | "Welche Farbe hat eine Orange?" als Phrase eingeben, "Orange" als Antwort und "Früchte" als Kategorie | Erfolgreiche Anlage der Phrase oder des Rätselwortes |
| 3.1  | Als Admin anmelden, Funktion zum Anlegen einer Kategorie öffnen | "Gemüse" als Kategorie angeben | Erfolgreiche Anlage der Kategorie |
| 4.1  | Als Admin anmelden, Spieler1 erstellen, Highscore-Liste aufrufen | Den Eintrag "Spieler1" aus der Highscore-Liste anwählen und auf "Löschen" klicken | Erfolgreiche Löschung des Eintrags "Spieler1|
| 5.1  | Öffnen Sie die Anwendung im Webbrowser | - | Anzeige der Anwendung im Webbrowser |
| 6.1  | Website aufrufen| "Max Mustermann" als Namen eingeben, Spiel starten und beenden | Der Name "Max Mustermann" erscheint auf der Highscore-Liste |
| 7.1  | Als Kandidat anmelden, Spiel beginnen | - | Anzeige des aktuellen Kontostands |
| 8.1  | Als Kandidat anmelden, Spiel beginnen | - | Anzeige der aktuellen Lebenspunkte |
| 9.1  | Als Kandidat anmelden, Spiel beginnen | "Orange" für die Phrase "Welche Farbe hat eine Orange?" wählen | Anzeige "richtig" |
| 9.2  | Als Kandidat anmelden, Spiel beginnen | "Blau" für die Phrase "Welche Farbe hat eine Orange?" wählen | Anzeige "falsch" |
| 10.1 | Als Kandidat anmelden, Highscore-Liste aufrufen | - | Anzeige der Highscore-Liste, das Rangs, des Namens, den Zeitpunkt des Spiels, den Geldbetrag und die Anzahl Spielrunden|
| 10.2 | Als Administrator anmelden, Highscore-Liste aufrufen | - | Anzeige der Highscore-Liste, das Rangs, des Namens, den Zeitpunkt des Spiels, den Geldbetrag und die Anzahl Spielrunden|
| 11.1 | Als Kandidat anmelden, auf Highscore-Liste gehen | - | Anzeige der Highscore-Liste sortiert nach Höhe des Geldbetrags (Je mehr Geld desto höher der Rang, bester Rang: 1). |
| 12.1 | Als Kandidat anmelden, Spiel beginnen | Spiel 10 Mal nacheinander spielen | Keine Wiederholung von Rätsel-Wörtern und Phrasen. |
| 13.1 | Als Kandidat anmelden, Spiel beginnen | Eine Antwort richtig wählen und auf "Aufhören" klicken. | Der aktuelle Gewinn des Kandidaten wird in die Highscore-Liste übernommen und das Spiel beendet. |
| 14.1 | Als Kandidat anmelden, Spiel beginnen | 1 Spiel spielen | Das Spiel enthält eine ausreichende Anzahl an Wörtern und Fragen für ein Spiel |
| 15.1 | Als Kandidat anmelden, Spiel beginnen | 3 Spiele spielen | Anzeige der Anzahl der gespielten Runden im Spiel |
| 16.1 | Als Admin anmelden,| Leeres Textfeld eingeben | Entsprechende Fehlermeldung wird ausgegeben. |
| 17.1 | Über Datenbankanbindungen informieren | - | Erfolgreiche Verbindung der Anwendung mit der gewählten Datenbank |
| 18.1 | Falsche Daten vorbereiten | Falsche Daten eingeben | Entsprechende Fehlermeldung wird ausgegeben. |
| 19.1 | - | Als Kandidat anmelden, als Passwort: "123" eingeben | Entsprechende Fehlermeldung wird ausgegeben. |
| 20.1 | Kandidat bereitstellen | Kandidat versucht Entwickler zu kontaktieren | Kandidat kann Entwickler erreichen. |


# 5 Prototyp
![Vorlage Login](https://user-images.githubusercontent.com/69579094/222450697-2bc2f68a-b82e-4a90-a729-0c872fed5276.png)

![Vorlage Glücksrad](https://user-images.githubusercontent.com/69579094/222450725-554f25f0-5a5b-47b4-a717-8d9776fe7969.png)

# 6 Implementation

| User Story | Datum | Beschreibung |
|------------|-------|--------------|
| US - 1 bis US - 15 | 23.02 | Fundament für diese Userstories gelegt|
| US - 1 bis US - 15 und US - 19 | 28.02 | Fundament für diese Userstories gelegt|
| US - 1 bis US - 15 | 01.03 | Habe versucht, das Glücksrad teilweise zum Laufen zu bringen |
| US - 20 | 02.03 | E-Mail auf der Seite mit dem Glücksrad eingefügt |

# 7 Projektdokumentation

| US | Erledigt? | Entsprechende Code-Dateien oder Erklärung |
| ---- | --------- | ----------------------------------------- |
| 1 | nein | Login ist in der index.xhtml Seite zu finden (nicht funktionsfähig)|
| 2 | nein | Noch nicht implementiert |
| 3 | nein | Noch nicht implementiert |
| 4 | nein | Noch nicht implementiert |
| 5 |  ja  | Das ganze Projekt ist für den Browser ausgelegt |
| 6 | nein | Noch nicht implementiert |
| 7 | nein | Noch nicht implementiert |
| 8 | nein | Noch nicht implementiert |
| 9 | nein | Noch nicht implementiert |
| 10 | nein | Noch nicht implementiert |
| 11 | nein | Noch nicht implementiert |
| 12 | nein | Noch nicht implementiert |
| 13 | nein | Noch nicht implementiert |
| 14 | nein | Noch nicht implementiert |
| 15 | nein | Noch nicht implementiert |
| 16 | nein | Noch nicht implementiert |
| 17 |  ja  | Ich habe wie geplant MySQL verwendet |
| 18 | nein | Noch nicht implementiert |
| 19 | nein | Der unvollständige Login ist auf der index.xhtml Seite |
| 20 |  ja  | Meine E-Mail kann auf der template.xhtml gesehen werden |

# 8 Testprotokoll

✍️ Fügen Sie hier den Link zu dem Video ein, welches den Testdurchlauf dokumentiert.

|        | Datum | Resultat | Tester |
| ------ | ----- | -------- | ------ |
| 1.1.1  | 02.03 |   NOK    |  Butz  |
| 2.1.1  | 02.03 |   NOK    |  Butz  |
| 3.1.1  | 02.03 |   NOK    |  Butz  |
| 4.1.1  | 02.03 |   NOK    |  Butz  |
| 5.1.1  | 02.03 |    OK    |  Butz  |
| 6.1.1  | 02.03 |   NOK    |  Butz  |
| 7.1.1  | 02.03 |   NOK    |  Butz  |
| 8.1.1  | 02.03 |   NOK    |  Butz  |
| 9.1.1  | 02.03 |   NOK    |  Butz  |
| 10.1.1  | 02.03 |   NOK    |  Butz  |
| 11.1.1  | 02.03 |   NOK    |  Butz  |
| 12.1.1  | 02.03 |   NOK    |  Butz  |
| 13.1.1  | 02.03 |   NOK    |  Butz  |
| 14.1.1  | 02.03 |   NOK    |  Butz  |
| 15.1.1  | 02.03 |   NOK    |  Butz  |
| 16.1.1  | 02.03 |   NOK    |  Butz  |
| 17.1.1  | 02.03 |    OK    |  Butz  |
| 18.1.1  | 02.03 |   NOK    |  Butz  |
| 19.1.1  | 02.03 |   NOK    |  Butz  |
| 20.1.1  | 02.03 |    OK    |  Butz  |

Fazit:
Dieses Projekt konnte nicht zufriedenstellend implementiert werden, da ich noch sehr viele andere Dinge zu tun hatte, welche wichtiger und zeitaufwändiger waren.

# 9 `README.md`

Alle Informationen und Unterlagen um dieses Projekt selbst ausführen zu könne, findet man in dem README.md Dokument.

# 10 Allgemeines

- [X] Ich habe die Rechtschreibung überprüft
- [X] Ich habe überprüft, dass die Nummerierung von Testfällen und User Stories übereinstimmen
- [ ] Ich habe alle mit ✍️ markierten Teile ersetzt
