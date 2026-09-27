# FAQ

Antworten auf die Fragen, die das Karussell am häufigsten aufwirft. Beispielzahlen vom Datenstand 25.09.2026.

> Keine Anlageberatung. Alle Zahlen beschreiben die Vergangenheit.

## Sind es 15 oder 16 ETFs?

Es sind 15 ETFs auf zehn MSCI-Sektoren und fünf MSCI-Faktoren. Dazu kommt ein ETF auf den MSCI World als Vergleich. Der Mix wird nur aus den 15 gebildet. Der MSCI World dient als Maßstab und als Ausweichziel der Trendregel.

## Was ist der Sektor-Radar-Mix?

Die Mischung aus den 15 ETFs, die in den letzten 12 Monaten am meisten Rendite je Schwankung gebracht hat, mit möglichst wenigen ETFs. Sie wird am Ende jedes Monats neu bestimmt und dann einen Monat gehalten. Am 31.08.2026 waren das Value 69% und Energie 31%, mit Daten bis 25.09.2026 Value 68% und Energie 32%.

## Was heißt „Rendite je Schwankung“?

Man zieht von der Rendite den Zins ab, den es ohne Risiko gegeben hätte, und teilt das Ergebnis durch die Schwankung. Fachleute nennen das Sharpe Ratio. Ein Wert von 2 bedeutet, dass je Prozentpunkt Schwankung zwei Prozentpunkte Mehrertrag herauskamen. „2,3-fach“ im Karussell heißt, dass der Mix 2,3-mal so viel Rendite je Schwankung brachte wie der MSCI World.

## Warum „1.000-mal neu gemischt“? Was haben 1.000 Jahre mit 12 Monaten zu tun?

Nichts, deshalb heißt es jetzt Zufallstest. Die rund 250 Handelstage der letzten 12 Monate werden in Stücke zu je 10 Tagen geschnitten und 1.000-mal in zufälliger Reihenfolge neu zusammengesetzt. Jede dieser Varianten besteht aus echten Tagen, nur in anderer Abfolge. In jeder Variante wird die Rendite je Schwankung des Mix mit der des MSCI World verglichen. Lag der Mix in 971 von 1.000 Varianten vorn, hängt sein Vorsprung nicht an ein paar Glückstagen. Das Verfahren heißt Block-Bootstrap (Künsch 1989).

## Was bedeuten die 84% auf der Methoden-Folie?

Wer 575 Mischungen durchprobiert, findet fast immer eine, die zufällig gut aussieht. Die Deflated Sharpe Ratio (Bailey und López de Prado 2014) hebt deshalb die Messlatte auf den Wert, den der beste von 575 reinen Zufallsversuchen erreichen würde. Übrig bleibt die Wahrscheinlichkeit, dass der Vorsprung mehr ist als ein Zufallstreffer. Zuletzt lag sie bei 84%.

## Warum 10 Monate bei der Trendregel und nicht 12?

Die Regel stammt aus der Studie „A Quantitative Approach to Tactical Asset Allocation“ von Mebane Faber (2007). Sie vergleicht den Kurs mit dem Durchschnitt der letzten 10 Monatsschlusskurse, was grob der bekannten 200-Tage-Linie entspricht. Die Studie wurde vielfach nachgerechnet, und der Autor hat sie später mit neueren Daten aktualisiert.

Für die 15 ETFs wurde zusätzlich nachgerechnet, wie sich 6, 8, 10 und 12 Monate und eine Variante ohne Trendregel geschlagen hätten. Alle Varianten liegen seit Januar 2024 zwischen +94,8% und +97,4%. Die Wahl von 10 ist also kein Glückstreffer. Die Tabelle steht in der [Gegenrechnung](gegenrechnung.md).

## Schaut der Rückblick in die Zukunft?

Nein. An jedem Monatsende rechnet das Radar nur mit Kursen bis zu diesem Tag. Die Mischung wird dann bis zum nächsten Monatsende gehalten, und erst dieser Folgemonat zählt. Beispiel: Am 30.09.2025 ergab sich Kommunikation 86% und Finanzen 14%. Im Oktober 2025 brachte das +3,1%. Alle 32 Monatsenden stehen in der [Gegenrechnung](gegenrechnung.md).

Eine Einschränkung bleibt. Die Einstellungen, etwa 12 Monate Rückblick, 95% Einfachheitsschwelle und 10 Monate Trendregel, wurden 2026 festgelegt, als der Zeitraum schon bekannt war. Das Ergebnis ist deshalb eher zu gut als zu schlecht.

## Warum steht bei Value einmal 55,9% und einmal 45,5%?

Die Tabelle und die Landkarte im Karussell zeigen die tatsächliche Wertentwicklung über 12 Monate, bei Value 55,9%. Für die Rendite je Schwankung braucht die Rechnung dagegen den Durchschnitt der Tagesrenditen, aufs Jahr hochgerechnet, bei Value 45,5%. Bei starken Anstiegen liegt die tatsächliche Wertentwicklung über diesem Durchschnitt, weil sich Gewinne auf Gewinne aufbauen. Beide Zahlen beschreiben denselben Zeitraum.

## Warum oft nur zwei ETFs?

Wegen der Regel „einfach vor kompliziert“. Die Mischung mit den meisten Punkten ist oft nur minimal besser als eine viel einfachere. Jede Mischung mit mindestens 95% der besten Punktzahl kommt in Frage, und unter diesen gewinnt die mit den wenigsten ETFs. Zwei ETFs bleiben trotzdem ein Klumpen, ein einzelner Sektor kann lange schwächeln.

## Sind Kosten und Steuern eingerechnet?

Nein. Monatliches Umschichten kostet Gebühren und kann Steuern auslösen. Sektor- und Faktor-ETFs haben außerdem höhere laufende Kosten als ein MSCI-World-ETF.

## Ist das eine Empfehlung?

Nein. Das Sektor-Radar ist eine Modellrechnung auf Basis vergangener Kurse. Es kennt keine Bewertungen, Nachrichten oder Zinsprognosen und sagt nichts über die Zukunft.

## Kann ich das nachrechnen?

Ja. Die [Methodik](methodik.md) enthält jede Formel mit Beispielzahlen, die sich mit einer Tabellenkalkulation nachvollziehen lassen. Ein Skript zum eigenen Nachrechnen mit frei verfügbaren Kursen ist in Arbeit.
