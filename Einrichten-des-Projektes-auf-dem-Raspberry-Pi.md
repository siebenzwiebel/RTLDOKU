# Benötigte Pakete
Die Angaben beziehen sich auf der Image "Rasbian Stretch with Desktop and recommended Software"
## Zum Ausführen des Projektes auf dem Pi:
Es wird ein Build von Qt 5 benötigt.

Die Abhängigkeit von qt5-multimedia-dev verschwindet, sobald wir Qt nicht mehr zum Abspielen von Sound verwenden
qt5-default qt5-multimedia-dev
```shell
sudo apt-get install qt5-default qt5-multimedia-dev
```
## Zum Kompilieren des Projektes:
Ggf müssen noch git, g++ & cmake installiert werden
```shell
sudo apt-get install git g++ cmake
```