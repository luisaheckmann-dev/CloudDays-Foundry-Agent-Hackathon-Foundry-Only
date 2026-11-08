# 210 Minuten - ein durchgaengiger Browser-Workshop

[Start](../README.md) | [Einzelschritte](PORTAL-GUIDE.md) | [Lehrperson](INSTRUCTOR.md)

**Zielgruppe:** Azure-/KI-Einsteiger mit Browser-Grundkenntnissen. Kein Python,
Terminal oder Machine-Learning-Training erforderlich. Eine Person pro Konto
und Projekt; Diskussionen koennen in Zweier- oder Dreierteams stattfinden.
Keine gemeinsamen Kennwoerter und kein geteiltes Admin-Konto.

| Start | Ende | Minuten | Arbeit und Ergebnis |
|---|---|---:|---|
| 00:00 | 00:20 | 20 | Instructor-Demo: unbelegte Antwort vs. belegte Empfehlung; Grenzen erklaeren |
| 00:20 | 00:35 | 15 | [Lab 0](PORTAL-GUIDE.md#lab-0-anmelden-und-orientieren): Konto, Kennwortwechsel/MFA, Projekt, vorhandenes Modell |
| 00:35 | 01:00 | 25 | [Lab 1](PORTAL-GUIDE.md#lab-1-agent-ohne-wissen): eigener Prompt Agent, Starterregeln, drei Baselinefragen |
| 01:00 | 01:35 | 35 | [Lab 2](PORTAL-GUIDE.md#lab-2-wissen-verbinden): Quellen oeffnen, File Search verbinden, Indexierung und Belege kontrollieren |
| 01:35 | 01:45 | 10 | Pause; keine neuen Requests, kein unbeaufsichtigtes Tool |
| 01:45 | 02:15 | 30 | [Lab 3](PORTAL-GUIDE.md#lab-3-regeln-verbessern): aktuelle/archivierte Policy, Bestand, Sperre, fehlende Fakten |
| 02:15 | 02:40 | 25 | [Lab 4](PORTAL-GUIDE.md#lab-4-manuell-evaluieren): sechs feste Tests, Rubrik, Referenzvergleich |
| 02:40 | 03:20 | 40 | [Lab 5](PORTAL-GUIDE.md#lab-5-team-challenge): messbare Verbesserung, Angriffstest, zwei neue Gegenbeispiele |
| 03:20 | 03:30 | 10 | [Lab 6](PORTAL-GUIDE.md#lab-6-pitch-und-abschluss): Kurzpitch, Grenzen und eigene Artefakte dokumentieren |
| **Summe** | | **210** | **3,5 Stunden inklusive Pause** |

Login und Modellzugang werden moeglichst bereits vor dem Event getestet.
Die 15 Minuten Lab 0 reichen nicht fuer neue Quota, Freigaben oder
Netzwerkausnahmen. Optional koennen registrierte Teilnehmer den ersten Login
und MFA vorher erledigen; persoenliche Mailadressen sind bei separat
zugeteilten Workshop-Konten technisch nicht erforderlich.

## Lernziele

Du kannst einen Prompt Agent erstellen, seine Konfiguration speichern,
eine echte Quelle kontrollieren, widerspruechliche Dokumente einordnen,
eine Bestellempfehlung von einer ausgefuehrten Bestellung unterscheiden
und die Verbesserung anhand derselben Fragen messen.

## Definition of Done

Ein eigenes Agentenartefakt liegt im eigenen Projekt. Vier Quellen sind
indexiert oder von der Lehrperson vorkonfiguriert; mindestens eine Antwort
hat eine aufklappbare, passende Retrieval-Quelle. Die sechs Kerntests E01,
E03, E05, E06, E07 und E09 wurden einzeln in frischen Chats bewertet.
Es gibt keine Behauptung einer Echtzeit-Lagerabfrage, Bestellung oder
technischen Freigabe. [Rubrik und harte Fehler](EVALUATION.md) gelten.

Ein Kontext-Paste ohne File Search oder die Demonstration der Lehrperson
ist **kein** bestandener individueller Cloud-/Retrieval-Nachweis.
Bei einem Blocker wird das in der Abgabe offen markiert.
