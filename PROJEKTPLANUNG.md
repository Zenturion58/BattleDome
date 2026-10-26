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
- [x] **Startablauf über `System.als`:** `Control.mrc` soll nur die Existenz von `System.als` prüfen und diese Alias-Datei laden. Danach soll ein Helfer aus `System.als` mit dem festgelegten Namen `system_defaults_check` aufgerufen werden, der die weiteren Systemprüfungen übernimmt. Die genaue technische Auslösung nach dem Laden ist noch offen. Entscheider: Nutzer. Datum: 2026-10-25.
- [x] **Zeitpunkt der Systemprüfung:** `system_defaults_check` soll beim eigentlichen Start von BattleDome ausgeführt werden, nicht bei jedem `ON CONNECT`-Ereignis. Der Nutzer hat die frühere Skizze mit `ON CONNECT` ausdrücklich korrigiert. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Umgang mit gefundenen Systemproblemen:** Wenn `System.als` bei Prüfungen Probleme in Verzeichnisstruktur, Datenbanken, Einstellungen oder anderen benötigten Bestandteilen findet, soll der Nutzer darauf hingewiesen werden. Der Start soll deswegen nicht automatisch verhindert werden; fehlende Bestandteile können allerdings später weitere Fehler verursachen. Der gesonderte Fall einer fehlenden unverzichtbaren Datei `System.als` bleibt davon unberührt und führt zum Startabbruch. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Umfang der ersten Version (Grundgerüst):** Die erste Version konzentriert sich auf das technisch funktionsfähige rundenbasierte PvE-Kampfsystem: Spieler können einem Kampf beitreten, Monster werden zufällig erzeugt und die teilnehmenden Spieler kämpfen gemeinsam gegen das Monster. Waffen, Ausrüstung, Skills, Fähigkeiten, Techniken, Gegenstände, Loot, Events, Quests, Dungeons und weitere Erweiterungen gehören ausdrücklich nicht zur ersten Version; sie können später schrittweise ergänzt werden. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Textausgaben von Programmcode trennen:** Allgemeine Bot- und Systemmeldungen sollen nicht direkt als feste Texte im Quellcode stehen, sondern aus einer vorgesehenen `Translation.dat` gelesen werden. Dazu zählen beispielsweise Kampfmeldungen, Fehlermeldungen, Registrierungs- und spätere Eventankündigungen. Inhaltsspezifische Texte wie Monsterbeschreibungen und -angriffe sowie Waffen-, Skill- oder Techniktexte sollen in den jeweils zuständigen Fachdatenbanken bzw. Dateien liegen. `$readini(...)` ist als möglicher Lesezugriff genannt; das genaue Dateiformat und Schema bleiben offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Spielerregistrierung und Kampfbeitritt trennen:** Die Registrierung eines Spielers ist ein eigener Vorgang und muss erfolgt sein, bevor der Spieler den Befehl zum Beitritt in einen Kampf verwenden darf. Der Kampfbeitrittsbefehl registriert keinen Spieler automatisch; unregistrierte Spieler dürfen ihn nicht nutzen. Der konkrete Registrierungsablauf und der Name des Kampfbeitrittsbefehls sind noch offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Grundablauf der Spielerregistrierung:** Der Spieler startet die Registrierung mit dem Befehl `registrieren`. BattleDome prüft, ob bereits ein Account zum Nicknamen existiert. Falls nicht, wird eine vorbereitete Spielervorlage in das vorgesehene Spielerverzeichnis kopiert und nach dem Spielernamen benannt. Vorhandene Standardwerte der Vorlage bleiben erhalten; vorgesehene individuelle Felder wie Spielername und Registrierungsdatum werden angepasst. Der Bot erzeugt ein zufälliges Passwort, speichert in der Spielerdatei nur einen Passwort-Hash und sendet das Klartextpasswort per privater IRC-Nachricht an den Spieler. Nach erfolgreicher Erstellung erhält der Spieler eine Registrierungsbestätigung. Die Vorlage soll unter anderem Standardwerte für Lebenspunkte und eine Charakterbeschreibung enthalten. Die genaue Dateistruktur und der konkrete Passwort-Hashing-Algorithmus sind noch offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Bereits vergebener Nickname bei der Registrierung:** Wenn beim Befehl `registrieren` bereits ein Account zum verwendeten Nicknamen existiert, muss die Registrierung sofort abgebrochen werden. Die vorhandene Registrierung und Spielerdatei dürfen keinesfalls überschrieben oder verändert werden. Der Bot informiert den Nutzer über eine Meldung aus `Translation.dat`, dass unter diesem Nicknamen bereits ein Account existiert, und fordert ihn auf, mit `/nick Neuernick` einen anderen Nicknamen zu wählen und die Registrierung erneut zu versuchen. Die Prüfung muss vor dem Kopieren der Spielervorlage oder anderen Änderungen an Spielerdateien stattfinden. Begründung: Schutz vor Überschreiben und Verlust fremder Spielerdaten. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Accountbindung und Entzug von Bot-Zugriffsrechten bei Nicknamenwechsel:** Ein Spieleraccount bleibt an den Nicknamen gebunden, unter dem er registriert wurde; ein Nicknamenwechsel benennt den Account nicht automatisch um und überträgt ihn nicht auf den neuen Nicknamen. Bei der Registrierung werden neben den Spielerdaten auch Bot-Zugriffsrechte über `/auser level nickname` eingerichtet. Wenn ein Nutzer seinen Nicknamen ändert, soll das `ON NICK`-Ereignis die zuvor eingerichteten Bot-Zugriffsrechte für den alten Nicknamen wieder entfernen (Gegenmaßnahme zu `/auser`; der konkrete mIRC-Befehl dafür ist noch festzulegen). Kehrt der Nutzer später zum ursprünglichen Nicknamen zurück, darf ein zuvor eingerichtetes Zugriffslevel nicht automatisch weiterwirken: Er muss sich erneut beim Bot anmelden, bevor er geschützte Bot-Funktionen nutzen kann. Begründung: Ein dauerhaft bestehen bleibendes Zugriffslevel könnte bei einem Nicknamenwechsel bzw. einer Rückkehr zu diesem Namen eine Sicherheitslücke verursachen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Anmeldebefehl `!ID passwort` ausschließlich privat verarbeiten:** Der Nutzer hat den bereits vorgesehenen Anmeldebefehl als `!ID passwort` festgelegt. Der Befehl darf ausschließlich als private Nachricht direkt an den Bot verarbeitet werden; eine Eingabe im IRC-Kanal darf keine Anmeldung und keine Vergabe von Zugriffsrechten auslösen. Es ist nicht erforderlich, technisch zu verhindern, dass ein Nutzer den Befehl versehentlich in einem Kanal veröffentlicht. Wer das Passwort selbst öffentlich postet, ist für diese Offenlegung verantwortlich; BattleDome muss dafür keine Sonderbehandlung implementieren. Bot-Zugriffsrechte dürfen erst nach erfolgreicher Passwortprüfung vergeben werden. Das Passwort darf nicht durch Bot-Antworten öffentlich ausgegeben oder unnötig protokolliert werden. Die konkrete Funktionsweise und der Code sind noch nicht festgelegt. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Keine Anmeldung zum Kampf:** Wenn sich während der Anmeldephase niemand anmeldet, wird der Kampf abgesagt und der Bot meldet, dass sich niemand angemeldet hat. Anschließend wartet das System eine noch festzulegende Zeit, bevor es eine neue Kampfankündigung startet. Dauer und konkrete Timer-Umsetzung bleiben offen. Entscheider: Nutzer. Datum: 2026-10-26.

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

### Trennung von Textausgaben und Programmcode

Allgemeine Bot- und Systemmeldungen sollen nicht als feste Nachrichtentexte im Quellcode eingebettet werden. Sie sollen aus einer zentral vorgesehenen `Translation.dat` gelesen werden. Beispiele sind Kampfankündigungen und Kampfmeldungen, Fehlermeldungen, Registrierungsnachrichten sowie spätere Eventankündigungen. Texte, die zu konkreten Spielinhalten gehören – etwa Monsterbeschreibungen und Monsterangriffe oder Waffen-, Skill- und Techniktexte – sollen in den jeweils zuständigen Fachdatenbanken bzw. Dateien liegen.

Der Nutzer nannte `$readini(Datei, Abschnitt, Schlüssel)` als möglichen Zugriff auf Einträge und stellte klar, dass für `readini` die Dateiendung (`.dat`, `.db`, `.txt` oder eine andere) nicht entscheidend ist. Maßgeblich ist, dass der Dateiinhalt die erwartete Struktur mit passenden Abschnitten und Schlüsseln besitzt. Das konkrete Schema, der Umgang mit fehlenden Texten und die Implementierung bleiben offen. Diese Vorgabe dient dazu, den Quellcode übersichtlich zu halten.

### Ablauf bei ausbleibenden Anmeldungen

Wenn während der Anmeldephase niemand dem Kampf beitritt, wird der Kampf abgesagt und der Bot meldet, dass sich niemand angemeldet hat. Danach soll das System eine noch festzulegende Zeit warten und erneut eine Kampfankündigung starten. Die konkrete Wartezeit, der Timer und der genaue Wiederholungsablauf sind noch offen.

### Verbindlicher Umfang der ersten Version

Die erste Version ist auf das technische Grundgerüst eines rundenbasierten PvE-Kampfsystems begrenzt. Sie soll Spielerbeitritt zu einem Kampf, zufällige Monstererzeugung und den grundlegenden gemeinsamen Kampfablauf ermöglichen. Die technische Basis muss dafür notwendige Startprüfungen, Einstellungen und Skriptstruktur enthalten.

Nicht Teil der ersten Version sind Waffen, Ausrüstung, Skills, Fähigkeiten, Techniken, Gegenstände, Loot, Events, Quests, Dungeons oder ähnliche Erweiterungssysteme. Diese Funktionen sind nicht verworfen, sondern ausdrücklich auf spätere Ausbaustufen verschoben. Sie sollen erst nach einem funktionsfähigen Grundgerüst schrittweise geplant und ergänzt werden.


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
- Nach dem Laden von `System.als` soll deren eigener Helper `system_defaults_check` aufgerufen werden.
- `system_defaults_check` soll die weiteren allgemeinen Systemprüfungen übernehmen. Die genauen einzelnen Prüfungen und die genaue Zuständigkeit des Helpers werden später festgelegt.
- Die technische Umsetzung des Übergangs nach dem Laden ist noch offen. Der Nutzer hat als mögliche Ansätze einen kurzen Timer oder eine If-Schleife erwähnt; es ist noch nicht entschieden, welcher Mechanismus verwendet wird.
- Der Entwurf sieht vor, dass `System.als` die nachgelagerten Prüfungen und das Laden weiterer benötigter Skriptdateien übernimmt.

**Ergänzung nach Nutzerklärung: Umfang und Zeitpunkt von `system_defaults_check`**

- Der Nutzer hat klargestellt, dass `system_defaults_check` für den eigentlichen Start von BattleDome vorgesehen ist und nicht bei jeder IRC-Verbindung (`ON CONNECT`) erneut ausgeführt werden soll.
- Als Aufgabenbild für diesen Helfer nannte der Nutzer die Prüfung von Einstellungen in einer vorgesehenen `System.dat` (beispielsweise maximale Rundenzahl, maximale Lebenspunkte und Dauer von Rundenankündigungen), das Ergänzen fehlender Standardeinstellungen sowie Prüfungen der Verzeichnisstruktur, benötigter Datenbanken (unter anderem Waffen- und Item-Datenbanken), Monsterdateien und des konfigurierten Monsterpfads.
- Bei gefundenen Problemen soll der Nutzer informiert werden, der Start soll aber nicht allein deshalb verhindert werden. Fehlende Daten oder Ressourcen können später dennoch zu Folgefehlern führen. Dies ist von der bereits bestätigten Regel zu unterscheiden, dass der Start bei fehlender unverzichtbarer `System.als` abgebrochen wird.
- Das vom Nutzer gezeigte mIRC-Codebeispiel ist ausdrücklich nur eine Skizze und kein endgültiger Entwurf. Namen, Syntax, Prüfreihenfolge, Standardwerte und technische Umsetzung bleiben offen.

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
- Wie die Spielervorlage und die individuellen Spielerdateien genau aufgebaut und abgelegt werden.
- Welcher geeignete Passwort-Hashing-Algorithmus und welche Parameter für die Speicherung der zufällig erzeugten Passwörter verwendet werden.
- Wie mit Nicknamenänderungen und späteren Wiederherstellungen von Zugangsdaten umgegangen werden soll, falls diese Themen für die erste Version relevant werden.
- Welchen Namen der Befehl zum Beitritt in einen Kampf erhält (beispielsweise `beitreten` oder `join`). Die Entscheidung ist offen.
- Welche weiteren IRC-Befehle Spieler verwenden, sobald Registrierung und Kampfbeitritt genauer geplant sind.
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

### 2026-10-26 – Umgang mit öffentlich eingegebenem Anmeldebefehl präzisiert

- Festgehalten, dass `!ID passwort` nur als private Nachricht an den Bot verarbeitet werden darf; eine Kanaleingabe darf keine Anmeldung auslösen.
- Auf ausdrücklichen Wunsch des Nutzers ergänzt, dass BattleDome nicht technisch verhindern muss, dass ein Nutzer den Befehl versehentlich im Kanal veröffentlicht. Die Verantwortung für die selbst verursachte Offenlegung liegt beim Nutzer; dafür ist keine besondere Bot-Reaktion festgelegt.
- Die Sicherheitsgrenze damit auf die private Verarbeitung und die Vergabe von Zugriffsrechten erst nach erfolgreicher Passwortprüfung eingegrenzt.

### 2026-10-26 – Privaten Anmeldebefehl `!ID passwort` festgelegt

- Den vom Nutzer vorgegebenen Anmeldebefehl `!ID passwort` dokumentiert.
- Als zwingende Sicherheitsvorgabe festgehalten, dass der Befehl ausschließlich als private Nachricht an den Bot verarbeitet werden darf und niemals eine Anmeldung aus einer Kanalnachricht auslösen darf.
- Festgehalten, dass Bot-Zugriffsrechte erst nach erfolgreicher Passwortprüfung vergeben werden dürfen.
- Darauf hingewiesen, dass Passwortausgaben in öffentlichen Antworten und unnötige Protokollierung zu vermeiden sind.
- Funktionsweise und Implementierungscode ausdrücklich als noch offen markiert.


### 2026-10-26 – Accountbindung und Bot-Zugriff bei Nicknamenwechsel festgelegt

- Dokumentiert, dass der Spieleraccount an den Nicknamen der Registrierung gebunden bleibt und bei einem Nicknamenwechsel nicht automatisch umbenannt oder übertragen wird.
- Festgehalten, dass die Registrierung Bot-Zugriffsrechte mit `/auser level nickname` einrichtet.
- Festgehalten, dass das `ON NICK`-Ereignis die zuvor gewährten Zugriffsrechte für den alten Nicknamen entfernen soll.
- Dokumentiert, dass bei einer späteren Rückkehr zum ursprünglichen Nicknamen eine erneute Anmeldung beim Bot erforderlich ist und das alte Zugriffslevel nicht bestehen bleiben darf.
- Den genauen Befehl zum Entfernen der Zugriffsrechte als noch offen markiert.


### 2026-10-26 – Verhalten bei bereits registriertem Nicknamen festgelegt

- Die Nutzerentscheidung dokumentiert, dass eine Registrierung bei einem bereits vorhandenen Account zum Nicknamen sofort abgebrochen wird.
- Festgehalten, dass die vorhandene Spielerdatei und Registrierung keinesfalls überschrieben oder verändert werden dürfen.
- Ergänzt, dass der Bot den Nutzer über `Translation.dat` informiert und ihn auffordert, mit `/nick Neuernick` den Nicknamen zu ändern und die Registrierung erneut zu versuchen.
- Festgehalten, dass die Prüfung vor dem Kopieren der Spielervorlage und vor Änderungen an Spielerdateien erfolgen muss.


### 2026-10-26 – Grundablauf der Spielerregistrierung festgelegt

- Den Befehl `registrieren` als Einstieg in die Registrierung dokumentiert.
- Festgehalten, dass vor dem Anlegen eines Accounts geprüft wird, ob bereits ein Account zum Nicknamen existiert.
- Den geplanten Ablauf mit Kopie und Umbenennung einer Spielervorlage, Anpassung vorgesehener Werte, zufälligem Passwort und privater Zustellung des Klartextpassworts festgehalten.
- Festgelegt dokumentiert, dass die Spielerdatei nur einen Passwort-Hash und nicht das Klartextpasswort enthalten soll.
- Standardwerte wie Lebenspunkte und Charakterbeschreibung als vorgesehene Vorlageninhalte aufgenommen.
- Konkreten Dateiaufbau und Hashing-Algorithmus ausdrücklich offen gelassen.

### 2026-10-26 – Spielerregistrierung vom Kampfbeitritt getrennt

- Festgehalten, dass Spielerregistrierung und Beitritt zu einem Kampf zwei getrennte Vorgänge sind.
- Nur bereits registrierte Spieler dürfen den später festzulegenden Kampfbeitrittsbefehl verwenden; der Beitrittsbefehl führt keine Registrierung durch.
- Den Befehlsnamen (z. B. `beitreten` oder `join`) ausdrücklich offengelassen.
- Die nächste Planungsfrage auf den Registrierungsablauf ausgerichtet.
- Präzisiert, dass bei `$readini(...)` die Dateiendung nicht maßgeblich ist; entscheidend ist die erwartete Datei- und Schlüsselstruktur.

### 2026-10-26 – Textausgaben und Ablauf ohne Anmeldungen festgelegt

- Dokumentiert, dass allgemeine Botmeldungen in `Translation.dat` und spielinhaltsspezifische Texte in den jeweils zuständigen Datenbanken bzw. Dateien abgelegt werden sollen, statt als feste Texte im Quellcode zu stehen.
- `$readini(...)` als vom Nutzer genannten möglichen Lesezugriff vermerkt; Format und Datenstruktur bleiben offen.
- Festgehalten, dass ein Kampf bei null Anmeldungen abgesagt wird, der Bot dies meldet und nach einer noch festzulegenden Wartezeit eine neue Ankündigung erfolgt.
- Wartezeit und Timer-Implementierung ausdrücklich offen gelassen.

### 2026-10-26 – Umfang der ersten Version und Name des Systemhelfers festgelegt

- Den ausdrücklich begrenzten Umfang des ersten Grundgerüsts dokumentiert: Spielerbeitritt, rundenbasierter gemeinsamer PvE-Kampf und zufällige Monstererzeugung.
- Waffen, Ausrüstung, Skills, Fähigkeiten, Techniken, Gegenstände, Loot, Events, Quests, Dungeons und weitere Erweiterungen als nicht Teil der ersten Version festgehalten; sie bleiben mögliche spätere Ausbaustufen.
- Den Namen des Helfers anhand der ursprünglichen Nutzerskizze korrigiert: `system_defaults_check`.
- Status: Nutzerentscheidung. Datum: 2026-10-26.

### 2026-10-26 – Umfang und Zeitpunkt von `system_defaults_check` präzisiert

- Festgehalten, dass der Helfer beim eigentlichen Botstart und nicht bei jedem `ON CONNECT` ausgeführt werden soll.
- Das Aufgabenbild aus der Nutzerskizze ergänzt: Systemeinstellungen und fehlende Standardwerte, `System.dat`, Verzeichnisstruktur, benötigte Datenbanken, Monsterdateien und Monsterpfad prüfen.
- Die Nutzerentscheidung dokumentiert, dass gefundene Probleme gemeldet werden, den Start aber nicht automatisch verhindern sollen; mögliche Folgefehler bleiben möglich.
- Das Beispiel des Nutzers ausdrücklich als unverbindliche Skizze markiert. Konkrete Umsetzung und Einzelregeln sind weiterhin offen.

### 2026-10-25 – Startablauf über `System.als` präzisiert

- Die Nutzerentscheidung dokumentiert, dass `Control.mrc` nur `System.als` auf Existenz prüft und lädt, statt alle weiteren Skriptdateien selbst zu laden.
- Den von Nutzer festgelegten Namen `system_defaults_check` für den nach dem Laden aufzurufenden Helper festgehalten.
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
 Der Helfer soll beim Botstart verschiedene Systemeinstellungen und Voraussetzungen prüfen, darunter Werte aus einer vorgesehenen `System.dat`, fehlende Standardwerte, Verzeichnisstruktur, Datenbanken wie Waffen und Items sowie Monsterdateien und den eingestellten Monsterpfad. Fehlende Standardeinstellungen können nach dem gezeigten Beispiel ergänzt und anschließend weiterverwendet werden. Die konkrete Umsetzung und die einzelnen Regeln sind noch offen; der Nutzer hat das Codebeispiel ausdrücklich als unverbindliche Skizze bezeichnet. Entscheider: Nutzer. Datum: 2026-10-26.

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
- Nach dem Laden von `System.als` soll deren eigener Helper `system_defaults_check` aufgerufen werden.
- `system_defaults_check` soll die weiteren allgemeinen Systemprüfungen übernehmen. Die genauen einzelnen Prüfungen und die genaue Zuständigkeit des Helpers werden später festgelegt.
- Die technische Umsetzung des Übergangs nach dem Laden ist noch offen. Der Nutzer hat als mögliche Ansätze einen kurzen Timer oder eine If-Schleife erwähnt; es ist noch nicht entschieden, welcher Mechanismus verwendet wird.
- Der Entwurf sieht vor, dass `System.als` die nachgelagerten Prüfungen und das Laden weiterer benötigter Skriptdateien übernimmt.

**Ergänzung nach Nutzerklärung: Umfang und Zeitpunkt von `system_defaults_check`**

- Der Nutzer hat klargestellt, dass `system_defaults_check` für den eigentlichen Start von BattleDome vorgesehen ist und nicht bei jeder IRC-Verbindung (`ON CONNECT`) erneut ausgeführt werden soll.
- Als Aufgabenbild für diesen Helfer nannte der Nutzer die Prüfung von Einstellungen in einer vorgesehenen `System.dat` (beispielsweise maximale Rundenzahl, maximale Lebenspunkte und Dauer von Rundenankündigungen), das Ergänzen fehlender Standardeinstellungen sowie Prüfungen der Verzeichnisstruktur, benötigter Datenbanken (unter anderem Waffen- und Item-Datenbanken), Monsterdateien und des konfigurierten Monsterpfads.
- Bei gefundenen Problemen soll der Nutzer informiert werden, der Start soll aber nicht allein deshalb verhindert werden. Fehlende Daten oder Ressourcen können später dennoch zu Folgefehlern führen. Dies ist von der bereits bestätigten Regel zu unterscheiden, dass der Start bei fehlender unverzichtbarer `System.als` abgebrochen wird.
- Das vom Nutzer gezeigte mIRC-Codebeispiel ist ausdrücklich nur eine Skizze und kein endgültiger Entwurf. Namen, Syntax, Prüfreihenfolge, Standardwerte und technische Umsetzung bleiben offen.

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

### 2026-10-26 – Umfang und Zeitpunkt von `system_defaults_check` präzisiert

- Festgehalten, dass der Helfer beim eigentlichen Botstart und nicht bei jedem `ON CONNECT` ausgeführt werden soll.
- Das Aufgabenbild aus der Nutzerskizze ergänzt: Systemeinstellungen und fehlende Standardwerte, `System.dat`, Verzeichnisstruktur, benötigte Datenbanken, Monsterdateien und Monsterpfad prüfen.
- Die Nutzerentscheidung dokumentiert, dass gefundene Probleme gemeldet werden, den Start aber nicht automatisch verhindern sollen; mögliche Folgefehler bleiben möglich.
- Das Beispiel des Nutzers ausdrücklich als unverbindliche Skizze markiert. Konkrete Umsetzung und Einzelregeln sind weiterhin offen.

### 2026-10-25 – Startablauf über `System.als` präzisiert

- Die Nutzerentscheidung dokumentiert, dass `Control.mrc` nur `System.als` auf Existenz prüft und lädt, statt alle weiteren Skriptdateien selbst zu laden.
- Den von Nutzer festgelegten Namen `system_defaults_check` für den nach dem Laden aufzurufenden Helper festgehalten.
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

Die erste Version ist auf das technische Grundgerüst eines rundenbasierten PvE-Kampfsystems begrenzt. Sie soll Spielerbeitritt zu einem Kampf, zufällige Monstererzeugung und den grundlegenden gemeinsamen Kampfablauf ermöglichen. Die technische Basis muss dafür notwendige Startprüfungen, Einstellungen und Skriptstruktur enthalten.

Nicht Teil der ersten Version sind Waffen, Ausrüstung, Skills, Fähigkeiten, Techniken, Gegenstände, Loot, Events, Quests, Dungeons oder ähnliche Erweiterungssysteme. Diese Funktionen sind nicht verworfen, sondern ausdrücklich auf spätere Ausbaustufen verschoben. Sie sollen erst nach einem funktionsfähigen Grundgerüst schrittweise geplant und ergänzt werden.


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
- Nach dem Laden von `System.als` soll deren eigener Helper `system_defaults_check` aufgerufen werden.
- `system_defaults_check` soll die weiteren allgemeinen Systemprüfungen übernehmen. Die genauen einzelnen Prüfungen und die genaue Zuständigkeit des Helpers werden später festgelegt.
- Die technische Umsetzung des Übergangs nach dem Laden ist noch offen. Der Nutzer hat als mögliche Ansätze einen kurzen Timer oder eine If-Schleife erwähnt; es ist noch nicht entschieden, welcher Mechanismus verwendet wird.
- Der Entwurf sieht vor, dass `System.als` die nachgelagerten Prüfungen und das Laden weiterer benötigter Skriptdateien übernimmt.

**Ergänzung nach Nutzerklärung: Umfang und Zeitpunkt von `system_defaults_check`**

- Der Nutzer hat klargestellt, dass `system_defaults_check` für den eigentlichen Start von BattleDome vorgesehen ist und nicht bei jeder IRC-Verbindung (`ON CONNECT`) erneut ausgeführt werden soll.
- Als Aufgabenbild für diesen Helfer nannte der Nutzer die Prüfung von Einstellungen in einer vorgesehenen `System.dat` (beispielsweise maximale Rundenzahl, maximale Lebenspunkte und Dauer von Rundenankündigungen), das Ergänzen fehlender Standardeinstellungen sowie Prüfungen der Verzeichnisstruktur, benötigter Datenbanken (unter anderem Waffen- und Item-Datenbanken), Monsterdateien und des konfigurierten Monsterpfads.
- Bei gefundenen Problemen soll der Nutzer informiert werden, der Start soll aber nicht allein deshalb verhindert werden. Fehlende Daten oder Ressourcen können später dennoch zu Folgefehlern führen. Dies ist von der bereits bestätigten Regel zu unterscheiden, dass der Start bei fehlender unverzichtbarer `System.als` abgebrochen wird.
- Das vom Nutzer gezeigte mIRC-Codebeispiel ist ausdrücklich nur eine Skizze und kein endgültiger Entwurf. Namen, Syntax, Prüfreihenfolge, Standardwerte und technische Umsetzung bleiben offen.

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

### 2026-10-26 – Umfang der ersten Version und Name des Systemhelfers festgelegt

- Den ausdrücklich begrenzten Umfang des ersten Grundgerüsts dokumentiert: Spielerbeitritt, rundenbasierter gemeinsamer PvE-Kampf und zufällige Monstererzeugung.
- Waffen, Ausrüstung, Skills, Fähigkeiten, Techniken, Gegenstände, Loot, Events, Quests, Dungeons und weitere Erweiterungen als nicht Teil der ersten Version festgehalten; sie bleiben mögliche spätere Ausbaustufen.
- Den Namen des Helfers anhand der ursprünglichen Nutzerskizze korrigiert: `system_defaults_check`.
- Status: Nutzerentscheidung. Datum: 2026-10-26.

### 2026-10-26 – Umfang und Zeitpunkt von `system_defaults_check` präzisiert

- Festgehalten, dass der Helfer beim eigentlichen Botstart und nicht bei jedem `ON CONNECT` ausgeführt werden soll.
- Das Aufgabenbild aus der Nutzerskizze ergänzt: Systemeinstellungen und fehlende Standardwerte, `System.dat`, Verzeichnisstruktur, benötigte Datenbanken, Monsterdateien und Monsterpfad prüfen.
- Die Nutzerentscheidung dokumentiert, dass gefundene Probleme gemeldet werden, den Start aber nicht automatisch verhindern sollen; mögliche Folgefehler bleiben möglich.
- Das Beispiel des Nutzers ausdrücklich als unverbindliche Skizze markiert. Konkrete Umsetzung und Einzelregeln sind weiterhin offen.

### 2026-10-25 – Startablauf über `System.als` präzisiert

- Die Nutzerentscheidung dokumentiert, dass `Control.mrc` nur `System.als` auf Existenz prüft und lädt, statt alle weiteren Skriptdateien selbst zu laden.
- Den von Nutzer festgelegten Namen `system_defaults_check` für den nach dem Laden aufzurufenden Helper festgehalten.
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
 Der Helfer soll beim Botstart verschiedene Systemeinstellungen und Voraussetzungen prüfen, darunter Werte aus einer vorgesehenen `System.dat`, fehlende Standardwerte, Verzeichnisstruktur, Datenbanken wie Waffen und Items sowie Monsterdateien und den eingestellten Monsterpfad. Fehlende Standardeinstellungen können nach dem gezeigten Beispiel ergänzt und anschließend weiterverwendet werden. Die konkrete Umsetzung und die einzelnen Regeln sind noch offen; der Nutzer hat das Codebeispiel ausdrücklich als unverbindliche Skizze bezeichnet. Entscheider: Nutzer. Datum: 2026-10-26.

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
- Nach dem Laden von `System.als` soll deren eigener Helper `system_defaults_check` aufgerufen werden.
- `system_defaults_check` soll die weiteren allgemeinen Systemprüfungen übernehmen. Die genauen einzelnen Prüfungen und die genaue Zuständigkeit des Helpers werden später festgelegt.
- Die technische Umsetzung des Übergangs nach dem Laden ist noch offen. Der Nutzer hat als mögliche Ansätze einen kurzen Timer oder eine If-Schleife erwähnt; es ist noch nicht entschieden, welcher Mechanismus verwendet wird.
- Der Entwurf sieht vor, dass `System.als` die nachgelagerten Prüfungen und das Laden weiterer benötigter Skriptdateien übernimmt.

**Ergänzung nach Nutzerklärung: Umfang und Zeitpunkt von `system_defaults_check`**

- Der Nutzer hat klargestellt, dass `system_defaults_check` für den eigentlichen Start von BattleDome vorgesehen ist und nicht bei jeder IRC-Verbindung (`ON CONNECT`) erneut ausgeführt werden soll.
- Als Aufgabenbild für diesen Helfer nannte der Nutzer die Prüfung von Einstellungen in einer vorgesehenen `System.dat` (beispielsweise maximale Rundenzahl, maximale Lebenspunkte und Dauer von Rundenankündigungen), das Ergänzen fehlender Standardeinstellungen sowie Prüfungen der Verzeichnisstruktur, benötigter Datenbanken (unter anderem Waffen- und Item-Datenbanken), Monsterdateien und des konfigurierten Monsterpfads.
- Bei gefundenen Problemen soll der Nutzer informiert werden, der Start soll aber nicht allein deshalb verhindert werden. Fehlende Daten oder Ressourcen können später dennoch zu Folgefehlern führen. Dies ist von der bereits bestätigten Regel zu unterscheiden, dass der Start bei fehlender unverzichtbarer `System.als` abgebrochen wird.
- Das vom Nutzer gezeigte mIRC-Codebeispiel ist ausdrücklich nur eine Skizze und kein endgültiger Entwurf. Namen, Syntax, Prüfreihenfolge, Standardwerte und technische Umsetzung bleiben offen.

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

### 2026-10-26 – Umfang und Zeitpunkt von `system_defaults_check` präzisiert

- Festgehalten, dass der Helfer beim eigentlichen Botstart und nicht bei jedem `ON CONNECT` ausgeführt werden soll.
- Das Aufgabenbild aus der Nutzerskizze ergänzt: Systemeinstellungen und fehlende Standardwerte, `System.dat`, Verzeichnisstruktur, benötigte Datenbanken, Monsterdateien und Monsterpfad prüfen.
- Die Nutzerentscheidung dokumentiert, dass gefundene Probleme gemeldet werden, den Start aber nicht automatisch verhindern sollen; mögliche Folgefehler bleiben möglich.
- Das Beispiel des Nutzers ausdrücklich als unverbindliche Skizze markiert. Konkrete Umsetzung und Einzelregeln sind weiterhin offen.

### 2026-10-25 – Startablauf über `System.als` präzisiert

- Die Nutzerentscheidung dokumentiert, dass `Control.mrc` nur `System.als` auf Existenz prüft und lädt, statt alle weiteren Skriptdateien selbst zu laden.
- Den von Nutzer festgelegten Namen `system_defaults_check` für den nach dem Laden aufzurufenden Helper festgehalten.
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
