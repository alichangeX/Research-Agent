# Abbildungen im Newsletter

Bilder und Grafiken kommen aus Airtable, Base `appb7eOfe2Au3Lp40`. Zwei Quellen, keine weiteren: Tabelle **Blog-Bilder** (`tblE7N7W8Z6frJwS1`) für Fotos, Tabelle **Grafik-Vorlagen** (`tbl6nRJ5CfnY9iBNV`) für eigene Grafiken. Kein Unsplash-Direktabruf, kein KI-Bild, keine Bilder aus der Tabelle LinkedIn-Bilder – die ist ausschließlich für LinkedIn, und ihr Nutzungszähler sperrt bereits gepostete Motive.

## Schritt 1 – Braucht diese Ausgabe überhaupt eine Abbildung?

Standard ist: **keine**. Eine erzählte Ausgabe von 500–700 Wörtern trägt sich über den Text, und jedes Bild verschiebt das Text-Bild-Verhältnis in Richtung der Deliverability-Grenze. Eine Abbildung kommt nur dazu, wenn sie eine der beiden Aufgaben erfüllt:

- **Grafik**, wenn die Struktur der Kernaussage die Aussage trägt: drei Stufen, ein Kreislauf, ein Vorher-Nachher, eine Matrix mit zwei Achsen. Der Leser versteht die Beziehung schneller als im Satz.
- **Foto**, wenn der Impuls eine Alltagsszene beschreibt und das Bild die Stimmung setzt, die der Text im P-Teil aufbaut.

Nicht als Abbildung: Kernaussage, Titel, Zahlen, Zitate, CTA. Die stehen als Text, sonst sind sie bei abgeschalteten Bildern weg (siehe Deliverability im SKILL.md).

**Maximal eine Abbildung pro Regel-Ausgabe.** In einer Nurture-Mail maximal eine, und nur in der Mail, deren Inhalt sie tatsächlich braucht.

## Schritt 2a – Foto aus Blog-Bilder wählen

Matching gegen die Kernaussage und den P-Teil der Ausgabe, in dieser Reihenfolge:

1. **Status** = „Freigegeben". „Neu" ist ungeprüft, „Gesperrt" nie verwenden.
2. **Themen-Assoziation** – das wichtigste Suchfeld. Schlagworte gegen das Thema der Ausgabe.
3. **Stimmung** – muss zum Abschnitt passen. Eine Ausgabe über stillen Widerstand bekommt kein Bild mit lachenden Menschen.
4. **Cluster** – Newsletter-Cluster gegen Bild-Cluster.
5. **Slot-Typ** – „Hero" oder „Motivfoto" taugen für die Mail, „Grafik" nur, wenn es genau die gesuchte Darstellung ist.
6. **Webflow-URL** – ist sie gefüllt, liegt das Bild schon im CDN und kann ohne Upload eingebunden werden. Das ist der bevorzugte Fall, weil Pipedrive dann nur die URL braucht.
7. **Nutzungszähler Blog** aufsteigend sortieren, damit nicht in jeder Ausgabe dasselbe Motiv steht.

Vorschlag immer 2–3 Kandidaten, finale Auswahl durch Christoph oder Ali. **Alt-Text** aus dem gleichnamigen Feld übernehmen und bei Bedarf auf die Ausgabe zuschneiden, max. 125 Zeichen, beschreibend.

Der Zähler „Nutzungszähler Blog" wird durch eine Newsletter-Verwendung **nicht** erhöht – er zählt Blogartikel. Newsletter-Nutzung nur in der Ausgabe dokumentieren.

## Schritt 2b – Grafik aus Grafik-Vorlagen wählen

Die Tabelle katalogisiert die befüllbaren Folien aus „ThinkCell Templates.pptx". Auswahl nach Aussage, nicht nach Optik:

1. **Aussagetyp** – das zentrale Kriterium. Die Form behauptet etwas: Trichter behauptet Reduktion, Pyramide Hierarchie, Zyklus Wiederkehr. Passt die Behauptung der Form nicht zur Kernaussage, ist es die falsche Vorlage, auch wenn sie gut aussieht.
2. **Slots** – muss zur Zahl der Elemente im Impuls passen. Drei Tipps brauchen drei Slots, nicht fünf.
3. **Blog-Eignung** – als Näherung für E-Mail-Eignung verwenden: „Gut" bevorzugen, „Nicht geeignet" ausschließen (zu textlastig oder zu breit ist in der Mail noch kritischer als im Blog).
4. **Befüllbar** – „Ja (Shapes)" lässt sich per Skript füllen. „Nein (think-cell)" heißt: nur manuell in PowerPoint, also nur wählen, wenn Ali die Zeit dafür hat.
5. **Nutzungszähler** aufsteigend, damit nicht jede Ausgabe denselben Trichter zeigt.
6. **Vorschau** ansehen, statt die PPTX zu öffnen.

Aus der gewählten Vorlage entsteht ein **Grafik-Auftrag** in genau der Slot-Struktur, die im Feld „Befüllungsstruktur" der Vorlage steht: Vorlagenname, Grafiktitel, Caption, Alt-Text und pro Slot der fertige Text innerhalb der Zeichengrenzen. Der Auftrag muss so vollständig sein, dass Ali ihn ohne Rückfrage ausführen kann.

## Schritt 3 – Export-Spec für E-Mail

Die Grafiken sind für Folien gebaut, nicht für Postfächer. Vor dem Einbinden:

- Breite **600 px** (Pipedrive-Contentbreite), 2× für Retina nur wenn die Dateigröße es zulässt
- Format WebP oder PNG, Ziel **unter 200 KB**
- Querformat oder Quadrat. Hochformat schneidet in der mobilen Vorschau ab
- Schrift in der Grafik mindestens so groß, dass sie bei 600 px noch lesbar ist. Wird sie das nicht, gehört der Inhalt in den Text und nicht ins Bild
- changeXperten-CI, kein Fremdbranding, kein Lorem ipsum (siehe `changexperten-brand`)
- **Alt-Text Pflicht**, aussagekräftig – bei abgeschalteten Bildern ist er das, was der Leser sieht
- Text-Bild-Verhältnis der Mail bleibt bei mindestens 60:40
- Das Bild ist kein Link auf den CTA. Der CTA bleibt Text-Link

## Airtable-Feldzuordnung

Kommt der Auftrag aus der Content-Pipeline (Tabelle Blog & Newsletter, `tblzTKBLsewsvoCis`), werden die bestehenden Bildfelder mitgenutzt:

| Zweck | Feld |
|---|---|
| Foto-Kandidaten | „Bildvorschläge Blog" (Verknüpfung auf Blog-Bilder) |
| Gewählte Grafikvorlage | „Grafik-Vorlagen" (Verknüpfung) |
| Befüllungsauftrag | „Grafik-Auftrag" |

Trägt dieselbe Zeile auch einen Blogartikel, gelten diese Felder primär für den Blog. Dann wird die Newsletter-Abbildung **nicht** zusätzlich dort eingetragen, sondern im Text des Feldes „Finaler Newsletter" am Ende als Block dokumentiert:

```
Abbildung: [Dateiname oder Vorlagenname] | Position: [nach Absatz X] | Alt-Text: [...] | Quelle: Blog-Bilder / Grafik-Vorlagen
```

**Offener Punkt für Christoph:** Sauberer wäre ein eigenes Feld „Bildvorschläge Newsletter" in Blog & Newsletter plus ein Zähler „Nutzungszähler Newsletter" in Blog-Bilder. Solange die nicht existieren, gilt die Dokumentation im Textfeld oben.

## Checkliste Abbildung

- [ ] Die Abbildung erfüllt eine der beiden zugelassenen Aufgaben – sie ist keine Dekoration
- [ ] Max. eine Abbildung in der Ausgabe
- [ ] Quelle ist Blog-Bilder oder Grafik-Vorlagen, nichts anderes
- [ ] Bei Foto: Status „Freigegeben", Stimmung passt zum Abschnitt
- [ ] Bei Grafik: Aussagetyp passt zur Kernaussage, Slots passen zur Zahl der Elemente
- [ ] Grafik-Auftrag vollständig in der Slot-Struktur der Vorlage
- [ ] 600 px, unter 200 KB, Querformat oder Quadrat
- [ ] Alt-Text vorhanden, max. 125 Zeichen
- [ ] Kernaussage, Titel, Zahlen und CTA stehen als Text, nicht im Bild
- [ ] Text-Bild-Verhältnis mindestens 60:40
