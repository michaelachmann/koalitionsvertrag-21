# Koalitionsvertrag '21

Jupyter Notebook & R-Projekt zur Auswertung der Wahlprogramme und des Koalitionsvertrags. Die Inhalte (=Wahlprogramme) werden via GRIPS zur Verfügung gestellt. Work in Progress Projekt für die nächsten Wochen.

## Korpusvorbereitung
Im ersten Schritt wurden die Parteiprogramme / der Koalitionsvertrag als PDF-Dokument heruntergeladen. Anschließend mit Hilfe von Acrobat Reader als `.txt`-Datei exportiert.
![Acrobat Reader PDF to Text Export](images/pdf-to-text1)

Die bereitgestellten Text-Dokumente wurden anschließend noch händisch minimal gesäubert: So wurden die Inhaltsverzeichnisseiten, Titelseiten und etwaige Stichwortregister durch löschen entfernt, deshalb der hinweis `_b` für *bearbeitet* im Dateinamen.

## Einstieg
Im ersten Schritt wurden mit Hilfe von `NLTK` und `pandas` die Wortfrequenzen gezählt und in mehreren `csv`-Dateien abgelegt.

## Warum Jupyter & R?
Eigentlich wäre es sinnvoll sich auf eine Technik zu konzentrieren, gerade dank `ggplot2` lassen sich mit R allerdings einfacher Plots erstellen, deshalb schon die Vorbereitung beide Programmiersprachen zu nutzen.