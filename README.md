# ETF-Radar · Almanach

Das ETF-Radar vergleicht jeden Tag 15 ETFs auf globale MSCI-Sektoren und -Faktoren mit dem MSCI World. Einmal im Monat erscheint auf LinkedIn ein Karussell mit den Monatsrenditen, einer Übersicht über 12 Monate und dem **ETF-Radar-Mix**. Der Mix ist die Mischung, die in den letzten 12 Monaten am meisten Rendite je Schwankung gebracht hat, mit möglichst wenigen ETFs. Er wird am Ende jedes Monats neu bestimmt und einen Monat gehalten. Als zweite, einfache Regel läuft „3 beste mit Trend“ mit.

Dieses Repository ist der Almanach zum ETF-Radar. Es erklärt, wie gerechnet wird, zeigt den Rückblick seit 2002, sammelt die Prüfberichte und beantwortet Fragen. Es enthält keinen Programmcode und keine Kursdaten.

> **Keine Anlageberatung.** Alle Zahlen beschreiben die Vergangenheit und sind eine Modellrechnung. Vergangene Wertentwicklung ist kein verlässlicher Hinweis auf künftige Ergebnisse. Kosten sind nur im Rückblick berücksichtigt, Steuern nur als Schätzung im [Prüfbericht](pruefbericht.md#steuern).

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
| 04.11.2026 | [Nachrechnung und Signifikanz](pruefbericht.md) | Stimmen die Zahlen, ist der Vorsprung gesichert, wie schlägt sich eine einfache Regel, was kosten Steuern? |
| 04.11.2026 | [Wechseln oder kombinieren?](varianten.md) | Lässt sich vorher erkennen, ob Mix oder 3er-Regel vorn liegen wird, und wie verbindet man beide am besten? |

## Teil IV · Fragen und Antworten

- [Sind es 15 oder 16 ETFs?](faq.md#sind-es-15-oder-16-etfs)
- [Was ist der ETF-Radar-Mix?](faq.md#was-ist-der-etf-radar-mix)
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
- [Kann man zwischen Mix und 3er-Regel wechseln, je nachdem wer gerade vorn liegt?](faq.md#kann-man-zwischen-mix-und-3er-regel-wechseln-je-nachdem-wer-gerade-vorn-liegt)
- [Was ist die Kombi aus Mix und 3er-Regel?](faq.md#was-ist-die-kombi-aus-mix-und-3er-regel)
- [Ist das eine Empfehlung?](faq.md#ist-das-eine-empfehlung)
- [Kann ich das nachrechnen?](faq.md#kann-ich-das-nachrechnen)

## Kurz erklärt

1. **15 Sektoren und Faktoren und der MSCI World.** Täglich die Indexstände von MSCI (Net Total Return in Euro), vor ETF-Kosten. Fehlt ein Indexstand, springen Schlusskurse der ETFs von ARIVA.DE ein.
2. **Rendite je Schwankung.** Rendite über dem Zins geteilt durch die Schwankung der letzten 12 Monate (Sharpe Ratio). Geprüft werden alle 32.767 Kombinationen der 15 ETFs.
3. **Einfach vor kompliziert.** Unter allen Mischungen mit mindestens 95% der besten Punktzahl gewinnt die mit den wenigsten ETFs.
4. **Zufallstest.** Die 12 Monate werden 1.000-mal in 10-Tage-Stücken neu gemischt. Der Mix muss in mindestens 95% dieser Fälle mehr Rendite je Schwankung haben als der MSCI World. Dazu kommt eine Korrektur dafür, dass viele Mischungen probiert wurden.
5. **Trendregel.** Fällt der Mix unter den Durchschnitt seiner letzten 10 Monatsschlusskurse, gilt der MSCI World. Liegt auch der unter seinem Durchschnitt, gilt Zins. Die 10 Monate stammen aus einer Studie von Mebane Faber (2007).
6. **3 beste mit Trend.** Die 3 Indizes mit der höchsten 12-Monats-Rendite zu gleichen Teilen, Zins, wenn der MSCI World unter seinem Durchschnitt der letzten 10 Monatsenden liegt.

## Stand

Die Beispielzahlen beziehen sich auf den Datenstand vom 30.10.2026, gerechnet mit MSCI-Indexständen. Das Karussell zeigt jeden Monat die aktuellen Werte.

Bis Oktober 2026 hieß das Projekt Sektor-Radar, daher der Name dieses Repos.

Stephan Büttig · Fragen und Hinweise gern als Kommentar unter dem LinkedIn-Beitrag.
