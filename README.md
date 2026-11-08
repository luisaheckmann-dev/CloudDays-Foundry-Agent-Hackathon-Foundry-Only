# Cloud Days: AI Agents mit Microsoft Foundry - nur im Browser

**Zweite Workshop-Version | 210 Minuten | Deutsch | Stand: 08.11.2026**

Baue einen Contoso-OrderOps-Agenten direkt im **neuen Foundry-Portal**:
Dokumente durchsuchen, aktuelle Regeln erkennen, synthetischen Bestand
einordnen, Empfehlungen begruenden und falsche Aussagen systematisch testen.

**Auf Teilnehmergeraeten sind kein Azure CLI, VS Code, Python, Git, Terminal
oder Paketinstallation erforderlich.** Du brauchst einen aktuellen Browser,
Internetzugang, dein zugeteiltes Workshop-Konto und ein vorbereitetes Projekt.
Die Anleitung kannst du direkt auf GitHub lesen. Dateien lassen sich mit dem
Browser herunterladen; alternativ stellt die Lehrperson die Wissensbasis bereit.

## Zuerst lesen

| Was du brauchst | Hier starten |
|---|---|
| Alle kleinen Einzelschritte | [Portal-Leitfaden](docs/PORTAL-GUIDE.md) |
| Ablauf mit Zeitangaben | [210-Minuten-Agenda](docs/AGENDA.md) |
| Vorbereitung, Konten und Freigaben | [Lehrenden-Runbook](docs/INSTRUCTOR.md) |
| Testfragen, Sollantworten und Bewertung | [Evaluation](docs/EVALUATION.md) |
| Login, Rechte, Modell oder Suche funktionieren nicht | [Fehlerhilfe](docs/TROUBLESHOOTING.md) |

**Schnellstart:** Bei `https://ai.azure.com` anmelden, das zugeteilte Projekt
waehlen, unter **Build > Agents** einen **Prompt Agent** erstellen und das
vorbereitete Modell waehlen. Danach mit [Lab 1](docs/PORTAL-GUIDE.md#lab-1-agent-ohne-wissen)
beginnen. Keinen neuen Foundry-Account oder ein neues Modell bereitstellen.

## Was laeuft wo?

| Baustein | Ausfuehrungsort |
|---|---|
| Instructions, Agentversionen, Modellantwort | Microsoft Foundry |
| Dokumentindex und File Search | Verwaltete Foundry-/Azure-Dienste des vorbereiteten Setups |
| Bedienung, Prompts, Quellenkontrolle | Browser |
| Bestand | Statisches synthetisches Dokument, **kein** Echtzeit-ERP |
| Empfehlung | Modellantwort, **keine** gespeicherte oder ausgefuehrte Bestellung |
| Testbewertung | Manuelle Rubrik; automatische Evaluatoren sind nicht Pflicht |

**Dieses Repository hostet nicht den Python-Code des Originalworkshops.**
Es ist ein eigenstaendiger Portal-Lernpfad. Das Hochladen einer Python-Datei
in eine Wissensbasis macht daraus keine laufende Anwendung.

## Unterschied zur Code-Version

Die [Originalversion](https://github.com/luisaheckmann-dev/CloudDays-Foundry-Agent-Hackathon)
bleibt der Lernpfad fuer Python, SDKs, Function Calling, lokale Validierung
und ein technisch erzwungenes Freigabegate.

| Lernziel | Foundry-Only-Version |
|---|---|
| Agent im Portal erstellen und verbessern | Enthalten |
| Aktuelle und archivierte Quellen unterscheiden | Enthalten |
| Echte Retrieval-Belege statt erfundener Quellen | Enthalten |
| Bestandsregeln und fehlende Fakten erkennen | Enthalten, dokumentgestuetzt |
| Gegenbeispiele und eingebettete Angriffe testen | Enthalten |
| Python-Funktion implementieren/debuggen | Nicht enthalten |
| Function-Call-Schleife und deterministischer Backendcheck | Nicht enthalten |
| SQLite, Freigabetransaktion oder echte Bestellung | Nicht enthalten |
| Foundry IQ, MCP, Hosted Agent oder Copilot harness | Nicht Pflichtbestandteil |

Die Frage "Darf ich eine Empfehlung abgeben?" laesst sich hier diskutieren.
Eine Chatbestaetigung ist aber **kein** technisches Freigabegate. Selbst ein
guter Prompt ist keine verlaessliche serverseitige Geschaeftsvalidierung.

## Dateien fuer den Workshop

| Datei | Zweck |
|---|---|
| [Aktuelle Portal-Richtlinie](assets/order-policy-portal-2026-11.txt) | Aktuelle Mengen-, Sperr- und Empfehlungsregeln |
| [Archiv-Richtlinie](assets/order-policy-archive-2025.txt) | Bewusst ungueltige Gegenquelle |
| [Bestandssnapshot](assets/inventory-snapshot-2026-11.txt) | Vier synthetische Produkte |
| [Lieferhinweise](assets/delivery-notes-2026-11.txt) | Bewusst nicht vorhandene Lieferzusagen |
| [Angriffsdokument](assets/untrusted-note.txt) | Optionaler, gekennzeichneter Sicherheitstest |
| [Starter-Instructions](prompts/01-starter.txt) | Eigene Regeln entwickeln |
| [Referenz-Instructions](prompts/02-reference.txt) | Vergleich, keine Erfolgsgarantie |
| [Kopierbare Testfragen](prompts/03-test-questions.txt) | Zehn reproduzierbare Szenarien |

Alle Inhalte sind **fiktiv und synthetisch**. Keine Kundendaten, Kennwoerter,
API-Keys, Tenant-IDs, persoenlichen Mailadressen oder privaten Endpoints sind
Bestandteil dieses Pakets.

## Vorbereitung und Abnahme

Die Lehrperson stellt die Projekte, das Modell, Teilnehmerrollen und
Wissensquellen **vor** dem Workshop bereit. Foundry User am richtigen Projekt
ist die Ausgangsbasis; fehlende Upload-/Storage- oder Portalrechte werden
gezielt untersucht, nicht durch pauschale Adminrechte ersetzt.

**Materialversion, kein bereits bewiesener Teilnehmer-Cloudlauf.** Die
Abnahme-Checkliste im [Runbook](docs/INSTRUCTOR.md#freigabecheck-vor-dem-workshop)
muss mit einem echten eingeschraenkten Teilnehmerkonto erfuellt werden.
Ein vorbereiteter Account oder ein erfolgreicher Admin-Chat reicht nicht.
Auch die Verfuegbarkeit der beschriebenen Portalaktionen muss im eigenen
Tenant geprueft werden; UI-Bezeichnungen und Rollouts koennen abweichen.

Bestehende freigegebene Foundry-Projekte und Modelle koennen wiederverwendet
werden. Dieses Paket erstellt keine Azure-Ressourcen, vergibt keine Rollen
und veraendert keine vorhandenen Agenten automatisch.

**Kosten:** Modellantworten, File Search und gegebenenfalls automatische
Playground-Evaluatoren verursachen Azureverbrauch. Browser-only bedeutet
nicht kostenlos. Keine Websuche oder zusaetzlichen Tools im Pflichtpfad.

Lizenz und Herkunft: [MIT](LICENSE), abgeleitet aus dem verlinkten
Contoso-OrderOps-Originalworkshop. Offizielle technische Quellen stehen im
[Lehrenden-Runbook](docs/INSTRUCTOR.md#offizielle-quellen).
