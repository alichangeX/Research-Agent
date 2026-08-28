# Änderungen

## 28.08.2026 – Eigene Tabelle, fertige Grafik

Anlass: Newsletter und Blog lagen bisher in einer gemeinsamen Airtable-Zeile („Blog & Newsletter"). Daraus kamen mehrere Sonderfälle, die der Skill mühsam abfangen musste. Die Tabellen sind jetzt getrennt.

**Korrigiert und neu gefasst**

- **Abschnitt „Airtable-Anbindung".** Komplett neu geschrieben. Die Ausgabe liegt in **„05 Newsletter"** (`tbleTYN8xt28onmIg`) mit eigenem Status, eigenem „Ziel-Monat", eigenem „Versanddatum" und eigenen Grafik-Feldern. Tabellenübersicht mit IDs ergänzt. Ziel: 2 Ausgaben pro Monat, Versand unverändert über Pipedrive.
- **Status-Steuerung.** Die alten Warnungen gelten so nicht mehr:
  - Es gibt im Newsletter **keinen Status „Ausgewählt"**. Der gehört allein zur Blog-Tabelle und ist Christophs Themenfreigabe. Damit entfällt die Überschreibungsgefahr, vor der der Skill gewarnt hat.
  - Die Ausgabe entsteht in der Aufgabe **„Content D"** (täglich, mit Gate) mit Status „Entwurf (P2)".
  - Christoph kommentiert an der Newsletter-Zeile; ein Kanal-Präfix ist nicht mehr nötig, weil die Zeile nur einen Kanal trägt.
  - **„Content C"** (tägliche Feedback-Runde) schreibt „Finaler Newsletter" und setzt „Finaler Entwurf (P3)".
  - **Newsletter ohne Blogartikel** sind der Normalfall, nicht der Sonderfall. Die frühere Regel „springt erst auf P3, wenn beide Kanäle final sind" ist entfallen.
- **Kernaussage und Beleg.** Verweise auf ein „Quellen-Feld" derselben Zeile zeigen jetzt korrekt auf den verknüpften Datensatz in „02 Studienrecherche" (Feld „Quellen" mit Präfix `Leitquelle:`, Feld „Inhalt" als vollständige Quellenabbildung).
- **Tabellennamen** in `references/bildauswahl.md` und im Abbildungs-Abschnitt auf „07 Blog-Bilder", „08 Grafik-Vorlagen", „06 LinkedIn-Bilder" gezogen.
- **Offener Punkt erledigt.** Der Skill notierte: „Sauberer wäre ein eigenes Feld für die Newsletter-Abbildung." Das gibt es jetzt – „Grafik" (Anhang, `fldfFt570fVF1PaM7`), „Grafik-Befüllung" (`fldSknAC1FAIFfTts`), „Grafik-Vorlage" (`fldI5HYutlet1z7Ji`). Das Textfeld-Provisorium ist gestrichen.

**Neu**

- **Die Grafik wird fertig gebaut, nicht nur beauftragt.** Bisher endete der Prozess beim Auftragstext. Jetzt: passende Vorlage aus „08 Grafik-Vorlagen" wählen (Aussagetyp, „Newsletter-Eignung" = „Gut" bevorzugt, bei Gleichstand niedrigster Nutzungszähler), verlinken, Befüllung dokumentieren, Grafik als SVG im changeXperten-CI bauen, zu PNG rendern und als Anhang in „Grafik" hochladen. Mit den harten Grenzen: Inhalte ausschließlich aus dem Newsletter-Text, keine erfundene Zahl, und die Form darf die Aussage nicht verfälschen. Kein ehrlicher Match → keine Grafik, offen melden.
- **Zähler-Regel** klargestellt: Der Nutzungszähler der Vorlage wird genau einmal pro Ausgabe erhöht, und zwar von der Feedback-Runde bei „Finaler Entwurf (P3)". Wer die Grafik baut, erhöht nichts.

**Unverändert**

Kolumnenformat „der Impuls", Erzählbogen, Kolumnenstimme, Betreff-/Preview-/Titel-Regeln, CTA-Rotation, Angebots-Landkarte, Proof Points, Deliverability-Grenzen, Quellentreue und Kennzahl-Platzhalter, sämtliche Referenzdateien.
