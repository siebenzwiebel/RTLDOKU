## Was ist Cmake?
CMake ist ein Build System Generator. Cmake erlaubt es, ein C++ Projekt platform und Buildsystem unabhängig zu beschreiben. Aus dieser abstrakten Beschreibung können dann Dateien für das Build System generiert werden, mit dem das Projekt kompiliert werden soll. In unsererem Fall ist das auf Windows z.B. "MinGW Makefiles", es könnte bei anderen Projekten aber auch Visual Studio sein. Eine Übersicht über alle derzeit verfügbaren Build Systeme liefert 
```shell
cmake -G
```
Cmake funktioniert über Textdateien, die CMakeLists.txt. In unseerem Projekt gibt es im Projektverzeichnis eine CMakeLists.txt, die folgendes tut:
- den Projektnamen festlegen
- den C++ Sprachstandart festzulegen
- Qt auf dem System suchen und verfügbar machen
- mittels add_subdirectory(src) wird Cmake mitgeteilt, dass es auch im Unterverzeichnis src nach CMakeLists.txt Dateien Ausschau halten soll

In der  src/CMakeLists.txt werden zwei ausführbare Dateien definiert, die vom Kompiler erzeugt werden. Für jede ausführbare Datei wird festgelegt, aus welchen Sources sie bestehen soll, wie sie heißen soll und wo sie später liegen soll. Für die ausführbare Datei mit QT wird zusätzlich definiert, dass diese ausführbare Datei gegen Qt gelinkt werden soll

