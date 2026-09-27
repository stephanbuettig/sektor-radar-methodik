# Wie das Sektor-Radar rechnet

Diese Seite erklärt das Verfahren so, dass man es ohne Vorwissen nachvollziehen und mit einer Tabellenkalkulation nachrechnen kann. Alle Beispielzahlen stammen aus dem Datenstand vom 25.09.2026.

> Keine Anlageberatung. Alle Zahlen beschreiben die Vergangenheit. Die Einstellungen wurden mit Kenntnis des gezeigten Zeitraums festgelegt, der Rückblick ist deshalb eher zu gut als zu schlecht.

## Die Idee in drei Sätzen

Der MSCI World ist der Maßstab, an dem sich jede Aufteilung messen lassen muss. Das Radar sucht jeden Tag die Mischung aus 15 Sektor- und Faktor-ETFs, die in den letzten 12 Monaten am meisten Rendite je Schwankung gebracht hat, und zwar mit so wenigen ETFs wie möglich. Diese Mischung heißt **Sektor-Radar-Mix**, sie wird am Ende jedes Monats neu bestimmt und einen Monat gehalten. Danach prüft es mit Zufallsstichproben und einer Trendregel, ob das Ergebnis belastbar oder nur Glück war.

## 1. Die 15 ETFs und der MSCI World

Alle ETFs bilden globale MSCI-Indizes ab. Der Mix wird nur aus den 15 Sektor- und Faktor-ETFs gebildet, der MSCI World dient als Vergleich. Die Kurse sind Schlusskurse in Euro am Handelsplatz Xetra, abgerufen bei ARIVA.DE.

| Kurzname | Gruppe | Index | WKN |
|---|---|---|---|
| MSCI World | Vergleich | MSCI World | A1XB5U |
| Kommunikation | Sektor | MSCI World Communication Services | A113FK |
| Zykl. Konsum | Sektor | MSCI World Consumer Discretionary | A113FH |
| Basis-Konsumgüter | Sektor | MSCI World Consumer Staples | A113FG |
| Energie | Sektor | MSCI World Energy | A113FF |
| Finanzen | Sektor | MSCI World Financials | A113FE |
| Gesundheit | Sektor | MSCI World Health Care | A113FD |
| Technologie | Sektor | MSCI World Information Technology | A113FM |
| Industrie | Sektor | MSCI World Industrials | A113FN |
| Grundstoffe | Sektor | MSCI World Materials | A113FL |
| Versorger | Sektor | MSCI World Utilities | A113FJ |
| Value | Faktor | MSCI World Enhanced Value | A12ATG |
| Qualität | Faktor | MSCI World Sector Neutral Quality | A12ATE |
| Nebenwerte | Faktor | MSCI World Mid Cap Equal Weight | A12ATH |
| Low Volatility | Faktor | MSCI World Minimum Volatility | A1J781 |
| Momentum | Faktor | MSCI World Momentum | A12ATF |

Sektoren teilen den Markt nach Branchen auf. Faktoren filtern nach Eigenschaften der Unternehmen, etwa günstige Bewertung (Value) oder starker Kursverlauf (Momentum).

## 2. Monatsrenditen

Die Monatsrendite ist die Veränderung vom Schlusskurs des letzten Handelstags im Vormonat zum Schlusskurs des letzten Handelstags im Monat. Genauso entstehen „1 Jahr“, „lfd. Jahr“ und „lfd. Monat“ im Blatt 🏆 Wertentwicklung. Ausschüttungen sind nicht eingerechnet.

## 3. Rendite und Schwankung

Für die Suche zählt ein Fenster von 12 Monaten, also rund 252 Handelstage. Aus den Tagesrenditen ergeben sich zwei Werte.

- **Rendite p. a.** ist der Durchschnitt der Tagesrenditen mal 252.
- **Schwankung p. a.** (Volatilität) ist die Standardabweichung der Tagesrenditen mal der Wurzel aus 252.

Beispiel Value: 45,5 % Rendite bei 15,4 % Schwankung. Energie 37,8 % bei 22,9 %, MSCI World 19,3 % bei 11,0 %.

Diese Rendite p. a. ist nicht dieselbe Zahl wie die Wertentwicklung über 12 Monate, die das Karussell in Tabelle und Landkarte zeigt. Bei Value lag die Wertentwicklung bei 55,9 %. Der Unterschied entsteht, weil sich über das Jahr Gewinne auf Gewinne aufbauen. Für die Rendite je Schwankung ist der Durchschnitt der Tagesrenditen die übliche Größe.

## 4. Punkte: Rendite je Schwankung

Die Punkte sind die Sharpe Ratio. Man zieht von der Rendite den Zins ab, den man ohne Risiko bekommen hätte, und teilt durch die Schwankung.

```
Punkte = (Rendite p. a. − Zins) / Schwankung p. a.
```

Als Zins dient der Durchschnitt des EZB-Einlagesatzes im selben 12-Monats-Fenster, zuletzt 2,08 %.

Beispiel Value: (45,5 % − 2,1 %) / 15,4 % = **2,81**. MSCI World: (19,3 % − 2,1 %) / 11,0 % = **1,57**.

Mehr Punkte heißt mehr Ertrag für dieselbe Unruhe im Depot. Ein ETF mit hoher Rendite und riesigen Ausschlägen kann weniger Punkte haben als ein ruhigerer.

## 5. Warum Mischen hilft

Zwei ETFs, die sich nicht im Gleichschritt bewegen, gleichen sich teilweise aus. Das misst die Korrelation zwischen −1 (genau gegenläufig) und +1 (genau gleich). Value und Energie hatten zuletzt −0,22, sie liefen also leicht gegeneinander.

Die Schwankung einer Mischung aus A und B mit den Anteilen a und b ist

```
Schwankung = Wurzel( a²·σA² + b²·σB² + 2·a·b·Korrelation·σA·σB )
```

Mit 68 % Value und 32 % Energie ergibt das 11,4 % Schwankung, weniger als bei jedem der beiden allein. Die Rendite ist einfach der gewichtete Durchschnitt, hier 43,0 %. Punkte der Mischung: (43,0 % − 2,1 %) / 11,4 % = **3,59**.

Das Radar rechnet mit festen Anteilen über das ganze Fenster. Das entspricht einem Depot, das laufend auf die Zielanteile zurückgesetzt wird.

## 6. Die Suche

Aus 15 ETFs lassen sich 32.767 Kombinationen bilden (jede Teilmenge außer der leeren). Das Radar geht in drei Stufen vor.

1. **Obere Schranke je Kombination.** Für jede der 32.767 Kombinationen wird exakt berechnet, wie viele Punkte die bestmögliche Aufteilung dieser ETFs erreichen könnte. Kombinationen, die selbst im besten Fall zu wenig schaffen, fallen heraus.
2. **Grobraster.** Alle Aufteilungen mit bis zu 3 ETFs in 5-%-Schritten.
3. **Feinraster.** Die vielversprechenden Kombinationen werden in 1-%-Schritten nachgerechnet, mit mindestens 5 % je ETF. Nur aus dieser Stufe kommen die Kandidaten und der Mix.

## 7. Einfach vor kompliziert

Die Mischung mit den meisten Punkten ist oft nur minimal besser als eine viel einfachere. Deshalb gilt eine Einfachheitsschwelle von 95 %. Jede Mischung, die mindestens 95 % der besten Punktzahl erreicht, ist ein Kandidat. Unter den Kandidaten, die auch die Gegenprobe aus Abschnitt 8 bestehen, gewinnt die mit den wenigsten ETFs. Bei Gleichstand entscheidet die PSR aus Abschnitt 9.

Die aktuelle Mischung erreicht 95,5 % der bestmöglichen Punktzahl und kommt mit zwei ETFs aus.

## 8. Gegenprobe mit Stichproben

Ein einzelnes Jahr kann Zufall sein. Deshalb baut das Radar 1.000 neue Jahre aus denselben Daten. Es schneidet die Tagesrenditen in Blöcke von 10 Handelstagen und setzt zufällig gezogene Blöcke zu einem neuen Jahr zusammen (Block-Bootstrap). Die Blöcke erhalten kurze Zusammenhänge wie ein paar schwache Tage hintereinander.

In jedem der 1.000 Jahre werden die Punkte der Mischung mit denen des MSCI World verglichen. Der Anteil der Siege ist das Ergebnis des Zufallstests, zuletzt 97,1 %, also 971 von 1.000. Eine Mischung braucht mindestens 95 %.

Aus denselben Stichproben stammt die **Bandbreite**. Das Radar sucht in jedem Stichprobenjahr die beste Aufteilung der gewählten ETFs und zeigt, in welchem Bereich der Anteil meistens lag. Für Value waren das 54 bis 83 %. Liegt die aktuelle Aufteilung in diesem Bereich, lohnt kein Umschichten wegen kleiner Verschiebungen.

## 9. Glück oder Können: PSR und DSR

Die **Probabilistic Sharpe Ratio (PSR)** schätzt, wie wahrscheinlich der Vorsprung der Mischung gegenüber dem MSCI World wirklich größer als null ist. Sie berücksichtigt, wie lang die Datenreihe ist und ob die Renditen schief verteilt sind oder dicke Ränder haben.

Wer sehr viele Mischungen durchprobiert, findet fast immer eine, die zufällig gut aussieht. Die **Deflated Sharpe Ratio (DSR)** rechnet das heraus. Sie hebt die Messlatte auf den Wert, den der beste von vielen reinen Zufallsversuchen erreichen würde. Als Zahl der Versuche zählen alle Kombinationen mit bis zu drei ETFs, also 15 + 105 + 455 = 575, jeweils mit ihrer besten Aufteilung im Grobraster. Die DSR lag bei 83,5 %.

## 10. Trendregel

Die Regel folgt Mebane Faber (2007), der 10 Monatsschlusskurse als Durchschnitt nutzt. Das entspricht grob der bekannten 200-Tage-Linie. Bei jedem Lauf wird der aktuelle Wert der Mischung mit dem Durchschnitt ihrer letzten 10 Monatswerte verglichen, der 10-Monats-Linie. Als Monatswert zählt jeweils der letzte Wert eines Monats, der laufende Monat eingeschlossen. Liegt die Mischung darüber, gilt der Mix. Liegt sie darunter, wechselt die Regel in den MSCI World, bis der Trend wieder intakt ist. Im Rückblick wird die Regel nur an Monatsenden angewendet.

Die Idee dahinter ist schlicht. Lange Abwärtsphasen beginnen selten aus heiterem Himmel, und wer unter einem fallenden Durchschnitt aussteigt, verpasst die größten Verluste. Der Preis sind Fehlsignale in Seitwärtsphasen. Zuletzt lag die Mischung 15,3 % über ihrer Linie. Ob 10 Monate auch für diese 15 ETFs passen, zeigt die [Gegenrechnung](gegenrechnung.md) mit 6, 8, 10 und 12 Monaten.

## 11. Rückblick

Die einzelnen Monate stehen in der [Gegenrechnung](gegenrechnung.md).

Der Rückblick beantwortet die Frage, was der Sektor-Radar-Mix gebracht hätte, wenn man ihn seit Januar 2024 an jedem Monatsende befolgt hätte. Für jedes Monatsende rechnet das Radar nur mit den Daten, die damals bekannt waren, setzt den Mix mit Trendregel um und hält ihn bis zum nächsten Monatsende. Die Monatsergebnisse werden verkettet.

Zum Vergleich laufen zwei einfache Wege mit, der MSCI World allein und alle 15 ETFs zu gleichen Teilen. Stand 25.09.2026 standen +97,4 % für den Mix gegen +51,7 % für den MSCI World und +46,8 % für alle 15 gleich.

Wichtig für die Einordnung:

- Kosten und Steuern fehlen. Monatliches Umschichten kostet Gebühren und kann Steuern auslösen.
- Die Einstellungen (12 Monate, 95 %, 10-Monats-Linie) wurden gewählt, nachdem der Zeitraum bekannt war. Das schönt das Ergebnis.
- 32 Monate sind ein kurzer Zeitraum.

## 12. Grenzen

- Zwei ETFs sind ein Klumpen. Ein Sektor kann lange schwächeln.
- 12 Monate Vergangenheit sagen wenig über die nächsten 12 Monate.
- Sektor- und Faktor-ETFs haben höhere laufende Kosten als ein MSCI-World-ETF.
- Das Radar kennt keine Bewertungen, Nachrichten oder Zinsprognosen. Es rechnet nur mit Kursen.

## Begriffe

| Begriff | Bedeutung |
|---|---|
| Rendite p. a. | Durchschnittlicher Tagesertrag hochgerechnet auf ein Jahr |
| Schwankung p. a. | Wie stark die Tageserträge streuen, hochgerechnet auf ein Jahr |
| Punkte, Sharpe Ratio | Rendite über dem Zins je Einheit Schwankung |
| Korrelation | Wie gleichförmig zwei Kurse laufen, von −1 bis +1 |
| Block-Bootstrap | Neue Jahre aus zufällig gezogenen Blöcken der echten Daten |
| PSR | Wahrscheinlichkeit, dass der Vorsprung echt ist |
| DSR | PSR mit Abzug für das Durchprobieren vieler Mischungen |
| 10-Monats-Linie | Durchschnitt der letzten 10 Monatsendwerte |
| Rückgang | Größter Verlust vom Höchststand im Fenster |
| Sektor-Radar-Mix | Die Mischung mit der meisten Rendite je Schwankung, monatlich neu bestimmt |
| Zufallstest | Block-Bootstrap mit 1.000 neu gemischten Varianten der letzten 12 Monate |

## Quellen

- William F. Sharpe (1966), Mutual Fund Performance, Journal of Business 39(1). Und (1994), The Sharpe Ratio, Journal of Portfolio Management 21(1).
- Mebane T. Faber (2007), A Quantitative Approach to Tactical Asset Allocation, Journal of Wealth Management 9(4), S. 69–79.
- David H. Bailey, Marcos López de Prado (2012), The Sharpe Ratio Efficient Frontier, Journal of Risk 15(2). Einführung der PSR.
- David H. Bailey, Marcos López de Prado (2014), The Deflated Sharpe Ratio, Journal of Portfolio Management 40(5).
- Hans R. Künsch (1989), The Jackknife and the Bootstrap for General Stationary Observations, Annals of Statistics 17(3).
- Europäische Zentralbank, Zinssatz für die Einlagefazilität, EZB-Datenportal.
