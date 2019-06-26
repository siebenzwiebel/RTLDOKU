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
sudo apt-get install git g++ cmake dh-autoreconf libudev-dev
```
Da CMake mit apt-get nur bis Version 3.10 installiert werden kann und eine neuere nötig ist, muss diese händisch nachinstalliert werden.
```shell
wget https://cmake.org/files/v3.14/cmake-3.14.3.tar.gz
tar xzf cmake-3.14.3.tar.gz
cd cmake-3.14.3
./bootstrap # dauert ca. 25 Minuten
make # dauert ca. 50 Minuten
sudo make install
```

# Projekt klonen
Erst ggf. SSH-Key generieren. Dann:
```shell
git clone git@projectbase.medien.hs-duesseldorf.de:cantes/19ss-raspitolight1.git
```

# Externe Libraries builden
In Projekt-Root-Verzeichnis (mit Python 2.7):
```shell
python build_external_libraries.py
```

# Swap file
Das Builden mit ```./build_x86.sh``` sollte mit einem kryptischen Fehler schiefgehen. Das Problem löst ein Swap file:
```shell
sudo dd if=/dev/zero of=/swapfile1GB bs=1M count=1024
sudo mkswap /swapfile1GB
sudo swapon /swapfile1GB
```

```sudo swapon /swapfile1GB``` muss nach jedem Booten ausgeführt werden (wenn der RAM zum Builden gebraucht wird).

# USB-Rechte
Standardmäßig existieren nur die benötigten Rechte zum Öffnen des USB-Devices, wenn das Programm als root ausgeführt wird. Um es auch ohne ```sudo``` ausführen zu können, folgendes tun:
```shell
sudo nano /etc/udev/rules.d/98-usb-permissions.rules
```
In die Datei ```SUBSYSTEM=="usb", ATTRS{idVendor}=="10cf", ATTRS{idProduct}=="8062", MODE="0666"``` schreiben.
Gegebenenfalls neu einloggen bzw. rebooten.

# Zusätzliche Installationen für QMediaPlayer
Sollte beim Klicken auf Play der 
```defaultServiceProvider::requestService(): no service found for - "org.qt-project.qt.mediaplayer"```
oder ein ähnlicher Fehler auftreten, müssen noch weitere Pakete zur Unterstützung des QMediaPlayers installiert werden. Die benötigten Pakete werden bei verschiedenen Paketen mit installiert, eine Möglichkeit ist
```sudo apt-get install libqt5multimedia5-plugins```