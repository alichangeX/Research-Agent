# Keyword-Freigabe und Content-Ziel

## Warum dieser Schritt existiert

Nicht jeder Blogartikel braucht ein Keyword. Keyword-Optimierung zahlt sich nur aus, wenn es echtes Suchvolumen **mit passender Suchintention** gibt. Studienbasierte Artikel wirken oft über einen anderen Kanal: sie werden von ChatGPT, Perplexity und Google AI Overviews zitiert, stärken die Themencluster als interne Linkziele und liefern Material für Newsletter und LinkedIn. Dafür braucht es kein Keyword, sondern klare Antworten, saubere Struktur und belegte Aussagen.

Ein schwaches Keyword in einen Text zu pressen verwässert ihn und bringt weder Rankings noch Zitate. Deshalb gibt es hier zwei mögliche Ergebnisse, die beide korrekt sind: SEO-Keyword oder GEO-Autorität. Dieser Schritt entscheidet, welches von beiden gilt, und dokumentiert die Entscheidung im Feld „Content-Ziel".

## Woher die Daten kommen

Der Regelweg ist automatisiert: Sobald **Christoph** eine Zeile in Tabelle **„04 Blog"** (`tblzTKBLsewsvoCis`) auf Status „Ausgewählt" setzt – das ist seine Themenfreigabe und die trifft er allein, Claude schlägt nur vor –, passiert Folgendes:

1. Das Make-Szenario „Blog Keywords finden + Suchvolumen" (ID 9553651) leitet aus Thema, Blog-Winkel, Cluster und Inhalt vier Seed-Keywords ab.
2. DataForSEO liefert dazu Keyword-Vorschläge mit echtem Suchvolumen für Deutschland. Alles ab 20 Suchanfragen/Monat landet als ungefilterte Rohliste im Feld „Blog-Keywords".
3. Ein Keyword-Gate prüft die Rohliste gegen Thema, Blog-Winkel, Kerninhalt und Quellen: es dedupliziert, verwirft Begriffe aus fremden Bedeutungsfeldern und schlägt eine kuratierte Auswahl plus ein Content-Ziel vor.

**Ersatzweg seit 08/2026 – nicht auf Make warten.** Der Produktionslauf ist täglich und kann ein Thema am Morgen nach der Freigabe aufgreifen; das Make-Szenario ist dann eventuell noch nicht durchgelaufen. Sind „Keyword-Auswahl" und „Content-Ziel" beim Start leer, recherchiert Claude selbst über den **DataForSEO-Konnektor**, statt den Artikel zu verschieben:

- `dataforseo_labs_google_keyword_ideas` oder `dataforseo_labs_google_keyword_suggestions` (`location_name` „Germany", `language_code` „de") auf Basis von Thema und Blog-Winkel
- `dataforseo_labs_google_keyword_overview` oder `kw_data_google_ads_search_volume` für das Volumen
- `dataforseo_labs_bulk_keyword_difficulty` für die Schwierigkeit

Auswahlmaßstab bleibt derselbe wie beim Make-Gate: relevant zur Kernaussage, Suchvolumen realistisch erreichbar. Im Zweifel Long-Tail mit klarer Intention statt Kopf-Keyword mit hoher Difficulty. Die Rohliste geht nach „Blog-Keywords", der kuratierte Vorschlag nach „Keyword-Auswahl", das Volumen nach „Haupt-Keyword-Volumen", und in „Notizen Redaktion" wird vermerkt, dass die Keywords direkt per Konnektor kamen. Findet DataForSEO kein tragfähiges Keyword: „Keyword-Auswahl" = „verworfen: [Grund]", „Content-Ziel" = „GEO-Autorität".

Google Keyword Planner braucht es für neue Artikel nicht. Die **Search Console** ist inzwischen über Pipedream angebunden und liefert monatlich echte Klick-, Impressions- und Positionsdaten in die Reporting-Tabellen – relevant für den Refresh bereits veröffentlichter Artikel (`seo-audit`) und für die Frage, ob ein Bestandsartikel für ein Keyword schon rankt.

## Die vier Felder und ihre Rollen

| Feld | Inhalt | Wer schreibt |
|---|---|---|
| Blog-Keywords | ungefilterte DataForSEO-Rohliste, Format „keyword (ca. X/Monat)" | Make; nur wenn das Feld leer geblieben ist, schreibt Claude die selbst recherchierte Rohliste hinein – eine von Make gefüllte Liste wird nie überschrieben |
| Keyword-Auswahl | kuratierter Vorschlag „Haupt: [Keyword] (Volumen) \| Sekundär: [Keyword] (Volumen), …" oder „verworfen: [Grund]" | Keyword-Gate, danach der Produktionslauf „Content D" / dieser Skill |
| Content-Ziel | SEO-Keyword · GEO-Autorität · Beides | Gate schlägt vor, dieser Skill entscheidet endgültig |
| Haupt-Keyword-Volumen | Suchvolumen des Haupt-Keywords | Keyword-Gate |

Eine von Make gefüllte Rohliste bleibt als Nachweis stehen. Wer sie überschreibt, macht die Entscheidung nicht mehr nachvollziehbar und bricht den Trigger des Make-Szenarios.

## Reihenfolge: Quelle zuerst, dann Keyword

Die Keyword-Entscheidung fällt **nach** dem Quellen-Refresh, nie davor. Wer sich zuerst auf ein Keyword festlegt und danach die Leitquelle liest, schreibt am Ende einen Text, der dem Keyword folgt statt der Quelle. Genau daraus entstehen Artikel, die nicht mehr zu ihren Quellen passen.

Ablauf:
1. Leitquelle abrufen, Kernaussage und die konkreten Zahlen mit ihren exakten Bezugsgrößen festhalten (siehe [recherche.md](recherche.md)).
2. Erst danach „Keyword-Auswahl" und „Content-Ziel" lesen.

## Die Freigabe-Prüfung

Prüfe genau eine Frage: **Beantwortet der Artikel, den diese Kernaussage hergibt, tatsächlich die Suchintention hinter dem Haupt-Keyword?**

- **Ja** → „Content-Ziel" bestätigen, „Keyword-Auswahl" unverändert lassen. Es gelten die SEO-Platzierungen.
- **Nein** → das Keyword zielt auf eine andere Frage, eine andere Zielgruppe oder eine allgemeinere Ebene, als die Quelle trägt. Setze „Content-Ziel" auf „GEO-Autorität", überschreibe „Keyword-Auswahl" mit „verworfen: [konkreter Grund]" und begründe es in „Notizen Redaktion". Es gelten die GEO-Pflichten.
- Steht in „Keyword-Auswahl" schon „verworfen: …" oder in „Content-Ziel" schon „GEO-Autorität": übernehmen, nichts nachprüfen, GEO-Pflichten anwenden.
- Steht „Beides": SEO-Platzierungen **und** GEO-Pflichten gelten gemeinsam.

Erzwinge in keinem Fall ein Keyword, das nicht in der Auswahl steht. Suche auch keinen Ersatz aus der Rohliste, wenn das Gate verworfen hat – das Gate hatte die Quellen bereits vorliegen.

## Wenn Felder leer sind

Sind „Keyword-Auswahl" und „Content-Ziel" beide leer, hat das Make-Szenario diese Zeile noch nicht verarbeitet. Dann nicht selbst recherchieren und nicht raten: Zeile liegen lassen, offen benennen, im nächsten Lauf mitnehmen. Läuft dieser Skill außerhalb der Pipeline (Einzelauftrag von Ali/Christoph ohne Airtable-Zeile), triff die Entscheidung nach denselben Schwellen selbst und benenne sie im Ergebnis:

- Haupt-Keyword: ab 50 Suchanfragen/Monat **und** Suchintention deckt sich mit der Kernaussage. Ein brauchbares Keyword nimmst du mit, auch wenn es nicht das volumenstärkste ist.
- Sekundär-Keywords: ab 20/Monat, maximal 5, müssen dieselbe Suchintention vertiefen.
- Kein Kandidat erfüllt das → GEO-Autorität. Keine Zahl schätzen, kein Volumen erfinden.

## Keine Keyword-Kannibalisierung

Vor der Freigabe eines Haupt-Keywords prüfen, ob ein bereits veröffentlichter Blogartikel dieselbe Suchintention bedient. Zwei Artikel auf dasselbe Haupt-Keyword schwächen sich gegenseitig im Ranking.

- **Bestandsquelle ist der Live-Bestand aus Webflow** – die veröffentlichte Blog-Collection (primär über den Webflow-Connector) oder als Fallback die Übersichtsseite https://www.changexperten.com/blog. **Nicht die SEO-Struktur-Excel** als Prüfgrundlage nutzen: Sie ist ein historischer Recherchestand, dessen Titel und Meta-Daten nicht mehr deckungsgleich mit den Live-Seiten sind. Live schlägt Excel.
- **Über Suchintention vergleichen, nicht über Wortgleichheit.** „Konfliktgespräch führen" und „Konflikte im Team lösen" teilen Wörter, bedienen aber verschiedene Intentionen – das ist keine Kollision. Entscheidend ist, ob ein Bestandsartikel dieselbe Frage derselben Zielgruppe beantwortet.
- **Kollision heißt nicht automatisch verwerfen.** Gibt es einen konkreten neuen Anlass (neue Studie/Statistik/Ereignis), ist die Aktualisierung des Bestandsartikels oft der bessere Weg als ein Konkurrenzartikel – mit Ali/Christoph klären, ob aktualisiert statt neu geschrieben wird. Ohne neuen Anlass: diesen Artikel auf GEO-Autorität umstellen oder das Thema fallen lassen.
- Ist der Live-Bestand nicht abrufbar, das Keyword regulär freigeben und die ungeprüfte Kollisionslage offen vermerken statt zu raten.

Innerhalb der automatisierten Pipeline findet diese Prüfung zweistufig statt: als frühes Gate beim Themenvorschlag und als zweites Netz vor der finalen Keyword-Freigabe im Produktionslauf. Bei manuellen Aufträgen greift sie hier an dieser Stelle.

**Zweite Prüfspur über echte Rankings (neu seit 08/2026):** Neben dem Live-Bestand aus Webflow prüft der Produktionslauf das Haupt-Keyword zusätzlich gegen die tatsächlichen Rankings der Domain – `dataforseo_labs_google_ranked_keywords` mit `target` „changexperten.com", Germany/de. Rankt eine bestehende Seite für das Keyword schon in den Top 20, gilt es als besetzt, selbst wenn der Titel des Bestandsartikels anders klingt. Dann ist die Aktualisierung dieser Seite der bessere Weg als ein neuer Artikel; der Vorschlag samt betroffener URL gehört in „Notizen Redaktion".
