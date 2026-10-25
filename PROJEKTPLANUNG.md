# BattleDome – Projektplanung und Übergabeprotokoll

> **Zweck dieser Datei:** Diese Datei ist die zentrale, fortlaufend gepflegte Quelle für Projektziele, bestätigte Entscheidungen, offene Fragen, den aktuellen Arbeitsstand und die Übergabe an ein neues ChatGPT-Gespräch. Sie soll verhindern, dass bei einem Gesprächswechsel wichtige Informationen verloren gehen.
>
> **Verbindliche Sprachregel:** Die Projektkommunikation und alle selbst verfassten Projektdateien, Dokumentationen, Kommentare, Bot-Meldungen, Befehlsbezeichnungen soweit sinnvoll sowie Git-Commit-Nachrichten werden auf **Deutsch** geführt. Offizielle technische Eigennamen wie mIRC, Git und GitHub bleiben unverändert.

## 1. Projektüberblick

- **Projektname:** BattleDome
- **Repository:** https://github.com/Zenturion58/BattleDome
- **GitHub-Konto / Eigentümer:** Zenturion58
- **Standardbranch:** `main`
- **Technische Grundlage:** Ein mIRC-Skript in der Skriptsprache von mIRC.
- **Betriebsmodell:** BattleDome soll als eigenständiger Bot im eigenen IRC-Netzwerk dauerhaft online sein.
- **Erster Funktionsbereich:** Ein rundenbasiertes PvE-Kampfsystem, in dem mehrere Spieler gemeinsam gegen ein vom Skript erzeugtes und gesteuertes Monster kämpfen.
- **Arbeitsweise:** Schrittweise und gemeinsam entwickeln. Entscheidungen des Nutzers werden festgehalten. Keine unnötigen Vorgriffe auf spätere Funktionen; zuerst den aktuellen Schritt sauber abschließen.

## 2. Projektziele und Leitlinien

1. **Mehrspieler von Anfang an:** Das erste Kampfsystem soll mehrere Spieler in einem gemeinsamen Kampf unterstützen.
2. **PvE statt PvP:** Die Spieler kämpfen gemeinsam gegen Monster und nicht gegeneinander.
3. **Modulare Struktur:** Der Code soll von Beginn an sinnvoll auf mehrere Dateien und Zuständigkeitsbereiche verteilt werden. Kein gesamtes Projekt in einer einzigen Skriptdatei.
4. **Erweiterbarkeit:** Spätere Erweiterungen sollen sich in die Struktur einfügen lassen, ohne das Grundgerüst unnötig umzubauen. Noch nicht besprochene Erweiterungen werden nicht vorzeitig festgelegt.
5. **Dokumentation und Übergabefähigkeit:** Wesentliche Ziele, Entscheidungen, offene Fragen und Arbeitsschritte werden hier dokumentiert. Diese Datei ist die zentrale Orientierung bei einem Wechsel in eine neue Unterhaltung.
6. **Deutsch als Projektsprache:** Selbst verfasste Dokumentation und Projekttexte sind deutschsprachig.
7. **Kontrollierte Änderungen:** Vor Änderungen an bestehenden Dateien wird deren aktueller Inhalt geprüft. Änderungen sollen nachvollziehbar und mit deutschen Commit-Nachrichten gespeichert werden.

## 3. Bisher bestätigter Ablauf des ersten Kampfsystems

Der Nutzer hat bisher folgenden groben Ablauf beschrieben:

1. Das System kündigt an, dass ein Kampf bevorsteht.
2. Es beginnt eine zeitlich begrenzte Anmeldephase.
3. Interessierte Spieler können sich innerhalb dieses Zeitfensters für den Kampf anmelden.
4. Bei der Ankündigung wird noch nicht verraten, welches Monster erscheinen wird.
5. Sobald die Anmeldezeit abgelaufen ist, wird die Anmeldung geschlossen.
6. Erst danach erzeugt das Skript im Hintergrund das Monster und bestimmt die Zugreihenfolge.
7. Die angemeldeten Spieler kämpfen gemeinsam gegen dieses Monster.

**Wichtig:** Das ist der bisher festgehaltene Grundablauf. Details wie genaue Zeitdauer, Befehle, Regeln für die Zugreihenfolge, Kampfwerte, Monsterdaten und Sieg-/Niederlagebedingungen sind noch nicht abschließend festgelegt. Sie dürfen nicht als bereits getroffene Entscheidungen dargestellt werden.

## 4. Verbindliche Entscheidungen des Nutzers

Diese Liste enthält nur Entscheidungen, die der Nutzer bereits ausdrücklich getroffen oder bestätigt hat.

- [x] Das Projekt heißt **BattleDome**.
- [x] Es wird als mIRC-Skript umgesetzt.
- [x] BattleDome soll als eigenständiger Bot im eigenen IRC-Netzwerk dauerhaft online sein.
- [x] Das erste Spielsystem ist ein rundenbasiertes PvE-Kampfsystem.
- [x] Mehrere Spieler sollen von Anfang an gemeinsam gegen ein Monster kämpfen können.
- [x] Das Skript erzeugt und steuert die Monster.
- [x] Der Kampf wird angekündigt und hat eine begrenzte Anmeldephase.
- [x] Bei der Ankündigung wird die Identität des Monsters noch nicht bekannt gegeben.
- [x] Monstererzeugung und Bestimmung der Zugreihenfolge erfolgen erst nach Ende der Anmeldung.
- [x] Das Projekt soll modular aufgebaut sein und nicht in einer einzigen Datei liegen.
- [x] Die Projekttexte und Dokumentation sollen vollständig auf Deutsch geführt werden, soweit es sich um selbst verfasste Texte handelt.
- [x] Das GitHub-Repository lautet https://github.com/Zenturion58/BattleDome.
- [x] Eine zentrale Planungsdatei soll Entscheidungen und Arbeitsstand so festhalten, dass ein neues Gespräch nahtlos weiterarbeiten kann.
- [x] **Jede Entscheidung wird dokumentiert.** Dazu gehören die Entscheidung selbst, wer sie getroffen hat (insbesondere der Nutzer), ihr Status und – wenn relevant – die Gründe sowie Auswirkungen. Vorschläge gelten erst nach Bestätigung als beschlossene Entscheidungen.
- [x] **Fehlende unverzichtbare Kerndatei verhindert den Start:** Fehlt eine für den Betrieb zwingend benötigte Datei wie `System.als`, muss die Initialisierung abgebrochen und der Nutzer verständlich auf den Fehler hingewiesen werden. Die Meldung soll dazu auffordern, die Originaldatei erneut aus dem offiziellen BattleDome-GitHub-Repository zu beziehen. Entscheider: Nutzer. Datum: 2026-10-25.
- [x] **Startablauf über `System.als`:** `Control.mrc` soll nur die Existenz von `System.als` prüfen und diese Alias-Datei laden. Danach soll ein Helfer aus `System.als` mit dem festgelegten Namen `system_default_check` aufgerufen werden, der die weiteren Systemprüfungen übernimmt. Die genaue technische Auslösung nach dem Laden ist noch offen. Entscheider: Nutzer. Datum: 2026-10-25.

## 5. Technischer und organisatorischer Stand

### GitHub

- Repository: https://github.com/Zenturion58/BattleDome
- Standardbranch: `main`
- Bei der letzten Zugriffsprüfung wurde das Repository über die GitHub-Anbindung gefunden.
- Die gemeldeten Berechtigungen umfassten Lesen (`pull: true`) und Schreiben (`push: true`).
- Vor dieser Planungsdatei war das Repository leer.
- Diese Planungsdatei ist der erste dokumentierte Projektinhalt, sobald der zugehörige Commit erfolgreich erstellt wurde.

### Entwicklungsstand

- [x] Projektname festgelegt.
- [x] Repository angelegt.
- [x] GitHub-Lese- und Schreibberechtigungen laut Verbindung geprüft.
- [ ] Projektgrundstruktur festlegen und dokumentieren.
- [ ] Zuständigkeiten und Dateiaufteilung der mIRC-Skripte festlegen.
- [ ] Erstes lauffähiges Grundgerüst erstellen.
- [ ] Kampfsystem schrittweise spezifizieren und umsetzen.

Die noch offenen Punkte sind Arbeitsaufgaben, keine bereits getroffenen Entscheidungen.

## 6. Noch offene Entscheidungen

### Architekturentwurf: vorgesehene Dateiaufteilung (noch nicht verbindlich)

**Status:** Entwurf des Nutzers vom 2026-10-25. Die Struktur dient vorerst als Orientierung für die Planung. Dateinamen und Zuständigkeiten können später noch geändert werden. Es ist noch keine endgültige Architekturentscheidung und legt keine konkreten Funktionen über die unten genannten Beispiele hinaus fest.

#### Vorgesehene Alias-Dateien (`.als`)

- `System.als`: vorgesehene allgemeine Kern-Helper, unter anderem für die Initialisierung des Skripts, Pfadfestlegung und übergreifende Systemabläufe.
- `battle.als`: vorgesehene kampfbezogene Helper, unter anderem für Zugreihenfolge, Anordnung der Spielerliste und Monstererzeugung.
- `BattleFormular.als`: vorgesehener Bereich für die Schadensformel und zugehörige Berechnungen.

Die Helper sollen in den Alias-Dateien liegen und nicht in den eigentlichen Programmdateien (`.mrc`). Die konkrete Aufrufstruktur und die genaue Abgrenzung der Zuständigkeiten sind noch offen.

#### Vorgesehene Programmdateien (`.mrc`)

- `Control.mrc`
- `character.mrc`
- `BattleAI.mrc`
- `Battle.mrc`

Die endgültigen Zuständigkeiten dieser Dateien sind noch nicht festgelegt. Die aufgeführten Namen sind vorläufig und können sich im weiteren Planungsverlauf ändern.

#### Ergänzung zum Entwurf: Start und Initialisierung über `Control.mrc`

Nach der weiteren Erläuterung des Nutzers ist für den Entwurf außerdem festzuhalten:

- `Control.mrc` soll den Systemstart und die Initialisierung von BattleDome steuern.
- Zu den vorgesehenen Aufgaben gehören unter anderem die Prüfung der Verzeichnisstruktur, der Charakterdateien und der Datenbanken sowie die Entscheidung, welche Hilfsfunktionen für den Start benötigt werden.
- `Control.mrc` soll dafür Helper aus `System.als` aufrufen.
- Die benötigten Alias-Dateien müssen geladen sein, bevor `Control.mrc` ihre darin definierten Helper aufruft. Andernfalls kann die Initialisierung fehlschlagen oder Probleme verursachen.
- Der vorgesehene Lade- und Aufrufablauf muss daher so geplant werden, dass benötigte Alias-Dateien zuerst verfügbar sind und erst danach die Initialisierungsschritte ausgeführt werden, die ihre Helper verwenden.

**Noch offen:** Der genaue Ladeablauf, die Reihenfolge der einzelnen Prüfungen, die Behandlung von Fehlern und die konkrete Umsetzung sind noch nicht festgelegt. Diese Punkte werden später einzeln besprochen. Auch diese Beschreibung bleibt Teil des unverbindlichen Architekturentwurfs.

**Ergänzung zum Entwurf: Prüfung und Laden benötigter Alias-Dateien**

Der Nutzer hat als möglichen Ansatz vorgeschlagen, dass `Control.mrc` einen kleinen, in der Control-Datei selbst enthaltenen Helfer besitzt. Dieser könnte beim Start prüfen, ob benötigte Alias-Dateien wie `System.als`, `battle.als` und `BattleFormular.als` am vorgesehenen Speicherort existieren, und vorhandene Dateien anschließend laden. Weitere Alias-Dateien könnten später ergänzt werden.

Als technischer Ansatz ist in der mIRC-Hilfe der Befehl `/load -a <datei>` zum Laden einer Alias-Datei dokumentiert. Für Remote-Skriptdateien wie `.mrc` ist dagegen `/load -rs <datei>` vorgesehen. Die mIRC-Identifikatoren `$exists(...)` und `$alias(...)` können grundsätzlich bei der Prüfung helfen: Ersterer prüft, ob eine Datei oder ein Verzeichnis existiert; Letzterer kann Auskunft darüber geben, ob eine Alias-Datei geladen ist.

Diese Informationen sind technische Orientierung und noch keine Festlegung der konkreten Implementierung. Insbesondere sind der Name des Prüfhelfers (beispielsweise `Check Scripts`, `Check System Helper` oder ein anderer Name), die genaue Pfadermittlung, die Lade-Reihenfolge und die Fehlerbehandlung noch offen. Es ist auch noch nicht entschieden, ob die vorgeschlagene Aufteilung genau so umgesetzt wird.

**Ergänzung nach Nutzerentscheidung: Übergabe von `Control.mrc` an `System.als`**

Der Nutzer hat den vorgesehenen Startablauf weiter präzisiert:

- `Control.mrc` prüft, ob `System.als` vorhanden ist, und lädt diese Datei, sofern sie existiert.
- `Control.mrc` soll nicht selbst alle weiteren Skript- und Alias-Dateien prüfen oder laden.
- Nach dem Laden von `System.als` soll deren eigener Helper `system_default_check` aufgerufen werden.
- `system_default_check` soll die weiteren allgemeinen Systemprüfungen übernehmen. Die genauen einzelnen Prüfungen und die genaue Zuständigkeit des Helpers werden später festgelegt.
- Die technische Umsetzung des Übergangs nach dem Laden ist noch offen. Der Nutzer hat als mögliche Ansätze einen kurzen Timer oder eine If-Schleife erwähnt; es ist noch nicht entschieden, welcher Mechanismus verwendet wird.
- Der Entwurf sieht vor, dass `System.als` die nachgelagerten Prüfungen und das Laden weiterer benötigter Skriptdateien übernimmt.

**Ergänzung nach Nutzerentscheidung: Verhalten bei fehlender Kernkomponente**

- `System.als` ist als unverzichtbarer Bestandteil der Kernfunktion vorgesehen. Es soll die allgemeinen Systemprüfungen übernehmen, darunter Prüfungen der Ordnerstruktur, der Monsterpfade, benötigter Dateien und möglicher fehlerhafter Datenbankeinträge.
- Fehlt `System.als`, darf die Initialisierung nicht fortgesetzt werden. Der Start wird abgebrochen und der Nutzer erhält eine verständliche Fehlermeldung.
- Die Fehlermeldung soll darauf hinweisen, die Originaldatei erneut aus dem offiziellen BattleDome-GitHub-Repository zu beziehen. Ein fehlerhafter Download ist ein vom Nutzer genanntes mögliches Beispiel für eine fehlende Datei.
- Welche weiteren Dateien als unverzichtbar gelten und wie Fehler beim Laden vorhandener Dateien behandelt werden, bleibt noch offen.
- Die genaue technische Umsetzung der Meldung und des Abbruchs ist noch nicht festgelegt.



Die folgenden Themen müssen bei Bedarf gemeinsam besprochen werden. Sie sind bewusst **nicht** vorweggenommen:

- Wie der Architekturentwurf endgültig ausgestaltet wird, einschließlich der genauen Dateiaufteilung und Zuständigkeiten.
- Ob die vorläufigen Dateinamen und Namenskonventionen beibehalten oder geändert werden.
- Welche mIRC-Version und welche konkreten Laufzeitbedingungen vorausgesetzt werden, falls dies relevant wird.
- Welche IRC-Befehle Spieler für Anmeldung und Kampf verwenden.
- Wie lang die Anmeldephase dauert und wie sie konfiguriert wird.
- Wie die Zugreihenfolge genau bestimmt wird.
- Wie Spieleraktionen, Monsteraktionen, Lebenspunkte, Schaden, Sieg und Niederlage geregelt werden.
- Wie Spielstände oder andere dauerhafte Daten gespeichert werden, falls erforderlich.

Neue offene Fragen sollen erst dann ergänzt und bearbeitet werden, wenn sie für den aktuellen Umsetzungsschritt relevant sind.

## 7. Arbeitsregeln für künftige Gespräche

1. **Diese Datei zuerst lesen:** Zu Beginn einer neuen Unterhaltung soll ChatGPT die aktuelle Version von `PROJEKTPLANUNG.md` im GitHub-Repository abrufen und als Ausgangspunkt verwenden.
2. **Den aktuellen Stand prüfen:** Zusätzlich ist bei Bedarf der tatsächliche Inhalt des Repositorys zu prüfen. Die Planung allein beweist nicht, dass eine Aufgabe bereits implementiert wurde.
3. **Jede Entscheidung dokumentieren:** Jede Projektentscheidung wird zeitnah in dieser Datei festgehalten – ausdrücklich auch kleine Entscheidungen, verworfene Ansätze, Änderungen an früheren Entscheidungen und die Person, die entschieden hat. Wenn bekannt, werden Datum, Begründung und Auswirkungen ergänzt. Nutzerentscheidungen werden als solche gekennzeichnet.
4. **Fakten und Vorschläge trennen:** Bestätigte Nutzerentscheidungen, Vorschläge, offene Fragen und erledigte Aufgaben müssen klar unterscheidbar bleiben. Ein Vorschlag ist keine Entscheidung, solange der Nutzer ihn nicht bestätigt hat.
5. **Nichts erfinden:** Unbekannte Werte oder Entscheidungen werden als offen gekennzeichnet, nicht stillschweigend festgelegt.
6. **Schrittweise vorgehen:** Immer den aktuellen Arbeitsschritt behandeln. Keine zusätzlichen Funktionen oder Planungsbereiche ausarbeiten, wenn der Nutzer sie noch nicht angehen möchte.
7. **Vor Änderungen prüfen:** Bestehende Dateien vor dem Bearbeiten lesen. Keine Inhalte überschreiben, ohne den aktuellen Stand zu berücksichtigen.
8. **Nach relevanten Änderungen dokumentieren:** Entscheidungen, Statusänderungen, neue offene Punkte und wichtige technische Erkenntnisse in dieser Datei aktualisieren.
9. **Commit-Nachrichten auf Deutsch:** Jede Projektänderung erhält eine kurze, aussagekräftige deutsche Commit-Nachricht.
10. **Übergabe knapp vorbereiten:** Am Ende einer Arbeitssitzung den Status dieser Datei aktualisieren und dem Nutzer mitteilen, welcher konkrete nächste Schritt ansteht.

## 8. Übergabe an ein neues ChatGPT-Gespräch

Wenn ein neues Gespräch begonnen wird, kann der Nutzer diese Anweisung verwenden:

> Wir arbeiten am Projekt BattleDome. Bitte lies zuerst die aktuelle Datei `PROJEKTPLANUNG.md` aus https://github.com/Zenturion58/BattleDome und prüfe den tatsächlichen Repository-Stand. Behandle die dort festgehaltenen Nutzerentscheidungen als verbindlich, unterscheide sie von Vorschlägen und offenen Fragen und fahre nur mit dem nächsten noch offenen Arbeitsschritt fort. Das gesamte Projekt soll auf Deutsch dokumentiert werden. Bitte nichts als erledigt annehmen, was nicht anhand des Repositorys oder der dokumentierten Arbeit bestätigt ist.

Falls die GitHub-Anbindung im neuen Gespräch nicht verfügbar ist, soll ChatGPT den Nutzer bitten, den Inhalt dieser Datei bereitzustellen, statt frühere Entscheidungen zu erraten.

## 9. Änderungsprotokoll

### 2026-10-25 – Startablauf über `System.als` präzisiert

- Die Nutzerentscheidung dokumentiert, dass `Control.mrc` nur `System.als` auf Existenz prüft und lädt, statt alle weiteren Skriptdateien selbst zu laden.
- Den von Nutzer festgelegten Namen `system_default_check` für den nach dem Laden aufzurufenden Helper festgehalten.
- Die Zuständigkeit von `System.als` für weitere Systemprüfungen und das Laden weiterer benötigter Skriptdateien ergänzt.
- Timer oder If-Schleife nur als vom Nutzer genannte mögliche Ansätze vermerkt; die konkrete technische Umsetzung bleibt offen.

### 2026-10-25 – Verhalten bei fehlender Kernkomponente festgelegt

- Die ausdrückliche Nutzerentscheidung dokumentiert, dass bei Fehlen einer unverzichtbaren Kernkomponente wie `System.als` die Initialisierung abgebrochen wird.
- Festgehalten, dass eine verständliche Fehlermeldung den Nutzer auffordern soll, die Originaldatei erneut aus dem offiziellen BattleDome-GitHub-Repository zu beziehen.
- Die vorgesehene Rolle von `System.als` als zentrale Datei für allgemeine Prüfungen präzisiert: Ordnerstruktur, Monsterpfade, erforderliche Dateien und mögliche fehlerhafte Datenbankeinträge.
- Offen gelassen, welche weiteren Dateien zwingend sind und wie die technische Fehlerbehandlung umgesetzt wird.

### 2026-10-25 – Ergänzung zum Entwurf: Prüfung und Laden von Alias-Dateien

- Den Vorschlag des Nutzers dokumentiert, in `Control.mrc` einen dort selbst enthaltenen Helfer zur Prüfung benötigter Alias-Dateien vorzusehen.
- Als technische Orientierung die mIRC-Befehle `/load -a` für Alias-Dateien und `/load -rs` für Remote-Skriptdateien sowie die Identifikatoren `$exists(...)` und `$alias(...)` festgehalten.
- Namen des Prüfhelfers, Pfade, Lade-Reihenfolge und Fehlerbehandlung ausdrücklich als offen markiert.
- Status: unverbindlicher Vorschlag und technische Orientierung, keine bestätigte Architekturentscheidung.

### 2026-10-25 – Ergänzung zum Architekturentwurf: Initialisierung

- Auf Grundlage der Erläuterung des Nutzers ergänzt, dass `Control.mrc` den Systemstart und die Initialisierung steuern soll.
- Als vorgesehene Aufgaben der Control-Datei festgehalten: benötigte Helper bestimmen, Verzeichnisstruktur prüfen sowie Charakterdateien und Datenbanken prüfen.
- Die Abhängigkeit dokumentiert, dass Alias-Dateien geladen sein müssen, bevor in ihnen definierte Helper während der Initialisierung aufgerufen werden.
- Ladeablauf, Prüfungsreihenfolge und Fehlerbehandlung ausdrücklich als noch offen markiert.
- Status: Ergänzung zum unverbindlichen Architekturentwurf, keine endgültige Festlegung der konkreten Umsetzung.

### 2026-10-25 – Vorläufiger Architekturentwurf

- Auf Grundlage des Nutzervorschlags einen ausdrücklich unverbindlichen Entwurf der Dateistruktur ergänzt.
- Als vorgesehene Alias-Dateien `System.als`, `battle.als` und `BattleFormular.als` mit vorläufigen Zuständigkeitsbeispielen festgehalten.
- Als vorgesehene Programmdateien `Control.mrc`, `character.mrc`, `BattleAI.mrc` und `Battle.mrc` festgehalten.
- Festgehalten, dass Dateinamen, Zuständigkeiten und konkrete Funktionen noch gemeinsam besprochen und später geändert werden können.
- Status: Entwurf des Nutzers, keine endgültige Architekturentscheidung.

### 2026-10-25 – Verbindliche Dokumentation jeder Entscheidung

- Auf ausdrücklichen Wunsch des Nutzers festgehalten: Jede Entscheidung muss dokumentiert werden.
- Ergänzt, dass Entscheidungen mit entscheidender Person, Status und – soweit bekannt – Datum, Begründung und Auswirkungen festgehalten werden.
- Klargestellt, dass Vorschläge erst nach Bestätigung als beschlossene Entscheidungen gelten.

### 2026-10-25 – Erste Projektplanungsdatei

- Zentrale Planungs- und Übergabedokumentation angelegt.
- Bekannte Projektziele und bestätigte Entscheidungen zusammengefasst.
- Den bisher beschriebenen Ablauf des ersten Kampfsystems festgehalten.
- Offene Entscheidungen ausdrücklich als offen markiert.
- Regeln für künftige Gespräche und eine Übergabeanweisung ergänzt.
