# ETF-Radar · Almanach

Der ETF-Radar vergleicht jeden Tag 15 ETFs auf globale MSCI-Sektoren und -Faktoren mit dem MSCI World. Daraus entstehen zwei gleichrangige Mischungen, beide am Ende jedes Monats neu bestimmt und einen Monat gehalten. Der **ETF-Mix Balance** ist breit aufgestellt. Er hält die drei Indizes mit der höchsten Rendite der letzten 12 Monate zu gleichen Teilen und schwankt weniger. Der **ETF-Mix Fokus** ist gebündelt und hält ein bis drei Indizes mit der besten Rendite je Schwankung der letzten 12 Monate. Einmal im Monat erscheint auf LinkedIn ein Karussell mit den Monatsrenditen und einer Übersicht über 12 Monate.

Dieses Repository ist der Almanach zum ETF-Radar. Es erklärt, wie gerechnet wird, zeigt den Rückblick seit 2002, sammelt die Prüfberichte und beantwortet Fragen. Es enthält keinen Programmcode und keine Kursdaten.

> **Keine Anlageberatung.** Alle Zahlen beschreiben die Vergangenheit und sind eine Modellrechnung. Vergangene Wertentwicklung ist kein verlässlicher Hinweis auf künftige Ergebnisse. Kosten sind nur im Rückblick berücksichtigt, Steuern nur als Schätzung im [Prüfbericht](pruefbericht.md#steuern).

Der ETF-Mix Fokus hieß bis November 2026 ETF-Radar-Mix, der ETF-Mix Balance lief bis dahin als Vergleichsregel ‚3 beste mit Trend‘.

## Teil I · Das Verfahren

| Seite | Inhalt |
|---|---|
| [Methodik](methodik.md) | Das Verfahren Schritt für Schritt, mit Rechenbeispielen zum Nachrechnen, Begriffe und Quellen |

## Teil II · Der Rückblick

| Seite | Inhalt |
|---|---|
| [Gegenrechnung](gegenrechnung.md) | Wie der Rückblick entsteht, Jahr für Jahr seit 2002, die letzten 36 Monate, Test verschiedener Trendregeln |
| [Kapitel](kapitel.md) | Die 25 Jahre seit 2002 in Phasen mit ähnlicher Zusammensetzung, mit Grafik |

## Teil III · Prüfberichte

Jeder Prüfbericht bleibt mit seinem Datum stehen. Spätere Berichte ergänzen ihn, statt ihn zu überschreiben.

| Datum | Bericht | Frage |
|---|---|---|
| 04.11.2026 | [Nachrechnung und Signifikanz](pruefbericht.md) | Stimmen die Zahlen, ist der Vorsprung gesichert, wie schneidet Balance gegen Fokus ab, was kosten Steuern? |
| 04.11.2026 | [Wechseln oder kombinieren?](varianten.md) | Lässt sich vorher erkennen, ob Fokus oder Balance vorn liegen wird, und wie verbindet man beide am besten? |

## Teil IV · Fragen und Antworten

- [Sind es 15 oder 16 ETFs?](faq.md#sind-es-15-oder-16-etfs)
- [Was sind ETF-Mix Balance und ETF-Mix Fokus?](faq.md#was-sind-etf-mix-balance-und-etf-mix-fokus)
- [Was heißt „Rendite je Schwankung“?](faq.md#was-heißt-rendite-je-schwankung)
- [Warum „1.000-mal neu gemischt“? Was haben 1.000 Jahre mit 12 Monaten zu tun?](faq.md#warum-1000-mal-neu-gemischt-was-haben-1000-jahre-mit-12-monaten-zu-tun)
- [Was bedeuten die 94,5% auf der Methoden-Folie?](faq.md#was-bedeuten-die-945-auf-der-methoden-folie)
- [Warum 10 Monate bei der Trendregel und nicht 12?](faq.md#warum-10-monate-bei-der-trendregel-und-nicht-12)
- [Schaut der Rückblick in die Zukunft?](faq.md#schaut-der-rückblick-in-die-zukunft)
- [Warum steht bei Value einmal 44,9% und einmal 38,8%?](faq.md#warum-steht-bei-value-einmal-449-und-einmal-388)
- [Warum oft nur zwei oder drei ETFs?](faq.md#warum-oft-nur-zwei-oder-drei-etfs)
- [Warum Indexstände und nicht die Kurse der ETFs?](faq.md#warum-indexstände-und-nicht-die-kurse-der-etfs)
- [Sind Kosten und Steuern eingerechnet?](faq.md#sind-kosten-und-steuern-eingerechnet)
- [Ist der ETF-Radar besser als der MSCI World?](faq.md#ist-der-etf-radar-besser-als-der-msci-world)
- [Kann man zwischen Fokus und Balance wechseln, je nachdem wer gerade vorn liegt?](faq.md#kann-man-zwischen-fokus-und-balance-wechseln-je-nachdem-wer-gerade-vorn-liegt)
- [Was ist die Kombi aus Fokus und Balance?](faq.md#was-ist-die-kombi-aus-fokus-und-balance)
- [Ist das eine Empfehlung?](faq.md#ist-das-eine-empfehlung)
- [Kann ich das nachrechnen?](faq.md#kann-ich-das-nachrechnen)

## Kurz erklärt

1. **15 Sektoren und Faktoren und der MSCI World.** Täglich die Indexstände von MSCI (Net Total Return in Euro), vor ETF-Kosten. Fehlt ein Indexstand, springen Schlusskurse der ETFs von ARIVA.DE ein.
2. **Rendite je Schwankung.** Rendite über dem Zins geteilt durch die Schwankung der letzten 12 Monate (Sharpe Ratio). Für den ETF-Mix Fokus werden alle 32.767 Kombinationen der 15 ETFs geprüft.
3. **Einfach vor kompliziert.** Unter allen Mischungen mit mindestens 95% der besten Rendite je Schwankung gewinnt die mit den wenigsten ETFs.
4. **Zufallstest.** Die 12 Monate werden 1.000-mal in 10-Tage-Stücken neu gemischt. Fokus muss in mindestens 95% dieser Fälle mehr Rendite je Schwankung haben als der MSCI World. Dazu kommt eine Korrektur dafür, dass viele Mischungen probiert wurden.
5. **Trendregel.** Fällt Fokus unter den Durchschnitt seiner letzten 10 Monatsschlusskurse, gilt der MSCI World. Liegt auch der unter seinem Durchschnitt, gilt der Geldmarkt, verzinst wie der EZB-Einlagesatz, etwa über einen Geldmarkt-ETF oder Tagesgeld. Die 10 Monate stammen aus einer Studie von Mebane Faber (2007).
6. **ETF-Mix Balance.** Ein eigener Mix neben Fokus. Er hält die 3 Indizes mit der höchsten 12-Monats-Rendite zu gleichen Teilen. Liegt der MSCI World unter seinem Durchschnitt der letzten 10 Monatsenden, gilt der Geldmarkt. Balance ist breiter gestreut als Fokus und schwankt weniger.

## Stand

Die Beispielzahlen beziehen sich auf den Datenstand vom 30.10.2026, gerechnet mit MSCI-Indexständen. Das Karussell zeigt jeden Monat die aktuellen Werte.

Bis Oktober 2026 hieß das Projekt Sektor-Radar, daher der Name dieses Repos.

Stephan Büttig · Fragen und Hinweise gern als Kommentar unter dem LinkedIn-Beitrag.
