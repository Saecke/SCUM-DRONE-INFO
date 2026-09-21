<p align="center">
  <img src="assets/logo.png" alt="D.R.O.N.E." width="360">
</p>

<h1 align="center">D.R.O.N.E.</h1>

<p align="center">
  <b>D</b>edicated <b>R</b>CON, <b>O</b>perations &amp; <b>N</b>ative <b>E</b>xecution<br>
  Ein Source-RCON-Server für SCUM-Dedicated-Server, als native UE4SS-Mod.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-0.6.0-brightgreen" alt="Version 0.6.0">
  <img src="https://img.shields.io/badge/Status-Testfassung-orange" alt="Status: Testfassung">
  <a href="LICENSE"><img src="https://img.shields.io/badge/Lizenz-free--to--use%20EULA-blue" alt="Lizenz"></a>
  <img src="https://img.shields.io/badge/Plattform-Windows%20x64-lightgrey" alt="Plattform: Windows x64">
</p>

> **English:** D.R.O.N.E. is a Source RCON server for SCUM dedicated servers,
> running as a native UE4SS mod inside the server process. It exposes all 233
> in-game admin commands over standard Source RCON, no online admin required,
> and it works on a completely empty server. Free to use, closed source.
> This repository is the public feature overview. The download itself is
> currently limited to testers, see [Woher bekommen](#woher-bekommen).
> The documentation is in German.

---

## Was das hier ist

Dieses Repo zeigt, **was die Mod kann**. Es ist die öffentliche Übersicht.

Die Mod selbst, die Installationsanleitung und die vollständige Bedienungs-
anleitung liegen in einem privaten Repo, das nur Tester sehen. Warum, steht
unter [Woher bekommen](#woher-bekommen).

Die vollständige Funktionsliste, nach Themen sortiert: **[FUNKTIONEN.md](FUNKTIONEN.md)**.

## Was es ist

Die Mod öffnet auf dem Server einen RCON-Port nach dem Source-RCON-Protokoll.
Jeder gängige RCON-Client und jeder Bot spricht es bereits. Bestehende Bots
laufen unverändert weiter, weil die Ausgabeformate an den etablierten
SCUM-RCON-Lösungen geeicht sind.

Sie läuft im Serverprozess selbst, nicht als Brücke daneben. Es muss kein Admin
online sein, und ein leerer Server ist kein Hindernis: Spawns, Events und
Teleports funktionieren auch nachts um vier, wenn niemand eingeloggt ist.

> **Das ist eine Testfassung.** Sie läuft auf mehreren Servern im Alltag,
> gehört aber nicht ungetestet auf einen Server mit echten Spielern.

## Was es kann

### Befehle über die Verbindung

- **Alle 233 Admin-Befehle des Spiels** über RCON, so wie ein Admin sie im
  Spielchat tippen würde. Die Befehlsliste holt sich die Mod bei jedem Start aus
  dem laufenden Spiel, sie veraltet nicht mit dem nächsten SCUM-Update.
- **Die echte Antwort des Spiels** statt nur "abgesetzt": wie viele Leichen
  entfernt wurden, warum ein Spawn nicht ging, was eine Abfrage ergab.
- **Befehle für einen bestimmten Spieler**, auch solche, die im Spiel nur auf
  den Aufrufer selbst wirken: unsterblich, Godmode, Attribute, Skills.
- **Spielerlisten aus der Server-Datenbank**, im Format der etablierten Bots:
  wer ist online, wer war je da, Flaggen, Squads, Fahrzeuge. Im Sekundentakt
  abfragbar, ohne dass der Server darunter leidet.
- **Chat und Ansagen** an alle oder an einen einzelnen Spieler, mit Farben und
  Einblendungen.
- **Geld und Fame** setzen oder ändern, einzeln oder für alle Online-Spieler.
- **Moderation**: kicken, bannen, entbannen, stummschalten, Chatverbot auf Zeit.
- **Spawnen** von Items, Fahrzeugen, Tieren, NPCs und Events an beliebigen
  Koordinaten. Die Höhe darf fehlen, die Mod misst den Boden selbst.
- **Aufräumen im Umkreis**: Zombies, Tiere, Leichen, einzelne Item-Typen.
- **Fahrzeuge finden und versetzen**, zum Spieler holen oder an einen Ort
  setzen, auch am anderen Kartenende. Dazu die Fahrzeuge eines einzelnen
  Spielers auflisten.
- **Kisten finden** über Name oder ID, samt Teleport eines Spielers dorthin.
- **Spieler befreien**, die feststecken oder wegen einer Quest nicht mehr
  einloggen können.
- **Serverregeln zur Laufzeit ändern**, ohne Neustart. Dazu Survival-Regler,
  Strahlenzonen, Zeit und Wetter.
- **Handelstabelle lesen**: was welcher Händler führt.
- **Ingame-Uhrzeit und Zeit bis zum Quest-Reset** abfragen.
- **Generatoren um eine Flagge** auflisten, mit Füllstand.
- **Bunker-Terminals**: wer zuletzt dort Daten geladen hat, mit Restsperre.

### Auch im Spielchat

- **Die Befehle der Mod** kann ein eingeloggter Admin im Chat tippen wie die
  Spielbefehle.
- **Für alle Spieler freigebbar**: die lesenden Befehle wie Uhrzeit und
  Quest-Reset, wenn der Betreiber das will.

### Was von allein läuft

Eingriffe ins Spiel sind ab Werk aus. Wer nichts einschaltet, merkt nichts.

- **Rechte je Admin.** SCUM kennt nur "Admin oder nicht". Mit der Mod bekommt
  jeder Admin genau die Befehle, die er haben soll, und Gruppen wie
  "Moderator" lassen sich einmal definieren und wiederverwenden.
- **Dev-Rechte ohne Datenbankeingriff.** Wer erweiterte Befehle nutzen darf,
  steht in einer einfachen Textdatei.
- **Generatoren, die nie leer werden.** Für Handelsposten, Com-Zone und
  Eventgelände.
- **Nachts andere Regeln**, zum Beispiel schnellere oder stärkere Zombies, mit
  sanftem Übergang bei Sonnenuntergang und -aufgang.
- **Obergrenzen des Spiels anheben**, etwa für mehr Rager, als SCUM erlaubt.
- **Fahrzeuge nach dem Neustart schneller in der Welt**: bei 700 Fahrzeugen
  rund 7 statt 23 Minuten.
- **Türen, die sich von selbst schließen**, je Türsorte wählbar.
- **Genähte Kleidung sieht wieder neu aus.** Normaler Verschleiß bleibt sichtbar.
- **Abreißen in der eigenen Squad-Base ab wählbarem Rang**, statt nur für
  Underboss und Boss.
- **Kisten-Sortierer**: räumt eine offene Kiste in die umstehenden Kisten,
  nach deren Namen. **Experimentell.**
- **Updates ohne Serverhalt.** Neue Version bei laufendem Server ablegen, die
  Mod prüft und übernimmt sie beim nächsten Neustart.

### Protokolle und Werkzeuge

- **Sessionlog** pro Serverlauf: jeder Befehl mit Zeitstempel und Antwort, auf
  Wunsch auch die Downloads an den Bunker-Terminals.
- **Inventar- und Leichen-Log**: wer welchen Behälter öffnet, mit Besitzer und
  Ort. **Experimentell.**
- **Konfigurator im Browser**, ohne Server und ohne Internet. Jede Einstellung
  ist dort erklärt.
- **Selbsttest**, der alle Befehle gegen den eigenen Server durchprobiert.
- **Kommandozeilen-Client** zum Ausprobieren von Hand.
- **Briefing für KI-Assistenten**: eine Datei, mit der ein Assistent den Server
  sofort steuern kann.

Alles im Detail: **[FUNKTIONEN.md](FUNKTIONEN.md)**.

## Woher bekommen

Die Mod ist derzeit eine **Testfassung**. Der Download und die vollständige
Dokumentation liegen in einem privaten Repo, zu dem Tester eingeladen werden.

Wer die Mod auf seinem Server testen möchte, meldet sich beim Betreiber dieses
Repos. Ein öffentlicher Download folgt, sobald die Testphase abgeschlossen ist.

## Lizenz

Closed Source, kostenlos nutzbar. Erlaubt ist der Betrieb auf beliebig vielen
Servern, auch auf solchen, die sich über Spenden oder VIP-Ränge finanzieren.
Nicht erlaubt ist, die Software selbst zu verkaufen, zu verändern oder außerhalb
der offiziellen Releases weiterzuverbreiten. Ohne Gewährleistung.

Vollständiger Text: [LICENSE](LICENSE).

## Kein Zusammenhang mit den Rechteinhabern von SCUM

D.R.O.N.E. ist eine unabhängige, inoffizielle Modifikation. Es besteht keine
Verbindung zu den Entwicklern, dem Herausgeber oder sonstigen Rechteinhabern
von SCUM, und keine Befürwortung durch sie. Alle Marken gehören ihren
jeweiligen Inhabern.
