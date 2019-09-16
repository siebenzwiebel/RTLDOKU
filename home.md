# 1. Projektmanagement
## [1.1 Änderungsnachweis](1.1 Änderungsnachweis)
Hier notieren Sie das Projektmanagement betreffende Erweiterungen und Modifikationen (Änderung des Zeitplans, neues Protokoll, etc.)
## [1.2 Zuständigkeiten](1.2 Zuständigkeiten)
Wer übernimmt welche Aufgaben und wer ist verantwortlich für das jeweilige Arbeitspaket?
## [1.3 Protokolle](1.3 Protokolle)
Für jedes Projekttreffen wird ein Protokoll geschrieben.
# 2. Spezifikationen
Zusammenfassung aller Vorgaben: SOLL
## [2.1 Aufgabenstellung](2.1 Aufgabenstellung)
Die **Aufgabenstellung** steckt einen groben Rahmen für Ihre Projekttätigkeit und **wird vom Projektanbieter vorgegeben**. 
## [2.2 Zielgruppe](2.2 Zielgruppe)
Wer wird Ihre Anwendung später benutzen?  
Welche Konsequenzen hat dies für die Entwicklung?
## [2.3 Technische Randbedingungen](2.3 Technische Randbedingungen)
Welche Anforderungen an Software und Hardware gibt es?  
Welche Sprachen, Bibliotheken und/oder Frameworks sollen eingesetzt werden?
## [2.4 Ziele](2.4 Ziele)
In dem durch die Aufgabenstellung gesteckten Rahmen **definieren die Projektteilnehmer in der Regel 5 bis 10 Ziele** (Beispiele: *"Spielen [der Anwendung] über das Netzwerk"* oder *"Bewegen von Figuren mit Drag'n'Drop"*). 
# 3. Umsetzung
Zusammenfassung aller durchgeführter Maßnahmen: IST
## [3.1 Hardware](3.1 Hardware)
### [3.1.1 Raspberry Pi](3.1 Hardware#311-raspberry-pi)
### [3.1.2 DMX-Interfaces](3.1 Hardware#312-dmx-interfaces)
## [3.2 Entwicklungsumgebung](3.2 Entwicklungsumgebung)
### [3.2.1 C++](3.2 Entwicklungsumgebung#321-c++)
### [3.2.2 Build-System](3.2 Entwicklungsumgebung#322-build-system)
### [3.2.3 IDE](3.2 Entwicklungsumgebung#323-ide)
### [3.2.4 Dependency Management](3.2 Entwicklungsumgebung#324-dependency-management)
### [3.2.5 Wie entwickeln wir für den Raspberry Pi?](3.2 Entwicklungsumgebung#325-wie entwickeln-wir-fuer-den-raspberry-pi)
### [3.2.6 Stack Traces mit C++](3.2 Entwicklungsumgebung#326-stack-traces-mit-c++)
## [3.3 Software–Architektur](3.3 Software-Architektur)
### [3.3.1 Motivation](3.3 Software–Architektur#331-motivation)
### [3.3.2 Separation GUI/Core](3.3 Software–Architektur#332-seperation-gui-core)
### [3.3.3 Logging](3.3 Software–Architektur#333-logging)
### [3.3.4 DMX Interfaces](3.3 Software–Architektur#334-dmx-interfaces)
### [3.3.5 MusicPlayer](3.3 Software–Architektur#335-musicplayer)
## [3.4 Analyse](3.4 Analyse)
### [3.4.1 Einlesen von Dateien](3.4 Analyse#341-einlesen-von-dateien)
### [3.4.2 Fourier-Analyse](3.4 Analyse#342-fourier-analyse)
### [3.4.3 Beat Detection](3.4 Analyse#343-beat-detection)
### [3.4.4 Segmentierung](3.4 Analyse#344-segmentierung)
### [3.4.5 Hilfsfunktionen](3.4 Analyse#345-hilfsfunktionen)
## [3.5 Lightshow](3.5 Lightshow)
### [3.5.1 Struktur](3.5 Lightshow#351-klassen-rund-um-eine-lightshow)
### [3.5.2 Generierung](3.5 Lightshow#352-generierung-einer-lightshow)
### [3.5.3 Persistierung](3.5 Lightshow#353-persistierung-von-lightshows)
### [3.5.4 Abspielen](3.5 Lightshow#354-abspielen-einer-lightshow)
### [3.5.5 Übertragung DMX](3.5 Lightshow#355-kommunikation-zwischen-anwendung-und-dmx-device)
### [3.5.6 Implementierung von Portaudio](3.5 Lightshow#357-implementierung-von-portaudio)
## [3.6 Graphical User Interface](3.6 Graphical User Interface)
### [3.6.1 Übersicht](3.6 Graphical User Interface#361-übersicht)
### [3.6.2 MainWindow](3.6 Graphical User Interface#362-mainwindow)
### [3.6.3 Fixture Management](3.6 Graphical User Interface#363-fixture-management)
### [3.6.4 Player-View](3.6 Graphical User Interface#364-player-view)
### [3.6.5 Playlist-View](3.6 Graphical User Interface#365-playlist-view)
### [3.6.6 Playlist](3.6 Graphical User Interface#366-playlist)
### [3.6.7 Hinzufügen eines Songs](3.6 Graphical User Interface#367-hinzufügen-eines-songs)
### [3.6.8 Löschen eines Songs](3.6. Graphical User Interface#368-löschen-eines-songs)
### [3.6.9 Playlist Reihenfolge verändern](3.6. Graphical User Interface#369-playlist-reihenfolge-verändern)
### [3.6.10 Songauswahl durch Doppelt klicken](3.6. Graphical User Interface#3610-songauswahl-durch-doppelt-klicken)
# [4. Quellen & Ressourcen](4. Quellen & Ressourcen)