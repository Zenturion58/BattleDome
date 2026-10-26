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
- [x] **Nach jeder IRC-Verbindung neu anmelden:** Der Nutzer bevorzugt ausdrücklich Variante A: Nach einer Trennung und erneuten Verbindung muss ein Spieler sich erneut mit `!ID passwort` anmelden. Beim `ON QUIT`-Ereignis sollen die vorübergehend vergebenen Bot-Zugriffsrechte entfernt werden; die dauerhaften Account- und Spielerdaten bleiben bestehen. Die konkrete Implementierung des Ereignisses ist noch offen. Als mIRC-Befehl zum Entfernen eines Nutzers bzw. seiner Zugriffsrechte ist `/ruser` dokumentiert (nicht `/deluser` oder `/duser`); welche genaue Form im Skript erforderlich ist, wird bei der Implementierung geprüft. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Laufenden Kampf bei Verbindungsabbruch eines Teilnehmers beenden:** Wenn ein Spieler während eines laufenden Kampfes die IRC-Verbindung verliert, werden seine vorübergehend vergebenen Bot-Zugriffsrechte entfernt und der gesamte laufende Kampf wird beendet. Der Kampf läuft nicht ohne diesen Spieler weiter. Der Spieleraccount und die gespeicherten Spielerdaten bleiben bestehen; nach der Wiederverbindung muss sich der Spieler erneut anmelden. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Einfaches Kampfende bei Monstersieg in Version 1:** Wenn das Monster besiegt wird, endet der Kampf. Das Monster wird aus der Zugreihenfolge entfernt und die laufenden Kampfdaten werden verworfen; dauerhafte Accounts und gespeicherte Spielerdaten bleiben erhalten. In der ersten Version gibt es dabei noch keine Belohnungen oder weiteren Folgefunktionen. Belohnungen, Events, Monsterfähigkeiten, zusätzliche Monsterattribute und ähnliche Erweiterungen werden erst nach einem funktionierenden Grundgerüst schrittweise geplant. Sie sind aufgeschoben, nicht grundsätzlich ausgeschlossen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Einfaches Kampfende bei Niederlage aller Spieler in Version 1:** Sobald alle am Kampf teilnehmenden Spieler besiegt sind, endet der Kampf – auch wenn nur ein einziger Spieler teilnimmt. Das Monster wird aus der Zugreihenfolge entfernt und die laufenden Kampfdaten werden verworfen; dauerhafte Accounts und gespeicherte Spielerdaten bleiben erhalten. In Version 1 sind dafür keine zusätzlichen Folgen oder Belohnungsmechaniken vorgesehen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Monster und Kampfdaten bei Kampfende verwerfen:** Wird ein laufender Kampf durch den Verbindungsabbruch eines Teilnehmers beendet, endet der Kampf für alle Beteiligten, einschließlich des Monsters. Das Monster wird aus der Zugreihenfolge entfernt und die laufenden Kampfdaten werden geleert bzw. verworfen. Der Kampfzustand wird nicht fortgesetzt; bei einem späteren Kampf wird ein neues Monster erzeugt. Dauerhafte Accounts und gespeicherte Spielerdaten bleiben unberührt. Die konkrete technische Speicherung und Bereinigung der Kampfdaten ist noch offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Flucht aus einem laufenden Kampf mit `!flee`:** Der Befehl `!flee` lässt den aufrufenden Spieler aus dem laufenden Kampf fliehen. Dieser Spieler wird aus der Zugreihenfolge entfernt und `NumberOfPlayers` im Abschnitt `[Battle]` der Datei `Battle.txt` wird um eins verringert. Solange danach noch mindestens ein Spieler am Kampf teilnimmt, läuft der Kampf mit den übrigen Spielern weiter. Flieht der letzte verbliebene Spieler, endet der Kampf vollständig; das Monster wird aus der Zugreihenfolge entfernt und sämtliche aktiven Kampfdaten für Spieler und Monster werden verworfen. Dauerhafte Accounts und gespeicherte Spielerdaten bleiben erhalten. Es gibt für eine Flucht keine Belohnung oder sonstige Zusatzeffekte, da das Grundgerüst kein Belohnungssystem enthält. Der vorgesehene Helfer `$players_in_battle` liest `NumberOfPlayers` mit `$readini` aus `Battle.txt` und gibt den Wert zurück. Die konkrete Implementierung und die genaue Reihenfolge von Aktualisierung und Prüfung bleiben offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Rundenwechsel und gespeicherte Zwischenstände im Mehrspielerkampf:** Der Rundenzähler wird erst erhöht, nachdem die vollständige Zugreihenfolge aller beteiligten Spieler und Monster abgearbeitet wurde. Der aktive Kampfzustand muss die aktuelle Rundennummer und die aktuelle Zugposition getrennt abbilden. Unmittelbare Monstergegenangriffe gehören zum gerade laufenden Spielerzug und sind kein eigenständiger Zug in der regulären Reihenfolge. Wurde ein Monster bereits in derselben Runde angegriffen, wird sein späterer regulärer Zug übersprungen und als abgearbeitet behandelt. Die nötigen Zwischenstände müssen gespeichert werden, damit der Rundenwechsel im Mehrspielerkampf zuverlässig abläuft. Die konkrete technische Repräsentation und das endgültige Speicherformat bleiben offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Monsterzüge und Erfassung bereits erfolgter Angriffe:** In Version 1 wird in `Battle.txt` im Abschnitt `[RoundStatus]` über den Schlüssel `MonstersActed` festgehalten, welche Monster in der aktuellen Runde bereits angegriffen haben. Nach einem Angriff wird das betreffende Monster dort vermerkt; bei einem späteren Zug in derselben Runde wird anhand dieser Liste ein weiterer Angriff verhindert. Zu Beginn einer neuen Runde wird die Liste zurückgesetzt. Damit wird die bestätigte Regel umgesetzt, dass jedes Monster in Version 1 höchstens einmal pro Runde angreifen darf. Die konkrete technische Umsetzung und das genaue Speicherformat der Liste bleiben offen. Entscheider: Nutzer (Bestätigung des Vorschlags). Datum: 2026-10-26.\n- [x] **Zielauswahl von Spielern und Monstern in Version 1:** Spieler bestimmen ihr Angriffsziel selbst über einen dafür vorgesehenen Befehl; der genaue Befehlsname und die Eingabesyntax bleiben offen. Monster wählen ihre Ziele nach ihrer eigenen Schadenshistorie: Ein Monster, das Schaden erlitten hat, greift bevorzugt den Spieler an, der ihm zuletzt Schaden zugefügt hat, sofern dieser noch lebt und am Kampf teilnimmt. Es zählt ausschließlich die zeitlich letzte Schadensverursachung an diesem Monster; die Höhe des Schadens und der Gesamtschaden eines Spielers sind für diese Zielauswahl unerheblich. Auch ein geringer letzter Treffer ersetzt somit den vorherigen Angreifer als bevorzugtes Ziel. Ist dieses Ziel besiegt oder geflohen und damit nicht mehr als gültiges Ziel verfügbar, gilt das bisherige Ziel als verloren und das Monster wählt zufällig einen anderen gültigen, noch lebenden und am Kampf teilnehmenden Spieler. Ein Monster, das selbst noch keinen Schaden erlitten hat, darf ebenfalls zufällig einen gültigen Spieler auswählen. Die letzte Schadensquelle wird je Monster getrennt verfolgt. Beispiel: Verursacht Spieler A 100 Schaden an einem Monster und Spieler B danach 2 Schaden, bevorzugt dieses Monster Spieler B, solange B noch am Kampf teilnimmt; ein anderes, nicht angegriffenes Monster kann unabhängig davon zufällig ein Ziel wählen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Grundregel für Monsterzüge in Version 1:** Jedes lebende Monster soll regulär einen Zug erhalten, auch wenn kein Spieler es in dieser Runde angegriffen hat. Wird ein Monster von einem Spieler angegriffen, soll es grundsätzlich direkt danach einen Gegenzug ausführen. Die Zielauswahl richtet sich nach dem letzten erlittenen Schaden: Ein Monster greift bevorzugt den noch lebenden Spieler an, der ihm zuletzt Schaden zugefügt hat. Hat ein Monster im bisherigen Kampf keinen Schaden erlitten, darf es sein Ziel zufällig unter den gültigen, noch lebenden Spielern bestimmen. Diese Zielinformation ist pro Monster getrennt zu behandeln; der letzte Angreifer eines anderen Monsters beeinflusst sie nicht. Um Doppelzüge im Grundgerüst zu verhindern, darf jedes Monster in einer Runde insgesamt höchstens einmal angreifen: Hat es nach einem Spielerangriff bereits seinen unmittelbaren Gegenzug ausgeführt, entfällt sein späterer regulärer Zug in derselben Runde. Hat es seinen regulären Zug bereits ausgeführt, entfällt ein späterer zusätzlicher Gegenzug in dieser Runde. Besondere Fähigkeiten, die mehrere Angriffe pro Runde erlauben, sind für spätere Versionen vorgesehen und gehören nicht zum Grundgerüst. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Zentrale Zugverarbeitung durch `$next_turn` (Zielarchitektur):** Der Helfer `$next_turn` ist allgemein für die Verarbeitung des nächsten Zuges zuständig, nicht nur für Monsterzüge. Er prüft unter anderem, wer als Nächstes am Zug ist, wie viele Monster noch im Kampf sind, wie viele Spieler leben, ob ein Monster in der Runde bereits gehandelt hat und welche Kampfbedingungen für die nächste Aktion relevant sind. Zu den möglichen Prüfungen gehören in späteren Ausbaustufen Immunität gegen Schaden, Taumel-Effekte und die Frage, ob ein Angriff Status- oder Folgeschaden wie Vergiftung auslösen kann. `$next_turn` ist als zentraler, vergleichsweise kleiner Ablaufhelfer vorgesehen und kann bei Bedarf weitere spezialisierte Helfer aufrufen. Welche zusätzlichen Helfer es geben wird und wie die Aufgaben genau verteilt werden, ist noch offen. `Battle.txt` enthält grundlegende Informationen zum laufenden Kampf; die eigentliche Verarbeitung der Zuglogik und die Prüfung weiterer Informationen soll nicht ausschließlich auf Daten beschränkt sein, die in `Battle.txt` stehen. Diese Zielarchitektur wird für das spätere Endprodukt berücksichtigt; der Prototyp bleibt einfacher. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Monsterdatei als Vorlage für das spätere Endprodukt:** Die vom Nutzer bereitgestellte Datei `neues_monster.char` dient als Vorlage für die Monsterdatei des späteren Endprodukts, nicht als verbindliche Vorgabe für den Prototypen. Sie veranschaulicht eine datenbasierte Struktur mit unter anderem Grundwerten, Kampfwerten, Beschreibungen, allgemeinen Monsterinformationen und Eigenschaften, Statuszuständen, Waffen, Skills, Techniken, Ausrüstung, natürlichen Rüstungen, Limitbreaks sowie Schadensmodifikatoren und Resistenzen. Das spätere Kampfsystem soll die jeweils relevanten Monsterdaten im passenden Ablauf auswerten können. Die konkrete Verarbeitung der einzelnen Felder und die Aufteilung auf `$next_turn` sowie weitere Helfer werden schrittweise geplant; die Namen und Zuständigkeiten zusätzlicher Helfer sind noch offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Gegenreaktionen nicht allein vom verursachten Schaden abhängig machen:** Ein Spielerangriff kann eine Monsterreaktion beziehungsweise einen Gegenangriff auslösen, auch wenn der berechnete Schaden 0 beträgt, etwa aufgrund einer späteren Immunität oder eines anderen Modifikators. Ob das Monster die Reaktion tatsächlich ausführen kann, wird anhand der geltenden Zugregeln und weiterer Bedingungen geprüft; beispielsweise kann ein Status wie Paralyse oder Lähmung die Handlung verhindern. Schadensermittlung, Reaktionsauslösung und Handlungsfähigkeit sind daher als logisch getrennte Aspekte zu behandeln. Konkrete Statusmechaniken und ihre Umsetzung gehören zu späteren Versionen; diese Architekturvorgabe ändert den bewusst einfachen Funktionsumfang des Prototyps nicht. Entscheider: Nutzer. Datum: 2026-10-26.
- [ ] **Monster-Nachschub und maximale Monsterzahl (spätere Version):** Die Nachschubmechanik ist eine eigenständige Spielmechanik und weder grundsätzlich vom Tod eines Monsters noch vom Typ des auslösenden Monsters abhängig. Sie kann beispielsweise nach dem Besiegen eines Monsters, während eines Angriffs auf ein noch lebendes Monster oder während eines Zuges ausgelöst werden, in dem ein Monster noch lebt und handelt. Ein Auslöser kann somit auch eintreten, wenn ein anderes Monster noch am Leben ist oder eine zusätzliche Aktion wie ein Double Turn stattfindet. Künftige Monsterfähigkeiten oder Spielereignisse können Auslöser bereitstellen; es ist aber nicht festgelegt, dass dafür ein bestimmter Monstertyp oder eine spezielle Monster-Eigenschaft erforderlich ist. Bei Auslösung wird die Nachschubchance beziehungsweise die zugehörige Bedingung geprüft; erscheint ein neues Monster, wird es in die laufende Zugreihenfolge aufgenommen und der Kampf geht weiter. Die Mechanik kann im selben Kampf mehrfach auftreten und auch bei ursprünglich einem oder zwei Monstern relevant sein. Als vorläufiger Richtwert wurde eine Chance von 10 % genannt; diese Wahrscheinlichkeit und die Frage, ob sie für alle Auslöser gleichermaßen gilt, sind noch nicht endgültig festgelegt. `Max Numbers of Monsters` ist der vorläufige Name für die Obergrenze gleichzeitig lebender beziehungsweise aktiver Monster im Kampf, nicht für die Gesamtzahl aller Monster, die während des Kampfes nacheinander erscheinen dürfen. Besiegte Monster werden aus dem aktiven Kampf entfernt und belegen keinen Platz unter dieser Obergrenze. Vor jedem Spawn muss geprüft werden, ob noch ein Platz frei ist; die Obergrenze darf niemals überschritten werden. Ist das Maximum erreicht, darf kein weiteres Monster hinzugefügt werden, auch wenn die Nachschubmechanik ausgelöst wurde. Der Kampf darf nicht als endgültig gewonnen beendet werden, solange ein durch diese Mechanik tatsächlich erscheinendes neues Monster den Kampf fortsetzt. Die konkreten Auslösezeitpunkte und Bedingungen bleiben noch zu spezifizieren. Konfigurationsort und endgültiger Variablen-/Schlüsselname bleiben offen. Diese Mechanik gehört zu späteren Versionen und verändert Version 1 nicht. Status: als spätere Mechanik vorgemerkt; 10 % und technischer Name vorläufig, genaue Auslöser offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [ ] **Verteidiger-Monster (spätere Version):** Als geplante Monster-Eigenschaft soll es Monster geben können, die nicht aktiv handeln. Wenn sie in der Zugreihenfolge an der Reihe wären, wird ihr Zug übersprungen. Auch im Zusammenhang mit einem solchen Monster kann die eigenständige Nachschubmechanik ausgelöst werden, selbst wenn das Verteidiger-Monster noch lebt. Der konkrete Eigenschaftsname und die vollständigen Regeln für Verteidiger-Monster sind noch offen. Diese Mechanik gehört zu späteren Versionen und verändert Version 1 nicht. Status: vorgemerkt, Detailregeln offen. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Zugkosten und spätere Zusatzaktionsmechaniken voneinander unterscheiden:** Für spätere Versionen gilt als vom Nutzer mitgeteilter Planungsgrundsatz: Die Aktivierung eines Skills, einer Waffenmechanik, einer Technik, eines Gegenstands oder einer vergleichbaren Fähigkeit kostet grundsätzlich einen Zugpunkt. Ein Skill, der für eine Runde zwei Aktionen ermöglicht, gewährt dadurch keinen sofortigen Zusatzangriff: Die Aktivierung kostet zunächst den Zugpunkt; die zusätzliche Aktionsmöglichkeit greift erst bei der späteren regulären Gelegenheit des Spielers innerhalb der Zugreihenfolge. Davon getrennt ist die spätere interne Spielmechanik **Double Turn**: Wenn sie ausgelöst wird, soll sie dem Spieler unmittelbar einen weiteren Angriff innerhalb desselben Zugablaufs ermöglichen. Ob die Mechanik zufällig ausgelöst wird oder nach anderen Bedingungen funktioniert, ist ausdrücklich noch offen; ebenso sind konkrete Auslösebedingungen und Wahrscheinlichkeiten nicht festgelegt. Double Turn ist keine Aktivierung und nicht dieselbe Mechanik wie ein Skill, der zwei Aktionen in einer Runde ermöglicht. Die konkreten Regeln und Umsetzung dieser späteren Mechaniken werden erst in den jeweiligen Versionen festgelegt. Sie ändern die Regeln von Version 1 nicht. Status: für spätere Versionen vorgemerkte Regelbeschreibung, noch keine Implementierungsentscheidung. Entscheider: Nutzer. Datum: 2026-10-26.
- [x] **Ablauf und Reihenfolge bei Double Turn:** Wenn Double Turn während eines Spielerangriffs ausgelöst wird, führt derselbe Spieler seinen zusätzlichen Angriff unmittelbar aus, bevor der Kampfablauf zum nächsten regulären Beteiligten oder zum Monstergegenangriff übergeht. Schadensverarbeitung und zugehörige Angriffsmeldungen des ersten Angriffs werden vor der Auslösung des Double Turn ausgegeben; der zusätzliche Angriff wird ebenfalls abgewickelt, bevor das Monster reagieren darf. Double Turn ist kein eigener regulärer Zug und wird nicht in die Zugreihenfolge einsortiert, sondern vollständig innerhalb des laufenden Spielerangriffs abgewickelt. Beispiel: Bei der Zugreihenfolge Spieler A → Monster A → Spieler B greift Spieler A Monster A an; nach Schadensmeldung wird Double Turn ausgelöst; Spieler A greift Monster A erneut an; erst danach darf Monster A agieren, anschließend folgt Spieler B gemäß Zugreihenfolge. Diese Regel gilt als Planung für spätere Versionen und ändert Version 1 nicht. Entscheider: Nutzer. Datum: 2026-10-26. Bei mehreren Monstern gilt zusätzlich: Wird das zuerst angegriffene Monster durch den ersten Angriff besiegt, beendet das allein den Kampf nicht, solange weitere Monster am Kampf beteiligt und noch am Leben sind. Der durch Double Turn gewährte zusätzliche Angriff darf dann gegen ein anderes gültiges Monsterziel gerichtet werden. Double Turn wird abhängig davon abgewickelt, ob der Kampf nach dem ersten Angriff noch läuft und ein gültiges Ziel vorhanden ist. Übergeordnete Kampfendregel: Sobald alle feindlichen Monster beziehungsweise alle gültigen feindlichen Monsterziele beseitigt sind, endet der Kampf sofort – unabhängig davon, wodurch oder unter welchen Bedingungen dies geschieht. Es werden danach keine weiteren Monsterangriffe, Gegenangriffe oder regulären Monsterzüge ausgeführt. Diese allgemeine Regel gilt unabhängig von Double Turn und ist nicht auf eine bestimmte Auslöse- oder Angriffssituation beschränkt.
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

### Flucht aus einem laufenden Kampf mit `!flee`

Der Befehl `!flee` soll den aufrufenden Spieler aus der Zugreihenfolge entfernen und `NumberOfPlayers` in `Battle.txt` unter `[Battle]` um eins reduzieren. Der vorgesehene Helfer `$players_in_battle` liest diesen Wert mit `$readini` und gibt ihn zurück. Der Kampf läuft weiter, solange nach der Flucht mindestens ein Spieler übrig bleibt.

Flieht der letzte verbliebene Spieler, endet der Kampf vollständig. Dabei wird das Monster aus der Zugreihenfolge entfernt und sämtliche aktiven Kampfdaten für Spieler und Monster werden verworfen. Dauerhafte Accounts und gespeicherte Spielerdaten bleiben erhalten. Für Flucht gibt es keine Belohnung und keine sonstigen Zusatzeffekte; ein Belohnungssystem ist nicht Teil des Grundgerüsts.

**Noch offen:** Die konkrete mIRC-Implementierung des Helfers sowie die genaue Reihenfolge von Zählwertaktualisierung, Prüfung und Bereinigung der Kampfdaten.

### Mehrere Spieler und mehrere Monster: Zugablauf

**Bestätigte Grundregel für Version 1:** Jedes lebende Monster kann regulär angreifen, auch wenn die Spieler in ihren Zügen ausschließlich ein anderes Monster angreifen. Ein Spielerangriff auf ein Monster löst grundsätzlich unmittelbar danach einen Gegenzug dieses angegriffenen Monsters aus. Das angegriffene Monster wählt für diesen Gegenzug zufällig einen noch lebenden teilnehmenden Spieler als Ziel.

Doppelzüge sind im Grundgerüst ausgeschlossen: Ein Monster darf in einer Runde insgesamt höchstens einmal angreifen. Führt es nach einem Spielerangriff bereits seinen unmittelbaren Gegenzug aus, wird sein regulärer Zug später in derselben Runde ausgelassen. Hat es seinen regulären Zug bereits ausgeführt, gibt es bei einem späteren Angriff auf dieses Monster in derselben Runde keinen zusätzlichen Gegenzug. Besondere Fähigkeiten, mit denen ein Monster später mehrmals pro Runde angreifen kann, bleiben zukünftigen Versionen vorbehalten.

**Vorläufige Skizze der Datei `Battle.txt`:** Der Nutzer hat als mögliches Datenlayout die Abschnitte `[BattleInfo]` (unter anderem `BattleID` und `NumberOfPlayers`), `[Stats]` (unter anderem `NumberOfMaxRounds` und eine Liste mehrerer Monster im Schlüssel `Monsters`) sowie `[BattleOrder]` (Schlüssel `Players` mit der Zugreihenfolge von Spielern und Monstern) beschrieben. Mehrere Einträge in den Listen könnten durch Punkte getrennt werden, etwa `PlayerA.PlayerB.MonsterA`. Dies ist zunächst eine konzeptionelle Skizze, keine festgelegte oder implementierte Dateistruktur. Die Erfassung bereits erfolgter Monsterangriffe soll über `[RoundStatus]` und `MonstersActed` erfolgen: Bereits angreifende Monster werden in der laufenden Runde vermerkt, und die Liste wird zu Beginn der nächsten Runde geleert. Dieses Prinzip wurde vom Nutzer am 2026-10-26 bestätigt.

**Verbindliche Regel für Rundenwechsel und Zwischenstände:** Der Rundenzähler wird nicht nach jedem einzelnen Zug erhöht. Eine Runde endet erst, wenn die vollständige Zugreihenfolge aller beteiligten Spieler und Monster abgearbeitet wurde. Der aktive Kampfzustand muss aktuelle Rundennummer und aktuelle Position innerhalb der Zugreihenfolge getrennt festhalten. Unmittelbare Monstergegenangriffe gehören zum laufenden Spielerzug und sind kein eigenständiger Zug in der regulären Reihenfolge. Hat ein Monster bereits in derselben Runde angegriffen, wird sein späterer regulärer Zug übersprungen; dieser Eintrag gilt trotzdem als abgearbeitet. Die für den fehlerfreien Mehrspielerkampf nötigen Zwischenstände müssen im aktiven Kampfzustand gespeichert werden. Die konkrete technische Umsetzung, das genaue Speicherformat und die Ablaufsteuerung bleiben offen.

Entscheider der bestätigten Kampfregel: Nutzer. Datum: 2026-10-26.

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

### 2026-10-26 – Letzte Schadensverursachung statt Schadenshöhe bestimmt Monsterziel

- Bestätigt, dass für das bevorzugte Monsterziel immer der Spieler zählt, der diesem Monster zuletzt Schaden zugefügt hat.
- Die Höhe des letzten Schadens und der gesamte bisher verursachte Schaden spielen für die Zielauswahl keine Rolle; auch ein kleiner letzter Treffer ersetzt den vorherigen Angreifer als bevorzugtes Ziel.
- Die Regel wird je Monster separat angewendet. Entscheider: Nutzer. Datum: 2026-10-26.

### 2026-10-26 – Ungültig gewordenes Monsterziel neu bestimmen

- Ergänzt, dass ein Monster sein bisheriges Ziel verliert, wenn dieser Spieler besiegt wurde oder geflohen ist und nicht mehr als gültiges Ziel zur Verfügung steht.
- Das Monster wählt dann zufällig einen anderen gültigen, noch lebenden und am Kampf teilnehmenden Spieler.
- Die Regel ergänzt die bestehende Zielauswahl und gilt pro Monster. Entscheider: Nutzer. Datum: 2026-10-26.

### 2026-10-26 – Zielauswahl von Spielern und Monstern festgelegt

- Dokumentiert, dass Spieler ihr Angriffsziel selbst über einen vorgesehenen Befehl auswählen; Befehlsname und Syntax bleiben offen.
- Festgelegt, dass ein Monster bevorzugt den noch lebenden Spieler angreift, der ihm zuletzt Schaden zugefügt hat.
- Festgelegt, dass ein Monster, das selbst keinen Schaden erlitten hat, sein Ziel zufällig unter den gültigen, noch lebenden Spielern auswählen darf.
- Klargestellt, dass die letzte Schadensquelle pro Monster getrennt verfolgt wird, damit das Kampfgeschehen eines Monsters die Zielauswahl eines anderen Monsters nicht beeinflusst.
- Die bisherige allgemeine Zufallsziel-Regel für Monster nach einem Spielerangriff entsprechend präzisiert. Entscheider: Nutzer. Datum: 2026-10-26.

### 2026-10-26 – Rundenwechsel und Zwischenstände im Mehrspielerkampf festgelegt

- Eine Runde endet erst, wenn die vollständige Zugreihenfolge aller beteiligten Spieler und Monster abgearbeitet wurde. Der Rundenzähler wird nicht nach jedem einzelnen Zug erhöht.
- Der aktive Kampfzustand muss aktuelle Rundennummer und aktuelle Position in der Zugreihenfolge getrennt festhalten.
- Unmittelbare Monstergegenangriffe gehören zum laufenden Spielerzug und sind kein eigenständiger Zug in der regulären Reihenfolge.
- Hat ein Monster bereits in dieser Runde angegriffen, wird sein späterer regulärer Zug übersprungen; der Eintrag gilt trotzdem als abgearbeitet.
- Die notwendigen Zwischenstände müssen für einen fehlerfreien Mehrspielerkampf gespeichert werden. Die konkrete technische Umsetzung und das Speicherformat bleiben offen.

### 2026-10-26 – Erfassung bereits erfolgter Monsterangriffe pro Runde festgelegt

- Die Nutzerbestätigung dokumentiert, dass `Battle.txt` einen Abschnitt `[RoundStatus]` mit dem Schlüssel `MonstersActed` erhalten soll.
- Darin werden Monster vermerkt, die in der aktuellen Runde bereits angegriffen haben, damit sie in derselben Runde keinen zweiten Angriff ausführen.
- Zu Beginn jeder neuen Runde wird diese Liste zurückgesetzt.
- Die Entscheidung legt das Prinzip fest, nicht die endgültige Dateistruktur oder den mIRC-Code; die technische Umsetzung bleibt offen.

### 2026-10-26 – Monsterzüge bei mehreren Spielern und Monstern präzisiert

- Die Nutzerentscheidung dokumentiert, dass jedes lebende Monster regulär angreifen können muss, auch wenn kein Spieler dieses Monster angegriffen hat.
- Festgehalten, dass ein Spielerangriff grundsätzlich einen unmittelbaren Gegenzug des angegriffenen Monsters auslöst und das Monster dabei zufällig einen noch lebenden Spieler als Ziel auswählt.
- Für Version 1 Doppelzüge ausgeschlossen: Ein Monster darf insgesamt höchstens einmal pro Runde angreifen. Ein bereits ausgeführter unmittelbarer Gegenzug ersetzt den späteren regulären Zug; ein bereits ausgeführter regulärer Zug verhindert einen zusätzlichen Gegenzug in derselben Runde.
- Mehrfachangriffe durch besondere Monsterfähigkeiten ausdrücklich auf spätere Versionen verschoben.
- Die vom Nutzer skizzierte mögliche Struktur von `Battle.txt` unter `[BattleInfo]`, `[Stats]` und `[BattleOrder]` als vorläufigen Entwurf dokumentiert. Datenformat und technische Umsetzung bleiben offen.



### 2026-10-26 – Kampfende bei Flucht des letzten Spielers präzisiert

- Die Nutzerentscheidung festgehalten, dass die Flucht des letzten verbliebenen Spielers den Kampf vollständig beendet.
- Festgelegt, dass dabei das Monster aus der Zugreihenfolge entfernt und sämtliche aktiven Kampfdaten für Spieler und Monster verworfen werden; dauerhafte Accounts und gespeicherte Spielerdaten bleiben erhalten.
- Klargestellt, dass Flucht keine Belohnung oder sonstige Zusatzeffekte auslöst, da ein Belohnungssystem nicht zum Grundgerüst gehört.


### 2026-10-26 – Fluchtbefehl und Spielerzählung dokumentieren

- Festgehalten, dass `!flee` den aufrufenden Spieler aus dem Kampf und der Zugreihenfolge entfernt.
- `NumberOfPlayers` in `Battle.txt` wird bei jeder Flucht um eins verringert.
- Der Kampf läuft weiter, solange nach der Flucht mindestens ein Spieler verbleibt; flieht der letzte Spieler, endet der Kampf.
- Den vorgesehenen Helfer `$players_in_battle` ergänzt, der den Zählwert mit `$readini` aus `[Battle]` liest und zurückgibt. Die Implementierungsdetails bleiben offen.

### 2026-10-26 – Kampfende bei Niederlage aller Spieler festhalten

- Die Nutzerentscheidung dokumentiert, dass der Kampf endet, sobald alle teilnehmenden Spieler besiegt sind.
- Ausdrücklich klargestellt, dass die Regel auch für einen Kampf mit nur einem teilnehmenden Spieler gilt.
- Für das Kampfende werden das Monster aus der Zugreihenfolge entfernt und die laufenden Kampfdaten verworfen; dauerhafte Accounts und Spielerdaten bleiben erhalten.
- Für Version 1 sind keine zusätzlichen Folgen oder Belohnungsmechaniken vorgesehen.

### 2026-10-26 – Einfaches Kampfende bei Monstersieg festhalten

- Die Nutzerentscheidung dokumentiert, dass ein besiegtes Monster in Version 1 zum unmittelbaren Ende des Kampfes führt.
- Festgehalten, dass das Monster aus der Zugreihenfolge entfernt und die laufenden Kampfdaten verworfen werden, während dauerhafte Spielerdaten erhalten bleiben.
- Belohnungen, Events, Monsterfähigkeiten, zusätzliche Monsterattribute und weitere Erweiterungen ausdrücklich auf spätere Ausbaustufen verschoben; sie sind nicht verworfen.
- Den Fokus der ersten Version auf ein funktionierendes technisches Kampfgrundgerüst bekräftigt.

### 2026-10-26 – Monster und Kampfdaten bei abgebrochenem Kampf verwerfen

- Die Nutzerentscheidung dokumentiert, dass bei einem durch Verbindungsabbruch beendeten Kampf der gesamte Kampf für Spieler und Monster endet.
- Festgehalten, dass das Monster aus der Zugreihenfolge entfernt und die laufenden Kampfdaten verworfen werden.
- Klargestellt, dass bei einem späteren Kampf ein neues Monster erzeugt wird und dauerhafte Accounts sowie gespeicherte Spielerdaten erhalten bleiben.
- Die konkrete technische Speicherung und Bereinigung der Kampfdaten ausdrücklich offen gelassen.

### 2026-10-26 – Kampfende bei Verbindungsabbruch eines Teilnehmers festgelegt

- Die Nutzerentscheidung dokumentiert, dass ein laufender Kampf vollständig beendet wird, wenn ein teilnehmender Spieler die IRC-Verbindung verliert.
- Festgehalten, dass beim Verbindungsabbruch die vorübergehenden Bot-Zugriffsrechte entfernt werden, während Account und gespeicherte Spielerdaten bestehen bleiben.
- Klargestellt, dass der Kampf nicht ohne den getrennten Spieler fortgesetzt wird und nach erneuter Verbindung eine neue Anmeldung beim Bot erforderlich ist.

### 2026-10-26 – Erneute Anmeldung nach Verbindungsabbruch festgelegt

- Die Nutzerentscheidung dokumentiert, dass Spieler nach einer IRC-Trennung und erneuten Verbindung erneut `!ID passwort` eingeben müssen.
- Festgehalten, dass beim `ON QUIT`-Ereignis die vorübergehenden Bot-Zugriffsrechte entfernt werden sollen, während Account- und Spielerdaten erhalten bleiben.
- Den mIRC-Befehl `/ruser` anhand der mIRC-Hilfe als Befehl zum Entfernen eines Nutzers bzw. von Zugriffsleveln identifiziert; genaue Verwendung im BattleDome-Skript bleibt bis zur Implementierung zu prüfen.

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




### 2026-10-26 – Nachschubmechanik als typunabhängigen Auslöser präzisiert

- Die vorherige Beschreibung korrigiert: Die Nachschubmechanik ist weder an den Tod eines Monsters noch an einen bestimmten Monstertyp oder eine besondere Monster-Eigenschaft gebunden.
- Als mögliche Beispiele festgehalten: Nachschub kann während eines Angriffs auf ein noch lebendes Monster, nach dem Besiegen eines Monsters oder während einer Aktion eines weiterhin lebenden Monsters ausgelöst werden; auch Abläufe mit Double Turn können dazu führen.
- Die Schutzregel präzisiert: Vor jedem tatsächlichen Hinzufügen eines Monsters muss unabhängig vom Auslöser geprüft werden, ob die Obergrenze gleichzeitig lebender/aktiver Monster eingehalten werden kann. Ist kein Platz frei, wird kein Monster hinzugefügt.
- Version 1 bleibt unverändert. Entscheider: Nutzer. Datum: 2026-10-26.

### 2026-10-26 – Zufälligen Monster-Nachschub und maximale Monsterzahl vorgemerkt
- Präzisiert, dass `Max Numbers of Monsters` die maximale Zahl gleichzeitig lebender/aktiver Monster begrenzen soll, nicht die Gesamtzahl aller Monster über die gesamte Kampfdauer.
- Festgehalten, dass besiegte Monster aus dem aktiven Kampf entfernt werden und keinen Platz mehr belegen; vor jedem Spawn muss das Limit geprüft werden, damit es niemals überschritten wird.
- Festgehalten, dass ein tatsächlich erscheinendes neues Monster den Kampf fortsetzt und in die laufende Zugreihenfolge aufgenommen wird.
- Einen offenen Widerspruch zum Spawn-Zeitpunkt dokumentiert: vollständiger Abschluss der Zugreihenfolge und letztes Monster besiegt versus Spawn direkt nach einem einzelnen Monster-Kill, während andere Monster noch leben.
- Die Spawn-Zeitpunktfrage aktualisiert: Methode A wurde vom Nutzer bestätigt – Nachschub kann direkt nach dem Besiegen eines einzelnen Monsters geprüft werden, auch wenn weitere Monster noch leben.
- Ergänzt, dass Nachschub nicht vom Tod oder Typ eines Monsters abhängig ist und auch während eines Angriffs beziehungsweise während ein Monster noch lebt ausgelöst werden kann.
- Die geplante Eigenschaft **Verteidiger-Monster** ergänzt: Solche Monster führen keinen aktiven Zug aus; ihre reguläre Gelegenheit wird übersprungen. Auch bei ihnen kann Nachschub ausgelöst werden.
- Festgehalten, dass `Max Numbers of Monsters` vor jedem Spawn unabhängig vom Auslöser geprüft werden muss, damit die Obergrenze lebender/aktiver Monster niemals überschritten wird.
- Offen gelassen, ob die vorläufigen 10 % für alle Auslöser gelten, sowie die genauen Auslösebedingungen und der Eigenschaftsname.

- Die geplante spätere Mechanik dokumentiert, nach vollständigem Abschluss der aktuellen Zugreihenfolge und dem Besiegen des letzten Monsters der bisherigen Kampfsituation zufällig ein weiteres Monster erscheinen lassen zu können.
- Festgehalten, dass ein neu erscheinendes Monster den Kampf fortsetzt und die Mechanik auch bei ursprünglich einem oder zwei Monstern greifen kann.
- 10 % als vorläufigen Wahrscheinlichkeitsrichtwert aufgenommen, nicht als endgültig festgelegte Chance.
- Den vorläufigen Konfigurationsnamen `Max Numbers of Monsters` für die maximale Monsterzahl eines Kampfes dokumentiert; genaue Zählweise, Speicherort und endgültiger Schlüsselname bleiben offen.
- Klargestellt, dass die Mechanik für spätere Versionen vorgesehen ist und Version 1 nicht verändert.

### 2026-10-26 – Allgemeine Kampfendregel bei beseitigten Monsterzielen festgelegt

- Die Nutzerentscheidung dokumentiert, dass der Kampf sofort endet, sobald alle feindlichen Monster beziehungsweise gültigen feindlichen Monsterziele beseitigt sind.
- Festgehalten, dass diese Regel unabhängig von den Bedingungen gilt, unter denen die Monster besiegt wurden, und nicht nur Double Turn betrifft.
- Klargestellt, dass nach dem Beseitigen aller feindlichen Ziele keine weiteren Monsterangriffe, Gegenangriffe oder regulären Monsterzüge ausgeführt werden.

### 2026-10-26 – Reihenfolge und gültige Ziele bei Double Turn festgelegt

- Den vom Nutzer beschriebenen Ablauf dokumentiert: Wenn Double Turn bei einem Spielerangriff ausgelöst wird, greift derselbe Spieler sofort erneut an, bevor das Monster seinen Gegenzug ausführen darf.
- Festgehalten, dass Double Turn innerhalb des laufenden Spielerangriffs abgewickelt wird und kein eigener Zug in der regulären Zugreihenfolge ist.
- Den Umgang mit besiegten Monstern unterschieden: Ist das einzige Monster nach dem ersten Angriff besiegt, endet der Kampf unmittelbar und der Zusatzangriff entfällt. Sind mehrere Monster beteiligt und leben weitere Monster, kann der Zusatzangriff gegen ein anderes gültiges Monsterziel erfolgen.
- Das Beispiel mit Spieler A, Monster A und Spieler B als Ablaufbeispiel ergänzt. Die Regel gilt für spätere Versionen; Version 1 bleibt unverändert.

### 2026-10-26 – Zugkosten, spätere Zusatzaktionen und Double Turn unterschieden

- Den Nutzerhinweis ergänzt, dass die Aktivierung von Skills, Waffenmechaniken, Techniken, Gegenständen und vergleichbaren Aktionen grundsätzlich einen Zugpunkt kostet.
- Festgehalten, dass ein Skill für zwei Aktionen pro Runde nicht sofort einen Zusatzangriff auslöst: Seine zusätzliche Aktionsmöglichkeit greift erst bei einer späteren regulären Gelegenheit innerhalb der Zugreihenfolge.
- Die interne Spielmechanik **Double Turn** klar davon getrennt: Wenn sie ausgelöst wird, soll sie unmittelbar einen weiteren Angriff ermöglichen und ist kein aktivierter Skill.
- Festgehalten, dass noch offen ist, ob Double Turn zufällig oder nach anderen Bedingungen ausgelöst wird; Auslösebedingungen und Wahrscheinlichkeiten sind nicht festgelegt.
- Die konkreten Regeln bleiben späteren Versionen vorbehalten; Version 1 wird dadurch nicht geändert.

### 2026-10-26 – Zentrale Zugverarbeitung durch `$next_turn` und Monsterdatei als Endprodukt-Vorlage festgehalten

- Korrigiert und präzisiert, dass `$next_turn` für die Verarbeitung des nächsten Zuges allgemein zuständig ist und nicht ausschließlich Monsterzüge behandelt.
- Festgehalten, dass `$next_turn` relevante Kampfbedingungen prüft und weitere spezialisierte Helfer aufrufen kann; deren genaue Anzahl und Zuständigkeiten bleiben offen.
- Die Rolle von `Battle.txt` als Speicher grundlegender Kampfinformationen von der eigentlichen Zugverarbeitung abgegrenzt.
- Die vom Nutzer bereitgestellte `neues_monster.char` als Vorlage für die Monsterdatei des späteren Endprodukts dokumentiert, nicht für den Prototypen.
- Festgehalten, dass Monsterdaten und Statuszustände später im passenden Zugablauf ausgewertet werden sollen, ohne die vollständige Statusmechanik jetzt vorwegzunehmen.
- Präzisiert, dass Gegenreaktionen nicht allein von positivem Schaden abhängen: Ein Angriff kann auch bei 0 Schaden eine Reaktion auslösen; Statuszustände und andere Kampfbedingungen können die tatsächliche Handlung weiterhin verhindern.
