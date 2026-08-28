# Änderungen

## 28.08.2026 – Anpassung an die neue Airtable-Struktur

Anlass: Der Content-Betrieb wurde in der Base „changeXperten Content" (`appb7eOfe2Au3Lp40`) neu aufgebaut. Der Skill zeigte an mehreren Stellen noch auf Tabellen und Felder, die es so nicht mehr gibt.

**Korrigiert**

- **Vorfall-Speicher.** Phase 0 verwies auf eine Tabelle „Vorfälle". Die gibt es nicht (mehr). Der Vorfall-Speicher ist **„01 Themenspeicher"** (`tbl2dxL3ot78QpLqC`). Die Auswahllogik ist jetzt ausgeschrieben: Status „Freigegeben"/„Beantwortet", Vertraulichkeit ≠ „Gesperrt", Priorität „A – sofort" zuerst, dann Reifegrad „Postreif" vor „Angereichert", dann niedrigster Nutzungszähler. Themen mit Reifegrad „Rohmaterial" werden nicht produziert – dort werden Fragen als Record-Kommentar hinterlassen und der Status auf „Fragen offen" gesetzt. Gleiche Korrektur in `references/interview-fragen.md`.
- **Bildindex.** Das Zielfeld „Bildvorschläge LinkedIn" lag laut Skill in „Content-Research" mit einer Feld-ID, die nicht mehr stimmt. Richtig ist Tabelle **„03 LinkedIn-Posts"** (`tblNfTJDJjCia6a1I`), Feld `fldGzdiY66nuC4ojk`. „Content-Research" ist jetzt „90 Archiv – Content-Research (bis 08/2026)" und nur noch Leseablage.
- **Zähler-Buchung.** Der Skill schrieb, den Nutzungszähler fasse ausschließlich das Make-Szenario „Content-Publishing" (9521520) an. Das ist falsch: Dieses Szenario bedient nur Webflow. Den LinkedIn-Bildzähler bucht die geplante Aufgabe **„Content C: Tägliche Feedback- und Finalisierungsrunde"** – genau dann, wenn ein Bild für den finalen Post gebucht wird. Nicht gewählte Kandidaten werden aus dem Vorschlagsfeld entfernt und sind sofort wieder verfügbar; das gewählte Bild wird in „Gewähltes Bild" (`fldDQuzQTkq5najKd`) verlinkt.
- **Kategorie-Mapping.** Die alten Labels stehen nur noch im Archiv und in Feldern mit dem Präfix `zzz Archiv –`. Für neue Zeilen gilt „LinkedIn-Format" plus „Post-Typ" am Thema.
- **Schreibweise.** „Christoph Gretel" → „Christoph Gredel" (Frontmatter und Referenzdatei).

**Geändert**

- **Frequenz.** Bisher stand „2 Posts pro Woche, Montag und Mittwoch". Christophs Betriebsziel ist **12 Posts pro Monat** (ca. 3 pro Woche); darauf rechnet die Produktionsaufgabe. Die Benchmark-Einordnung bleibt erhalten, aber als Bedingung formuliert: Drei pro Woche tragen nur mit echter Nachbereitung – lieber 9 begleitete als 12 unbegleitete Posts, und das dann offen berichten.
- **Publishing.** LinkedIn hängt an keinem Make-Szenario. Gepostet wird manuell nach dem Feld „Zieldatum".

**Neu**

- Abschnitt **„Airtable-Anbindung und automatisierter Betrieb"** vor dem Workflow: Tabellenübersicht mit IDs, vollständige Feldzuordnung in „03 LinkedIn-Posts", Statuskette, die Regel „nie über Entwurf (P2) hinaus", der Sonderfall Fragenkatalog-Altzeile, wer wann läuft – und die Gate-Logik: Jede geplante Aufgabe zählt zuerst den Bestand im Zielmonat und endet still, wenn nichts zu tun ist. Für die Arbeit im Chat ändert sich dadurch nichts.
- Hinweis auf den Reporting-Rückkanal („10 KPI-Monatswerte", „13 Landingpage-Performance"), relevant für Recycling-Entscheidungen.

**Unverändert**

Alle inhaltlichen Regeln: sechs Templates, Hook-Frameworks, Lackmustest, krumme Zahlen, Artefakt-Frage, Humanizer, Soft-Sell-Regel, Bild-Persona und sämtliche Referenzdateien zu Benchmark, Hooks, Beispielposts, Algorithmus und Leser-Resonanz.
