# Was D.R.O.N.E. kann

Die vollständige Funktionsliste, nach Themen sortiert. Das hier beschreibt,
**was** die Mod tut. Wie man sie bedient und einrichtet, steht in der
Anleitung, die dem Paket beiliegt.

Stand: Version 0.6.0.

---

## Verbindung

- **Standard-Source-RCON.** Jeder gängige RCON-Client und jeder Bot spricht das
  Protokoll bereits. Kein eigener Dialekt, keine Sonderbibliothek.
- **Läuft im Serverprozess.** Keine Brücke, kein zweites Programm, kein Admin,
  der online sein muss.
- **Funktioniert auf dem leeren Server.** Spawns, Events, Teleports und
  Aufräumbefehle gehen auch, wenn niemand eingeloggt ist.
- **Bots laufen unverändert weiter.** Die Ausgabeformate der Spielerlisten sind
  byte-genau an den etablierten SCUM-RCON-Lösungen geeicht.
- **Lange Antworten kommen vollständig**, auch bei mehreren tausend Zeichen.
- **UTF-8.** Spieler mit Umlauten im Namen werden gefunden.
- **Befehle der Mod kosten den Server nichts.** Spielerlisten dürfen im
  Sekundentakt abgefragt werden, ohne dass der Spielablauf darunter leidet.

## Spielbefehle

- **Alle 233 Admin-Befehle des Spiels** über die Verbindung, genau so, wie ein
  Admin sie im Spielchat tippen würde.
- **Die Befehlsliste kommt live aus dem Spiel.** Bringt ein SCUM-Update neue
  Befehle, sind sie sofort da. Eine Nachschlagefunktion zeigt jeden Befehl mit
  seinen Argumenten.
- **Befehle für einen bestimmten Spieler**, auch solche, die im Spiel nur auf
  den Aufrufer selbst wirken (unsterblich, Godmode, Attribute, Skills,
  Ohnmacht). Über die Verbindung treffen sie den gewünschten Spieler.
- **Die fachliche Antwort des Spiels abholen.** Statt nur "abgesetzt" bekommt
  man die echte Rückmeldung: wie viele Leichen entfernt wurden, warum ein Spawn
  nicht ging, was eine Abfrage ergab.
- **Dieselben Zusatzbefehle auch im Spielchat.** Wer als Admin eingeloggt ist,
  kann die Befehle der Mod dort tippen wie die Spielbefehle.

## Spieler

- **Wer ist online**, mit SteamID, Kontostand und Live-Position.
- **Wer war je da**: alle Spieler aus der Server-Datenbank.
- **Einen Spieler nachschlagen** über Namen, SteamID oder Spielnummer, auch
  während der Server noch startet.
- **Steckbrief abfragen**, ohne dass der Spieler etwas davon im Chat sieht.
- **Chat an alle oder an einen einzelnen Spieler**, in acht Farben.
- **Ansagen** als Einblendung für alle.
- **Teleportieren**: an Koordinaten, zu einem anderen Spieler, zu einem
  Fahrzeug, zu einer Kiste.
- **Steckengebliebene befreien** mit einem Befehl.
- **Geld und Fame** setzen oder ändern, einzeln oder für alle Online-Spieler.
- **Spielerzustand**: unsterblich, Godmode, unendlich Munition, Attribute,
  Skills, Magen, Ohnmacht, Fallschirm.

## Fahrzeuge

- **Alle Fahrzeuge auflisten** mit ID, Typ, Position und Besitzer.
- **Die Fahrzeuge eines Spielers auflisten**, über Namen oder SteamID.
- **Ein Fahrzeug zum Spieler holen.** Das kann SCUM selbst nicht, nur den
  Spieler zum Fahrzeug.
- **Ein Fahrzeug an Koordinaten setzen.** Die Höhe wird vorher geprüft, ein
  Fahrzeug fällt nicht mehr aus der Welt.
- **Alle Fahrzeuge eines Typs auf ein Raster stellen**, etwa zum Aufräumen
  eines Parkplatzes.
- **Trockenlauf**: erst anzeigen, welches Fahrzeug gemeint wäre, dann bewegen.
  Bei Zweifeln bewegt die Mod lieber nichts als das falsche Auto.
- **Auch am anderen Kartenende.** Fahrzeuge, die gerade nicht geladen sind,
  holt die Mod selbst in den Speicher.
- **Fahrzeuge nach dem Neustart schneller in die Welt bringen.** Ab Werk setzt
  der Server eines alle zwei Sekunden, bei 700 Fahrzeugen sind das 23 Minuten.
  Mit der Mod sind es rund 7.

## Kisten

- **Kisten finden** über einen Teil des Namens oder über die ID, mit Position
  und Besitzer. Auch Kisten, die in anderen Behältern oder Fahrzeugen stecken.
- **Einen Spieler zur Kiste teleportieren.**
- **Kisten-Sortierer**: räumt eine offene Kiste in die umstehenden Kisten, nach
  deren Namen. **Experimentell**, ab Werk aus. Er arbeitet noch nicht
  zuverlässig, es geht aber nichts verloren.

## Spawnen

- **Items, Behälter voller Items, Zombies, Tiere, NPCs, Fahrzeuge** an
  beliebigen Koordinaten oder direkt vor einem Spieler.
- **Events**: Cargo-Drops und andere Weltereignisse an einem Ort oder beim
  Spieler.
- **Die Höhe darf fehlen.** Die Mod misst den Boden selbst und trägt sie nach.
  Findet sie keinen Boden, sagt sie es, statt zu raten. Die Bodenhöhe lässt
  sich auch einzeln abfragen.
- **Aufräumen im Umkreis**: Zombies, Tiere, Leichen, einzelne Item-Typen. Dazu
  Basisbau und Flaggen eines Spielers.

## Welt und Regeln

- **Zeit, Zeitgeschwindigkeit, Wetter, Nebel** stellen.
- **Ingame-Uhrzeit abfragen**, sekundengenau aus dem laufenden Server: eine
  Zeile für Menschen, eine für Bots. Auch während der Server noch startet.
- **Survival-Regler** zur Laufzeit: wie schnell Spieler dreckig oder nass
  werden, wie schnell Schuhe verschleißen, wie schnell Kleidung trocknet, und
  mehr. Als Faktor auf das normale Spiel, jederzeit zurücksetzbar.
- **Strahlenzonen** einzeln oder alle auf einmal: Reichweite, Kern, Stärke,
  Verlauf. Zonen abschalten oder verstärken, ohne Neustart.
- **Spielwerte setzen, für die es keine Serveroption gibt.** Türen, die sich
  von selbst schließen, sind das Paradebeispiel. Alles zur Laufzeit, alles
  zurücksetzbar.
- **Handelstabelle lesen**: was welcher Händler zu welchem Preis führt. Damit
  lässt sich zum Beispiel klären, warum ein Spieler etwas nirgends verkaufen
  kann.

- **Obergrenzen von Servereinstellungen anheben.** Manche Werte deckelt der
  Server beim Start stillschweigend, etwa die Zahl der Rager. Mit der Mod
  bleibt der eingetragene Wert stehen.

## Server und Moderation

- **Kicken, bannen, entbannen, stummschalten, Chatverbot auf Zeit.**
- **Squads und Flaggen** auflisten, mit Mitgliedern, Besitzern und Positionen.
- **Generatoren um eine Flagge** auflisten, mit Füllstand.
- **Server herunterfahren**, mit Ansage davor.
- **Sessionlog** pro Serverlauf, im Logordner von SCUM: jeder Befehl mit
  Zeitstempel und Antwort.
- **Bunker-Terminals**: wer zuletzt an den Terminals der Abandoned Bunker
  Daten geladen hat, mit Restsperre. Auf Wunsch steht jeder Download im
  Sessionlog.
- **Inventar- und Leichen-Log**: wer welchen Behälter öffnet, mit Besitzer und
  Ort; Leichen von Spielern sind mit dem Namen des Toten markiert. Nur
  mitschreiben, nichts sperren. **Experimentell**, ab Werk aus.
- **Diagnose**: lebt die Mod, ist alles bereit, was kostet welcher Befehl.

## Quests

- **Ausgesperrte Spieler wieder hereinlassen.** Manche Quests werfen den
  Spieler beim Login vom Server, bevor er sie abbrechen kann. Die Mod findet
  diese Spieler, befreit einen oder alle, und sichert vorher, was sie löscht.
- **Zeit bis zum Quest-Reset** abfragen, per Verbindung und im Spielchat.

## Rechte

- **Rechte je Admin.** SCUM kennt nur "Admin oder nicht": wer kicken darf, darf
  auch Basen löschen. Mit der Mod bekommt jeder Admin genau die Befehle, die er
  haben soll. Wer nichts einträgt, bleibt Admin wie bisher.
- **Gruppen.** "Moderator", "Eventleitung", "Beobachter" einmal definieren,
  Gruppen dürfen aufeinander aufbauen.
- **Dev-Rechte ohne Datenbankeingriff.** Welche Spieler erweiterte Befehle
  nutzen dürfen, steht in einer einfachen Textdatei. Die Mod trägt es beim
  Serverstart ein.
- **Befehle für alle Spieler freigeben.** Ab Werk dürfen nur Admins die
  Befehle der Mod im Chat nutzen. Die lesenden (Uhrzeit, Quest-Reset) lassen
  sich für jeden Spieler öffnen.
- **Anzeigen, wer was darf**, und neu einlesen ohne Neustart.

## Was von allein läuft

Alles hier ist ab Werk aus. Wer nichts einschaltet, merkt nichts.

- **Generatoren, die nie leer werden.** Für Handelsposten, Com-Zone,
  Eventgelände: die Generatoren um eine Flagge werden bei jedem Serverstart
  vollgetankt.
- **Türen, die sich von selbst schließen**, je Türsorte wählbar. Fertige
  Auswahl für Wohnhäuser, Plattenbau, Schule, Krankenhaus und Garagen.
- **Genähte Kleidung sieht wieder neu aus.** Im Spiel behält genähte Kleidung
  ihre weißen Fäden, obwohl sie heil ist. Mit der Mod verschwinden sie,
  normaler Verschleiß bleibt sichtbar.
- **Abreißen in der eigenen Squad-Base ab wählbarem Rang.** Seit einem
  SCUM-Update dürfen nur noch Underboss und Boss Bauteile wegnehmen. Mit der
  Mod geht es wieder ab dem Rang, den der Betreiber wählt.
- **Nachts andere Regeln.** Spielwerte wie Tempo, Leben oder Schaden der
  Zombies ab Sonnenuntergang anders setzen. Die Mod fährt sie schrittweise hoch
  und bei Sonnenaufgang genauso zurück auf den Tagwert.
- **Updates ohne Serverhalt.** Neue Version bei laufendem Server ablegen, die
  Mod prüft die Prüfsummen, übernimmt die Dateien, ergänzt neue Einstellungen
  und archiviert, was sie ersetzt hat. Geladen wird beim nächsten Neustart.

## Werkzeuge

- **Konfigurator im Browser.** Eine einzelne HTML-Datei, läuft ohne Server und
  ohne Internet. Jede Einstellung ist dort erklärt.
- **Kommandozeilen-Client** zum Ausprobieren von Hand.
- **Selbsttest**, der alle Befehle gegen den eigenen Server durchprobiert.
- **Briefing für KI-Assistenten.** Eine einzelne Datei, mit der ein Assistent
  den Server sofort steuern kann, samt aller Fallen.

---

[Zurück zur Übersicht](README.md)
