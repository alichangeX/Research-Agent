# SEO-Metadaten, verbindliche Linkziele, Bilder und On-Page-Check

## 1. Meta-Beschreibungen

Aus dem fertigen Blogtext ableiten. Meta-Titel, Meta-Description, Slug und H1 sind **immer** Pflicht – unabhängig vom Content-Ziel. Das ist Grundhygiene, kein Keyword-Thema. Nur die Keyword-Spalte ist bedingt:

| Element | Vorgabe (immer) | Zusätzlich bei Content-Ziel SEO-Keyword/Beides |
|---|---|---|
| Meta-Titel | 50–60 Zeichen, ansprechend formuliert, trägt die Kernaussage | Haupt-Keyword möglichst am Anfang |
| Meta-Description | 140–160 Zeichen, Suchintention bzw. beantwortete Frage klar adressiert, mit Call-to-Action | Haupt-Keyword enthalten |
| URL/Slug | kurz, sprechend, nur Kleinbuchstaben, Bindestriche | Haupt-Keyword enthalten |
| H1 | prüfen, ob sie zum Meta-Titel passt – darf etwas länger/erklärender sein | Haupt-Keyword enthalten |

Bei Content-Ziel „GEO-Autorität" werden Titel, Description, Slug und H1 aus der Kernaussage formuliert. Kein Keyword hineinkonstruieren, keinen Begriff aus der Rohliste als Ersatz einsetzen.

Ergebnis in einer klaren Tabelle liefern und in die „Seo-Texte"-Datei eintragen. Wird bei Fertigstellung **immer** mitgeliefert, auch bei Einzelaufgaben.

## 2. Verbindliche interne Linkziele

**Nur diese flachen URLs verwenden** (live geprüft, Stand aus der Web-Publishing-Wissensdatei):

- https://www.changexperten.com/change-management-beratung-und-coaching
- https://www.changexperten.com/change-management-training
- https://www.changexperten.com/change-agent-ausbildung-training
- https://www.changexperten.com/teamcoaching
- https://www.changexperten.com/workshop-moderation
- https://www.changexperten.com/konfliktmoderation-teamkonflikte-loesen
- https://www.changexperten.com/fuehrungskraefte-coaching
- https://www.changexperten.com/fuehrungskraefte-weiterbildung
- https://www.changexperten.com/leitbildentwicklung
- https://www.changexperten.com/kulturentwicklung

**Kategorie-Hubs** (übergeordnet, ebenfalls verwendbar): `/organisationsentwicklung` · `/teamentwicklung` · `/fuehrungskraefteentwicklung`

**Wichtig:** Keine anderen internen URLs konstruieren oder aus Vermutung ableiten. Passt keine der Listen-URLs thematisch, das offen benennen statt eine ungefähr passende URL zu erfinden.

**Bekannter Altlast-Punkt:** Ältere Blogartikel könnten noch auf falsche, verschachtelte Pfade verlinken (z. B. `/teamentwicklung/teamcoaching` statt `/teamcoaching`). Bei der Überarbeitung bestehender Artikel solche Pfade korrigieren; bei neuen Artikeln von vornherein nur die flachen URLs oben verwenden.

Externe Links (1–2/1.000 Wörter): seriöse Quellen wie Springer, HBR, McKinsey, BCG, Deloitte, Gallup.

## 3. Tags

Genau drei Tags vergeben, die den Artikel passend beschreiben. **Nur Tags verwenden, die in Webflow bereits angelegt sind** – keine neuen Tags erstellen. Bei Unsicherheit, welche Tags existieren, vor der Vergabe nachfragen statt zu raten.

## 4. Bilder

### Anzahl & Platzierung
- Ca. 1 Bild pro 300–500 Wörter
- Mindestens 1 Bild „above the fold" (im Einleitungsbereich)
- Pro H2-Abschnitt möglichst ein Bild vorgesehen

### Bildtypen
- Verschiedene Bildarten mischen: Stockfotos, Infografiken, Zitatkarten, Modelle/Frameworks
- Mindestens 1 Infografik oder ein visuelles Zitat (social-media-fähig)

### Herkunft
1. Passende Bilder im changeXperten-Design auf Unsplash recherchieren (groß, ohne Caption)
2. Ergänzende Grafiken im CI erstellen (Modelle aus Quellen oder eigenen Trainingsunterlagen) – eher klein, mit Caption. Farben/Stil aus `changexperten-brand`.

### SEO-Optimierung pro Bild
- Sprechender Dateiname, der das Bildmotiv beschreibt; bei Content-Ziel SEO-Keyword/Beides das Haupt-Keyword darin verwenden
- Alt-Text: max. 125 Zeichen, in erster Linie **beschreibend** – er erklärt, was auf dem Bild zu sehen ist (Barrierefreiheit). Bei Content-Ziel SEO-Keyword/Beides das Haupt-Keyword einbauen, wenn es die Beschreibung nicht verzerrt; bei GEO-Autorität rein beschreibend, ohne Keyword (in Webflow: Image → Werkzeug → Alt Text → Custom description)
- Format WebP, optimiert (max. ~150 KB)
- Header-Bild wird ganz unten im Element „Bild" eingefügt, dort auch Kategorie etc. angeben

Für die Bildauswahl/-optimierung selbst zusätzlich den `image`-Skill nutzen.

## 5. On-Page-Check (bei jeder Fertigstellung als Tabelle ausgeben)

Der Check ist zweispurig: Grundhygiene gilt immer, die Spur darunter richtet sich nach dem Feld „Content-Ziel". Nenne das Content-Ziel über der Tabelle, damit nachvollziehbar ist, welche Spur geprüft wurde.

**Immer (Grundhygiene):**

| Prüfpunkt | Erfüllt? | Anmerkung |
|---|---|---|
| Meta-Titel 50–60 Z., Meta-Description 140–160 Z., Slug kurz und sprechend | | |
| H-Struktur logisch: eine H1, H2 mit mind. 2 H3, Überleitungstexte vorhanden | | |
| Themen vollständig abgedeckt (verwandte Begriffe/Entitäten da) | | |
| Interne (2–5) + externe (1–2) Links pro 1.000 W., interne Links aus der verbindlichen Liste | | |
| Jede Zahl belegt, mit korrekter Bezugsgröße, Quelle am Satz | | |
| Kernaussage entspricht der Leitquelle, nicht verallgemeinert oder umgedeutet | | |

**Zusätzlich bei Content-Ziel „SEO-Keyword" oder „Beides":**

| Prüfpunkt | Erfüllt? | Anmerkung |
|---|---|---|
| Haupt-Keyword in Title, H1, erste 100 W., mind. 1 H2 | | |
| Haupt-Keyword in Meta-Titel, Meta-Description, Slug | | |
| Sekundär-Keywords natürlich über H2/H3 verteilt (kein Stuffing) | | |
| Keine Platzierung hat die Kernaussage verbogen (Vorrangregel eingehalten) | | |

**Zusätzlich bei Content-Ziel „GEO-Autorität" oder „Beides":**

| Prüfpunkt | Erfüllt? | Anmerkung |
|---|---|---|
| Antwort zuerst: zitierfähiger Kernsatz in den ersten 2–3 Sätzen | | |
| Jede Zahl mit Quelle **und** Veröffentlichungsdatum direkt am Satz | | |
| H2/H3 als echte Fragen formuliert | | |
| Definitions- oder Fazit-Block vorhanden, eigenständig verständlich | | |
| 2–3 interne Links auf Cluster-Linkziele gesetzt | | |

Bei Abweichungen in der Grundhygiene oder den GEO-Punkten gezielt nachschärfen, ohne Lesefluss zu stören und ohne Inhalte zu streichen.

**Was hier ausdrücklich nicht passiert:** kein nachträgliches Einbauen von Keywords in einen fertigen Text, um eine Zeile abzuhaken. Fehlt bei Content-Ziel „SEO-Keyword" eine Platzierung und lässt sie sich nicht natürlich ergänzen, ist das ein Signal, dass das Keyword nicht zum Artikel passt: „Content-Ziel" auf „GEO-Autorität" umstellen, Grund vermerken, GEO-Spur prüfen. Bei „GEO-Autorität" wird ein fehlendes Keyword nie als Abweichung behandelt – das ist der gewollte Zustand.
