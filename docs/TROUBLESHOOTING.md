# Fehlerhilfe - ohne Installationen und ohne riskante Abkuerzungen

[Start](../README.md) | [Leitfaden](PORTAL-GUIDE.md) | [Lehrperson](INSTRUCTOR.md)

| Symptom | Jetzt tun | Nicht tun |
|---|---|---|
| Nur Foundry-Produktseite | **Sign in** waehlen und Workshop-Konto verwenden | Dev Pack, CLI oder VS Code installieren, nur weil die Landingpage sie zeigt |
| Falsches Konto/Verzeichnis | Eigenes Browserprofil/InPrivate und genaue Zuteilung pruefen | Gleichen Anzeigenamen "Contoso" als Nachweis nehmen |
| Kennwortwechsel/MFA blockiert | Lehrperson mit konkreter Meldung kontaktieren; Zugang privat klaeren | Kennwort oder MFA-Code im Gruppenchat posten |
| Projekt fehlt | Zugewiesene Nummer und Projektrolle durch Lehrperson pruefen lassen | Neues Projekt erstellen oder fremdes Konto teilen |
| Agent erstellen fehlt | Eigenen vorbereiteten Portalagenten verwenden, wenn zugeteilt | Global Administrator fuer Teilnehmer verlangen |
| Kein Modell waehlbar | Vorhandenes Projekt/Deployment/Rechte pruefen; stoppen | Automatisches neues Modell oder neue Region bestaetigen |
| Portal zeigt classic | Vorgesehenen New-Foundry-Pfad und Projekt pruefen | Classic-Agent als gleichwertigen Nachweis ausgeben |
| File Search nicht angeboten | Vorkonfigurierten eigenen Agenten/Wissensindex mit Lehrperson pruefen | Websuche, unbekannten MCP-Server oder IQ auf Verdacht anhaengen |
| Download/Upload gesperrt | Lehrperson nutzt Vorindexierung; Dateien im Browser lesen | IT-Richtlinien oder TLS umgehen |
| Upload liefert 403 | Tatsaechlichen Daten-/Storagepfad und passende Rechte pruefen lassen | Pauschal Owner/Contributor oder fremde Storage-Rollen vergeben |
| Index noch nicht bereit | Status fuer alle vier Dateien kontrollieren und auf Abschluss warten | Wiederholt gleiche Dateien/Indizes anlegen |
| Antwort nennt 100 als aktuelle Grenze | Neue Unterhaltung, aktuelle Policy/Archivstatus/Anweisungen pruefen | Antwort nachtraeglich als "eigentlich richtig" praesentieren |
| Dateiname, aber kein aufklappbarer Beleg | Quelle/Toolkonfiguration und verfuegbare Retrievaldetails pruefen | Einen technischen Quellenbeleg erfinden |
| Bestand klingt live | Snapshotdatum und Grenze in Instructions/Antwortschema verankern | Statischen Dokumentabruf als ERP-Toolcall bezeichnen |
| Antwort behauptet Bestellung | Als harten Fehler bewerten und Instructions korrigieren | Chat-"Ja" als technisch gespeicherten Auftrag behandeln |
| 429 / Rate limit | Keine neue Anfrage; warten und mit Lehrperson in kleinere Wellen starten | Unbegrenztes Wiederholen oder neue Deployments anlegen |
| Lange Antwort/Timeout | Eine Frage je frischem Chat; begrenzte Antwortlaenge verlangen; Status festhalten | Unfertige Antwort als bestanden zaehlen |
| Zugriff auf fremdes Projekt | Stoppen und Lehrperson informieren; Isolation pruefen lassen | Fremde Dateien ansehen, kopieren oder veraendern |
| Modell/Portal komplett ausgefallen | Synthetische Dokumente und Sollantworten gemeinsam analysieren | Einen nicht ausgefuehrten Cloudtest als erfolgreich markieren |

## Wann stoppen?

Nach fuenf Minuten ohne individuellen Cloudzugang halte den Blocker fest
und beteilige dich an einer Teamdemonstration. Keine Kontoteilung. Die
Lehrperson entscheidet, ob der eigene Versuch spaeter wiederholt wird.
Eine Demo zaehlt nicht als bestandener individueller Login-/Retrieval-Test.

## Keine lokale Entwicklungsumgebung noetig

Buttons wie **Open in VS Code**, **View code**, **Cloud Shell**, **Get SDK**
oder Installationsbefehle gehoeren nicht zum Pflichtpfad. Ein Tab fuer
GitHub-Dokumente und einer fuer den Foundry-Agenten genuegen.

**Ausnahme:** Der Weg mit eigenem Dateiupload benoetigt Browser-Download
und -Upload der Textdateien, aber keine Anwendung oder Paketinstallation.
Wenn auch das nicht erlaubt ist, muss die Lehrperson den Index vorbereiten.

## Portal hat andere Beschriftungen

Suche nach der Funktion, nicht nur nach einem Label: Agentliste,
Instructions, vorhandenes Modell, File Search, Dokumentindex, Testchat
und Quellenansicht. Fehlen Funktion oder Rechte tatsaechlich, benenne die
Grenze. Kein Beispiel-Screenshot ersetzt eine im Tenant verfuegbare Aktion.

## Nach dem Workshop

Browser schliessen ist keine Artefaktloeschung. Loesche keine Ressourcen
auf Verdacht. Eigene Agent-/Indexnamen privat notieren und den
vereinbarten Cleanup mit der Lehrperson durchfuehren.
