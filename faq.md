[Almanach](README.md) · [Methodik](methodik.md) · [Gegenrechnung](gegenrechnung.md) · [Kapitel](kapitel.md) · [Prüfbericht](pruefbericht.md) · [Wechsel und Kombi](varianten.md) · [Fragen](faq.md)

# FAQ

Antworten auf die Fragen, die das Karussell am häufigsten aufwirft. Beispielzahlen vom Datenstand 30.10.2026.

> Keine Anlageberatung. Alle Zahlen beschreiben die Vergangenheit.

## Sind es 15 oder 16 ETFs?

Es sind 15 ETFs auf zehn MSCI-Sektoren und fünf MSCI-Faktoren. Dazu kommt ein ETF auf den MSCI World als Vergleich. Fokus und Balance werden nur aus den 15 gebildet. Der MSCI World dient als Maßstab und als Ausweichziel der Trendregel.

## Was sind ETF-Mix Balance und ETF-Mix Fokus?

Zwei gleichrangige Mischungen aus den 15 ETFs. Beide werden am Ende jedes Monats neu bestimmt und dann einen Monat gehalten.[^namen]

Der **ETF-Mix Balance** ist breit aufgestellt. Er hält die drei Indizes mit der höchsten Rendite der letzten 12 Monate zu gleichen Teilen und schwankt weniger.

Der **ETF-Mix Fokus** ist gebündelt. Er hält die Mischung, die in den letzten 12 Monaten am meisten Rendite je Schwankung gebracht hat, mit möglichst wenigen ETFs, meist ein bis drei Indizes. Am 30.09.2026 waren das Value 67% und Energie 33%, am 30.10.2026 Value 42%, Energie 31% und Gesundheit 27%.

## Was heißt „Rendite je Schwankung“?

Man zieht von der Rendite den Zins ab, den es ohne Risiko gegeben hätte, und teilt das Ergebnis durch die Schwankung. Fachleute nennen das Sharpe Ratio. Ein Wert von 2 bedeutet, dass je Prozentpunkt Schwankung zwei Prozentpunkte Mehrertrag herauskamen. „3,2-fach“ im Karussell vom Oktober 2026 heißt, dass Fokus 3,2-mal so viel Rendite je Schwankung brachte wie der MSCI World.

## Warum „1.000-mal neu gemischt“? Was haben 1.000 Jahre mit 12 Monaten zu tun?

Nichts, deshalb heißt es jetzt Zufallstest. Die rund 261 Tagesrenditen der letzten 12 Monate werden in Stücke zu je 10 Tagen geschnitten und 1.000-mal in zufälliger Reihenfolge neu zusammengesetzt. Jede dieser Varianten besteht aus echten Tagen, nur in anderer Abfolge. In jeder Variante wird die Rendite je Schwankung von Fokus mit der des MSCI World verglichen. Lag Fokus in 993 von 1.000 Varianten vorn (Oktober 2026), hängt sein Vorsprung nicht an ein paar Glückstagen. Das Verfahren heißt Block-Bootstrap (Künsch 1989).

## Was bedeuten die 94,5% auf der Methoden-Folie?

Wer 575 Mischungen durchprobiert, findet fast immer eine, die zufällig gut aussieht. Die Deflated Sharpe Ratio (Bailey und López de Prado 2014) hebt deshalb die Messlatte auf den Wert, den der beste von 575 reinen Zufallsversuchen erreichen würde. Übrig bleibt die Wahrscheinlichkeit, dass der Vorsprung mehr ist als ein Zufallstreffer. Am 30.10.2026 lag sie bei 94,5%.

## Warum 10 Monate bei der Trendregel und nicht 12?

Die Regel stammt aus der Studie „A Quantitative Approach to Tactical Asset Allocation“ von Mebane Faber (2007). Sie vergleicht den Kurs mit dem Durchschnitt der letzten 10 Monatsschlusskurse, was grob der bekannten 200-Tage-Linie entspricht. Die Studie wurde vielfach nachgerechnet, und der Autor hat sie später mit neueren Daten aktualisiert.

Für die 15 ETFs wurde zusätzlich nachgerechnet, wie sich 6, 8, 10 und 12 Monate und eine Variante ohne Trendregel geschlagen hätten. Über den Zeitraum ab Dezember 2001 senken 6 bis 12 Monate den größten Verlust nach Kosten von 50,1% ohne Regel auf 20,7 bis 23,7%. Die Rendite liegt bei allen zwischen 10,1 und 10,3% im Jahr. Die Wahl von 10 ist also kein Glückstreffer, aber auch nicht besser als 8 oder 12. Die Tabelle steht in der [Gegenrechnung](gegenrechnung.md).

## Schaut der Rückblick in die Zukunft?

Nein. An jedem Monatsende rechnet der Radar nur mit Indexständen bis zu diesem Tag. Gekauft wird erst zum Schlussstand des nächsten Handelstags und gehalten bis zum Handelstag nach dem nächsten Monatsende. Beispiel: Am 30.09.2025 ergab sich Kommunikation 51% und Finanzen 49%. Vom 01.10. bis 03.11.2025 brachte das nach Kosten +2,2%. Jedes Jahr seit 2002 und die letzten 36 Monatsenden stehen in der [Gegenrechnung](gegenrechnung.md).

Eine Einschränkung bleibt. Die Einstellungen, etwa 12 Monate Rückblick, 95% Einfachheitsschwelle und 10 Monate Trendregel, wurden 2026 festgelegt, als der Zeitraum schon bekannt war. Das Ergebnis ist deshalb eher zu gut als zu schlecht.

## Warum steht bei Value einmal 44,9% und einmal 38,8%?

Die Tabelle und die Landkarte im Karussell zeigen die tatsächliche Wertentwicklung über 12 Monate, bei Value 44,9% am 30.10.2026. Für die Rendite je Schwankung braucht die Rechnung dagegen den Durchschnitt der Tagesrenditen, aufs Jahr hochgerechnet, bei Value 38,8%. Bei starken Anstiegen liegt die tatsächliche Wertentwicklung über diesem Durchschnitt, weil sich Gewinne auf Gewinne aufbauen. Beide Zahlen beschreiben denselben Zeitraum.

## Warum oft nur zwei oder drei ETFs?

Wegen der Regel „einfach vor kompliziert“ beim ETF-Mix Fokus. Die Mischung mit der höchsten Rendite je Schwankung ist oft nur minimal besser als eine viel einfachere. Jede Mischung mit mindestens 95% des besten Werts kommt in Frage, und unter diesen gewinnt die mit den wenigsten ETFs. Im Oktober 2026 reichten zwei ETFs nicht, die beste Zweiermischung schaffte nur 89% des besten Werts. Zwei oder drei ETFs bleiben trotzdem ein Klumpen, ein einzelner Sektor kann lange schwächeln.

## Warum Indexstände und nicht die Kurse der ETFs?

Seit November 2026 rechnet der Radar mit den täglichen Indexständen von MSCI (Net Total Return in Euro). Vorher waren es Schlusskurse der ETFs von Xetra. Xetra schließt um 17:30 Uhr, der Index erst mit der US-Börse. Fällt der US-Markt am Nachmittag des letzten Handelstags, fehlt das im ETF-Kurs bis zum nächsten Tag. Im Oktober 2026 zeigte der ETF auf Kommunikation deshalb −10,0%, der Index −12,0%. Mit Indexständen lassen sich alle Zahlen mit öffentlichen Daten von MSCI nachprüfen und mit anderen Monatsübersichten vergleichen. Fokus änderte sich dadurch kaum, am 30.10.2026 von 44/30/26 auf 42/31/27.

## Sind Kosten und Steuern eingerechnet?

Im Rückblick ja, Steuern nein. Seit November 2026 kauft der Rückblick am Handelstag nach dem Monatsende und zieht die laufenden Kosten der ETFs (0,19 bis 0,30% im Jahr) und 0,1% Handelskosten je Kauf und Verkauf ab. Seit Januar 2024 bleiben bei Fokus so +86,5% statt +93,9%, ab Ende 2001 10,3% statt 11,9% im Jahr. Die übrigen Kennzahlen wie Rendite je Schwankung und die 12-Monats-Werte gelten vor Kosten, weil die Indexstände keine ETF-Kosten enthalten. Monatliches Umschichten löst im Privatdepot Steuern aus. Eine Schätzung im [Prüfbericht](pruefbericht.md#steuern) kommt auf rund 1,6 Prozentpunkte im Jahr weniger, beim MSCI World auf 0,7. Sektor- und Faktor-ETFs haben außerdem höhere laufende Kosten als ein MSCI-World-ETF.

## Ist der ETF-Radar besser als der MSCI World?

Belegen lässt sich das nicht. Nach Kosten kam Fokus ab Ende 2001 auf 10,3% im Jahr, der MSCI World auf 7,3%. Der Abstand ist statistisch nicht gesichert und stammt fast ganz aus den Jahren 2002 bis 2008. Danach lag mal der eine, mal der andere vorn. Ein Teil der frühen Jahre beruht außerdem auf Faktorindizes, die MSCI erst 2008 bis 2014 gestartet und davor nachträglich berechnet hat. Ab August 2014, als alle Indizes liefen, lagen Fokus und MSCI World fast gleichauf.

| nach Kosten, im Jahr | ab Ende 2001 | ab August 2014 | größter Verlust ab 2001 |
|---|---|---|---|
| ETF-Mix Fokus | 10,3% | 12,0% | 23,7% |
| ETF-Mix Balance | 10,2% | 8,9% | 14,3% |
| MSCI World mit Trendregel (Faber) | 8,5% | 7,3% | 16,4% |
| MSCI World | 7,3% | 11,9% | 51,7% |

Fokus fällt in schweren Abstürzen weniger tief, weil die Trendregel aussteigt. Balance, in einem Satz erklärt, war über 25 Jahre genauso gut. Ob die aufwendigere Rechnung etwas bringt, zeigt erst der Vergleich ab November 2026. Die Einzelheiten stehen in der [Methodik, Abschnitt 11](methodik.md#11-rückblick), die Prüfung aller Zahlen mit Grafiken im [Prüfbericht](pruefbericht.md).

## Kann man zwischen Fokus und Balance wechseln, je nachdem wer gerade vorn liegt?

Im Rückblick hat das nicht geholfen. Wer jeweils der Regel folgte, die in den letzten 12 Monaten vorn lag, kam auf 9,4% im Jahr und damit schlechter weg als mit Fokus oder Balance allein. Ob Fokus als Nächstes vorn liegt, lässt sich aus seinem bisherigen Vorsprung kaum ablesen. 16 Wechselregeln wurden geprüft, die beste kam auf 11,3%, aber dieser Wert ist beim Durchprobieren so vieler Regeln auch ohne echten Vorteil zu erwarten. Alle Regeln und Prüfungen stehen im [Prüfbericht zu Wechsel und Kombi](varianten.md).

## Was ist die Kombi aus Fokus und Balance?

Statt zu wechseln, hält die Kombi jeden Monat halb die Anteile von Fokus und halb die von Balance. Im Rückblick kam sie netto auf 10,4% im Jahr bei 15,0% größtem Verlust, vor und nach 2014 fast gleich. Weil beide nicht im Gleichschritt laufen, gleichen sich ihre schwachen Phasen teilweise aus. Die genaue Aufteilung spielt dabei kaum eine Rolle ([Prüfbericht](varianten.md#warum-die-kombi-trägt)). Die Kombi ist nur ein Ergebnis dieser Prüfung und wird nicht als eigener Mix angeboten.

## Ist das eine Empfehlung?

Nein. Der ETF-Radar ist eine Modellrechnung auf Basis vergangener Indexstände. Er kennt keine Bewertungen, Nachrichten oder Zinsprognosen und sagt nichts über die Zukunft.

## Kann ich das nachrechnen?

Ja. Die [Methodik](methodik.md) enthält jede Formel mit Beispielzahlen, die sich mit einer Tabellenkalkulation nachvollziehen lassen. Die Indexstände gibt es auf msci.com, die Codes stehen in Abschnitt 1 der Methodik. Ein Skript zum eigenen Nachrechnen ist in Arbeit.

[^namen]: Der ETF-Mix Fokus hieß bis November 2026 ETF-Radar-Mix, der ETF-Mix Balance lief bis dahin als Vergleichsregel ‚3 beste mit Trend‘.
