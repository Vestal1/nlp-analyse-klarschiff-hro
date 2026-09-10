# nlp-analyse-klarschiff-hro
NLP-gestützte Untersuchung der Klarschiff.HRO-Meldungen mit CountVectorizer, TF-IDF, LDA und NMF


# NLP-Analyse der Klarschiff.HRO-Meldungen

In diesem Projekt werden die Beschreibungstexte aus dem Datensatz Klarschiff.HRO untersucht. Ziel ist es, häufige Themen in den Meldungen mit einfachen Verfahren aus dem Bereich Natural Language Processing zu erkennen.

## Datensatz

Verwendet wird der öffentliche Datensatz „Klarschiff.HRO-Meldungen“ der Hanse- und Universitätsstadt Rostock.

Quelle:  
https://www.opendata-hro.de/dataset/klarschiffhro-meldungen

Der Datensatz wird im Notebook direkt über die bereitgestellte CSV-Adresse eingelesen. Da der Datensatz regelmäßig aktualisiert wird, können sich die Ergebnisse bei einer späteren Ausführung etwas verändern.

## Vorgehen

Für die Untersuchung wurden folgende Schritte durchgeführt:

1. Einlesen und erste Betrachtung des Datensatzes
2. Entfernen fehlender Beschreibungstexte
3. Entfernen exakter Wiederholungen
4. Ausschluss von Texten mit weniger als fünf Wörtern
5. Einfache Bereinigung der Texte
6. Darstellung mit CountVectorizer und TF-IDF
7. Themenanalyse mit LDA und NMF
8. Vergleich der Ergebnisse

Für die weitere Analyse konnten 1.807 Beschreibungstexte verwendet werden.

## Ergebnisse

Die Ergebnisse von NMF waren verständlicher als die Ergebnisse von LDA. Bei NMF wurden vier Themen ausgewählt:

- Verkehr und Parken
- Grünflächen und Bewuchs
- Müll und Sperrmüll
- abgestellte Gegenstände

Die Themen passen grundsätzlich zu den vorhandenen Hauptkategorien. Eine genaue Übereinstimmung wurde aber nicht erreicht.

## Dateien

- `notebooks/klarschiff_nlp_analyse.ipynb`: Durchführung der Untersuchung
- `requirements.txt`: benötigte Python-Bibliotheken
- `data/README.md`: Informationen zum Datensatz

## Ausführung

Das Notebook kann mit Jupyter Notebook oder Google Colab geöffnet und ausgeführt werden. Die benötigten Bibliotheken stehen in der Datei `requirements.txt`.

## Einschränkungen

Die Benennung der Themen wurde anhand der wichtigsten Wörter vorgenommen und ist deshalb teilweise subjektiv. Außerdem beeinflussen die ausgewählten Stoppwörter und die Anzahl der Themen das Ergebnis.
