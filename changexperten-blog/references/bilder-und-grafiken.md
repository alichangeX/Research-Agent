# Bilder und Grafiken für Blogartikel

Diese Datei ist die einzige Quelle für alles Visuelle am Blogartikel. Sie gilt gleichermaßen für den täglichen Produktionslauf „Content D" (Bildplan, Unsplash-Fotos, Grafik-Aufträge), die tägliche Feedback-Runde „Content C" (finale Auswahl, Abgleich gegen den finalen Text, Zähler-Buchung beim Livegang) und für manuelle Einzelaufträge im Chat.

## 1. Zugriffsgrenze – warum die Architektur so aussieht

Die Routinen laufen automatisiert und können **keine Binärdateien aus SharePoint lesen**. Der Microsoft-365-Connector liefert ausschließlich extrahierten Text; ein JPG ist damit unsichtbar und eine PPTX nicht öffenbar. Alles, was eine Routine für die Bildauswahl braucht, muss deshalb vorher **nach Airtable gespiegelt** sein – dort haben Attachments abrufbare URLs.

Daraus folgen zwei Sync-Strecken, die Make bereitstellt und die nicht Teil dieses Skills sind:

| Strecke | Von | Nach | Frequenz |
|---|---|---|---|
| Bild-Sync | `5_Webseite / Blog / {Cluster} / {Leistung} / {Thema}` und `5_Webseite / Bilder Webseite` | Tabelle `Blog-Bilder`, Feld „Bild" + „SharePoint-ID" + Pfad in „Setting & Kontext" | wöchentlich, inkrementell über SharePoint-ID |
| Vorlagen-Sync | `Marketing 2.0 / 3_Lead Magneten / ThinkCell Templates.pptx` | Tabelle `Grafik-Vorlagen`, Feld „Vorschau" (Folie als PNG) | einmalig, danach bei Änderung der PPTX |

Solange eine Strecke nicht läuft, arbeitet die Routine mit dem, was in Airtable steht, und meldet die Lücke. Sie versucht **nicht**, SharePoint direkt zu lesen.

## 2. Datenquellen und Feld-IDs

Base „ChangeXperten": `appb7eOfe2Au3Lp40`

| Zweck | Tabelle / Feld | ID |
|---|---|---|
| Bildbestand Blog | Tabelle `07 Blog-Bilder` | `tblE7N7W8Z6frJwS1` |
| Vorlagenkatalog | Tabelle `08 Grafik-Vorlagen` | `tbl6nRJ5CfnY9iBNV` |
| Artikelzeile | Tabelle `04 Blog` | `tblzTKBLsewsvoCis` |
| Bildplan (Slot-Tabelle) | Feld „Blog-Bildplan" | `fldxWuw7JZ8iOAiFc` |
| Bildkandidaten | Feld „Bildvorschläge Blog" | `fld3Iccjz37FkGcnV` |
| Befüllungsauftrag | Feld „Grafik-Auftrag" | `fldohribEPD9sdqXD` |
| Gewählte Vorlage | Feld „Grafik-Vorlagen" (Link) | `fldEbkzqGov1ouU9n` |

## 3. Drei Ebenen pro Artikel

| Ebene | Anzahl | Funktion |
|---|---|---|
| 1 – Hero | genau 1 | Above the fold, gleichzeitig OG-/Twitter-Image. Trägt das Thema, keine Textelemente im Bild |
| 2 – Motivfotos | 4–6 | Ein Bild pro H2-Abschnitt, Richtwert 1 Bild pro 300–500 Wörter. Atmosphärisch, ohne Caption |
| 3 – Eigene Grafik | 1–2, mindestens 1 ist Pflicht | Modell, Phasenlogik oder Zahlenkarte aus dem Vorlagenkatalog. Kleiner gesetzt, **mit** Caption in Kursiv |

Ebene 3 ist der Slot mit dem größten Hebel: Sie erhöht die Zitierfähigkeit für GEO/AEO, liefert das social-media-fähige Asset für die LinkedIn-Promotion und ist das einzige Bild, das kein Wettbewerber hat.

## 4. Bildplan – Struktur

Der Bildplan geht in das Feld „Bildplan" und ist eine Zeile pro Slot:

`Slot-Nr | Ebene | Position (nach welcher H2/H3) | Motiv-Briefing | Quelle | Alt-Text | Dateiname | Kandidaten`

Das Motiv-Briefing beschreibt in einem Satz, was zu sehen sein soll und welche Stimmung der Abschnitt braucht. Es ist gleichzeitig Suchanfrage für den Bildindex und, falls es bis zur KI-Stufe kommt, Prompt-Grundlage.

## 5. Quellenlogik für Ebene 1 und 2

Erst zur nächsten Stufe gehen, wenn die vorherige nichts Passendes liefert:

**1. Tabelle `Blog-Bilder`.** Suche mit `search_records` über die Stichworte des Motiv-Briefings. Feldpriorität beim Abgleich: Themen-Assoziation > Stimmung > Cluster > Setting & Kontext. Bei weniger als zwei Treffern die Suche einmal mit einem breiteren Begriff wiederholen.

Zulässig ist nur, was alle drei Bedingungen erfüllt:
- `Status` = „Freigegeben" (Neu und Gesperrt fallen aus)
- `Slot-Typ` passt zur Ebene (kein Hero-Bild als Inline-Motiv, keine Grafik als Motivfoto)
- Das Bild ist im selben Artikel nicht bereits für einen anderen Slot vorgesehen

Ranking unter den Zulässigen: Stimmung schlägt Motiv (ein Abschnitt über Widerstand bekommt kein Bild mit lachenden Menschen, auch wenn es thematisch näher liegt), danach gewinnt der niedrigere `Nutzungszähler Blog`. Wiederverwendung über Artikel hinweg ist ausdrücklich erlaubt – anders als bei LinkedIn. Der Zähler dient der Streuung, nicht der Sperre. Bilder mit gefüllter Webflow-URL brauchen keinen neuen Upload.

**2. SharePoint-Fundus** (nur wenn der Index leer bleibt, und nur als Auftrag an Ali, nicht als eigener Zugriff). Der artikelbezogene Pfad ist `5_Webseite / Blog / {Cluster} / {Leistung} / {Artikelthema}`; die Cluster-Ebene hat drei Ordner (Führungskräfteentwicklung, Organisationsentwicklung, Teamentwicklung), darunter die Leistung, darunter ein Ordner pro Artikelthema. Zuerst prüfen lassen, ob zum eigenen Thema schon ein Ordner existiert – dann sind die Bilder thematisch vorsortiert. Allgemeine Motive liegen unter `5_Webseite / Bilder Webseite`.

Bei allen Slots mit Menschen, Workshop- oder Beratungssituationen hat diese Quelle Vorrang vor Stockfotos, auch wenn ein Stockfoto technisch besser aussieht. Echte Bilder aus echten Workshops sind der Glaubwürdigkeitsvorsprung.

**3. Stockfoto** (Unsplash/Pexels). Nur wenn 1 und 2 leer bleiben. Lizenz und Quell-URL sind Pflichtfelder im Bildindex.

**4. KI-generiert.** Nur für abstrakte oder gegenstandsbezogene Motive – Kompass, Laptops auf einem Tisch, Schreibtischdetails, Architektur, Whiteboard ohne Personen. **Nicht** für Menschen in Beratungs- oder Workshopsituationen: ein KI-generiertes Team in einem Beratungsblog untergräbt genau die Glaubwürdigkeit, die der Artikel aufbaut. Der Prompt gehört ins Feld „Quelle-URL oder Prompt".

### Motiv-Katalog aus dem Markenbriefing

Motiv-Briefings greifen auf die Bildwelt zurück, die Christoph selbst formuliert hat, statt beliebige Metaphern zu erfinden:

- **Dynamik im Team:** Menschen gemeinsam im Ruderboot
- **Gemeisterte Veränderung:** aus etwas Altem etwas Neues, z. B. verfallenes Grundstück zu neuem Haus
- **Erreichter Meilenstein:** Berggipfelankunft mit Führer
- **Musterwechsel:** begangene Wege werden verlassen, neue entstehen
- **Beratungssituationen:** Moderation vor dem Flipchart, 1:1-Coaching am Tisch, Ideenfindung im Meetingraum, Workshop-Settings

Auswahlmaßstab aus `changexperten-brand`: warme, echte, dokumentarische Team-Fotografie, kein Stock-Glanz.

## 6. Ebene 3 – Vorlage wählen

Die Grafik entsteht **nicht** durch freies Gestalten, sondern durch Auswahl und Befüllung einer Vorlage aus `Grafik-Vorlagen`. Auswahl in drei Schritten:

**Schritt 1 – Aussagetyp der Kernaussage bestimmen.** Was behauptet der Abschnitt strukturell?

| Aussagetyp | Passende Formen |
|---|---|
| Sequenz (Schritte bauen aufeinander auf) | Five steps, Four steps, Infographic process I/III/V, Three stairs |
| Sammlung gleichrangiger Punkte | Six circle segments, Four circle segments, Honeycomb, Building blocks |
| Hierarchie (Ebenen mit Über-/Unterordnung) | 3D pyramid, Pyramid with four layers, Iceberg |
| Kreislauf (mit Rückkopplung) | Process circle, Four circle segments |
| Gegenüberstellung | Matrices with four areas, SWOT analysis II, Pros and cons III |
| Reduktion (aus viel wird wenig) | Funnel III |
| Überschneidung | Intersection |
| Ursache-Wirkung | Cause and effect IV, Two obstacles, Iceberg |
| Anteile / Zahlen | Density |

**Die Form darf die Aussage nicht verfälschen.** Das ist die wichtigste Regel dieses Abschnitts, weil ein Formfehler wie eine inhaltliche Behauptung wirkt: Ein Trichter behauptet, dass aus vielen wenige werden. Eine Pyramide behauptet Über- und Unterordnung. Ein Zyklus behauptet Wiederkehr. Sechs gleichrangige Erfolgsfaktoren in einen Trichter zu setzen, behauptet eine Auslese, die der Artikel nicht belegt. Passt keine Vorlage zum Aussagetyp, ist das ein zulässiges Ergebnis: dann trägt der Artikel keine Ebene-3-Grafik und der Slot wird mit Begründung als offen gemeldet, statt eine falsche Form zu wählen.

**Schritt 2 – Slots abgleichen.** Das Feld „Slots" muss zur Zahl der inhaltlichen Punkte passen. Sechs Punkte in eine Vier-Slot-Vorlage zu quetschen (oder zwei Slots leer zu lassen) ist ein Ausschlussgrund, kein Detail.

**Schritt 3 – Zulässigkeit prüfen.** `Blog-Eignung` = „Gut" (bei „Bedingt" nur mit Begründung im Auftrag), `Befüllbar` = „Ja (Shapes)". Vorlagen mit `Befüllbar` = „Nein (think-cell)" tragen ihre Daten in einem Add-in-Datenblatt; sie sind nur wählbar, wenn Ali die Zahlen manuell setzt, und das muss im Auftrag ausdrücklich stehen. Bei gleichwertigen Kandidaten gewinnt der niedrigere `Nutzungszähler` – sonst zeigt jeder Artikel denselben Trichter.

## 7. Grafik-Auftrag – Format

Der Produktionslauf schreibt den Auftrag in das Feld „Grafik-Auftrag", exakt nach der „Befüllungsstruktur" der gewählten Vorlage und **innerhalb der dort genannten Zeichengrenzen**. Der Auftrag ist so vollständig, dass die Befüllung ohne Rückfrage möglich ist – egal ob durch Claude mit hochgeladener PPTX oder durch Ali in PowerPoint.

```
VORLAGE: Six circle segments (recbpIz8XVctSKK0L)
AUSSAGETYP: Sammlung gleichrangiger Punkte · SLOTS: 6/6 belegt
GRAFIKTITEL: Sechs Erfolgsfaktoren der digitalen Transformation
CAPTION: Erfolgsfaktoren der digitalen Transformation
ALT-TEXT: Übersicht der sechs Erfolgsfaktoren digitaler Transformation
DATEINAME: erfolgsfaktoren-digitale-transformation.webp

SLOT 1 | Kurztitel: Sinn und Standort | Beschreibung: Erst das Warum klären, dann über Tools reden
SLOT 2 | Kurztitel: Lernschleifen | Beschreibung: Kurze Zyklen statt starrer Meilensteine
...
QUELLE DER INHALTE: Abschnitt „Der Weg dorthin" des finalen Blogartikels, keine Ergänzungen
```

**Der Inhalt kommt ausschließlich aus dem fertigen Artikeltext.** Keine Faktoren, Zahlen oder Phasen ergänzen, die im Text nicht vorkommen. Eine Grafik, die mehr behauptet als der Artikel, ist ein Quellentreue-Verstoß wie eine erfundene Zahl.

## 8. Befüllung ausführen

Nur möglich, wenn die PPTX als Datei vorliegt (Chat-Upload oder Airtable-Attachment). Ablauf:

1. Foliengrid rendern, um die Zielfolie zu finden: `python scripts/thumbnail.py "ThinkCell Templates.pptx" tc-thumbs`
2. Folie duplizieren, damit die Vorlage unberührt bleibt: `python scripts/add_slide.py unpacked/ slideN.xml`
3. Texte in `ppt/slides/slideN.xml` ersetzen – ein `<a:p>` pro Listenpunkt, `run.text` statt `text_frame.text`
4. Packen, dann `soffice.py --headless --convert-to pdf`, dann `pdftoppm -jpeg -r 150`
5. Auf WebP konvertieren, Zielgröße **≤150 KB** bei 2000 px Breite
6. Gerendertes Bild ansehen und auf Textüberlauf prüfen – der häufigste Fehler beim Befüllen von Vorlagen sind zu lange Texte, die aus ihrer Form laufen
7. Ergebnis als Datensatz in `Blog-Bilder` anlegen: `Slot-Typ` = Grafik, `Quelle` = Eigene Grafik, Vorlagenname im Feld „Quelle-URL oder Prompt"

Details zum PPTX-Handling: Skill `pptx`. Die Fußzeile der Vorlagensammlung trägt noch „WISKA Hoppmann GmbH" aus der Quellvorlage – beim Befüllen mit entfernen.

## 9. Harte Regeln

**Herkunftsnachweis ist Freigabevoraussetzung.** Kein Bild geht live, dessen Herkunft nicht im Bildindex dokumentiert ist: Quelle gesetzt, bei Stockfotos zusätzlich Lizenz und Quell-URL, bei KI der vollständige Prompt, bei eigenen Fotos der SharePoint-Pfad. Ein Bild, dessen Herkunft niemand rekonstruieren kann, ist ein offenes Risiko – nicht weil eine Abmahnung wahrscheinlich ist, sondern weil sie im Fall der Fälle nicht abwehrbar wäre.

Weiter gilt:

- Kein Bild ohne Alt-Text und ohne Eintrag in `Blog-Bilder`
- Keine erkennbaren echten Personen ohne dokumentierte Einwilligung. Bei Fotos aus Kundenworkshops einmalig prüfen, ob die Einwilligung die Nutzung auf der Website abdeckt
- Keine Kundenlogos oder Kundenräume ohne Freigabe
- Format WebP, ≤150 KB, sprechender Dateiname
- Alt-Text max. 125 Zeichen, in erster Linie beschreibend; Haupt-Keyword nur bei Content-Ziel SEO-Keyword/Beides und nur, wenn es die Beschreibung nicht verzerrt

## 10. Nach der Veröffentlichung

Pro genutztem Bild in `07 Blog-Bilder`: `Nutzungszähler Blog` um 1 erhöhen, Webflow-URL eintragen, Verknüpfung zur `04 Blog`-Zeile setzen. Bei der genutzten Vorlage in `08 Grafik-Vorlagen` ebenfalls `Nutzungszähler` um 1 erhöhen. Beides passiert **nur beim tatsächlichen Publish**, nie beim Vorschlagen – so zählt nur, was wirklich live ging.

**Wer das bucht (geklärt 08/2026):** Die tägliche Feedback-Runde „Content C" übernimmt die Buchung. Sie sucht Blog-Zeilen mit Status „Veröffentlicht", in deren „Feedback-Verlauf" noch kein Vermerk `Zähler gebucht` steht, erhöht die Zähler und schreibt `Zähler gebucht [Datum]` in den Verlauf. Damit wird jede Zeile genau einmal gebucht, auch wenn der Lauf sie mehrmals sieht. Das Make-Szenario „Content-Publishing" (ID 9521520) fasst die Zähler nicht an; manuelles Nachzählen durch Ali ist nicht mehr nötig.
