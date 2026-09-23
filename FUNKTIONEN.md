# Was D.R.O.N.E. kann

Die vollständige Funktionsliste, nach Themen sortiert. Das hier beschreibt,
**was** die Mod tut. Wie man sie bedient und einrichtet, steht in der
Anleitung, die dem Paket beiliegt.

Stand: Version 0.7.0.

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
- **Abo-Kanal für Bots.** Statt jede Sekunde nachzufragen, meldet sich ein Bot
  einmal an und bekommt von selbst geliefert: jede Sekunde alle Spieler mit
  Position, Blickrichtung und Neigung, jede Minute Ruhm, Geld, Gold und
  Spielzeit, dazu jeden Kill an Zombies, NPCs und Tieren, sobald er passiert.
  Eine JSON-Zeile je Meldung, über dieselbe RCON-Verbindung, kein zweiter
  Port. Ein Fehler sieht nie aus wie ein leerer Server. Ab Werk aus.

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

## Zeit und Wetter

- **Zeit, Zeitgeschwindigkeit, Wetter, Nebel** stellen.
- **Ingame-Uhrzeit abfragen**, sekundengenau aus dem laufenden Server: eine
  Zeile für Menschen, eine für Bots. Auch während der Server noch startet.
- **Regen, der die Felder nicht erreicht.** Ein bekanntes SCUM-Rätsel: es
  regnet sichtbar, Kleidung wird nass, aber kein Gartenfeld bekommt Wasser. Die
  Mod erklärt die Ursache und behebt es ohne Neustart, und sie löst es selbst
  nie aus.
- **Handelstabelle lesen**: was welcher Händler zu welchem Preis führt. Damit
  lässt sich zum Beispiel klären, warum ein Spieler etwas nirgends verkaufen
  kann.

## Strahlenzonen

Die Insel hat **28 Strahlungsquellen**, und sie sind sehr unterschiedlich groß:
fünf reichen anderthalb Meter weit, eine einzige überspannt 3500 x 2500 m. Wer
"die Strahlung" regeln will, meint fast immer diese eine, denn sie ist der
Grund, warum die Stadt neben dem Kraftwerk niemand betritt.

- **Alle Zonen auflisten**, mit Standort, Kantenlänge, Kerngröße, Stärke und
  Verlauf. Daraus liest man ab, welche Zone man eigentlich meint, und die
  Nummer dahinter ist der Griff für alles Weitere.
- **Vier Regler je Zone**: wie weit die Zone insgesamt reicht, wie groß der
  Kern mit voller Stärke ist, wie stark es dort strahlt, und wie der Übergang
  vom Kern zum Rand verläuft.
- **Eine Zone abschalten**, ohne die anderen anzufassen. Oder umgekehrt eine
  kleine Zone auf ein ganzes Gelände ausweiten.
- **Alle Zonen auf einmal**, als Anteil statt als feste Zahl: "überall halb so
  stark" geht in einer Zeile, und die Verhältnisse zwischen den Zonen bleiben
  dabei erhalten.
- **Zur Laufzeit, ohne Neustart.** Ein Befehl holt alle Zonen wieder auf den
  Stand vom Serverstart zurück.
- **Dauerhaft in der Konfiguration**, mit denselben vier Reglern je Zone.
- **Eine Warnung gehört dazu:** der Geigerzähler im Spiel taugt nicht zum
  Prüfen. Seine Nadel malt der Client aus einer fest eingebauten
  Strahlungskarte, und die ändert sich nie. Eine abgeschaltete Zone zeigt er
  weiter als gefährlich an, während der Körper längst nichts mehr aufnimmt.
  Verlässlich ist nur der Sv-Wert im Charakterbogen.

## Survival-Regler

Sieben Regler dafür, wie hart das Überleben ist. Alle zur Laufzeit, ohne
Neustart, und jederzeit komplett zurücksetzbar:

| Regler | was er dreht |
|---|---|
| Dreck | wie schnell Spieler dreckig werden |
| Nässe | wie schnell sie nass werden |
| Schuhe | wie schnell Schuhwerk verschleißt |
| Füße | wie schnell die Füße wund werden |
| Trocknen | wie schnell Kleidung wieder trocken wird |
| Aufsaugen | wie schnell Wasser in die Kleidung wandert |
| Abgeben | wie schnell sie es wieder abgibt |

- **Der Wert ist ein Faktor auf das normale Spiel.** 1 ist der
  Auslieferungszustand, 0,15 ist ein Siebtel davon, 0 ist aus. Niemand muss
  wissen, welche Zahl SCUM intern führt.
- **Das Spiel unterscheidet 43 Untergründe** - Asphalt, Gras, Schlamm, Wasser,
  Schnee und so weiter -, und jeder hat eigene Werte. Die Mod zeigt auf Wunsch
  alle 43 mit ihren Einzelwerten, damit nachvollziehbar bleibt, warum der
  Waldweg anders wirkt als die Straße.
- **Dauerhaft in der Konfiguration**, oder eben nur für diesen einen Serverlauf.

## Stellschrauben: Werte, für die es keine Serveroption gibt

Die `ServerSettings.ini` gibt eine Handvoll Regler heraus. Die Mod gibt den Rest
heraus: Werte, die SCUM fest eingebaut hat und an die sonst niemand herankommt.
Je Wert eine Zeile, und es braucht dafür keine neue Version der Mod.

Was sich damit einstellen lässt, quer durch das Spiel:

| Bereich | Beispiele |
|---|---|
| Spieler | Lauftempo und alles andere an der Spielfigur |
| Zombies, Tiere, Wächter | Tempo, Verhalten, wie weit sie sehen und hören |
| Fahrzeuge und Boote | wie sie sich im Wasser verhalten, wie lange ein Wrack liegen bleibt |
| Türen | ob sie von selbst zufallen und nach wie langer Zeit |
| Sprengstoff | Schaden und Radius von Granaten und Fallen |
| Kleidung | wie schnell Wasser hineinzieht und wieder heraus |
| Gerät | Kettensäge, Angelrute und was sonst Werte hat |
| Gartenfelder | bis wohin sich gießen lässt und bis wohin der Regen füllt |
| Bunker | wie stark er bei Alarm nachlegt |

- **Es ist kein Kasten mit zwanzig Schaltern.** Über hundert Bereiche des
  Spiels sind erreichbar, zusammen weit über tausend Einzelwerte. Allein an der
  Spielfigur hängen mehrere hundert.
- **Absolut oder als Anteil.** "Spieler laufen zehn Prozent schneller" lässt
  sich hinschreiben, ohne zu wissen, welche Zahl SCUM dafür führt.
- **So breit oder so eng, wie du willst.** Alle Türen einer Bauart auf einmal,
  oder genau ein einzelnes Tor. Damit geht eine Regel für den ganzen Server und
  daneben eine Ausnahme.
- **Beim Serverstart oder mitten im Betrieb**, und mit einem Befehl alles zurück
  auf Auslieferungszustand. Ein verdrehter Wert kostet keinen Neustart.
- **Du läufst nicht ins Leere.** Ein Wert, den es so nicht gibt, wird abgelehnt
  statt stillschweigend geschluckt. Wo eine Servereinstellung dasselbe regelt
  und ohnehin gewinnen würde, sagt die Mod es dir. Und eine geprüfte Liste liegt
  bei, damit niemand bei null anfangen muss.

### Was Betreiber damit machen

- **Türen, die von selbst zufallen.** SCUM hat das eingebaut und fast überall
  abgeschaltet. Eine fertige Vorlage liegt bei, für Wohnhäuser, Plattenbau,
  Schule, Krankenhaus, Polizei, Kirche und die drei Garagentore: rund 4.600
  Türen, mit einstellbarer Zeit bis zum Zufallen.
- **Fahrzeuge nach dem Neustart schneller in der Welt**, rund 7 Minuten statt 23.
- **Wie nass ein Gartenfeld werden darf.** Zwei Grenzen, die SCUM fest
  eingebaut hat: von Hand gießen endet bei 4,75 Litern, und Regen füllt ein Feld
  nur bis 1,8 Liter - darüber bringt er nichts mehr, egal wie lange es schüttet.
  Beide Grenzen sind frei einstellbar, Regen darf ein Feld also auch ganz
  volllaufen lassen.
- **Einen Bunker, der bei Alarm härter zur Sache geht.**
- **Schnellere Spieler**, oder langsamere.
- **Mehr, als das Spiel zulässt.** Manche Zahlen in der `ServerSettings.ini`
  deckelt der Server beim Start stillschweigend, etwa die Menge der Rager. Der
  eingetragene Wert steht dann zwar da, gilt aber nicht. Mit der Mod bleibt er
  stehen.

Und für die Türen gibt es Hilfe: die Mod zeigt, welche Türarten auf deinem
Server überhaupt vorkommen und wie viele es davon gibt. Wenn du im Spiel die
Türen aufmachst, um die es dir geht, nennt sie dir danach genau diese - statt
dich aus 415 Bauarten raten zu lassen.

### Zombies live umstellen

Tempo, Leben und Schaden der Zombies hängen nicht an diesen Werten, sondern an
eigenen Schaltern der Spiel-Engine. Die Mod stellt auch die: beim Serverstart
oder mitten im laufenden Betrieb, ohne dass jemand etwas davon merkt.

## Server und Moderation

- **Kicken, bannen, entbannen, stummschalten, Chatverbot auf Zeit.**
- **Squads und Flaggen** auflisten, mit Mitgliedern, Besitzern und Positionen.
- **Generatoren um eine Flagge** auflisten, mit Füllstand.
- **Server herunterfahren**, mit Ansage davor.
- **Sessionlog** pro Serverlauf, im Logordner von SCUM: jeder Befehl mit
  Zeitstempel und Antwort, dazu der komplette Satz Einstellungen, mit dem
  dieser Lauf gestartet ist. Das Passwort steht nicht darin, nur seine Länge.
- **Bunker-Terminals**: wer zuletzt an den Terminals der Abandoned Bunker
  Daten geladen hat, mit Restsperre. Auf Wunsch steht jeder Download im
  Sessionlog.
- **Inventar- und Leichen-Log**: wer welchen Behälter öffnet, mit Besitzer und
  Ort; Leichen von Spielern sind mit dem Namen des Toten markiert. Nur
  mitschreiben, nichts sperren. **Experimentell**, ab Werk aus.
- **Kill-Log für alles außer Spielern.** SCUM schreibt nur Kills an Spielern
  mit. Die Mod schreibt den Rest: wer tötet welchen Zombie, NPC, welches Tier,
  welchen Mech, Razor oder Dropship, womit, aus welcher Entfernung, an welcher
  Stelle und wo. Es zählt der letzte Treffer. Als Datenquelle für Events und
  Ranglisten. Ab Werk aus.
- **Diagnose**: lebt die Mod, ist alles bereit, was kostet welcher Befehl. Und
  die eine Frage, die nach jedem SCUM-Update zuerst kommt: sitzen die Stellen
  im Programm noch, auf die die Mod aufsetzt.

## Quests

- **Ausgesperrte Spieler wieder hereinlassen.** Manche Quests werfen den
  Spieler beim Login vom Server, bevor er sie abbrechen kann. Die Mod findet
  diese Spieler, befreit einen oder alle, und sichert vorher, was sie löscht.
- **Mit einer Reißleine.** Passt die Auswahl auf mehr Spieler als erlaubt,
  bricht der Lauf ab und löscht gar nichts - ein zu weit gefasster Eintrag
  würde sonst dem halben Server die Quests nehmen.
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
  Befehle der Mod im Chat nutzen. Die lesenden lassen sich einzeln für jeden
  Spieler öffnen: die Ingame-Uhrzeit und die Zeit bis zum Quest-Reset, jeweils
  deutsch oder englisch.
- **Anzeigen, wer was darf**, und neu einlesen ohne Neustart.
- **Das Entwicklerwerkzeug ist ab Werk gesperrt.** Was tief in den Server
  hineingreift, antwortet ohne einen ausdrücklich gesetzten Schalter mit einem
  Hinweis statt zu laufen. Auf einem Server mit Spielern bleibt der Schalter
  aus.

## Was von allein läuft

Alles hier ist ab Werk aus. Wer nichts einschaltet, merkt nichts.

- **Generatoren, die nie leer werden.** Für Handelsposten, Com-Zone,
  Eventgelände: die Generatoren um eine Flagge werden bei jedem Serverstart
  vollgetankt. Angegeben wird entweder eine Flagge samt Umkreis oder ein
  einzelner Generator; statt randvoll geht auch eine bestimmte Füllmenge, und
  der Verbrauch je Stunde lässt sich mitverstellen.
- **Türen, die sich von selbst schließen**, je Türsorte wählbar. Fertige
  Auswahl für Wohnhäuser, Plattenbau, Schule, Krankenhaus und Garagen.
- **Genähte Kleidung sieht wieder neu aus.** Im Spiel behält genähte Kleidung
  ihre weißen Fäden, obwohl sie heil ist. Mit der Mod verschwinden sie,
  normaler Verschleiß bleibt sichtbar. Drei Stellungen: wie ausgeliefert, der
  Anzeige folgen, oder die Abnutzungsanzeige optisch einfrieren. Dazu ein
  Befehl, der alle geladenen Kleidungsstücke sofort nachzieht.
- **Abreißen in der eigenen Squad-Base ab wählbarem Rang.** Seit einem
  SCUM-Update dürfen nur noch Underboss und Boss Bauteile wegnehmen. Mit der
  Mod geht es wieder ab dem Rang, den der Betreiber wählt. Fremde bleiben
  ausgesperrt, daran ändert die Einstellung nichts.
- **Nachts andere Regeln.** Spielwerte wie Tempo, Leben oder Schaden der
  Zombies ab Sonnenuntergang anders setzen. Die Mod fährt sie in kleinen
  Schritten hoch und bei Sonnenaufgang genauso zurück auf den Tagwert. Den
  Tagwert muss man nicht eintragen, den holt sie sich selbst. Wie viele
  Schritte, wie weit auseinander und ab wann es losgeht, ist einstellbar.
- **Eigene Sätze für die Gedanken des Spielers.** Der kurze Text links unten
  im HUD (Hunger, nasse Füße, Blutung ...) kommt vom Server und lässt sich
  ersetzen: je Gedanke beliebig viele eigene Sätze, die Mod wechselt zufällig.
  Änderungen ohne Neustart.
- **Und es bleibt so, wie es gesetzt wurde.** Die Mod sieht regelmäßig nach,
  ob die Nachtwerte noch stehen, und setzt sie nach, wenn nicht. Sonst kann es
  passieren, dass die Zombies bis zum nächsten Neustart stark bleiben, ohne dass
  es irgendwo auffällt. Ein Admin kann im Spielchat nachsehen, ob gerade Tag
  oder Nacht ist und was anliegt.
- **Ausgesperrte Spieler beim Serverstart befreien**, damit der Betroffene frei
  ist, bevor er sich das nächste Mal verbindet.
- **Updates ohne Serverhalt.** Neue Version bei laufendem Server ablegen, die
  Mod prüft die Prüfsummen, übernimmt die Dateien, ergänzt neue Einstellungen
  und archiviert, was sie ersetzt hat. Geladen wird beim nächsten Neustart.

## Werkzeuge

- **Konfigurator im Browser.** Eine einzelne HTML-Datei, läuft ohne Server und
  ohne Internet. Jede Einstellung ist dort erklärt, in sechs Bereichen sortiert,
  und am Ende kommt die fertige Konfiguration heraus.
- **Web-Panel** als Konsole im Browser: eine Python-Datei, keine Zusatzpakete.
  Verlauf, Vervollständigung, klickbare Ausgabe (eine Kisten-ID springt zum
  Teleport weiter, eine SteamID zum Steckbrief) und eine Referenz aller
  Befehle, die ihre Beschreibungen live aus dem Spiel holt.
- **Kommandozeilen-Client** zum Ausprobieren von Hand.
- **Selbsttest**, der alle Befehle gegen den eigenen Server durchprobiert. Er
  liest die Beispiele direkt aus der Anleitung, es gibt also keine zweite Liste,
  die veralten könnte.
- **Briefing für KI-Assistenten.** Eine einzelne Datei, mit der ein Assistent
  den Server sofort steuern kann, samt aller Fallen.

---

[Zurück zur Übersicht](README.md)
