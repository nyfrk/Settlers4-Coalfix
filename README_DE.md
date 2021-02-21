

# Die Siedler 4: Kohlefix Plugin

![kohlefix](kohlefix.png)

Standardmäßig wird die Größe Deiner Wirtschaft durch den so genannten Kohle-Bug begrenzt. Das ist der Fall, wenn die Wirtschaft eines Spielers mehr Güter verbraucht, als das Spiel den Trägern Trageaufträge zuweisen kann. Da Kohle das am meisten verarbeitete Gut ist, ist es in der Regel auch das erste, welches davon betroffen ist - was letztlich dazu führt, dass die Schmieden oder Schmelzen verhungern, obwohl mehr als genug Kohle produziert wird. 

Dieses Plugin behebt den Kohlebug für Die Siedler 4.

Für dieses README gibt es eine [englische Version](README.md). Bitte beachte, dass die deutsche Übersetzung ggf. veraltet sein kann.


![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)![coalcarrier](coalcarrier.gif)



## Features

* Behebt den Kohle-Bug - für Kohle und jedes andere Gut im Spiel.
* Entfernt die Verzögerung beim Zuweisen eines Auftrags an einen Träger. Träger reagieren viel schneller auf Deine Befehle!
* Kompatibilität: Das Plugin läuft sowohl mit der Gold Edition als auch der History Edition von Die Siedler 4.
* Multiplayerfähig: Alle Teilnehmern müssen das Plugin verwenden, ansonsten kommt es zu Desyncs!



## Installation

Du benötigst einen ASI Loader um die Mod zu nutzen. Ich empfehle den [The Settlers 4: ASI Loader](https://github.com/nyfrk/Settlers4-ASI-Loader), da er gut mit der Gold und History Edition von Die Siedler 4 funktioniert und keinerlei Konfiguration erfordert. 

1. Lade ein [Release](https://github.com/nyfrk/Settlers4-Coalfix/releases) herunter.
2. Entpacke die Dateien in dein `plugins` Verzeichnis.
3. Starte das Spiel. Das Plugin sollte nun automatisch geladen werden.

Um das Plugin zu deinstallieren, entferne die `CoalFix.asi` aus dem `plugins`-Verzeichnis. 



## Bekannte Probleme

* Dieses Plugin behebt nicht wirklich den Kohle-Bug, sondern erhöht stattdessen das Limit. Anstatt alle 16 Ticks einen Auftrag an einem Träger zuzuweisen, wird nun jeden Tick ein Auftrag zugewiesen. Um den Bug wirklich zu beheben, müssten wir die offenen Trageaufträge in einer Schleife durchlaufen und jeweils einem Träger zuweisen, solange noch ein freier Träger irgendwo vorhanden ist.

  

## Probleme und Fragen

Das Projekt verwendet den Github Issue Tracker. Bitte öffne [hier](https://github.com/nyfrk/Settlers4-Coalfix/issues) ein Ticket für dein Anliegen. 



## Mitmachen

Das offizielle Repository dieses Projekts ist unter https://github.com/nyfrk/Settlers4-Coalfix verfügbar. 

##### Kompilieren

Lade Visual Studio 2017 oder 2019 mit der C++-Toolchain herunter. Das Projekt ist so konfiguriert, dass es mit der Windows XP-kompatiblen **v141_xp**-Toolchain gebaut wird. Du solltest jedoch die Toolchain nach Belieben ändern können. Es sind keine zusätzlichen Bibliotheken erforderlich, sodass das Projekt ohne weiteres gebaut werden kann. 

#### Wie funktioniert das Plugin?

Das Spiel weist einen Trageauftrag alle 16 Ticks (~1,14 s) einem Träger zu (bei Kohle sind es sogar zwei). Beim Erstellen eines Jobs wendet das Spiel eine Verzögerung von 32 Ticks (~2,28 s) an. Das Plugin verringert die Timings in beiden Fällen auf 1 Tick (~0,07 s) und verschiebt damit das Limit, welches letztlich zum Kohle-Bug führt.

## Lizenz

Das Projekt ist unter der [MIT](LICENSE.md)-Lizenz lizenziert. 
