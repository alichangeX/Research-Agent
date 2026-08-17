# Performance-Tracking für Themen-Recycling

## Warum diese Datei nötig ist

Dieser Skill hat keinen direkten Zugriff auf LinkedIn-Analytics. Es gibt aktuell keinen Connector, der Impressions, Saves oder Kommentarzahlen automatisch abruft. Ohne eine Datenquelle kann nicht erkannt werden, welcher Post gut performt hat. Deshalb basiert das Themen-Recycling in Phase 0 auf einem einfachen, manuell gepflegten Log statt auf einer automatischen Auswertung.

## Empfohlenes Format: Post-Performance-Log

Eine einfache Tabelle, die nach jedem Post kurz ergänzt wird (z. B. als eigenes Tab in Content_Planning.xlsx oder als separates Dokument in SharePoint unter Marketing 2.0):

| Datum | Thema | Kategorie | Hook (Kurzfassung) | Format | Saves | Kommentare | Impressions | Recycling-Status |
|---|---|---|---|---|---|---|---|---|
| 2026-06-12 | Kündigung als Führungserfolg | Leadership Thought | "Mein bester Mitarbeiter hat gekündigt..." | Text | 34 | 22 | 8.100 | offen |
| 2026-06-19 | 3 Schritte gegen Silodenken | Actionable Guide | "70% der Reorganisationen scheitern..." | Carousel | 51 | 14 | 6.400 | offen |

**Pflegeaufwand:** ca. 1 Minute pro Post, im Idealfall direkt nach dem Login in LinkedIn Analytics (Post-Statistiken sind dort ca. 7 Tage nach Veröffentlichung stabil genug für einen Eintrag).

## Wie der Skill damit arbeitet

1. **Log vorhanden** (als hochgeladene Datei im Chat, verlinktes SharePoint-Dokument oder eingefügter Text): Die 1–2 Einträge der letzten 4–6 Wochen mit den höchsten Save- und Kommentarzahlen identifizieren. Deren Thema als Recycling-Vorschlag einbringen, mit Hinweis auf die ursprünglichen Zahlen ("Der Post zu X lief mit 51 Saves überdurchschnittlich, ein neuer Blickwinkel darauf könnte sich lohnen").
2. **Kein Log vorhanden oder nicht zugänglich:** Direkt und konkret nachfragen, nicht raten: "Gab es in den letzten 4–6 Wochen einen Post, der besonders gut lief (viele Saves/Kommentare)? Welches Thema war das?" Ohne Antwort normal mit Phase 0 (neue Themenfindung) fortfahren, das Recycling ist ein Bonus-Schritt, kein Blocker.
3. **Nach Fertigstellung eines neuen Posts:** Christoph/Ali daran erinnern, den neuen Post nach ca. 1 Woche ins Log einzutragen, damit das Recycling beim nächsten Mal wieder funktioniert. Das ist eine Erinnerung, keine Pflicht, die den Skill-Ablauf blockiert.

## Was der Skill NICHT kann

- Kein automatisches Auslesen von LinkedIn-Statistiken
- Keine Erkennung von Performance ohne das gepflegte Log oder eine direkte Angabe von Christoph
- Sollte künftig ein LinkedIn-Analytics-Connector verfügbar werden, kann dieser Mechanismus durch einen automatischen Abruf ersetzt werden. Bis dahin ist das manuelle Log der einzig verlässliche Weg.
