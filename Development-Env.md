# Development Env
## Installation
- git installieren: https://git-scm.com/download/win
- ssh Key für Gitlab generieren und in Gitlab hinterlegen. Siehe https://projectbase.medien.hs-duesseldorf.de/profile/keys
- cmake installieren: https://cmake.org/download/
- MinGW 64 installieren ist nicht nötig, wir benutzen MinGW, dass mit Qt kommt
- Qt installieren: https://www.qt.io/download, wir  benutzen die Open Source Variante
- Eine CMake fähige Entwicklungsumgebung. Eclipse scheint derzeit noch nicht zu funktionieren, aber Clion (https://www.jetbrains.com/clion) hat bisher durch Einfachheit in der Bedienung überzeugt. Gibt es kostenlos über das Jetbrains Studentenprogramm: https://www.jetbrains.com/student/

## Umgebungsvariablen:
Windows:
Windowstaste -> Umgebungsvariablen bearbeiten:
PATH: Pfad/zu/Qt/Tools/mingw730_64/bin
Qt5Widgets_DIR: Pfad/zu/Qt/<Qt Version>/mingw73_64


Übersicht über das Projekt:
src: Ordner für Quelldateien
CMakeLists.txt: Konfigurationsdateien für Cmake, siehe "Was ist Cmake?"
build_x86.bat bzw. build_x86.sh: Kompiliert das Projekt für das aktuelle System, die .bat ist für Windows und .sh ist für Linux/Mac OS

Kurzer Test:
```shell
g++ --version
```
```shell
git --version
```
```shell
cmake --version
```
Keines dieser Commands sollte auf der Kommandozeile einen Fehler produzieren.

## Test: Projekt kompilieren und ausführen
Auf der Kommandozeile in ein Verzeichnis wechseln, in dem das Projekt abgelegt werden soll. Git wird automatisch einen Ordner mit dem Projektnamen anlegen
```shell
git clone git@projectbase.medien.hs-duesseldorf.de:cantes/19ss-raspitolight1.git
cd 19ss-raspitolight1
build_x86.bat
```
Wenn es keine Fehler gibt, können die Hello World Anwendungen ausgeführt werden:
```shell
build/src/raspitolight
```
Sollte "Hello world" auf der Konsole ausgeben
```shell
raspitolight_QT.exe
```
Sollte ein Fenster öffnen mit einem Button, auf dem "Hello World" steht.

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

