---
title: LXDB MediaSorter Installation unter Linux
image: "/images/lms/lms.png"
draft:
layout: "lms"
---

---
Bringen sie ihre Dateien in Ordnung !

# LXDB MediaSorter ? - Aber was ist das ?

## Idee

Diese Situation ist ihnen bestimmt bekannt - In der modernen Zeit macht man viele Fotos oder Videos, aber man hat nicht die Zeit alle diese Dateien in Ordnung zu bringen - Wenn es nur einfacher ginge ...

Genau dafür wurde LXDB MediaSorter erschaffen - Um einfach auf Knopfdruck Ordnung in Ihre Dateien zu bringen.

## Doch wie funktioniert LXDB MediaSorter ?

![lms](/images/lms/lms-1.png)

Die Nutzung von LXDB MediaSorter ist kinderleicht.

Einfach einen Ordner mit Bildern oder Videos auswählen, Datei- und gegebenenfalls Ordnernamenschema auswählen und auf Start klicken - nach nur ein paar Sekunden herrscht Ordnung in ihren Mediendateien.

## Was kann LXDB MediaSorter ?

![vhnh](/images/lms/vorher-nachher-bt.png)

- Dateien nach Erstellungsdatum und eigenem Nennungschema umbenennen und in Ordner einsortieren

![Metadaten](/images/lms/lms-metadata.png)

- Metadaten von Bidern und Videos anzeigen

![Vorschau](/images/lms/lms-preview.png)

- Foto- und Videovorschau
![Terminal-Version](/images/lms/lms-cli.png)

- Textbasierende Terminal-Version

## LXDB MediaSorter installieren

LXDB MediaSorter ist unter den meisten Linux-Distributionen installierbar.

### Installationsmethoden

- Installation als Python-Paket aus GIT-Repository(```exiftool``` muss als Abhängigkeit extra installiert werden)

- Installation aus der LXDB-Paketquelle(Alle Abhängigkeiten werden mitinstalliert)

- Installation aus einem DEB/RPM-Paket

#### 1. Installation als Python-Paket

[PyPi.org](https://pypi.org) ist die größte Paketquelle für Python-Programme und Bibliotheken. Um LXDB MediaSorter aus der PyPi-Quelle zu installieren, muss das Paket ```python3-pip``` im System installiert sein.

Zur Installation muss der folgende Befehl ausgeführt werden:

```bash
python3 -m pip install git+https://github.com/lxdb/lms.git
```

Desweiteren muss das Kommandozeilenprogramm `exiftool` installiert werden.

Dieses ist z.B. unter RPM-Distributionen im Paket `perl-Image-ExifTool` oder unter DEB-Distributionen im Paket `libimage-exiftool-perl` verfügbar.

#### 2. Installation aus der LXDB-Paketquelle

Im LXDB-Repository sind fertige DEB- und RPM-Pakete verfügbar, die in allen Debian- und RPM-basierenden Distributionen installiert werden können.

##### Installation mit APT-Paketmanager

1. Repository hinzufügen:

   Zum hinzufügen vom LXDB-Repository für Debian-basierende Distributionen müssen folgend Befehle in der Kommandozeile ausgeführt werden:

   ```bash
   echo 'deb https://dl.bintray.com/lxdb/deb /' | sudo tee -a /etc/apt/sources.list
   wget -qO - "https://bintray.com/user/downloadSubjectPublicKey?username=bintray" | sudo apt-key add -
   sudo apt update
   ```

2. Paket installieren:

   ```bash
   sudo apt install python3-lms
   ```

##### Installation mit DNF-Paketmanager

1. Repository hinzufügen:

   Zum hinzufügen vom LXDB-Repository für RPM-Distributionen mit DNF-Paketmanager müssen folgende Befehle in der Kommandozeile ausgeführt werden:

   ```bash
   wget "https://bintray.com/lxdb/rpm/rpm" -O bintray-lxdb-rpm.repo
   sudo dnf config-manager --add-repo bintray-lxdb-rpm.repo
   sudo dnf check-update
   ```

2. Paket installieren:

   ```bash
   sudo dnf install lms
   ```

##### Instalation mit YUM-Paketmanager

1. Repository hinzufügen:

   Zum hinzufügen vom LXDB-Repository für RPM-Distributionen mit YUM-Paketmanager müssen folgende Befehle in der Kommandozele ausgeführt werden:

   ```bash
   wget "https://bintray.com/lxdb/rpm/rpm" -O bintray-lxdb-rpm.repo
   sudo mv bintray-lxdb-rpm.repo /etc/yum.repos.d/
   sudo yum update
   ```

2. Paket installieren:

   ```bash
   sudo yum install lms
   ```

##### Installation mit ZYPPER-Paketmanager

1. Repository hinzufügen:

   Zum hinzufügen vom LXDB-Repository für RPM-Distributionen mit ZYPPER-Paketmanager müssen folgende Befehle in der Kommandozele ausgeführt werden:

   ```bash
   wget "https://bintray.com/lxdb/rpm/rpm" -O bintray-lxdb-rpm.repo
   sudo zypper ar bintray-lxdb-rpm.repo
   sudo zypper refresh
   ```

2. Paket installieren:

   ```bash
   sudo zypper in lms
   ```

#### 3. Installation mit DEB- oder RPM-Datei

[DEB-Datei herunterladen](https://dl.bintray.com/lxdb/deb/lms_2020.4_amd64.deb)

[RPM-Datei herunterladen](https://dl.bintray.com/lxdb/rpm/lms_2020.4_amd64.rpm)
