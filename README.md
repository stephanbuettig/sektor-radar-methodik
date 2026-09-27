# Sektor-Radar · Methodik

Das Sektor-Radar vergleicht jeden Tag 15 ETFs auf globale MSCI-Sektoren und -Faktoren mit dem MSCI World. Einmal im Monat erscheint auf LinkedIn ein Karussell mit den Monatsrenditen, einer Übersicht über 12 Monate und dem **Sektor-Radar-Mix**. Der Mix ist die Mischung, die in den letzten 12 Monaten am meisten Rendite je Schwankung gebracht hat, mit möglichst wenigen ETFs. Er wird am Ende jedes Monats neu bestimmt und einen Monat gehalten.

Dieses Repository erklärt, wie gerechnet wird. Es enthält keinen Programmcode und keine Kursdaten.

> **Keine Anlageberatung.** Alle Zahlen beschreiben die Vergangenheit und sind eine Modellrechnung. Vergangene Wertentwicklung ist kein verlässlicher Hinweis auf künftige Ergebnisse. Kosten und Steuern sind nicht berücksichtigt.

## Seiten

| Seite | Inhalt |
|---|---|
| [Methodik](methodik.md) | Das Verfahren Schritt für Schritt, mit Rechenbeispielen zum Nachrechnen |
| [Gegenrechnung](gegenrechnung.md) | Der Rückblick Monat für Monat und der Test verschiedener Trendregeln |
| [FAQ](faq.md) | Antworten auf die häufigsten Fragen zum Karussell |

## Kurz erklärt

1. **15 ETFs und der MSCI World.** Täglich nach Börsenschluss die Schlusskurse in Euro, Quelle ARIVA.DE.
2. **Rendite je Schwankung.** Rendite über dem Zins geteilt durch die Schwankung der letzten 12 Monate (Sharpe Ratio). Geprüft werden alle 32.767 Kombinationen der 15 ETFs.
3. **Einfach vor kompliziert.** Unter allen Mischungen mit mindestens 95% der besten Punktzahl gewinnt die mit den wenigsten ETFs.
4. **Zufallstest.** Die 12 Monate werden 1.000-mal in 10-Tage-Stücken neu gemischt. Der Mix muss in mindestens 95% dieser Fälle mehr Rendite je Schwankung haben als der MSCI World. Dazu kommt eine Korrektur dafür, dass viele Mischungen probiert wurden.
5. **Trendregel.** Fällt der Mix unter den Durchschnitt seiner letzten 10 Monatsschlusskurse, gilt der MSCI World. Die 10 Monate stammen aus einer Studie von Mebane Faber (2007).

## Stand

Die Beispielzahlen beziehen sich auf den Datenstand vom 25.09.2026. Das Karussell zeigt jeden Monat die aktuellen Werte.

Stephan Büttig · Fragen und Hinweise gern als Kommentar unter dem LinkedIn-Beitrag.
