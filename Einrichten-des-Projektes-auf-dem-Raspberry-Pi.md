# Benötigte Pakete
Die Angaben beziehen sich auf der Image "Rasbian Stretch with Desktop and recommended Software"
## Zum Ausführen des Projektes auf dem Pi:
Es wird ein Build von Qt 5 benötigt.

Die Abhängigkeit von qtmultimedia5-dev verschwindet, sobald wir Qt nicht mehr zum Abspielen von Sound verwenden

```shell
sudo apt-get install qt5-default qtmultimedia5-dev
```
## Zum Kompilieren des Projektes:
Ggf müssen noch git, g++ & cmake installiert werden
```shell
sudo apt-get install git g++ cmake
```