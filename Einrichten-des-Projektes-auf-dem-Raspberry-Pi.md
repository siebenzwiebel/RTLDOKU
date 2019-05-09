# Intro
Das Projekt wurde für den Raspberry Pi 3 B+ mit Ubuntu Mate (64 bit) entwickelt und auch nur dort getestet! Die folgenden Angaben beziehen sich darauf, das Projekt in einer solchen Umgebung auszuführen.

# Ubuntu Mate (64 bit)
Direkter Download-Link des Images: [https://ubuntu-mate.org/raspberry-pi/ubuntu-mate-18.04.2-beta1-desktop-arm64+raspi3-ext4.img.xz](https://ubuntu-mate.org/raspberry-pi/ubuntu-mate-18.04.2-beta1-desktop-arm64+raspi3-ext4.img.xz).

Flashen auf eine SD-Karte ist besonders einfach mit dem Tool [Etcher](https://www.balena.io/etcher/).

# Benötigte Pakete
## Zum Ausführen des Projektes auf dem Pi:
Es wird ein Build von Qt 5 benötigt.

Die Abhängigkeit von qtmultimedia5-dev verschwindet, sobald wir Qt nicht mehr zum Abspielen von Sound verwenden

```shell
sudo apt-get install qt5-default qtmultimedia5-dev
```
## Zum Kompilieren des Projektes:
Ggf müssen noch git, g++ & cmake installiert werden.
```shell
sudo apt-get install git g++ cmake
```
Da CMake mit apt-get nur bis Version 3.10 installiert werden kann und eine neuere nötig ist, muss diese händisch nachinstalliert werden.
```shell
wget https://cmake.org/files/v3.14/cmake-3.14.3.tar.gz
tar xzf cmake-3.14.3-Linux-x86_64.tar.gz
cd cmake-3.14.3-Linux-x86_64
./bootstrap
make
sudo make install
```