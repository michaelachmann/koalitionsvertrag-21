# Koalitionsvertrag '21

Jupyter Notebook & R-Projekt zur Auswertung der Wahlprogramme und des Koalitionsvertrags. Die Inhalte (=Wahlprogramme) werden via GRIPS zur Verfügung gestellt. Work in Progress Projekt für die nächsten Wochen.

## Korpusvorbereitung
Im ersten Schritt wurden die Parteiprogramme / der Koalitionsvertrag als PDF-Dokument heruntergeladen. Anschließend mit Hilfe von Acrobat Reader als `.txt`-Datei exportiert.
![Acrobat Reader PDF to Text Export](images/pdf-to-text1.png)

Die bereitgestellten Text-Dokumente wurden anschließend noch händisch minimal gesäubert: So wurden die Inhaltsverzeichnisseiten, Titelseiten und etwaige Stichwortregister durch löschen entfernt, deshalb der hinweis `_b` für *bearbeitet* im Dateinamen.

## 1. Einstieg: Wortfrequenzen
Im ersten Schritt wurden mit Hilfe von `NLTK` und `pandas` die Wortfrequenzen gezählt und in mehreren `csv`-Dateien abgelegt. Der zugehörige Code findet sich im Notebook `1_word_frequencies`.

## 2. Vertiefung Stoppwörter & Satzzeichen
In diesem Notebook werden die Effekter einzelner Schritte der NLP-Pipeline an den Wahlprogrammen demonstriert.

## 3. Wordcloud(s)
Hier werden mit wenigen Zeilen Code Wortwolken für die Wahlprogramme erstellt.

## 4. Topic Modelling mit LDA
Demonstration des Topic-Modellings mit dem *LDA*-Algorithmus. Dafür werden die Dokumente zunächst eingelesen, tokenisiert und mit Stoppwortlisten abgeglichen. Im Anschluss nutzen wir `HanTa` zur Lemmatisierung. Nachdem der Text vorbereitet ist müssen wir aus unserer geringen Anzahl an Dokumenten künstlich eine größere Zahl erzeugen, daür splitten wir die Dokumente in *n*-Wörter lange Dokumente auf und erhalten in der Größenordnung 1000 Dokumente. Dann kann das `gensim`-Paket genutzt werden um ein Modell zu Trainieren, das schließlich mit `pyLDAvis` interaktiv visualisiert wird.


## Warum Jupyter & R?
Eigentlich wäre es sinnvoll sich auf eine Technik zu konzentrieren, gerade dank `ggplot2` lassen sich mit R allerdings einfacher Plots erstellen, deshalb schon die Vorbereitung beide Programmiersprachen zu nutzen.