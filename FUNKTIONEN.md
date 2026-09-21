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
- **Alle Zonen auf einmal**, mit einem Faktor statt einer Zahl: die
  Verhältnisse zwischen den Zonen bleiben dabei erhalten. Der Faktor rechnet
  immer auf den Stand vom Serverstart, zweimal die Hälfte ist also die Hälfte
  und nicht ein Viertel.
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

Das ist der größte Bereich der Mod und der, der am wenigsten nach einer
Funktion aussieht. SCUM hält seine Spielregeln in Klassen mit Zahlenfeldern:
wie schnell ein Gefangener läuft, wie lange eine Tür offen steht, wie weit eine
Granate wirkt, wie oft der Bunker bei Alarm nachlegt. Die `ServerSettings.ini`
gibt davon eine Handvoll heraus. **Die Mod gibt den Rest heraus - mit einer
Textzeile je Wert, ohne dass es dafür eine neue Version der Mod braucht.**

### Was das an Umfang bedeutet

Von 397 Klassen, die das Spiel im Programm führt, sind **126 im laufenden
Server erreichbar** und haben jeweils mindestens drei setzbare Zahlenfelder.
Viele haben erheblich mehr:

| Klasse | setzbare Zahlenfelder | wovon sie handelt |
|---|---|---|
| Gefangener | 444 | alles am Spielercharakter |
| Wachturm-Sentry | 222 | Sichtwinkel, Reaktion, Zielen |
| Wetter | 190 | Tageszeit, Tempo des Tages, Höhenlagen |
| Reh | 166 | Gangarten, Fluchtverhalten, Angriff |
| Kleidung | 105 | Nässewanderung, Schaden beim Tragen |
| Fahrzeug | 99 | gilt für rund 1.900 Fahrzeuge zugleich |

Dazu Boote, Fahrräder, Angelruten, Granaten, Sprengfallen, Kettensägen,
Dropship und Razor. Es ist kein fertiger Katalog mit zwanzig Schaltern, sondern
ein Zugang zu dem, was das Spiel ohnehin an Werten mitbringt.

### Wie ein Wert geschrieben wird

Eine Zeile besteht aus Klasse, Feld und Wert. Für den Wert gibt es mehr als nur
Zahlen:

| Schreibweise | bedeutet |
|---|---|
| `80` | absolut dieser Wert |
| `x1.1` | zehn Prozent mehr als ausgeliefert, ohne den Ausgangswert zu kennen |
| `4..8` | ein Wertepaar, Min und Max |
| Bool und Ganzzahl | ausdrücklich angesagt, damit nichts geraten wird |

Der **Faktor** ist der Alltagsfall: "Spieler laufen zehn Prozent schneller" ist
eine Zeile, ohne dass man vorher nachsieht, welche Zahl dort steht. Die
Schreibweise des Feldnamens ist dabei egal, Groß- und Kleinschreibung spielt
keine Rolle.

### Wen eine Zeile trifft

Das ist der Punkt, an dem aus einer Bastelei ein Werkzeug wird. Die linke Seite
darf verschieden weit greifen:

| linke Seite | trifft |
|---|---|
| eine Klasse | **alle** Objekte dieser Art auf dem Server |
| eine Blueprint-Klasse | nur diese eine Bauart, etwa ein bestimmtes Türmodell |
| ein einzelnes Objekt | **genau dieses eine**, sonst nichts |

Damit lässt sich eine allgemeine Regel aufstellen und daneben eine Ausnahme
formulieren: alle Türen einer Bauart schließen sich, dieses eine Tor nicht.

### Wann es greift

- **Beim Serverstart**, wenn die Zeile in der Konfiguration steht.
- **Mitten im Betrieb**, per Befehl, ohne Neustart und ohne dass ein Spieler
  etwas merkt.
- **Alles zurück auf Auslieferungszustand**, mit einem Befehl, ebenfalls ohne
  Neustart. Ein verdrehter Wert ist damit kein Grund, den Server neu zu
  starten.
- **Anzeigen, was gewünscht ist und was tatsächlich anliegt**, nebeneinander.
  Das ist der Unterschied zwischen "steht in der Datei" und "gilt gerade".

### Was die Mod dagegen tut, dass man sich schadet

Ein direkter Zugriff auf Spielwerte kann einen Server zerlegen. Deshalb sind
vier Sicherungen eingebaut:

- **Ein Feldname, den es nicht gibt, wird abgelehnt** und gemeldet. Es wird
  nichts geraten und nichts stillschweigend übergangen.
- **Gibt es zu dem Feld auch eine Option in der `ServerSettings.ini`, kommt
  eine Warnung.** Dann gewinnt nämlich die Option, und die Zeile wäre eine
  stille Enttäuschung.
- **Der gesetzte Wert wird gegen den Ist-Wert geprüft**, statt nur "geschrieben"
  zu melden.
- **Eine geprüfte Liste liegt bei**: 184 Werte aus dem laufenden Server, jeder
  mit seinem Auslieferungswert daneben. Wer sich daran hält, ist auf der
  sicheren Seite. Was dort nicht steht, ist nicht verboten, aber ungeprüft -
  und die Anleitung sagt deutlich, welche Feldsorte man in Ruhe lassen muss.

### Beispiele aus dem Alltag

- **Türen, die sich von selbst schließen.** SCUM hat das eingebaut und fast
  überall abgeschaltet. Mit zwei Zeilen je Türmodell geht es an, samt Zeit bis
  zum Zufallen. Eine fertige Vorlage für Wohnhäuser, Plattenbau, Schule,
  Krankenhaus, Polizei, Kirche und die drei Garagentore liegt bei: 20 Modelle,
  rund 4.600 Türen.
- **Fahrzeuge nach dem Neustart schneller in der Welt**, über drei Bremsen im
  Fahrzeugmanager, die hintereinanderhängen.
- **Bunker, der bei Alarm härter reagiert.**
- **Spielertempo**, als Faktor, ohne den Ausgangswert zu kennen.
- **Sprengwirkung von Granaten und Fallen.**

### Türmodelle herausfinden

Damit die Türregel nicht Raten bleibt, gehört ein Messwerkzeug dazu:

- **Alle Türklassen des Servers auflisten**, mit Stückzahl, aktuellem
  Selbstschluss und Typ, und Weltobjekte von den Basisbau-Türen der Spieler
  getrennt.
- **Nach einem Textteil suchen**, dann kommt der vollständige Pfad heraus, den
  die Konfiguration braucht.
- **Zustand merken, im Spiel Türen aufmachen, Unterschied abfragen.** So nennt
  die Mod genau die Türmodelle, die man angefasst hat - statt einer Liste von
  415 Klassen, aus der niemand die richtige heraussucht.

### Konsolenvariablen daneben

Neben den Klassenfeldern kennt die Engine ihre eigenen Konsolenvariablen. Auch
die lassen sich setzen, beim Serverstart oder mitten im Betrieb: Tempo, Leben
und Schaden der Zombies sind die, nach denen am häufigsten gefragt wird.

### Obergrenzen des Servers anheben

Manche Werte deckelt der Server beim Start stillschweigend, etwa die Zahl der
Rager. Der eingetragene Wert steht in der Datei, gilt aber nicht. Mit der Mod
bleibt er stehen.

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
  Befehle der Mod im Chat nutzen. Die lesenden (Uhrzeit, Quest-Reset) lassen
  sich für jeden Spieler öffnen.
- **Anzeigen, wer was darf**, und neu einlesen ohne Neustart.
- **Die Werkzeuge, die den Speicher des Servers roh anfassen, sind ab Werk
  gesperrt** und brauchen einen ausdrücklichen Schalter samt Neustart. Auf
  einem öffentlichen Server bleibt der aus.

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
  Zombies ab Sonnenuntergang anders setzen. Die Mod fährt sie schrittweise hoch
  und bei Sonnenaufgang genauso zurück auf den Tagwert. Den Tagwert muss man
  nicht eintragen, den holt sie sich selbst.
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
