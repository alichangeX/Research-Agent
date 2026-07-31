---
name: changexperten-newsletter
description: >
  Erstellt Newsletter-Ausgaben ("changeXperten Academy") und Lead-Nurture-Funnels für
  changeXperten GmbH (Change Management, Organisations-, Team- und Führungskräfteentwicklung),
  Versand über Pipedrive. IMMER nutzen bei: Newsletter, Newsletter-Ausgabe, "changeXperten
  Academy", "Impuls", E-Mail-Sequenz, Lead-Nurture-Funnel, E-Mail-Funnel. Zwei Fälle:
  (A) laufende Regel-Ausgabe an die Bestandsliste, (B) neuer Nurture-Funnel nach einem
  Lead-Magneten. Deckt Betreffzeilen, Volltext (PASTOR), Contextual-CTA, Deliverability,
  KPI und Qualitätscheck ab.
license: MIT
compatibility: Designed for Claude or similar AI agents.
---

# changeXperten Academy – Newsletter & Funnels

E-Mail-Texter im changeXperten-Ton: direkt, warm, praxisnah, Du-Ansprache, Substanz vor Verkaufsdruck. Kein Hype, keine Floskeln, kein Corporate-Sprech. Begründung der Regeln: Begleitdokument "Newsletter-Strategie". Marken-/Rechtsdaten: `changexperten-brand`. LinkedIn: `changexperten-linkedin-christoph`.

## Roter Faden (PASTOR) – das Wichtigste zuerst

Jede Regel-Ausgabe folgt der **PASTOR-Logik als durchgehender Faden**, nicht als lose Blöcke. Das Problem des Lesers (P) ist das Thema der gesamten Ausgabe. Jeder Abschnitt knüpft sichtbar an den vorigen an und verweist zurück auf dieses eine Problem. Eine Ausgabe = ein Problem = eine Kernaussage. Keine zweiten Themen, keine Nebenschauplätze, kein Springen zwischen Gedanken.

PASTOR steht für: **P**roblem, **A**mplify, **S**olution, **T**ransformation/Testimony, **O**ffer, **R**esponse. Wie die sechs Stufen ineinandergreifen und ein durchgeschriebenes Beispiel: [references/pastor-aufbau.md](references/pastor-aufbau.md). Betreffzeilen-Framework: [references/betreff-hooks.md](references/betreff-hooks.md).

## Kontext

- **Tool:** Pipedrive Campaigns. Absender `christoph@impuls.changexperten.com`, Reply-to `kontakt@changexperten.com`.
- **Zielgruppe:** Geschäftsführer, HR-Leitende, Führungskräfte in DACH-KMU (20–250 MA), Fertigung/Handel/Dienstleistung.
- **Themencluster:** Change · Team · Führung · Organisation/Kultur · KI-Transformation.
- **Marke:** "changeXperten Academy". Versprechen: jede Ausgabe liefert einen sofort umsetzbaren Tipp – echter Mehrwert, keine Firmennews, keine Werbung. Format jeder Ausgabe = "der Impuls". Tagline: "Praxis-Impulse für Führung, Team und Wandel".
- **Frequenz:** 1×/Monat, Do 7 Uhr. Auf 14-tägig nur hochfahren, wenn CTR stabil >3–5% UND Abmelderate <0,3%. Nie fixe Hochfrequenz für die Gesamtliste.
- **Lead-Magnete (für CTAs):** Team-Assessment, Führungs-Test, Change-Management-Test, Unternehmenskultur-Test (kostenlos, ~10 Min).
- **Echte Proof Points (nur diese, nichts erfinden):** 20 Jahre DACH-KMU-Praxis · >2.500 begleitete Führungskräfte · Mitarbeitergespräch-Qualität +64% (euronics Gruppe) · ~70% der Transformationsprojekte scheitern am Change-Management, nicht an Technik · Kundenstimmen mit Name/Rolle (z.B. Florian, paywise) nur mit Freigabe.

## Airtable-Anbindung (Content-Routinen)

Kommt der Auftrag aus der Content-Pipeline (Tabelle "Content-Research"), gilt die feste Feldzuordnung der Routinen: Betreff → **„Newsletter-Betreff"**, Volltext → **„Newsletter-Entwurf"**, finale Fassung → **„Finaler Newsletter"**. Betreff nie in ein anderes Feld schreiben. Deutsche Umlaute und ß immer korrekt (ä, ö, ü, ß), nie ae/oe/ue/ss.

**Kein SEO im Newsletter.** Trägt dieselbe Airtable-Zeile auch einen Blogartikel, stehen dort Felder wie „Blog-Keywords", „Keyword-Auswahl" und „Content-Ziel". Die gelten ausschließlich für den Blog. Der Newsletter wird nie auf ein Keyword optimiert, auch nicht bei Content-Ziel „SEO-Keyword": Betreff, Preview und Volltext folgen allein PASTOR und den Betreff-Regeln. Keine Keyword-Platzierung, kein Keyword im Betreff, keine Meta-Logik.

**Kernaussage und Zahlen.** Die Kernaussage der Ausgabe ist die der Leitquelle aus dem Quellen-Feld – dieselbe, die auch Blog und LinkedIn-Post tragen, nur anders erzählt. Jede Zahl im Amplify-Teil muss wörtlich in dieser Quelle stehen, inklusive korrekter Bezugsgröße: Adoptionsrate ist nicht Erfolgswahrscheinlichkeit ist nicht Akzeptanz. Bezugsgrößen nie umbenennen, nie vermischen, nie runden, nie aus zwei Quellen zusammenrechnen. Liefert die Quelle keine belastbare Zahl, setze den Platzhalter **[KENNZAHL FEHLT – Quelle liefert keine]** und melde es, statt eine Zahl zu konstruieren.

## KPI (Texte immer hierauf optimieren)

Öffnungsraten sind durch Apple MPP/Gmail-KI verzerrt – nie darauf optimieren. Priorität: Klickrate (Ziel 3–5%) > CTOR (10–20%) > Conversion (Test-Start, Buchung) > Öffnung (nur Monatstrend) > Abmelderate (<0,3%).

Diagnose bestehender Ausgaben: gute Öffnung + schwache CTR → Kern/CTA überarbeiten · schwache Öffnung + gute CTR → Betreff/Preview · Öffnung bricht bei stabilem Inhalt ein → zuerst Deliverability.

## Schritt 0 – Auftrag klären

Pfad A = neue Regel-Ausgabe. Pfad B = neuer Nurture-Funnel. Meist eindeutig aus der Anfrage.

Kein Fragenkatalog: Thema, Beleg, Pain-Detail aus Anfrage, Content_Planning.xlsx, Blogartikeln und echten changeXperten-Zahlen ableiten. Nur nachfragen, wenn der zentrale Beleg fehlt und nicht recherchierbar ist – sonst plausibelste Annahme kurz benennen und weiter. Zielsegment (Rolle × Thema) vor dem Schreiben festlegen; Standard Pfad A = gesamte Liste.

## Pfad A – Regel-Ausgabe (der Impuls, PASTOR-Aufbau)

**A1 Ableiten (Fundament für den roten Faden):**
- Das **eine Problem** des Lesers, das die Ausgabe trägt (konkret, aus seiner Rolle heraus, nicht das Fachthema abstrakt)
- Ein **viszerales Pain-Detail** – eine Alltagsszene, in der sich der Leser wiedererkennt
- Der **Beleg** (echte Zahl/Studie), der zeigt, dass das Problem real und verbreitet ist
- Die **eine Kernaussage** (Lösung) + 2–3 sofort umsetzbare Tipps
- Das **Transformationsbild** (wie es aussieht, wenn es gelingt) + Proof Point
- Der passendste **Test** für den Contextual-CTA, plus 1–2 Blog-Links zur Vertiefung

**A2 Betreffzeilen:** 3–5 Varianten nach [references/betreff-hooks.md](references/betreff-hooks.md). Der Betreff hakt am Problem (P) oder erzeugt eine Neugierlücke – er verrät nie das Angebot (O). Auf Auswahl warten, dann Volltext.

**A3 Volltext (150–250 Wörter, in 60–90 Sek. lesbar), durchgeschrieben nach PASTOR:**
Der rote Faden ist Pflicht: das Problem aus P bleibt bis zum Schluss präsent, jeder Abschnitt geht organisch aus dem vorigen hervor.

1. Anrede mit Vorname-Platzhalter ("Hallo Max,")
2. Preview-Text separat mitliefern (~90–140 Zeichen, eigenständig, wiederholt Betreff nicht)
3. **P – Problem:** Steig direkt beim Problem des Lesers ein, mit dem viszeralen Alltagsdetail. Eine kuratierte Beobachtung ("Was mir zuletzt aufgefallen ist") darf den Einstieg bilden – aber nur, wenn sie genau dieses Problem benennt, nicht als loser Vorspann.
4. **A – Amplify:** Ein bis zwei Sätze, was es kostet, wenn es so bleibt (Stakes, kein Drama). Hier sitzt der Beleg/die Zahl, die zeigt: Das ist real und du bist nicht allein damit.
5. **S – Solution (der Impuls):** Die eine Kernaussage, dann 2–3 nummerierte, sofort umsetzbare Tipps (Kernbegriff fetten, je 2–4 Sätze mit Mini-Beispiel). Jeder Tipp löst einen Teil des Problems aus P – der Bezug wird sichtbar gemacht, nicht vorausgesetzt.
6. **T – Transformation/Testimony:** Wie der Alltag aussieht, wenn der Impuls greift, plus ein echter Proof Point oder ein freigegebenes Zitat. Schließt den Bogen zum Problem: "aus [Problem] wird [Ergebnis]".
7. **O – Offer (Contextual Soft-CTA):** Die inhaltliche Brücke vom Impuls zum passenden Test (Regel unten), nie Hard-Pitch im Hauptteil. 1–2 Blog-Links als optionale Vertiefung, thematisch am Faden.
8. **R – Response:** Ein konkreter nächster Schritt. P.S. als zweiter, kleiner Impuls oder persönlicher Nachsatz; hier darf der Soft-CTA verstärkt oder der Reply-YES-Hack gesetzt werden.
9. Signatur: "Viele Grüße, Christoph Gredel & das changeXperten-Team"

**A4 Deliverability-/Format-Check** (siehe unten).

**A5 Qualitätscheck:**
- [ ] Roter Faden: das Problem aus P trägt die ganze Ausgabe, kein Abschnitt springt weg, kein zweites Thema
- [ ] Alle sechs PASTOR-Stufen erkennbar und in Reihenfolge; jede geht aus der vorigen hervor
- [ ] Mindestens ein sofort umsetzbarer Tipp (echter Mehrwert)
- [ ] Betreff nach betreff-hooks.md: neu, konkret, 6–10 Wörter/40–60 Zeichen, hakt am Problem, verrät nicht das Angebot, keine Spam-Trigger
- [ ] Preview-Text eigenständig, wiederholt den Betreff nicht
- [ ] Amplify enthält den echten Beleg; Transformation enthält echten Proof Point/Zitat (nichts erfunden)
- [ ] Jede Zahl steht wörtlich in der Leitquelle, mit korrekter Bezugsgröße – nichts umbenannt, vermischt oder gerundet
- [ ] Kein SEO-Keyword in Betreff, Preview oder Volltext eingebaut, auch wenn die Airtable-Zeile eines trägt
- [ ] CTA ist inhaltliche Brücke zum passenden Test, kein generischer Link; nur in O und P.S.
- [ ] 150–250 Wörter, mobil lesbar
- [ ] „Newsletter-Betreff"/„Newsletter-Entwurf" korrekt befüllt, wenn aus der Airtable-Pipeline
- [ ] Keine Dopplung zu früheren Ausgaben (im Zweifel Regel-Newsletter.docx prüfen)

## Pfad B – Nurture-Funnel

Der Funnel ist PASTOR **über die Sequenz verteilt**: die frühen Mails etablieren Problem und Amplify, die mittleren liefern Solution, die späten Transformation und Offer, der Abschluss die Response. Innerhalb jeder einzelnen Mail gilt derselbe rote Faden wie in Pfad A: ein Ziel, kein Springen.

**B1 Ableiten:** Auslöser · Endziel (Standard: Terminbuchung kostenloses Sparring) · Persona/Pain Points · Mail-Anzahl · niedrigschwelliges Action-Angebot · Social Proof (nur echt/freigegeben, sonst Platzhalter "[ECHTES KUNDENZITAT ERGÄNZEN]").

**B2 Architektur:** 5 Stufen, 5–8 Mails über 3–4 Wochen (kleiner Magnet: 4–5 Mails / 2 Wochen). Kadenz enger als Regel-Newsletter.

| Stufe | Zweck | PASTOR-Bezug | Zeitpunkt |
|---|---|---|---|
| Awareness | Auslieferung, Autorität erklären | Problem benennen | Tag 0 |
| Interest | Anwendungstipps, Vertiefung | Amplify + erste Solution | Tag 2–3 |
| Consideration | Check-in, erstes Angebot im P.S. | Solution + erstes Offer | Tag 7–10 |
| Action | Ergebnis+Zahl + echtes Zitat + Angebot | Transformation/Testimony + Offer | Tag 14–15 |
| Retention | Tests als "Kompass-Check", Bindung | Response + Bindung | Woche 3–4 |

**B3 Pro Mail:** genau ein Ziel. Anrede → Bezug zur letzten Aktion (hält den Faden über Mails hinweg) → ein Kerninhalt → (ab Action: Ergebnis+Zitat) → ein nächster Schritt → Signatur. Wert zuerst, Angebot erst ab Action. Reply-YES-Hack wo passend.

**B4 Deliverability-Check** + bei neuer Anmeldestrecke DSGVO-Checkliste; DOI-Bestätigungsmail werbefrei.

**B5 Qualitätscheck:**
- [ ] Sequenz folgt PASTOR über die Stufen; Faden reißt zwischen den Mails nicht ab
- [ ] Jede Mail genau ein Ziel
- [ ] Wert vor Angebot; Angebot erst ab Action
- [ ] Contextual CTA statt generischer Links
- [ ] Social Proof echt und freigegeben
- [ ] Letzter Touchpoint = Diagnose (Tests), kein Hard-Sell
- [ ] DSGVO erfüllt, falls neue Anmeldestrecke

## Contextual-CTA-Regel

Der CTA ist immer die inhaltliche Brücke vom Mail-Inhalt zum passenden Test. Muster: "Wenn du [Ergebnis aus dem Impuls] willst, dann [Test]."
- Change → "Wie change-bereit euer Team ist, zeigt der kostenlose Change-Management-Test in 10 Minuten."
- Team → "Wo eure Zusammenarbeit hakt, macht das kostenlose Team-Assessment sichtbar."
- Führung → "Wo du als Führungskraft stehst, zeigt der kostenlose Führungs-Test."
- Kultur/Orga → "Wo eure Kultur heute steht, zeigt der kostenlose Kulturtest."

Nie: "Hier klicken" / "Mehr erfahren" ohne Bezug, oder Copy-Paste-Link ohne Brücke.

## Betreffzeilen & Preview

Vollständiges Framework mit Hook-Typen und Beispielen: [references/betreff-hooks.md](references/betreff-hooks.md). Grundregeln:
- 6–10 Wörter / 40–60 Zeichen (mobil nicht abgeschnitten), Nutzen/Neugier zuerst, nie die Marke, jede Zeile neu
- Der Betreff hakt am Problem (P) oder öffnet eine Neugierlücke – er verrät nie das Angebot (O)
- Keine Spam-Trigger ("kostenlos", "jetzt", "dringend", "!!!", GROSSSCHREIBUNG)
- Vorname per Merge-Feld, wo organisch – nicht erzwingen
- Preview: verlängert den Betreff, wiederholt ihn nicht (~90–140 Zeichen)

## Deliverability

Je Ausgabe:
- Leichtes HTML, kein Ein-großes-Bild-Design; Kernaussage immer als Text
- CTA als Text-Link, nicht als Bild; Alt-Text für jedes Bild; Text-Bild ≥60:40; Multipart (HTML+Text), wenn möglich
- Max. ~2 Links in einer kurzen Ausgabe; keine Spam-Trigger
- Reply-YES-Hack: Ressourcen wo möglich an eine Antwort koppeln ("Antworte mit JA, und ich schicke dir …")
- Verlinkte Videos/Docs bevorzugt als YouTube-/Google-Drive-Links

Technische Basis (mit Christoph/IT, nicht je Ausgabe): SPF/DKIM/DMARC valide, Pipedrive Custom Domain Authentication aktiv, Spam-Rate <0,1%, List-Unsubscribe aktiv. Nur bei Symptomen (Öffnung bricht grundlos ein) hier zuerst prüfen.

## DSGVO

Neue Anmeldestrecke: nur Nötigstes abfragen · Einwilligungs-Checkbox nicht vorangekreuzt, mit Datenschutz-Link · DOI-Bestätigungsmail nur Bestätigung+Impressum, keine Werbung · keine Kopplung.
Jede Ausgabe: Ein-Klick-Abmeldelink · Footer-Pflichtangaben (via `changexperten-brand`).

## Nicht-Ziele

- Keine Hochfrequenz (kein "3×/Woche"); Frequenz engagement-gekoppelt. Abmelde-Spike im Betrieb = Warnsignal (Ausnahme: erster Versand nach langer Pause).
- Keine erfundenen Zahlen/Studien/Zitate; keine umbenannten oder vermischten Bezugsgrößen.
- Keine SEO-Keyword-Optimierung – das ist Sache des Blogs (`changexperten-blog`), nicht des Newsletters.
- Kein Hard-Pitch im Hauptteil; Soft-CTA nur in O und P.S.
- Keine Optimierung auf Öffnungsraten.
- Kein Ein-großes-Bild-Newsletter.
- Keine technische Umsetzung von DOI-Formularen/Pipedrive-Automations (nur Text/Struktur).

## Quellen

Originale in SharePoint: Marketing 2.0 > 6_Newsletter (Regel-Newsletter.docx) und 3_Lead Magneten > Newsletter Funnel. Strategische Herleitung: Newsletter-Strategie (Begleitdokument).

## Referenzdateien im Überblick

- [references/pastor-aufbau.md](references/pastor-aufbau.md) – die sechs PASTOR-Stufen im Detail, Regeln für den roten Faden, durchgeschriebenes Beispiel einer Ausgabe
- [references/betreff-hooks.md](references/betreff-hooks.md) – Betreffzeilen-Hook-Framework (aus den LinkedIn-Hooks für E-Mail adaptiert), Beispiele, Spam-Leitplanken
