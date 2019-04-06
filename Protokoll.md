# Raspi to Light

## 1. Projekttreffen

## 2. Projekttreffen — 4. April 2019

* Cross-Compilation möglich (Multichain), muss also nicht auf dem Pi gemacht werden (Erstes GOogle-Ergebnis: "raspberry pi eclipse c++)
* STFT in C++ Beispiel: https://stackoverflow.com/questions/31475842/getting-values-for-specific-frequencies-in-a-short-time-fourier-transform
* CMake soll genutzt werden (IDE und OS Uabhängigkeit, Tutorial wird noch in Moodle bereitgestellt)
* GitLab Runner installieren (außerhalb der Sitzung) für GitLab CI (Server benötigt, Docker Anleitungen gibt es zu Hauf)
* Qt mit Widgets soll genutzt werden (GUI)
* Kommunikation via WhatsApp

* Aufgabenverteilung
  * Oberfläche (mit Qt / MIIP)
    * Player-Verwaltung (Jens Dolfus)
    * Fixture-Verwaltung (Sebastian Rindfleisch)
    * Edit-Ansicht (Beide)
  * SigV
    * Einlesen Audisignal
    * Abtastung Audiosignal
    * Algorithmus STFT (Steven Drewers)
    * Mapping Audio/Licht (Johannes Hirth)
  * I/O
    * DMX Hardware Ausgabe / GPIO (Johannes Hirth)
    * Datei-Handling / Speichern & Laden von Shows (Fabian Krüger)
  * Bonus
    * GPIOs nutzen, Extension Board bauen, UART-DMX (Steven Einkaufsliste)
  * Entwicklungsumgebung aufsetzen (erste Aufgabe / MIMP)
    * Aufsetzen
    * Tutorial
