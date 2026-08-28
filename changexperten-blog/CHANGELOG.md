# Änderungen

## 28.08.2026 – Neue Struktur, täglicher Lauf, echtes Tracking

Anlass: Die frühere Tabelle „Blog & Newsletter" ist aufgeteilt, der Produktionslauf läuft jetzt täglich statt zweimal im Monat, und Search Console, Analytics und DataForSEO sind angebunden.

**Korrigiert**

- **Tabellennamen und IDs.** „Blog & Newsletter" → **„04 Blog"** (die Tabellen-ID `tblzTKBLsewsvoCis` ist geblieben, der Newsletter hat mit „05 Newsletter" eine eigene Tabelle bekommen). „Blog-Bilder" → „07 Blog-Bilder", „Grafik-Vorlagen" → „08 Grafik-Vorlagen". Betroffen: `SKILL.md`, `references/keyword-und-content-ziel.md`, `references/bilder-und-grafiken.md`, `references/textstruktur.md`.
- **Routine-Bezeichnungen.** „Routine 1/2/3" hieß nichts mehr. Ersetzt durch die tatsächlichen geplanten Aufgaben: **„Content D: Blog- und Newsletter-Produktion"** (Bildplan, Keywords, Artikel, Grafik-Aufträge) und **„Content C: Tägliche Feedback- und Finalisierungsrunde"** (finale Auswahl, Abgleich gegen den finalen Text, Zähler-Buchung).
- **Zähler-Buchung – offener Punkt erledigt.** Der Skill notierte, dass die Zähler beim Publish noch niemand erhöht und Ali sie manuell setzen müsse. Das übernimmt jetzt „Content C": Sie sucht Blog-Zeilen mit Status „Veröffentlicht", in deren „Feedback-Verlauf" noch kein `Zähler gebucht` steht, erhöht „Nutzungszähler Blog" und den Vorlagen-Zähler und schreibt `Zähler gebucht [Datum]` in den Verlauf. Damit wird jede Zeile genau einmal gebucht.
- **Quellendatum.** Verweise auf ein „Quellen-Feld der Airtable-Zeile" zeigen jetzt auf den verknüpften Datensatz in „02 Studienrecherche" (bei Altzeilen `zzz Archiv – Quellen`).

**Geändert**

- **Themenfreigabe.** Explizit festgehalten: Den Status „Ausgewählt" setzt **Christoph**. Claude schlägt Themen vor und setzt diesen Status nie selbst.
- **Rhythmus.** Ziel bleiben 2 Artikel pro Monat, aber der Lauf startet **täglich** und beginnt mit einem Gate: produzieren, sobald eine Zeile auf „Ausgewählt" steht – sonst still beenden (Monatsziel erreicht, Vorschläge warten schon, oder der LinkedIn-Prozess des Monats ist noch zu früh für einen belastbaren Vorschlag). Ein Lauf ohne Arbeit schreibt nichts und schickt keine Mail.
- **Webflow-Veröffentlichung.** Das Make-Szenario „Content-Publishing" (9521520) legt den Artikel als **Webflow-Entwurf** an und überträgt alle Einzelheiten mit – Textkörper, Blog-Titel, Meta-Titel, Meta-Description, Slug, Tags, Kategorie, Bilder samt Alt-Text und Unsplash-Attribution. Die Schritte in `references/veroeffentlichung.md` sind jetzt Prüfliste am Entwurf statt Handarbeit.

**Neu**

- **DataForSEO-Ersatzweg für Keywords.** Weil der Lauf täglich ist, kann er ein Thema am Morgen nach der Freigabe aufgreifen, bevor Make durchgelaufen ist. Sind „Keyword-Auswahl" und „Content-Ziel" leer, recherchiert Claude selbst über den DataForSEO-Konnektor (`keyword_ideas` / `keyword_suggestions`, `keyword_overview` bzw. `google_ads_search_volume`, `bulk_keyword_difficulty`; Germany/de) und vermerkt die Herkunft in „Notizen Redaktion". Eine von Make gefüllte Rohliste wird dabei nie überschrieben.
- **Zweite Prüfspur gegen Kannibalisierung.** Zusätzlich zum Live-Bestand aus Webflow wird das Haupt-Keyword gegen die echten Rankings der Domain geprüft (`dataforseo_labs_google_ranked_keywords`, target changexperten.com). Rankt eine bestehende Seite in den Top 20, gilt das Keyword als besetzt – dann Aktualisierung der Bestandsseite vorschlagen statt neuen Artikel schreiben.
- **Tracking als Strecke.** `references/veroeffentlichung.md` beschreibt jetzt die monatliche Aufgabe **„Content F: SEO/GEO-Reporting"** (am 2. für den Vormonat): GSC und GA4 über Pipedream, DataForSEO für Keyword-Bestand und ETV, Ablage in „10 KPI-Monatswerte", „12 Query-Performance" und „13 Landingpage-Performance", Monatsbefund, Maßnahmenvorschläge in „14 Growth-Maßnahmen" und ein Dashboard, das monatlich unter derselben Adresse aktualisiert wird. Einzelne Artikel sind über das Feld „Blog" in „13 Landingpage-Performance" direkt mit ihrer Blog-Zeile verknüpft.
- **Tracking-Schwellenwerte** – offener Punkt beantwortet: Sie stehen als Formeln („Diagnose", „Potenzial Klicks/Monat") in „13 Landingpage-Performance" und sind dort nachlesbar und anpassbar.

**Unverändert**

Prioritätenhierarchie, Leitquellen-Regel, Content-Ziel-Logik (SEO-Keyword vs. GEO-Autorität), Textstruktur und GEO-Pflichten, Literaturverzeichnis, Drei-Ebenen-Bildmodell, Grafik-Auftragsformat, On-Page-Check, interne Linkziele, Personas und freigegebene Proof Points.
