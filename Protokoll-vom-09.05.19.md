Protokoll RTL 09.05.19



STFT: Ausgabe nicht in Funktionswerten, sondern im Bereich 0-256.


-erster Test der Lampen(Datenübertragung). 

STFT: Festlegung der Zeitabstände für die Übertragung von Signalen an die Lampe 
 (idealerweise 0.5). 

-Probleme beim Ausführen in Linux (Fehler mit libraries).

!!!!AUFGABE: Bis nächste Woche versuchen zum Laufen zu kriegen!!!! 



-Wie werden Daten übergeben ? (XML-Datei mit Speichern und Auslesen oder direkt verarbeiten?)

-Austesten mit dem PI(Johannes) 



STFT: 2205 windowsize damit dann 25ms steps ( für 40 Werte die Sekunde) 


-merged STFT+GUI in Struktur mit dem Masterbranch 



GUI:

-noch keine USB-Ausgabe
-Probleme mit QT(crasht), Variante funktioniert
-Anzeigen der Spuren klappt noch nicht so ganz 

Ziel: Slider zum Laufen kriegen, danach Spuren und Ansicht.

!!!Augabe(?): GUI mit den Funktionen der Klasse STFT verbinden(Nicht unbedingt bis nächste Woche)!!!


STFT : Wie klappt eine vernünftige universelle Beat Detection ? 
-Lampen müssten nach den Schlägen faden. 
-Bei 40 Schlägen könnte das egal sein. 


WICHTIG: Alle arbeiten auf der gemerged Version 
	 Bugs bis nächste Woche beheben 
	 