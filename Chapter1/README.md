# Install QGIS on Ubuntu

```bash
lsb_release -a

sudo gedit /etc/apt/sources.list

# repo qgis 3.8 https://qgis.org/ubuntu
deb     https://qgis.org/ubuntu bionic main
deb-src https://qgis.org/ubuntu bionic main
deb     https://qgis.org/debian bionic main
deb-src https://qgis.org/debian bionic main

# repo qgis 3.4 ltr https://qgis.org/ubuntu-ltr
deb     https://qgis.org/ubuntu-ltr bionic main
deb-src https://qgis.org/ubuntu-ltr bionic main
deb     https://qgis.org/debian-ltr bionic main
deb-src https://qgis.org/debian-ltr bionic main

sudo apt-get update

wget -O - https://qgis.org/downloads/qgis-2019.gpg.key | gpg --import
gpg --fingerprint 51F523511C7028C3
gpg --export --armor 51F523511C7028C3 | sudo apt-key add -

sudo apt-get install qgis qgis-plugin-grass

sudo apt-get install qgis qgis-plugin-grass saga

```
# Remove QGIS 3 on Ubuntu

```bash
# alt1
sudo apt-get autoremove
sudo apt-get autoclean
sudo apt-get -f install
sudo apt-get autoremove qgis
sudo apt-get --purge remove qgis

sudo apt-get install python-software-properties
sudo add-apt-repository ppa:ubuntugis/ubuntugis-unstable
sudo apt-get update
sudo apt-get install qgis python-qgis qgis-plugin-grass

# alt2
sudo apt-get remove qgis
sudo apt-get remove --auto-remove qgis
sudo apt-get purge qgis
sudo apt-get purge --auto-remove qgis

```