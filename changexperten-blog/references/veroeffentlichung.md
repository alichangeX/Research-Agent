# Veröffentlichung, Promotion und Tracking

## 1. Voraussetzung: inhaltliche Freigabe

Kein Schritt in diesem Dokument beginnt, bevor Christoph den fertigen Artikel freigegeben hat. Für die Freigabe immer mitliefern:
- Text final, Struktur- und Tonalitätsvorgaben erfüllt
- Meta-Titel + Meta-Description + Slug + H1
- On-Page-Check-Tabelle (siehe [seo-und-bilder.md](seo-und-bilder.md))
- Interne Links aus der verbindlichen URL-Liste, externe Links vorhanden
- Quellenblock am Artikelende vorhanden und vollständig (Leitquelle zuerst, Datum, Link aufs Original)
- Bilder inkl. Alt-Text, WebP/≤150 KB, sprechende Dateinamen
- Drei Tags aus bestehenden Webflow-Tags, Kategorie gesetzt
- Thematisch passender Lead-Magnet als CTA eingebunden
- Fallbeispiele anonymisiert, keine Kundennamen, nur freigegebene Proof Points

Bei offenen Rückfragen von Christoph: Klärung abwarten, nicht vorsorglich schon veröffentlichen.

## 2. Erstellung in Webflow

**Automatisiert seit 08/2026:** Das Make-Szenario „Content-Publishing" (ID 9521520) legt den Artikel als **Webflow-Entwurf** an und überträgt dabei alle Einzelheiten – Textkörper, Blog-Titel, Meta-Titel, Meta-Description, Slug, Tags, Kategorie, Bilder samt Alt-Text und die Unsplash-Attribution. Die Schritte unten sind damit die Prüfliste am Entwurf, nicht mehr Handarbeit: durchsehen, Formatierung kontrollieren, dann in Webflow veröffentlichen. Nur wenn das Szenario nicht läuft, wird manuell eingepflegt.

1. Artikel im CMS prüfen bzw. einpflegen: Text, Bilder, interne Links, Alt-Tags, Formatierung. Der Quellenblock ist Teil des Rich-Text-Felds am Ende des Artikels, kein separates CMS-Feld; alle Links darin auf „open in new tab" setzen
2. Meta-Titel und Meta-Description final gegenprüfen (siehe [seo-und-bilder.md](seo-und-bilder.md))
3. Kategorie eintragen, die drei zuvor festgelegten (bestehenden) Tags anlegen
4. Artikel veröffentlichen
5. Christoph über die Veröffentlichung informieren

## 3. Weiterleitung zur Promotion

Nach Veröffentlichung wird der Artikel an das Content-/Marketing-Team zur Promotion weitergegeben:
1. LinkedIn-Post über das changeXperten-Firmenprofil erstellen (Teaser + Verlinkung auf den Artikel)
2. Übernahme der Kerninhalte für einen oder mehrere Einzelposts auf Christophs persönlichem Profil – dafür `changexperten-linkedin-christoph` nutzen, der Artikel liefert dort die Rohgeschichte/das Thema für Phase 0

**Hinweis:** Das ursprüngliche Prozessdokument nennt hierfür „Antonia" als zuständige Person. Das sollte vor dem produktiven Einsatz einmal mit dem aktuellen Team abgeglichen werden.

## 4. Tracking

Läuft seit 08/2026 automatisiert über die monatliche Aufgabe **„Content F: SEO/GEO-Reporting"** (jeweils am 2. für den Vormonat). Sie zieht die Zahlen selbst und schreibt sie in die Base:

- **Google Search Console** (über Pipedream): Klicks, Impressionen, CTR und Ø Position je Seite und je Query → Tabellen „13 Landingpage-Performance" und „12 Query-Performance". Die Formelfelder dort rechnen Deltas, CTR, eine Diagnose und ein Klick-Potenzial aus.
- **Google Analytics 4** (über Pipedream): Sitzungen, Engagement-Rate und Key Events je Kanal und Landingpage. Der Kanal „AI Assistant" misst die Zugriffe aus KI-Assistenten.
- **DataForSEO:** rankende Keywords, Anzahl in den Top 10, Sichtbarkeitswert ETV → „10 KPI-Monatswerte".

Dazu entstehen ein Monatsbefund in Klartext, drei bis fünf Vorschläge in „14 Growth-Maßnahmen" (Status immer „Vorgeschlagen", freigeben tut Christoph) und ein Dashboard, das jeden Monat unter derselben Adresse aktualisiert wird. Wer einen einzelnen Artikel bewerten will, findet ihn über das Feld „Blog" in „13 Landingpage-Performance" direkt mit seiner Blog-Zeile verknüpft.

Nach 4–6 Wochen prüfen, ob Nachjustierung nötig ist, z. B.:
- Zwischenüberschriften anpassen
- interne Links ergänzen
- neue Absätze einfügen, wenn Verweildauer oder Ranking hinter den Erwartungen zurückbleiben

Diese Auswertung ist noch nicht abschließend definiert ("to be defined" im Originaldokument) – bei Bedarf mit Ali/Christoph klären, welche konkreten Schwellenwerte eine Nachjustierung auslösen sollen.
