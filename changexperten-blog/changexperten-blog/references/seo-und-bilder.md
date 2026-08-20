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

**Wichtig:** Diese Leistungsseiten-URLs nie aus Vermutung ableiten oder abwandeln. Passt keine der Listen-URLs thematisch, das offen benennen statt eine ungefähr passende URL zu erfinden. Ausgenommen von dieser festen Liste sind ausschließlich Blog-zu-Blog-Links (siehe „Zweite Ebene" unten), deren gültige URLs live aus Webflow kommen – auch die nie raten.

**Bekannter Altlast-Punkt:** Ältere Blogartikel könnten noch auf falsche, verschachtelte Pfade verlinken (z. B. `/teamentwicklung/teamcoaching` statt `/teamcoaching`). Bei der Überarbeitung bestehender Artikel solche Pfade korrigieren; bei neuen Artikeln von vornherein nur die flachen URLs oben verwenden.

### Zweite Ebene: Blog-zu-Blog-Links (auf veröffentlichte Artikel)

Zusätzlich zu den Leistungsseiten-Links oben verlinkt jeder neue Artikel **2–3 thematisch passende, bereits veröffentlichte Blogartikel**. So entsteht ein dichtes internes Netz, das sowohl SEO (Themencluster, Linkfluss) als auch GEO (Zitierfähigkeit im Kontext) stärkt.

- **Nur wenn der verlinkte Artikel die Aussage wirklich vertieft** – kein Link um des Links willen.
- **Ankertext natürlich in den Satz einbetten**, kein nacktes Keyword als Anker.
- **Quelle für gültige Blog-URLs ist ausschließlich der Live-Bestand aus Webflow** – die veröffentlichte Blog-Collection (primär über den Webflow-Connector) oder als Fallback die Übersichtsseite https://www.changexperten.com/blog. **Nie aus dem Gedächtnis und nie aus der SEO-Struktur-Excel** – die Excel ist ein historischer Recherchestand und nicht mehr deckungsgleich mit den Live-Seiten.
- Ist der Live-Bestand nicht abrufbar: keine Blog-zu-Blog-Links setzen, das offen melden, keine Slugs raten.

Die konkrete Abruf-Mechanik (Connector, Site-/Collection-ID) liegt in der jeweiligen Routine, nicht hier im Skill – dieser Skill legt nur fest, *dass* und *woraus* verlinkt wird.

Externe Links (1–2/1.000 Wörter): seriöse Quellen wie Springer, HBR, McKinsey, BCG, Deloitte, Gallup.

## 3. Tags

Genau drei Tags vergeben, die den Artikel passend beschreiben. **Nur Tags verwenden, die in Webflow bereits angelegt sind** – keine neuen Tags erstellen. Bei Unsicherheit, welche Tags existieren, vor der Vergabe nachfragen statt zu raten.

## 4. Bilder und Grafiken

Vollständig ausgelagert: [bilder-und-grafiken.md](bilder-und-grafiken.md). Dort stehen Drei-Ebenen-Modell, Bildplan, Quellenlogik, Vorlagenkatalog, Grafik-Auftrag und die Lizenzregeln. Diese Datei enthält bewusst keine zweite Fassung davon.

Kurzfassung für den On-Page-Check unten: 1 Hero, 4–6 Motivfotos, mindestens 1 eigene Grafik. Alt-Text max. 125 Zeichen, beschreibend. WebP, ≤150 KB. Kein Bild ohne dokumentierte Herkunft.

## 5. On-Page-Check (bei jeder Fertigstellung als Tabelle ausgeben)

Der Check ist zweispurig: Grundhygiene gilt immer, die Spur darunter richtet sich nach dem Feld „Content-Ziel". Nenne das Content-Ziel über der Tabelle, damit nachvollziehbar ist, welche Spur geprüft wurde.

**Immer (Grundhygiene):**

| Prüfpunkt | Erfüllt? | Anmerkung |
|---|---|---|
| Meta-Titel 50–60 Z., Meta-Description 140–160 Z., Slug kurz und sprechend | | |
| H-Struktur logisch: eine H1, H2 mit mind. 2 H3, Überleitungstexte vorhanden | | |
| Themen vollständig abgedeckt (verwandte Begriffe/Entitäten da) | | |
| Interne Links: Leistungsseiten aus der festen Liste (2–5/1.000 W.) + 2–3 Blog-zu-Blog-Links auf veröffentlichte Artikel (Live-URLs, nicht geraten); externe 1–2/1.000 W. | | |
| Jede Zahl belegt, mit korrekter Bezugsgröße, Quelle am Satz | | |
| Quellenblock „Quellen" als letzter Abschnitt: Leitquelle zuerst, Datum JJJJ-MM, Link aufs Original | | |
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
