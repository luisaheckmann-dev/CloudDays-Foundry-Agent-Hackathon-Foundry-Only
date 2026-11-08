# Runbook fuer die Lehrperson

[Start](../README.md) | [Agenda](AGENDA.md) | [Teilnehmerpfad](PORTAL-GUIDE.md)

## Architektur und Freigabeumfang

Dieser Track verwendet Prompt Agents und File Search im neuen Foundry.
Er fuehrt keine eigenen Python-Funktionen aus. Die Policy wurde deshalb
als **OPS-PORTAL-2026-11** angepasst: Empfehlungen statt lokaler
Bestellentwuerfe mit CLI-Freigabe. Die Original-Policy und ihr Ausfuehrungs-
versprechen nicht ungeaendert in diesen Track uebernehmen.

Vorhandene, bereits freigegebene Foundry-Ressource, Modell und Projekte
koennen genutzt werden. Neue Portalagenten erhalten eigene Namen wie
`orderops-p01-portal`; vorhandene SDK-Agenten und ihre Indizes bleiben
unangetastet. Vorindexierung und Agentanlage sind Azure-Schreibzugriffe
und benoetigen einen expliziten Scope-/Kostenentscheid.

Dieses Repository ist nur das Materialpaket. Es vergibt keine Rollen,
erstellt keine Konten und deployed keine Ressourcen automatisch.

## Vor dem Event vorbereiten

1. Lege den privaten Betriebszettel fest: Tenant, Kontozuordnung,
   Projektnummern, Modell-Deploymentname und Supportkontakt. Diese Werte
   werden nicht in dieses oeffentliche Repository geschrieben.
2. Eine native Workshopidentitaet pro Person verwenden. Firmen-Mailadressen
   sind dafuer technisch nicht erforderlich. Die Kontonummer kann erst
   bei Ankunft einer Person zugeteilt werden.
3. Stelle der Person ihr eigenes initiales Kennwort sicher bereit.
   Ein Windows-verschluesselter Credential-Export der Lehrperson ist kein
   Teilnehmerdownload und auf anderen Rechnern nicht einfach entschluesselbar.
4. Ersten Login, Kennwortwechsel und gegebenenfalls MFA rechtzeitig pruefen.
   Fuer ein Testkonto keine eigene MFA an einen spaeter fremd zugeteilten
   Account binden, ohne vor Uebergabe einen geregelten Reset vorzunehmen.
5. Pruefe **Foundry User am zugeordneten Projekt**. Native Konten allein
   reichen nicht. Entra User Administrator fuer Kontenverwaltung ist eine
   andere Berechtigung als Azure-Projekt-RBAC und nicht Teilnehmerstandard.
6. Pruefe Portalnavigation und Deploymentzugriff mit eingeschraenktem Konto.
   Falls gezielte Leserechte fuer Navigation benoetigt werden, Scope und
   Folgen gesondert bewerten. Nicht pauschal Owner/Contributor auf der
   Subscription oder Foundry User auf der gesamten Ressource vergeben.
7. Nutze das freigegebene vorhandene Modell, z. B. `orderops-model`.
   Modell- und Regionsunterstuetzung fuer File Search separat kontrollieren.
   Keine automatische Bereitstellung eines anderen Modells akzeptieren.
8. Pruefe Unternehmensnetz: Anmeldung, `ai.azure.com`, Modell-/Agentzugriff
   und GitHub sind erreichbar. Datei-Download, Upload und Zwischenablage
   koennen separat gesperrt sein. Browser-only hebt IT-Richtlinien nicht auf.
9. Plane die Wissensvorbereitung nach einem der beiden folgenden Wege.

## Weg A: Teilnehmer laden Dateien im Portal

Nur verwenden, wenn der aktuelle Portal-Rollout und die Teilnehmerrechte
den gesamten Upload-/Index-/Anhaengepfad erlauben. Vorher mit einem echten
Teilnehmeraccount testen. Alle vier Core-Dateien sind kleine UTF-8-Texte.

Die offiziellen File-Search-Voraussetzungen nennen Storage Blob Data
Contributor fuer Uploads in den eigenen Projektstorage. Das konkrete
Basic-/Managed-Storage-Setup kann sich davon unterscheiden. Keine fremde
Storage-Ressource auf Verdacht freigeben; den tatsaechlichen Pfad pruefen.

Dieser Weg benoetigt keine lokale Installation, aber Browserdatei-Download
und Browserupload. Ein `.py`-Upload waere nur Dokumentinhalt, kein Codehosting.

## Weg B: Lehrperson bereitet Wissen vor

**Empfohlen fuer restriktive Kundengeraete.**

1. Oeffne jedes vorhandene Teilnehmerprojekt mit berechtigtem Konto.
2. Erzeuge einen eindeutig diesem Track zugeordneten Dokumentindex, z. B.
   `orderops-p01-knowledge`, und lade die vier Core-Dateien aus `assets/` hoch.
3. Warte auf vollstaendige Indexierung aller vier Dateien.
   Pruefe die Ablauffrist des Indexes und seine Bereitschaft kurz vor dem
   Event erneut. Ein frueherer erfolgreicher Upload ist keine Garantie,
   dass der Index am Workshoptag noch verfuegbar ist.
4. Konfiguriere File Search mit genau diesem Index. Nur Quellen desselben
   zugeordneten Projekts verwenden. Keine tenantweiten Freigaben voraussetzen.
5. Wenn Teilnehmer im Portal vorhandene Indizes auswaehlen koennen, lass
   sie in Lab 1 ihren eigenen Agenten erstellen und in Lab 2 verbinden.
6. Wenn das Portal die Anhaengeaktion nicht bietet, lege einen **separaten**
   Portalagenten mit Starter-Instructions und vorbereitetem File Search an.
   Die Teilnehmer bearbeiten diesen Agenten im eigenen Projekt.
7. Fuer Lab 1/File-Search-Baseline kann die Lehrperson einen zweiten
   ungrounded Agenten vorkonfigurieren. Den Coreindex dafuer nicht loeschen.
   Ist weder eigener Agentbau noch Zugriff auf vorbereitete Agenten
   moeglich, ist die individuelle Portalabnahme blockiert.
8. Optional die Agentanlage durch die Lehrperson automatisieren; das ist
   kein Teilnehmerbedarf und kein Bestandteil dieses Repositorypakets.
   Ein SDK-erstellter Prompt Agent muss im aktuellen Portal editierbar und
   testbar sein, bevor er als Vorbereitungsweg eingesetzt wird.
9. Pruefe das Ergebnis mit dem echten eingeschraenkten Teilnehmerkonto,
   nicht nur mit Instructor-/Adminrechten.

## Freigabecheck vor dem Workshop

Nutze zunaechst ein eindeutig reserviertes Testkonto und danach eine
Anmelde-/Zugangspruefung fuer jede Zuteilung.

| Pruefung | Muss-Ergebnis |
|---|---|
| Konto und Verzeichnis | Genau die zugeteilte native Workshopidentitaet |
| Erstlogin | Kennwortwechsel/MFA moeglich, kein unerledigter Kontoblocker |
| Projekt | Eigenes vorhandenes Projekt erreichbar |
| Agent | Erstellen oder vorbereiteten eigenen Portalagenten bearbeiten |
| Modell | Vorhandenes Deployment nutzbar; keine neue Bereitstellung |
| Vier Core-Dateien | Vollstaendig indexiert und dem Agenten zugeordnet |
| E01 | Richtige aktuelle Grenze und passende aufklappbare Quelle |
| E03/E06/E07 | Bestand, Sperre und aktuelle Policy korrekt eingeordnet |
| E05/E09 | Keine behauptete Bestellung und keine Liefergarantie |
| Isolation | Kein Zugriff auf Agenten/Dateien eines fremden Teilnehmerprojekts |
| Sicherheit | Keine aktive Websuche oder unbekannten Tools |
| Konfiguration | Eigene Portalagenten, Original-SDK-Agenten unveraendert |
| Kosten | Freigegebenes Deployment, Kontingent und Beobachtung eingerichtet |

**Status hier bewusst: Teilnehmer-Liveabnahme NOT_RUN.** Nach eigener
Durchfuehrung privat Konto, Zeitpunkt, Agentstand, Resultat und Blocker
festhalten. Dieses Materialpaket behauptet keinen erfolgreichen Kundenlauf.

Wenn die Quellenmarkierung nur einen Dateinamen zeigt, aber kein Treffer
aufklappbar ist, pruefe verfuegbare Retrieval-/Traceinformationen. Fehlt
jeder technische Beleg, ist der Quellencheckpoint nicht bestanden.

## Durchfuehrung ohne Installationen

Teile pro Person privat Login, Startkennwort, Projektnummer und die
vorbereitete Agent-/Wissensbasis-Zuordnung aus. Keine Geheimnisse auf Folien,
GitHub oder im Gruppenchat. Teilnehmer brauchen keine `.env` und keine Keys.

Starte Testfragen in Wellen, z. B. zehn Teilnehmer nacheinander statt alle
30 gleichzeitig. Jeder wartet auf den Abschluss einer Antwort. Diese
Wellen sind eine organisatorische Startstrategie, keine garantierte
Quota- oder Kapazitaetsberechnung. Tatsaechliche TPM/RPM und 429 beobachten.

Automatische Playground-Evaluatoren koennen standardmaessig aktiviert und
kostenpflichtig sein. Wenn im Portal Metriken/Evaluatoren angeboten werden,
fuer den Pflichtpfad alle automatischen Evaluatoren abwaehlen. Die Rubrik
ist manuell. Kein Application Insights, Search-Service, Remote-Backend,
Hosted Compute oder Code Interpreter ist Pflichtneuaufbau dieses Tracks.

Die Demo zeigt drei Kontraste: keine Quellen vs. Retrieval, Archiv vs.
aktuelle Policy und Empfehlung vs. behauptete Bestellung. Zahlen aus dem
Snapshot nicht als "gerade im ERP abgefragt" praesentieren.

## Wenn etwas ausfaellt

Bei einzelnen Kontoblockern kann die Person an einer Teamdemonstration
teilnehmen. Nicht das Kennwort eines anderen Teilnehmers weitergeben.
Bei gesperrtem Upload nutze Weg B. Bei fehlendem File Search ist ein
Kontext-Paste eine klar markierte Promptuebung ohne Retrieval-Abnahme.
Bei Portal-/Modellausfall nutze die Dokumente und Rubrik zur gemeinsamen
Sollantwortanalyse. Das ist kein ausgefuehrter Cloud-Workshop.

## Optionales bewusst getrennt halten

Code Interpreter kann in einem verwalteten Sandboxkontext Berechnungen
ausfuehren, hostet aber nicht automatisch die Originalanwendung. Er verursacht
zusaetzliche Kosten und ist nicht fuer das Pflichtlernen erforderlich.

Ein remote MCP-/OpenAPI-Backend koennte echte deterministische
Geschaeftsfunktionen ergaenzen; es laeuft dann nicht allein in Foundry.
Ein Hosted Agent koennte angepassten Anwendungscode ausfuehren, benoetigt
aber gesonderte Bereitstellung, Berechtigungen und Protokollanpassung.
Copilot harness und visual Workflow sind keine stillen Ersatzpfade.
Der Workflow-Designer ist laut aktueller Dokumentation zur Einstellung
am 01.12.2026 vorgesehen; diesen Workshop nicht darauf aufbauen.

## Abschluss und Betrieb

Privat Agentnamen, eigene Indizes und entstandene Kosten festhalten.
Eigene Artefakte nur gezielt nach Cleanup-Freigabe entfernen. Keine
bestehenden Projekte, Modellbereitstellungen oder fremden Inhalte loeschen.
Ein Budget ist eine Warnung, kein hartes Limit. Schliessen des Browsers
beendet keine Azure-Ressourcen.

Nach dem Event die Workshopkonten, MFA-Zuordnungen und Rolle/Projektzugriffe
nach dem vereinbarten Lebenszyklus deaktivieren oder entfernen lassen.
Nicht automatisch oder ausserhalb des freigegebenen Umfangs handeln.

## Offizielle Quellen

Alle Links wurden fuer den Materialstand 08.11.2026 herangezogen;
Service-Rollouts und Dokumentation koennen sich weiterentwickeln.

| Thema | Quelle |
|---|---|
| Prompt Agents; Portal braucht keine Installation | [Prompt-Agent-Quickstart](https://learn.microsoft.com/en-us/azure/foundry/agents/quickstarts/prompt-agent) |
| Playground, Quellen und kostenpflichtige Evaluatoren | [Foundry Playgrounds](https://learn.microsoft.com/en-us/azure/foundry/concepts/concept-playgrounds) |
| File Search, Indexierung, Basic-/Standard-Setup | [File Search](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/file-search) |
| Foundry User und projektspezifische Rechte | [Foundry RBAC](https://learn.microsoft.com/en-us/azure/foundry/concepts/rbac-foundry) |
| Modelle, Regionen, Quota | [Limits and regions](https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/limits-quotas-regions) |
| FunctionTool fordert Client-Ausfuehrung an | [Function Calling](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/function-calling) |
| Code-Interpreter-Sandbox | [Code Interpreter](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/code-interpreter) |
| Eigenen Code hosten ist ein anderer Pfad | [Hosted Agent code deployment](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/deploy-hosted-agent-code) |
| Lebenszyklus visual Workflows | [Workflows](https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/workflow) |
| Modelle, Tools und Hostingkosten | [Foundry Agent Service pricing](https://azure.microsoft.com/en-us/pricing/details/foundry-agent-service/) |
