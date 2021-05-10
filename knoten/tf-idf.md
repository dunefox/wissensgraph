# TF-IDF
Tags: #documentscoring #similarity 

## Term Frequency
$tf_{t,d} = log_{10}(count(t, d) + 1)$

Zählt die Vorkommen des Terms $t$ im Dokument $d$. 1 wird für [[Smoothing]] addiert (Termfrequenz v. 0 im Dokument).

##  Inverse Document Frequency
$idf_{t} = log_{10}(\frac{N}{df_{t}})$
$df_{t} = number\ of\ documents\ t\ occurs\ in$

N entspricht der gesamten Anzahl von Dokumenten. Je weniger Dokumente $t$ enthalten, desto höher das Gewicht.

## TF-IDF
$tf-idf(t, d) = tf_{t, d} * idf_{t}$

![[Pasted image 20210510181518.png]]

## Document Score
$score(q, d) = cos(q, d) = \frac{\textbf{q} * \textbf{d}}{|\textbf{q}| * |\textbf{d}|} = \Sigma_{t \in Q}{\frac{tf-idf(t, d)}{|d|}}$

Für alle Terme der Anfrage q wird die TF-IDF berechnet und durch die Länge des Dokuments normalisiert. Das Ergebnis beschreibt die Ähnlichkeit zwischen Anfrage und Dokument dar.

## Links
* Jurafsky: [Speech and Language Processing, Kap. Question Answering, S. 3](https://web.stanford.edu/~jurafsky/slp3/23.pdf)