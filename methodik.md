[Almanach](README.md) · [Methodik](methodik.md) · [Gegenrechnung](gegenrechnung.md) · [Kapitel](kapitel.md) · [Prüfbericht](pruefbericht.md) · [Wechsel und Kombi](varianten.md) · [Fragen](faq.md)

# Wie der ETF-Radar rechnet

Diese Seite erklärt das Verfahren so, dass man es ohne Vorwissen nachvollziehen und mit einer Tabellenkalkulation nachrechnen kann. Alle Beispielzahlen stammen aus dem Datenstand vom 30.10.2026 und lassen sich mit den Indexständen von MSCI nachrechnen.

> Keine Anlageberatung. Alle Zahlen beschreiben die Vergangenheit. Die Einstellungen wurden mit Kenntnis des gezeigten Zeitraums festgelegt, der Rückblick ist deshalb eher zu gut als zu schlecht.

Der ETF-Mix Fokus hieß bis November 2026 ETF-Radar-Mix, der ETF-Mix Balance lief bis dahin als Vergleichsregel ‚3 beste mit Trend‘.

## Die Idee in Kürze

Der MSCI World ist der Maßstab, an dem sich jede Aufteilung messen lassen muss. Der Radar sucht jeden Tag die Mischung aus 15 Sektor- und Faktor-ETFs, die in den letzten 12 Monaten am meisten Rendite je Schwankung gebracht hat, und zwar mit so wenigen ETFs wie möglich. Diese Mischung heißt **ETF-Mix Fokus**, sie wird am Ende jedes Monats neu bestimmt und einen Monat gehalten. Danach prüft er mit Zufallsstichproben und einer Trendregel, ob das Ergebnis belastbar oder nur Glück war. Gleichrangig daneben steht der **ETF-Mix Balance**, der jeden Monat die drei Indizes mit der höchsten Rendite der letzten 12 Monate zu gleichen Teilen hält. Die Abschnitte 3 bis 10 beschreiben Fokus, Balance steht in Abschnitt 11.

## 1. Die 15 ETFs und der MSCI World

Alle ETFs bilden globale MSCI-Indizes ab. Fokus und Balance werden nur aus den 15 Sektoren und Faktoren gebildet, der MSCI World dient als Vergleich. Gerechnet wird mit den täglichen Indexständen von MSCI (Net Total Return in Euro), für Tabellen, Grafiken und beide Mischungen gleichermaßen. Alle Kennzahlen gelten deshalb vor den Kosten der ETFs, die bei diesen Sektor- und Faktor-ETFs rund 0,25 bis 0,30 % im Jahr betragen. Nur der Rückblick (Abschnitt 11) rechnet nach Kosten. Mit dem Code findet man jeden Index auf msci.com. Die WKN nennen ETFs, die den jeweiligen Index abbilden. Bei Low Volatility ist es die Fassung, die MSCI in US-Dollar optimiert, in Euro umgerechnet wie alle anderen.

| Kurzname | Gruppe | Index | Code bei MSCI | WKN eines ETFs |
|---|---|---|---|---|
| MSCI World | Vergleich | MSCI World | 990100 | A1XB5U |
| Kommunikation | Sektor | MSCI World Communication Services | 106804 | A113FK |
| Zykl. Konsum | Sektor | MSCI World Consumer Discretionary | 106799 | A113FH |
| Basis-Konsumgüter | Sektor | MSCI World Consumer Staples | 106800 | A113FG |
| Energie | Sektor | MSCI World Energy | 106796 | A113FF |
| Finanzen | Sektor | MSCI World Financials | 106802 | A113FE |
| Gesundheit | Sektor | MSCI World Health Care | 106801 | A113FD |
| Technologie | Sektor | MSCI World Information Technology | 106803 | A113FM |
| Industrie | Sektor | MSCI World Industrials | 106798 | A113FN |
| Grundstoffe | Sektor | MSCI World Materials | 106797 | A113FL |
| Versorger | Sektor | MSCI World Utilities | 106805 | A113FJ |
| Value | Faktor | MSCI World Enhanced Value | 705130 | A12ATG |
| Qualität | Faktor | MSCI World Sector Neutral Quality | 705169 | A12ATE |
| Nebenwerte | Faktor | MSCI World Mid Cap Equal Weight | 705043 | A12ATH |
| Low Volatility | Faktor | MSCI World Minimum Volatility (USD) | 129896 | A1J781 |
| Momentum | Faktor | MSCI World Momentum | 703755 | A12ATF |

Sektoren teilen den Markt nach Branchen auf. Faktoren filtern nach Eigenschaften der Unternehmen, etwa günstige Bewertung (Value) oder starker Kursverlauf (Momentum).

## 2. Monatsrenditen

Die Monatsrendite ist die Veränderung vom Indexstand des letzten Handelstags im Vormonat zum Indexstand des letzten Handelstags im Monat. Genauso entstehen „lfd. Jahr“ und „lfd. Monat“. „1 Jahr“ läuft von Monatsende zu Monatsende, wenn der Datenstand der letzte Werktag seines Monats ist, also etwa vom 31.10.2025 bis 30.10.2026. Mitten im Monat zählt derselbe Kalendertag ein Jahr zuvor.

Die Indexstände kommen von MSCI als Net Total Return in Euro, also mit wieder angelegten Dividenden nach Quellensteuer. Diese Zahlen sind auch in Monatsübersichten anderer Anbieter üblich. Bis Oktober 2026 rechnete der Radar mit Schlusskursen der ETFs von Xetra. Die eignen sich für einzelne Monate schlechter. Xetra schließt um 17:30 Uhr, der Index erst mit der US-Börse. Fällt der US-Markt am Nachmittag des letzten Handelstags, fehlt das im ETF-Kurs bis zum nächsten Tag. Im Oktober 2026 zeigte der ETF auf Kommunikation deshalb −10,0 %, der Index −12,0 %. Über 12 Monate gleicht sich das weitgehend aus.

Fehlt ein Indexstand oder ist er am Monatsersten noch nicht veröffentlicht, rechnet der Radar ersatzweise mit Schlusskursen der ETFs von Xetra (Quelle ARIVA.DE). Dann gilt das für den ganzen Lauf, damit Fokus, Balance und Vergleich dieselbe Grundlage haben, und das Karussell nennt ARIVA.DE als Quelle.

## 3. Rendite und Schwankung

Für die Suche zählt ein Fenster von 12 Monaten. MSCI rechnet die Weltindizes an jedem Wochentag, weil immer irgendeine Börse offen hat, das sind rund 261 Tage im Jahr. Aus den Tagesrenditen ergeben sich zwei Werte.

- **Rendite p. a.** ist der Durchschnitt der Tagesrenditen mal 261.
- **Schwankung p. a.** (Volatilität) ist die Standardabweichung der Tagesrenditen mal der Wurzel aus 261.

Rechnet ein Lauf ersatzweise mit ETF-Kursen, gilt 252, die Zahl der Xetra-Handelstage.

Beispiel am 30.10.2026, Fenster vom 30.10.2025 bis 30.10.2026: Value 38,8 % Rendite bei 14,8 % Schwankung. Energie 51,5 % bei 20,8 %, Gesundheit 26,0 % bei 14,6 %, MSCI World 15,7 % bei 10,6 %.

Diese Rendite p. a. ist nicht dieselbe Zahl wie die Wertentwicklung über 12 Monate, die das Karussell in Tabelle und Landkarte zeigt. Bei Value lag die Wertentwicklung bei 44,9 %. Der Unterschied entsteht, weil sich über das Jahr Gewinne auf Gewinne aufbauen. Für die Rendite je Schwankung ist der Durchschnitt der Tagesrenditen die übliche Größe.

## 4. Rendite je Schwankung

Die Rendite je Schwankung (Sharpe Ratio) setzt den Mehrertrag ins Verhältnis zur Unruhe. Man zieht von der Rendite den Zins ab, den man ohne Risiko bekommen hätte, und teilt durch die Schwankung.

```
Rendite je Schwankung = (Rendite p. a. − Zins) / Schwankung p. a.
```

Als Zins dient der Durchschnitt des EZB-Einlagesatzes im selben 12-Monats-Fenster, am 30.10.2026 waren das 2,12 %.

Beispiel Value: (38,8 % − 2,1 %) / 14,8 % = **2,48**. MSCI World: (15,7 % − 2,1 %) / 10,6 % = **1,28**.

Eine höhere Rendite je Schwankung heißt mehr Ertrag für dieselbe Unruhe im Depot. Ein ETF mit hoher Rendite und riesigen Ausschlägen kann eine niedrigere Rendite je Schwankung haben als ein ruhigerer.

## 5. Warum Mischen hilft

Zwei ETFs, die sich nicht im Gleichschritt bewegen, gleichen sich teilweise aus. Das misst die Korrelation zwischen −1 (genau gegenläufig) und +1 (genau gleich). Value und Energie hatten am 30.10.2026 −0,14, sie liefen also leicht gegeneinander. Gesundheit lief mit beiden fast unabhängig (0,02 und −0,06).

Die Schwankung einer Mischung aus A und B mit den Anteilen a und b ist

```
Schwankung = Wurzel( a²·σA² + b²·σB² + 2·a·b·Korrelation·σA·σB )
```

Bei drei ETFs kommen die Paare B und C sowie A und C nach demselben Muster dazu. Mit 42 % Value, 31 % Energie und 27 % Gesundheit ergibt das 9,1 % Schwankung, weniger als bei jedem der drei allein und weniger als beim MSCI World. Die Rendite ist einfach der gewichtete Durchschnitt, hier 39,3 %. Rendite je Schwankung der Mischung: (39,3 % − 2,1 %) / 9,1 % = **4,10**.

Der Radar rechnet mit festen Anteilen über das ganze Fenster. Das entspricht einem Depot, das laufend auf die Zielanteile zurückgesetzt wird.

## 6. Die Suche

Aus 15 ETFs lassen sich 32.767 Kombinationen bilden (jede Teilmenge außer der leeren). Der Radar geht in drei Stufen vor.

1. **Obere Schranke je Kombination.** Für jede der 32.767 Kombinationen wird exakt berechnet, welche Rendite je Schwankung die bestmögliche Aufteilung dieser ETFs erreichen könnte. Kombinationen, die selbst im besten Fall zu wenig schaffen, fallen heraus.
2. **Grobraster.** Alle Aufteilungen mit bis zu 3 ETFs in 5-%-Schritten.
3. **Feinraster.** Die vielversprechenden Kombinationen werden in 1-%-Schritten nachgerechnet, mit mindestens 5 % je ETF. Nur aus dieser Stufe kommen die Kandidaten und der ETF-Mix Fokus.

## 7. Einfach vor kompliziert

Die Mischung mit der höchsten Rendite je Schwankung ist oft nur minimal besser als eine viel einfachere. Deshalb gilt eine Einfachheitsschwelle von 95 %. Jede Mischung, die mindestens 95 % des besten Werts erreicht, ist ein Kandidat. Unter den Kandidaten, die auch die Gegenprobe aus Abschnitt 8 bestehen, gewinnt die mit den wenigsten ETFs. Bei Gleichstand entscheidet die PSR aus Abschnitt 9.

Am 30.10.2026 lag die bestmögliche Rendite je Schwankung bei 4,15. Die beste Mischung aus nur zwei ETFs (59 % Value, 41 % Energie) schaffte 3,70, also 89 %, und blieb damit unter der Schwelle. Die Mischung aus drei ETFs erreicht 98,6 %.

## 8. Gegenprobe mit Stichproben

Ein einzelnes Jahr kann Zufall sein. Deshalb baut der Radar 1.000 neue Jahre aus denselben Daten. Er schneidet die Tagesrenditen in Blöcke von 10 Handelstagen und setzt zufällig gezogene Blöcke zu einem neuen Jahr zusammen (Block-Bootstrap). Die Blöcke erhalten kurze Zusammenhänge wie ein paar schwache Tage hintereinander.

In jedem der 1.000 Jahre wird die Rendite je Schwankung der Mischung mit der des MSCI World verglichen. Der Anteil der Siege ist das Ergebnis des Zufallstests, am 30.10.2026 waren es 99,3 %, also 993 von 1.000. Eine Mischung braucht mindestens 95 %.

Aus denselben Stichproben stammt die **Bandbreite**. Der Radar sucht in jedem Stichprobenjahr die beste Aufteilung der gewählten ETFs und zeigt, in welchem Bereich der Anteil meistens lag. Am 30.10.2026 lag der Anteil von Value meistens zwischen 26 und 60 %, von Energie zwischen 19 und 45 % und von Gesundheit zwischen 5 und 43 %. Liegt die aktuelle Aufteilung in diesem Bereich, lohnt kein Umschichten wegen kleiner Verschiebungen.

## 9. Glück oder Können: PSR und DSR

Die **Probabilistic Sharpe Ratio (PSR)** schätzt, wie wahrscheinlich der Vorsprung der Mischung gegenüber dem MSCI World wirklich größer als null ist. Sie berücksichtigt, wie lang die Datenreihe ist und ob die Renditen schief verteilt sind oder dicke Ränder haben.

Wer sehr viele Mischungen durchprobiert, findet fast immer eine, die zufällig gut aussieht. Die **Deflated Sharpe Ratio (DSR)** rechnet das heraus. Sie hebt die Messlatte auf den Wert, den der beste von vielen reinen Zufallsversuchen erreichen würde. Als Zahl der Versuche zählen alle Kombinationen mit bis zu drei ETFs, also 15 + 105 + 455 = 575, jeweils mit ihrer besten Aufteilung im Grobraster. Am 30.10.2026 lag die DSR bei 94,5 %.

## 10. Trendregel

Die Regel folgt Mebane Faber (2007), der 10 Monatsschlusskurse als Durchschnitt nutzt. Das entspricht grob der bekannten 200-Tage-Linie. Bei jedem Lauf wird der aktuelle Wert der Mischung mit dem Durchschnitt ihrer letzten 10 Monatswerte verglichen. Als Monatswert zählt jeweils der letzte Wert eines Monats, der laufende Monat eingeschlossen. Liegt die Mischung darüber, wird sie gehalten. Liegt sie darunter, wechselt die Regel in den MSCI World, bis der Trend wieder intakt ist. Im Rückblick wird die Regel nur an Monatsenden angewendet.

Dasselbe Ausweichziel gilt, wenn an einem Monatsende keine Mischung alle Prüfungen besteht. Der MSCI World ist dabei nur so lange der sichere Hafen, wie er selbst über seinem Durchschnitt der letzten 10 Monate liegt. Liegt auch er darunter, wechselt die Regel in den Geldmarkt, verzinst wie der EZB-Einlagesatz, etwa über einen Geldmarkt-ETF oder Tagesgeld. Bis November 2026 galt in beiden Fällen fest der MSCI World. Im Rückblick ab Dezember 2001 senkt die neue Regel den größten Verlust von 48,9 % auf 23,6 %, etwa in der Baisse 2002/03 und in der Finanzkrise 2008/09. In ruhigen Jahren kostet sie Rendite, wenn sie im Geldmarkt sitzt, während der Markt steigt. Seit Januar 2024 brachte Fokus deshalb +93,9 % statt +105,1 %.

Die Idee dahinter ist schlicht. Lange Abwärtsphasen beginnen selten aus heiterem Himmel, und wer unter einem fallenden Durchschnitt aussteigt, verpasst die größten Verluste. Der Preis sind Fehlsignale in Seitwärtsphasen. Am 30.10.2026 lag die Mischung 16,0 % über ihrem Durchschnitt der letzten 10 Monate. Ob 10 Monate auch für diese 15 ETFs passen, zeigt die [Gegenrechnung](gegenrechnung.md) mit 6, 8, 10 und 12 Monaten.

## 11. Rückblick

Die Jahre seit 2002 und die letzten 36 Monate stehen in der [Gegenrechnung](gegenrechnung.md), die Phasen seit 2002 in den [Kapiteln](kapitel.md). Der [Prüfbericht](pruefbericht.md) rechnet alle Zahlen dieses Abschnitts nach und erklärt, was sie aussagen. Ob sich ein Wechsel zwischen Fokus und Balance lohnt oder eine Kombi aus beiden, steht im [zweiten Prüfbericht](varianten.md).

Der Rückblick beantwortet die Frage, was der ETF-Mix Fokus gebracht hätte, wenn man ihn an jedem Monatsende befolgt hätte. Er beginnt am 31.12.2001, dem ersten Monatsende mit 12 Monaten Indexständen aller 16 Indizes, und umfasst 298 Monate. Die LinkedIn-Folie zeigt davon die Zeit seit Januar 2024. Für jedes Monatsende rechnet der Radar nur mit den Daten, die damals bekannt waren, und bestimmt Fokus mit Trendregel. Umgesetzt wird er zum Schlussstand des nächsten Handelstags, denn der Indexstand des Monatsendes ist erst danach bekannt. Gehalten wird bis zum Handelstag nach dem nächsten Monatsende. Die Monatsergebnisse werden verkettet.

Seit November 2026 rechnet der Rückblick nach Kosten, vor Steuern:

- Laufende Kosten (TER) der ETFs taggenau, 0,19 % für den MSCI World, 0,30 % für Nebenwerte und Low Volatility, 0,25 % für die übrigen Sektoren und Faktoren.
- Handelskosten von 0,1 % je Kauf und je Verkauf auf den umgeschichteten Anteil. Umgeschichtet wird gegen die Anteile, die sich im Vormonat durch die Kursbewegung ergeben haben. Der erste Kauf zählt einfach.
- Der Geldmarktanteil bekommt den tatsächlichen EZB-Einlagesatz jedes Haltetags.

Der MSCI World und „alle 15 gleich“ laufen genauso, also mit TER, erstem Kauf und für „alle 15 gleich“ mit monatlichem Ausgleich auf gleiche Teile.

Seit November 2026 läuft gleichrangig der **ETF-Mix Balance** mit. An jedem Monatsende werden die 3 Sektoren und Faktoren mit der höchsten Rendite über die letzten 12 Monate zu gleichen Teilen gekauft. Liegt der MSCI World unter dem Durchschnitt seiner letzten 10 Monatsenden, gilt der Geldmarkt. Kosten und Umsetzung sind dieselben wie bei Fokus. Die Regel beruht auf der bekannten Momentum-Forschung und auf Faber (2007). Der Vergleich beider zeigt, ob die aufwendigere Suche nach der besten Rendite je Schwankung mehr bringt als eine Regel, die sich in einem Satz erklären lässt. Ab Ende 2001 lagen beide netto fast gleichauf (10,26 % gegen 10,22 % im Jahr), Balance mit dem kleineren größten Verlust (14,3 % gegen 23,7 %). Seit Januar 2024 lag Fokus vorn. Beide wurden mit Kenntnis dieser 25 Jahre gewählt. Belastbar ist erst der Vergleich ab November 2026, im November 2028 wird neu entschieden. Das Blatt 🧭 Rückblick zeigt daneben die Bruttowerte wie bis November 2026 (vom Monatsende bis zum nächsten Monatsende, Zins des Rechenfensters, ohne Kosten).

Zum Vergleich laufen zwei einfache Wege mit, der MSCI World allein und alle 15 ETFs zu gleichen Teilen. Stand 30.10.2026 standen netto +86,5 % für Fokus gegen +51,0 % für den MSCI World, +49,1 % für alle 15 gleich und +53,3 % für Balance. Vor Kosten und mit Kauf zum Monatsende wären es +93,9 %, +53,2 % und +51,6 %. Die Werte seit Januar 2024 stammen aus dem Rückblick ab Ende 2001, auf Ende Januar 2024 = 100 umgestellt. Ab Ende 2001 gerechnet kam Fokus netto auf 10,3 % im Jahr, der MSCI World auf 7,3 %. Fokus schichtet im Schnitt 462 % im Jahr um. Bei 0,2 % Handelskosten je Seite blieben rund 9,3 % im Jahr, bei 0,5 % rund 6,3 %.

Wichtig für die Einordnung:

- Steuern fehlen. Monatliches Umschichten kann Steuern auslösen. Im deutschen Privatdepot kosten sie nach einer Schätzung rund 1,6 Prozentpunkte im Jahr ([Prüfbericht](pruefbericht.md#steuern)). Die Kosten sind angesetzt, tatsächliche Spreads und Gebühren hängen von Broker und Ordergröße ab.
- Die Einstellungen (12 Monate, 95 %, Durchschnitt der letzten 10 Monate) wurden gewählt, nachdem der Zeitraum bekannt war. Das schönt das Ergebnis.
- Die LinkedIn-Folie zeigt nur 33 Monate, ein kurzer Zeitraum. Erst die 298 Monate ab 2001 enthalten mehrere Abstürze.
- Der Vorsprung ist statistisch nicht gesichert. Ab Ende 2001 lag Fokus netto 2,9 Prozentpunkte im Jahr vor dem MSCI World. Der t-Wert nach Newey-West liegt bei 1,17, als gesichert gilt ein Wert ab etwa 2. Fast der ganze Vorsprung stammt aus 2002 bis 2008 mit 11,6 Prozentpunkten im Jahr. 2009 bis 2014 lag Fokus 2,0 Prozentpunkte zurück, 2015 bis 2020 3,9 Prozentpunkte, 2021 bis 2026 lag er 3,6 Prozentpunkte vorn. Über je 5 Jahre gerechnet lag er nur in 44 % der Zeitfenster vor dem MSCI World.
- Die fünf Faktorindizes gibt es erst seit 2008 bis 2014. Laut den Factsheets von MSCI startete Low Volatility am 14.04.2008, Momentum am 11.12.2013, Nebenwerte am 25.07.2014, Value und Qualität am 11.08.2014. Die Stände davor hat MSCI nachträglich berechnet. In 38 der 298 Monate enthielt Fokus einen Faktor vor dessen Start, bis August 2014 im Schnitt 19 % der Mischung. Ab dem 29.08.2014, als alle Indizes liefen, kam Fokus netto auf 12,0 % im Jahr, der MSCI World auf 11,9 %.
- Die einfache Regel von Balance war über 25 Jahre gleich gut. Balance kam netto auf 10,2 % im Jahr gegen 10,3 % für Fokus, mit 14,3 % statt 23,7 % größtem Verlust. Ab August 2014 lag Fokus vorn (12,0 % gegen 8,9 % im Jahr). Warum Fokus und Balance so verschieden verlaufen, zeigt der [Prüfbericht](pruefbericht.md#fokus-gegen-balance).

## 12. Grenzen

- Bei Fokus sind zwei oder drei ETFs ein Klumpen. Ein Sektor kann lange schwächeln.
- 12 Monate Vergangenheit sagen wenig über die nächsten 12 Monate.
- Sektor- und Faktor-ETFs haben höhere laufende Kosten als ein MSCI-World-ETF.
- Der Radar kennt keine Bewertungen, Nachrichten oder Zinsprognosen. Er rechnet nur mit Indexständen.

## Begriffe

| Begriff | Bedeutung |
|---|---|
| Rendite p. a. | Durchschnittlicher Tagesertrag hochgerechnet auf ein Jahr |
| Schwankung p. a. | Wie stark die Tageserträge streuen, hochgerechnet auf ein Jahr |
| Rendite je Schwankung | Rendite über dem Zins je Einheit Schwankung, in der Fachsprache Sharpe Ratio |
| Korrelation | Wie gleichförmig zwei Kurse laufen, von −1 bis +1 |
| Block-Bootstrap | Neue Jahre aus zufällig gezogenen Blöcken der echten Daten |
| PSR | Wahrscheinlichkeit, dass der Vorsprung echt ist |
| DSR | PSR mit Abzug für das Durchprobieren vieler Mischungen |
| Durchschnitt der letzten 10 Monate | Durchschnitt der letzten 10 Monatsendwerte, Grundlage der Trendregel |
| Max. Verlust | Größter Verlust vom Höchststand im Fenster |
| ETF-Mix Fokus | Die Mischung mit der meisten Rendite je Schwankung, monatlich neu bestimmt |
| ETF-Mix Balance | Die 3 Indizes mit der höchsten 12-Monats-Rendite zu gleichen Teilen, monatlich neu bestimmt |
| Geldmarkt | Ausweichziel der Trendregel, verzinst wie der EZB-Einlagesatz |
| Zufallstest | Block-Bootstrap mit 1.000 neu gemischten Varianten der letzten 12 Monate |

## Quellen

- William F. Sharpe (1966), Mutual Fund Performance, Journal of Business 39(1). Und (1994), The Sharpe Ratio, Journal of Portfolio Management 21(1).
- Mebane T. Faber (2007), A Quantitative Approach to Tactical Asset Allocation, Journal of Wealth Management 9(4), S. 69–79.
- David H. Bailey, Marcos López de Prado (2012), The Sharpe Ratio Efficient Frontier, Journal of Risk 15(2). Einführung der PSR.
- David H. Bailey, Marcos López de Prado (2014), The Deflated Sharpe Ratio, Journal of Portfolio Management 40(5).
- Hans R. Künsch (1989), The Jackknife and the Bootstrap for General Stationary Observations, Annals of Statistics 17(3).
- Europäische Zentralbank, Zinssatz für die Einlagefazilität, EZB-Datenportal.
- MSCI Inc., End-of-Day-Indexstände, Net Total Return in Euro, msci.com.
