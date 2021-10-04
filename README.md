[RobotName]: Adeept_Rasptank
[RobotURL]: https://github.com/adeept/adeept_rasptank
[RobotGit]: https://github.com/adeept/adeept_rasptank.git
[Official Raspberry Pi website]: https://www.raspberrypi.org/downloads/
[Image file for the Raspberry Pi Robot]: https://adeept-my.sharepoint.com/personal/tomsun_adeept_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ftomsun%5Fadeept%5Fonmicrosoft%5Fcom%2FDocuments%2FadeeptRaspTank&amp ; originalPath = aHR0cHM6Ly9hZGVlcHQtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvdG9tc3VuX2FkZWVwdF9vbm1pY3Jvc29mdF9jb20vRXZCZmhES1dJVEJLb1ZLejFJTThta01CaWc5SHRiZG9sMXdLQU83WTk5cFJWdz9ydGltZT1rUWxJeE9EMjEwZw
[Official website]: https://www.adeept.com/
[GitHub]: https://github.com/adeept/adeept_rasptank/
[Documentation for structure assembly]: https://www.adeept.com/learn/

Erste Schritte mit Raspberry Pi Robot und Python
----
* [Erste Schritte mit Raspberry Pi Robot und Python](#getting-started-with-raspberry-pi-robot-and-python)
    * [1. Prämisse](#1-Prämisse)
       * [1.1 STEAM und Raspberry Pi](#11-steam-and-raspberry-pi)
       * [1.2 Über die Dokumentation](#12-über-die-dokumentation)
    * [2. Erste Schritte mit dem Raspberry Pi](#2-Getting-to-use-the-raspberry-pi)
       * [2.1 Das Raspberry Pi-Image auf eine SD-Karte schreiben](#21-write-the-raspberry-pi-image-to-an-sd-card)
          * [2.1.1 Methode A: 'Raspbian' mit Raspberry Pi Imager auf die SD-Karte schreiben](#211-method-a-write-raspbian-to-the-sd-card-by-raspberry-pi-imager)
          * [2.1.2 Methode B: Laden Sie die Image-Datei Raspbian herunter und schreiben Sie sie manuell auf die SD-Karte](#212-method-b-download-the-image-file-raspbian-and-write-it-to-the-SD-Karte-manuell)
          * [2.1.3 Methode C: Laden Sie die von uns bereitgestellte Bilddatei manuell herunter und schreiben Sie sie auf die SD-Karte (nicht empfohlen)](#213-method-c-manually-download-the-image-file-provided-by-uns-und-schreiben-es-auf-die-sd-karte-nicht-empfohlen)
       * [2.2 SSH-Server von Raspberry Pi aktivieren](#22-enable-ssh-server-of-raspberry-pi)
          * [2.2.1 Methode A: SSH mit Peripheriegeräten aktivieren](#221-method-a-enable-ssh-with-peripherals)
          * [2.2.2 Methode A: SSH ohne Peripheriegeräte aktivieren](#222-method-a-enable-ssh-ohne-peripheriegeräte)
       * [2.3 WLAN auf Raspberry Pi konfigurieren](#23-configure-wifi-on-raspberry-pi)
          * [2.3.1 Methode A: WiFi-Verbindung mit Peripheriegeräten](#231-Methode-eine-WLAN-Verbindung-mit-Peripheriegeräten)
          * [2.3.2 Methode A: WiFi-Verbindung ohne Peripheriegeräte](#232-Methode-eine-WLAN-Verbindung-ohne-Peripheriegeräte)
    * [3. Softwareinstallation &amp; Betrieb auf Raspberry Pi](#3-software-installation--operation-on-raspberry-pi)
       * [3.1 Bei Raspberry Pi anmelden (Windows 10)](#31-log-in-raspberry-pi-windows-10)
       * [3.2 Anmelden bei Raspberry Pi (Linux oder Mac OS)](#32-log-in-raspberry-pi-linux-or-mac-os)
       * [3.3 Einloggen in Raspberry Pi (Windows)](#33-log-in-raspberry-pi-windows)
       * [3.4 Download-Programm des Raspberry Pi-Roboters](#34-download-program-of-the-raspberry-pi-robot)
       * [3.5 Entsprechende abhängige Bibliotheken installieren](#35-installieren-entsprechende-abhängige-Bibliotheken)
       * [3.6 Führen Sie das Programm des Raspberry Pi Robots aus](#36-run-the-raspberry-pi-robots-program)
    * [4. Vorsichtsmaßnahmen für die Strukturmontage](#4-Vorsichtsmaßnahmen-für-Strukturmontage)
          * [4.1 Dokumentation zur Strukturmontage](#41-Dokumentation-für-Strukturmontage)
          * [4.2 Vorsichtsmaßnahmen für die Strukturmontage](#42-Vorsichtsmaßnahmen-für-Strukturmontage)
    * [5. Roboter über WEB-App steuern](#5-Roboter-Steuerung-über-Web-App)
    * [6. Fragen und Antworten](#6-qa)


## 1. Prämisse
### 1.1 STEAM und Raspberry Pi
STEAM steht für Wissenschaft, Technologie, Ingenieurwesen, Kunst und Mathematik. Es ist eine Art transdisziplinäre Bildungsidee, die auf die Praxis ausgerichtet ist.
Als Board, das für die Ausbildung in Computerprogrammierung entwickelt wurde, hat Raspberry Pi viele Vorteile gegenüber anderen Roboterentwicklungsboards. Daher wird Raspberry Pi zur Funktionskontrolle des Roboters verwendet.

### 1.2 Über die Dokumentation
Diese Dokumentation ist eine Softwareinstallations- und Bedienungsanleitung für das Python-Roboterprodukt. Es beschreibt jedes Detail des gesamten Prozesses der Erfüllung des Roboterprojekts von Python und Raspberry Pi von Grund auf sowie einige Vorsichtsmaßnahmen. Ich hoffe, Sie können mit dem Raspberry Pi-Roboter auf Python loslegen und mit dieser Dokumentation weitere Kreationen erstellen.

![Meerjungfrau](images/mermaid.png)

e nach den unterschiedlichen Situationen verschiedener Benutzer wird es im Prozess dieses Dokuments einige Änderungen geben. Sie können sich auf den folgenden Prozess beziehen:

## 2. Wie Sie den Raspberry Pi verwenden

### 2.1 Das Raspberry Pi-Image auf eine SD-Karte schreiben


#### 2.1.1 Methode A: 'Raspbian' mit 'Raspberry Pi Imager' auf die SD-Karte schreiben
"Raspberry Pi Imager" ist ein von der Raspberry Pi Organization entwickeltes Tool zum Schreiben von Bildern auf eine SD-Karte. Es wird mit vielen Versionen geliefert, die auf verschiedenen Systemen funktionieren, und es ist ziemlich einfach zu bedienen; Sie müssen lediglich das Betriebssystem und die SD-Karte auswählen, Raspberry Pi Imager lädt die entsprechende Image-Datei für das System herunter und installiert sie auf der SD-Karte.

**Schritt-für-Schritt-Übersicht**

1. Bereiten Sie eine SD-Karte (16 GB oder größer) und einen SD-Kartenleser vor
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website](https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe) "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen."
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg) "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen." 
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb) "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen."
3. Installieren Sie den `Raspberry Pi Imager`
4. Schreiben Sie das Betriebssystem für Raspberry Pi auf die SD-Karte mit `Raspberry Pi Imager` `Raspbian Full - Eine Portierung von Debian mit Desktop und empfohlener Anwendung`
5. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website](https://www.raspberrypi.org/downloads/), suchen Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem und laden Sie ihn herunter. oder klicken Sie auf die obigen Links für das entsprechende System, um es direkt herunterzuladen und zu installieren.

  ![imagerDownload](images/imagerDownload.png)

- Legen Sie die SD-Karte in den Kartenleser ein, verbinden Sie den Kartenleser und Ihren Computer.

- Führen Sie den `Raspberry Pi Imager` aus, wählen Sie `CHOOSE OS` -> `Raspbian(other)` -> `Raspbian Full - A Port of Debian with desktop and Recommended applications`.

- Klicken Sie auf "SD-KARTE AUSWÄHLEN", damit die SD-Karte das "Raspbian Full" schreibt. Bitte beachten Sie, dass beim Schreiben des Bildes automatisch alle Dateien auf der SD-Karte gelöscht werden, falls vorhanden.

- Klicken Sie auf `WRITE`, warten Sie auf das Schreiben. Der `Raspberry Pi Imager` muss während des Vorgangs die `Raspbian`-Image-Datei herunterladen. Sie können die Datei nach dem Schritt in **2.1.2** herunterladen.

  ![imagerUse](images/imagerUse.png)

- Entfernen Sie nicht die angeschlossene SD-Karte, wenn der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung. Andernfalls, wenn Sie die Karte entfernen, in den Raspberry Pi einsetzen und booten, kann die WLAN-Konfiguration ohne Peripheriegeräte im folgenden Prozess fehlschlagen.


#### 2.1.2 Methode B: Laden Sie die Image-Datei `Raspbian` herunter und schreiben Sie sie manuell auf die SD-Karte
Da die Image-Datei mit dem `Raspberry Pi Imager` in **2.1.1** heruntergeladen wird, kann es aufgrund eines langsamen Netzwerks an manchen Stellen lange dauern. Sie können dann die Image-Datei `Raspbian` manuell herunterladen und mit dem `Raspberry Pi Imager` auf die SD-Karte schreiben.

**Schritt-für-Schritt-Übersicht**

1. Bereiten Sie eine SD-Karte (16 GB oder größer) und einen SD-Kartenleser vor
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website](https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe) "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen."
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg) "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen."
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb) "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen."
3. Installieren Sie den `Raspberry Pi Imager`
4. Laden Sie die IMAGE-Datei `Raspbian` . herunter
    - Torrent-Datei:
    [Raspbian - Raspbian Buster mit Desktop und empfohlener Software](https://downloads.raspberrypi.org/raspbian_full_latest.torrent) "Link zum Download der Torrent-Datei für Bild."
    - Zip-Datei: [Raspbian - Raspbian Buster mit Desktop und empfohlener Software](https://downloads.raspberrypi.org/raspbian_full_latest) "Link zum Download der Zip-Datei für das Bild."
5. Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
6. Schreiben Sie die auf die SD-Karte heruntergeladene Bilddatei `Raspbian` mit `Raspberry Pi Imager`
7. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website], suchen und laden Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem herunter oder klicken Sie auf die obigen Links, um das entsprechende System direkt herunterzuladen und Installieren.

  ![imagerDownload](images/imagerDownload.png)

- Wählen Sie auf der Raspberry Pi-Website [Offizielle Raspberry Pi-Website](https://www.raspberrypi.org/downloads/ ) über `Downloads` -> `Raspbian` -> `Raspbian Buster mit Desktop und empfohlener Software` und Klicken Sie zum Herunterladen auf die Torrent- oder ZIP-Datei. Entpacken Sie die Datei nach dem Download, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt; andernfalls öffnet `Raspberry Pi Imager` die `.img`-Datei möglicherweise nicht. Es wird empfohlen, die Datei `.img` im Stammverzeichnis der Festplatte `C:\` oder `D:\` zu speichern, **aber `.img` nicht auf der SD-Karte zu speichern**.

  ![RPiDownload](images/RPiDownload.png)

- Legen Sie die SD-Karte in den Kartenleser ein, verbinden Sie den Kartenleser und Ihren Computer.

- Führen Sie den `Raspberry Pi Imager` aus, wählen Sie `CHOOSE OS` und dann `Use custom`, um die extrahierte `.img` zu finden, klicken Sie auf `Open`.

- Wählen Sie "SD-KARTE AUSWÄHLEN" für die SD-Karte, um das "Raspbian" zu schreiben. Bitte beachten Sie, dass beim Schreiben von Bildern automatisch alle Dateien auf der SD-Karte gelöscht werden, falls vorhanden.

- Klicken Sie auf `WRITE`, warten Sie auf das Schreiben.

  ![imagerUse](images/imagerUse.png)

- Entfernen Sie nicht die angeschlossene SD-Karte, wenn der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung. Andernfalls, wenn Sie die Karte entfernen, in den Raspberry Pi stecken und hochfahren, kann die WLAN-Konfiguration ohne Peripheriegeräte im folgenden Prozess fehlschlagen.

#### 2.1.3 Methode C: Laden Sie die von uns bereitgestellte Bilddatei manuell herunter und schreiben Sie sie auf die SD-Karte (nicht empfohlen)
Die in **2.1.1** und **2.1.2** heruntergeladene Raspbian-Image-Datei ist die offizielle Quelle mit vorinstallierter Software. Um den Roboter zu bedienen, benötigen Sie möglicherweise viele abhängige Bibliotheken. Obwohl wir das einfache Skript für die Installation bereitstellen (siehe Details später), kann es während der Installation zu Fehlern kommen, wenn die Bibliothek nicht die neueste Version ist. Daher kann es trotz der Bereitstellung des Herunterladens der Raspbian-Image-Datei vorkommen, dass unsere Image-Datei und die abhängigen Bibliotheken nicht die aktuellsten Versionen sind. Bitte nur verwenden, wenn Sie auf die schwierigste Situation stoßen.
**Schritt-für-Schritt-Übersicht**

1. Bereiten Sie eine SD-Karte (16 GB oder größer) und einen SD-Kartenleser vor
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website](https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe) "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen."
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg) "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen."
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb) "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen."
3. Installieren Sie den `Raspberry Pi Imager`
4. Laden Sie die Bilddatei `Raspbian` . herunter
    - [Image-Datei für den Raspberry Pi-Roboter](https://adeept-my.sharepoint.com/personal/tomsun_adeept_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ftomsun%5Fadeept%5Fonmicrosoft%5Fcom%2FDocuments%2FadeeptRaspTank&originalPath=aHR0cHM6Ly9hZGVlcHQtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvdG9tc3VuX2FkZWVwdF9vbm1pY3Jvc29mdF9jb20vRXZCZmhES1dJVEJLb1ZLejFJTThta01CaWc5SHRiZG9sMXdLQU83WTk5cFJWdz9ydGltZT1rUWxJeE9EMjEwZw)
5. Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
6. Schreiben Sie die auf die SD-Karte heruntergeladene Bilddatei `Raspbian` mit `Raspberry Pi Imager`
7. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website](https://www.raspberrypi.org/downloads/), suchen Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem und laden Sie ihn herunter. oder klicken Sie auf die obigen Links für das entsprechende System, um es direkt herunterzuladen und zu installieren.

  ![imagerDownload](images/imagerDownload.png)

- Gehen Sie zu unserer [offiziellen Website](https://www.adeept.com/), suchen Sie die Image-Datei und laden Sie sie herunter - [Image-Datei für den Raspberry Pi-Roboter](https://adeept-my.sharepoint.com/personal/tomsun_adeept_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ftomsun%5Fadeept%5Fonmicrosoft%5Fcom%2FDocuments%2FadeeptRaspTank&originalPath=aHR0cHM6Ly9hZGVlcHQtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvdG9tc3VuX2FkZWVwdF9vbm1pY3Jvc29mdF9jb20vRXZCZmhES1dJVEJLb1ZLejFJTThta01CaWc5SHRiZG9sMXdLQU83WTk5cFJWdz9ydGltZT1rUWxJeE9EMjEwZw). Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt. andernfalls öffnet `Raspberry Pi Imager` die `.img`-Datei möglicherweise nicht. Es wird empfohlen, die Datei `.img` im Stammverzeichnis der Festplatte `C:\` oder `D:\` zu speichern, **aber `.img` nicht auf der SD-Karte zu speichern**.

- Legen Sie die SD-Karte in den Kartenleser ein, verbinden Sie den Kartenleser und Ihren Computer.

- Führen Sie den `Raspberry Pi Imager` aus, wählen Sie `CHOOSE OS` und dann `Use custom`, um die extrahierte `.img` zu finden, klicken Sie auf `Open`.

- Wählen Sie "SD-KARTE AUSWÄHLEN" für die SD-Karte, um das "Raspbian" zu schreiben. Bitte beachten Sie, dass beim Schreiben von Bildern automatisch alle Dateien auf der SD-Karte gelöscht werden, falls vorhanden.

- Klicken Sie auf `WRITE`, warten Sie auf das Schreiben.

  ![imagerUse](images/imagerUse.png)

- Entfernen Sie nicht die angeschlossene SD-Karte, wenn der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung. Andernfalls, wenn Sie die Karte entfernen, in den Raspberry Pi stecken und hochfahren, kann die WLAN-Konfiguration ohne Peripheriegeräte im folgenden Prozess fehlschlagen.

### 2.2 SSH-Server des Raspberry Pi aktivieren
- Per SSH (Secure Shell) Server können Sie die Kommandozeile des Raspberry Pi remote auf einem anderen Gerät verwenden. Im späteren Betrieb und bei der Nutzung des Raspberry Pi müssen Sie keine Maus, Tastatur oder Monitor daran anschließen, sondern einfach an einem Computer im selben LAN steuern.
- Seit der Version vom November 2016 ist bei Raspbian der SSH-Server standardmäßig deaktiviert. Sie müssen es manuell aktivieren.
- Die Methode zum Aktivieren von SSH in dieser Dokumentation finden Sie auf der offiziellen Raspberry Pi-Website [SSH(Secure Shell)](https://www.raspberrypi.org/documentation/remote-access/ssh/)

#### 2.2.1 Methode A: SSH mit Peripheriegeräten aktivieren
- Wenn Sie eine Maus, Tastatur oder einen Monitor an den Raspberry Pi angeschlossen haben, führen Sie diese Schritte aus, um SSH zu aktivieren.

    1. Entfernen Sie die SD-Karte aus dem Computer, stecken Sie sie in den Raspberry Pi ein, schließen Sie eine Maus, Tastatur und einen Monitor an den Raspberry Pi an, booten Sie ihn.
    2. Gehen Sie zum Menü "Einstellungen" und wählen Sie "Raspberry Pi-Konfiguration".
    3. Gehen Sie zur Option `Schnittstellen`.
    4. Wählen Sie `Aktivieren` neben `SSH`.
    5. Klicken Sie auf `OK`.
    
    ![configSSH](images/configSSH.png)

#### 2.2.2 Methode A: SSH ohne Peripheriegeräte aktivieren
- Wenn Sie keinen Monitor an den Raspberry Pi angeschlossen haben, führen Sie diese Schritte aus, um SSH zu aktivieren.

    1. Entfernen Sie die SD-Karte nicht, nachdem `Raspberry Pi Imager` die Image-Datei geschrieben hat.

    2. Erstellen Sie eine Datei namens `ssh` in einem beliebigen Verzeichnis ohne Erweiterungsnamen. Sie können eine `ssh.txt` erstellen und die `.txt` löschen.

    3. Kopieren Sie die `ssh`-Datei und fügen Sie sie in das Stammverzeichnis der SD-Karte ein. Der Raspberry Pi sucht beim Booten automatisch nach der `ssh`-Datei und aktiviert SSH, wenn die Datei gefunden wird. Sie müssen nur einmal kopieren, da der Raspberry Pi dann bei jedem Booten automatisch SSH aktiviert.

    4. Entfernen Sie die SD-Karte nicht, wenn Sie WLAN konfigurieren müssen.

### 2.3 WLAN auf Raspberry Pi konfigurieren
Es gibt viele Möglichkeiten, WLAN für Raspberry Pi zu verbinden. In dieser Dokumentation werden zwei Methoden bereitgestellt; Weitere Informationen finden Sie auf der offiziellen Raspberry Pi-Website: [Wireless-Konnektivität](https://www.raspberrypi.org/documentation/configuration/wireless/README.md).
#### 2.3.1 Methode A: WiFi-Verbindung mit Peripheriegeräten
- Wenn Sie eine Maus, Tastatur oder einen Monitor an den Raspberry Pi angeschlossen haben, führen Sie diese Schritte aus, um WLAN zu konfigurieren.

    1. Entfernen Sie die SD-Karte aus dem Computer, stecken Sie sie in den Raspberry Pi ein, schließen Sie eine Maus, Tastatur und einen Monitor an den Raspberry Pi an, booten Sie ihn.
    2. Wählen Sie das WiFi-Symbol in der oberen rechten Ecke des Monitors aus, suchen Sie das zu verbindende WiFi und wählen Sie es aus.
    3. Geben Sie das Passwort für das WLAN ein, verbinden Sie sich.
    4. Nach erfolgreicher Verbindung wird das WLAN gespeichert und der Raspberry Pi verbindet sich automatisch für den nächsten Start, sodass Sie nicht jedes Mal Peripheriegeräte anschließen müssen.

#### 2.3.2 Methode A: WLAN-Verbindung ohne Peripheriegeräte
- Wenn Sie keinen Monitor mit dem Raspberry Pi verbunden haben, gehen Sie wie folgt vor, um WLAN zu konfigurieren.
- Diese Methode basiert auf der [offiziellen Dokumentation](https://www.raspberrypi.org/documentation/configuration/wireless/headless.md)

    1. Entfernen Sie die SD-Karte nicht, nachdem `Raspberry Pi Imager` die Bilddatei geschrieben hat. (Diese Methode funktioniert für den Fall, dass die Raspbian-Image-Datei gerade auf die SD-Karte geschrieben wurde; wenn Sie die SD-Karte bereits in den Raspberry Pi gesteckt und nach dem Schreiben der Image-Datei neu gestartet haben, kann die Konfiguration fehlschlagen. )

    2. Erstellen Sie irgendwo auf Ihrem Computer eine Datei namens `wpa_supplicant.conf`.
    
    3. Öffnen Sie die mit Textbook erstellte Datei `wpa_supplicant.conf` und geben Sie den folgenden Code ein:

    ```
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    country=Insert country code here
    network={
     ssid="Name of your WiFi"
     psk="Password for your WiFi"
    ```

    4. Geben Sie Ihre eigenen Informationen für `Ländercode hier einfügen`, `Name Ihres WLANs` und `Passwort für Ihr WLAN` ein. Achten Sie auf die Groß-/Kleinschreibung. Siehe folgendes Beispiel:

    ```
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    country=USA
    network={
     ssid="MeinName"
     psk="12345678"
    }
    ```

    5. Speichern und beenden. Kopieren Sie die `wpa_supplicant.conf` in das Stammverzeichnis der SD-Karte.

    6. Wenn Sie die Datei `ssh` bereits wie in **2.2** beschrieben auf die SD-Karte kopiert haben, sind sowohl die WLAN- als auch die SSH-Einstellungen ohne Peripheriegeräte durchgeführt. Sie können die SD-Karte entfernen, in den Raspberry Pi einlegen und hochfahren.
    
    7. Weitere Informationen zur Datei `wpa_supplicant.conf` finden Sie in der offiziellen Dokumentation [WIRELESS-CLI](https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md)

## 3. Softwareinstallation & Betrieb auf Raspberry Pi
- Wenn Sie die Schritte in **2.2.1** und **2.3.1** für die SSH- und WiFi-Konfiguration befolgt haben, können Sie jetzt die Peripheriegeräte entfernen und später SSH verwenden, um den Raspberry Pi fernzusteuern.

- Wenn Sie die Schritte in **2.2.2** und **2.3.2** befolgt haben, können Sie nun die SD-Karte in den Raspberry Pi einlegen und diesen hochfahren. Der Raspberry Pi bootet automatisch und verbindet sich beim Einschalten mit WLAN, ohne dass Peripheriegeräte erforderlich sind.

- Einige der unten aufgeführten Schritte basieren auf der offiziellen Raspberry-Pi-Dokumentation [SSH](https://www.raspberrypi.org/documentation/remote-access/ssh/).

- Informationen zur Stromversorgung des Raspberry Pi finden Sie in der offiziellen Dokumentation [Stromversorgung](https://www.raspberrypi.org/documentation/hardware/raspberrypi/power/README.md).

- Das Robot HAT Board des Adeept Raspberry Pi Robot kann den Raspberry Pi über den GPIO-Port mit Strom versorgen. Da die Installation der Software auf dem Raspberry Pi jedoch längere Zeit in Anspruch nehmen kann, wird davon abgeraten, die Batterien während dieses Vorgangs mitzuliefern. Sie können die Installation des Robot HAT-Boards oder der Kamera während der Softwareinstallation überspringen; Sie müssen jedoch sicherstellen, dass die Treiberplatine und die Kamera für den Raspberry Pi bereit sind, um die installierte Software auszuführen, da sonst ein Programmfehler auftritt.

### 3.1 Bei Raspberry Pi anmelden (Windows 10)
- Für Windows 10 ist SSH in den Versionen nach Oktober 2018 eingebaut, Sie benötigen also keine Software von Drittanbietern.

- Bei niedrigeren Versionen des Windows-Betriebssystems ist SSH nicht integriert, und Sie können sich in der offiziellen Dokumentation [SSH using Windows](https://www.raspberrypi.org/documentation/remote-access/) beim Raspberry Pi anmelden. ssh/windows.md).

- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen. Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.

- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse](https://www.raspberrypi.org/documentation/remote-access/ip-address.md)

- Drücken Sie die Tasten <kbd>win</kbd>+<kbd>R</kbd>, geben Sie `cmd` ein und drücken Sie <kbd>Enter</kbd>.

- Der Standardnutzer ist "pi" und das Passwort ist "raspberry".

- Geben Sie `ssh pi@<IP>` in die Befehlszeile ein, ersetzen Sie das `<IP>` durch die IP-Adresse Ihres Raspberry Pi, wie unten gezeigt:

    >ssh pi@192.168.3.161

- Drücken Sie die Eingabetaste und es erscheint eine Eingabeaufforderung: `Sind Sie sicher, dass Sie die Verbindung fortsetzen möchten (ja/nein)?`

- Geben Sie `yes` ein, drücken Sie die Eingabetaste und es wird `pi@192.168.3.161's password:` angezeigt, geben Sie das anfängliche Passwort des Raspberry Pi ein, `raspberry` (achten Sie auf die Groß-/Kleinschreibung). Während der Eingabe ändert sich der Bildschirm nicht, aber das bedeutet nicht, dass Sie die Informationen nicht eingeben. Drücken Sie die <kbd>Eingabetaste</kbd>, nachdem Sie mit der Eingabe fertig sind.

- Jetzt haben Sie sich also beim Raspberry Pi angemeldet.

![winSSH](images/winSSH.png)

### 3.2 Bei Raspberry Pi anmelden (Linux oder Mac OS)

- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen. Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.

- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse](https://www.raspberrypi.org/documentation/remote-access/ip-address.md)

- Öffnen Sie das Terminalfenster (oder die Befehlszeile)

- Der Standardnutzer ist "pi" und das Passwort ist "raspberry".

- Geben Sie `ssh pi@<IP>` in die Befehlszeile ein, ersetzen Sie `<IP>` durch die IP-Adresse Ihres Raspberry Pi wie unten gezeigt:

    >ssh pi@192.168.3.161

- Drücken Sie die Eingabetaste und eine Eingabeaufforderung wird angezeigt: `Sind Sie sicher, dass Sie die Verbindung fortsetzen möchten (ja/nein)?`

- Geben Sie `yes` ein, drücken Sie die Eingabetaste und es wird `pi@192.168.3.161's password:` angezeigt, geben Sie das anfängliche Passwort des Raspberry Pi ein, `raspberry` (achten Sie auf die Groß-/Kleinschreibung). Während der Eingabe ändert sich der Bildschirm nicht, aber das bedeutet nicht, dass Sie die Informationen nicht eingeben. Drücken Sie die <kbd>Eingabetaste</kbd>, nachdem Sie mit der Eingabe fertig sind.

- Jetzt haben Sie sich also beim Raspberry Pi angemeldet.

### 3.3 Bei Raspberry Pi anmelden (Windows)
- Für niedrigere Versionen des Windows-Betriebssystems ist SSH nicht integriert, und Sie können sich beim Raspberry Pi anmelden, indem Sie sich auf die offizielle Dokumentation Raspberry Pi [SSH using Windows] (https://www.raspberrypi.org/documentation/remote-access/ssh/windows.md).
- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen. Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.
- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse](https://www.raspberrypi.org/documentation/remote-access/ip-address.md)
- Möglicherweise müssen Sie die `PuTTY`-Version für Ihr Betriebssystem herunterladen und sich mit dem Tool bei Raspberry Pi anmelden. [Klicken Sie hier, um PuTTY herunterzuladen](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
- Führen Sie `PuTTY` aus, geben Sie die IP-Adresse des Raspberry Pi als `Host Name` ein und klicken Sie auf <kbd>Öffnen</kbd>.
- Wenn die Meldung `Network error: Connection timed out` erscheint, haben Sie möglicherweise eine falsche IP-Adresse eingegeben.
- Wenn die Verbindung funktioniert, sehen Sie die unten angezeigte Sicherheitswarnung. Sie können es getrost ignorieren und auf die Schaltfläche "Ja" klicken. Sie sehen diese Warnung nur, wenn sich PuTTY zum ersten Mal mit einem Raspberry Pi verbindet, den es noch nie zuvor gesehen hat.
- Sie sehen nun die übliche Anmeldeaufforderung. Melden Sie sich mit demselben Benutzernamen und Passwort an, das Sie auf dem Pi selbst verwenden würden. Der Standard-Login für Raspbian ist `pi` mit dem Passwort `raspberry`.
- Sie sollten jetzt die Raspberry Pi-Eingabeaufforderung haben, die mit der auf dem Raspberry Pi selbst identisch ist.

![Putty](images/putty.png)

### 3.4 Download-Programm des Raspberry Pi-Roboters

- Der Code für das Roboterprodukt wurde auf [GitHub] hochgeladen. Möglicherweise müssen Sie ihn auf Ihren Raspberry Pi herunterladen und die entsprechenden abhängigen Bibliotheken installieren, um das Programm auszuführen.

- Im vorherigen Abschnitt haben Sie sich beim Raspberry Pi angemeldet und geben hier den folgenden Befehl im Terminalfenster ein:

    >sudo git-klon https://github.com/adeept/adeept_rasptank.git

- Drücken Sie <kbd>Enter</kbd>, um das Programm des Roboters von GitHub herunterzuladen. Es kann einige Zeit dauern, bitte warten Sie, bis es fertig ist.

### 3.5 Entsprechende abhängige Bibliotheken installieren
- Befolgen Sie die nachstehenden Schritte, um die Bibliotheken zu installieren, wenn Sie die Bilddatei basierend auf **2.1.1 Schreiben Sie 'Raspbian' mit `Raspberry Pi Imager`** auf die SD-Karte geschrieben und **2.1.2 Laden Sie die Image-Datei `Raspbian` und schreibe sie manuell auf die SD-Karte**.

- Sie sollten jedoch **diesen Abschnitt überspringen**, wenn Sie die Bilddatei auf Grundlage von **2.1.3 auf die SD-Karte geschrieben haben. Laden Sie die von uns bereitgestellte Bilddatei manuell herunter und schreiben Sie sie auf die SD-Karte**; siehe **2.4.5** für die Konfiguration des Autostart-Programms.

- Hier wird ein Skript bereitgestellt, um alle benötigten abhängigen Bibliotheken zu installieren und den Start der Kamera und anderer Autostart-Programme zu konfigurieren.

- Geben Sie den folgenden Code in das Terminalfenster ein, um die abhängigen Bibliotheken für das Skript `setup.py` auszuführen:

    > sudo python3 adeept_rasptank/setup.py

- Drücken Sie <kbd>Enter</kbd> und das Skript wird automatisch ausgeführt. Dies kann je nach Netzwerkstatus Minuten oder Stunden dauern. Bitte warten Sie, bis es fertig ist.

- Nach Abschluss der Installation werden die folgenden Eingabeaufforderungen angezeigt:

    >Das Programm im Raspberry Pi wurde installiert, getrennt und neu gestartet.
    >Sie können jetzt den Raspberry Pi ausschalten, um die Kamera und die Treiberplatine (Robot HAT) zu installieren. Nach dem erneuten Einschalten führt der Raspberry Pi automatisch das Programm aus, um das Servo-Port-Signal zu setzen, um die Servos in die mittlere Position zu drehen, was für die mechanische Montage praktisch ist.

- Wenn die Installation abgeschlossen ist, trennt der Raspberry Pi automatisch SSH und startet neu. Wenn Sie puTTy verwendet haben, um den Raspberry Pi zu verbinden, kann es zu einer Fehlermeldung wie `Netzwerkfehler: Software verursachte Verbindungsabbruch` kommen. Sie können es einfach ignorieren und schließen.

### 3.6 Führen Sie das Programm des Raspberry Pi-Roboters aus

- Raspberry Pi führt bei jedem Neustart automatisch das Programm für den Roboter aus. Dies ist der Teil `[RobotName]/server/webServer.py` (ersetzen Sie `[RobotName]` durch den Namen des Ordners für das Programm Ihres Roboterprodukts). Wenn die Raspberry Pi-Kamera oder RobotHAT jedoch nicht angeschlossen ist, kann der `webServer.py` nicht richtig laufen. Dies ist sinnvoll, da das Programm des Roboters die Kamera und den Chipsatz PCA9685 benötigt. RobotHAT steuert Servo mit PCA9685; der Raspberry Pi kommuniziert mit PCA9685 über I2C; Wenn Robot HAT also nicht mit Raspberry Pi verbunden ist, tritt bei der Instanziierung abhängiger Bibliotheken für PCA9685 aufgrund eines Kommunikationsfehlers ein Programmfehler auf.

- Raspberry Pi ausschalten, Kameramodul und RobotHAT verbinden, neu starten und nun kann `webServer.py` laufen.

- Im Allgemeinen müssen Sie `webServer.py` nicht manuell ausführen, da es bei jedem Start automatisch von Raspberry Pi ausgeführt wird.

- Öffnen Sie einen Webbrowser (zum Beispiel Google Chrome), geben Sie in der Adressleiste die IP-Adresse des Raspberry Pi ein, fügen Sie wie unten gezeigt `:5000` am Ende hinzu und drücken Sie <kbd>Enter</kbd>, um umzuleiten zur Webseite des Raspberry Pi:

    >http://192.168.3.161:5000/

- Wenn die Seite nicht aufgerufen werden kann, melden Sie sich über SSH am Raspberry Pi an, geben Sie den folgenden Befehl ein, um die automatische Ausführung des Programms beim Booten zu beenden, um Ressourcen freizugeben, oder Probleme wie ein Fehler bei der Kamerainitialisierung oder belegte Ports.

    > sudo killall python3

- Geben Sie den folgenden Befehl ein, um `webServer.py` auszuführen:

    > sudo python3 adeept_rasptank/server/webServer.py

- Überprüfen Sie, ob ein Fehler vorliegt, und beheben Sie ihn gemäß den Anweisungen im Abschnitt Fragen und Antworten unten.

## 4. Vorsichtsmaßnahmen für die Strukturmontage
#### 4.1 Dokumentation zur Strukturmontage
- [Dokumentation zur Strukturmontage](https://www.adeept.com/learn)

#### 4.2 Vorsichtsmaßnahmen für die Strukturmontage
- Da im Produkt viele Servos verwendet werden, ist die Servoinstallation für den Roboter kritisch. Bevor Sie den Kipphebel am Servo anbringen, müssen Sie das Servo an die Stromversorgung anschließen und die Servowelle in die Mittelposition drehen, damit sich der Kipphebel, der im angegebenen Grad installiert ist, in der Mittelposition befindet.

- Im Allgemeinen führt Raspberry Pi beim Booten automatisch `webServer.py` aus, wenn `webServer.py` alle mit Servos verbundenen Ports steuert, um ein Signal zum Drehen in die Mittelposition zu senden. Beim Zusammenbau des Servos können Sie es jederzeit an einen beliebigen Servoanschluss anschließen. Nach dem Anschließen des Servos an den Port drehen sich die Zahnräder in die Mittelposition; Montieren Sie den Kipphebel am Servo, trennen Sie das Servo vom Anschluss und setzen Sie weitere Servos ein, um die Kipphebelmontage zu wiederholen (alle Servos befinden sich in der Mittelposition).

- Wenn das Servo an die Stromversorgung angeschlossen ist, versuchen Sie, den Kipphebel zu bewegen. Wenn es nicht bewegt werden kann, zeigt es das Programm für die Servos an; andernfalls gibt es einen Fehler für das Servoprogramm. Führen Sie die Zeile `[RobotName]/initPosServos.py` aus (ersetzen Sie `[RobotName]` durch den Ordnernamen Ihres Roboterprogramms), um das Servo in die Mittelposition zu drehen.

- Beim Booten (es kann 30-50s dauern) dauert es eine Weile, bis der Raspberry Pi PCA9685 steuert, um das Signal aller Servoports für die Mittelpositionsdrehung einzustellen.

## 5. Roboter über die WEB-App steuern

- Die WEB-App wurde für normale Benutzer entwickelt, um den Roboter einfacher zu steuern. Es ist bequem, die WEB-App zu verwenden; Sie können damit den Roboter auf jedem Gerät mit einem Webbrowser drahtlos steuern (zum Testen wurde Google Chrome verwendet).

- Im Allgemeinen führt Raspberry Pi beim Booten automatisch `webServer.py` aus und baut einen Webserver im LAN auf. Sie können dann jeden anderen Computer, Handy oder Tablet im selben LAN verwenden, um die Webseite zu besuchen und den Roboter zu steuern.

- So erkennen Sie, ob der Roboter `webServer.py` ausgeführt hat oder nicht: Wenn die WS2812-LED mit dem Atemeffekt aufleuchtet, bedeutet dies, dass der Roboter gestartet wurde und das Programm automatisch ausführt.

- Wenn das Programm beim Booten des Roboters nicht ausgeführt wird, versuchen Sie, den Raspberry Pi über SSH zu verbinden, führen Sie `webServer.py` manuell mit Code aus und überprüfen Sie die Fehler. Lesen Sie die **Q&A** unten oder senden Sie uns eine E-Mail, um Hilfe zu erhalten (bevor Sie `webServer.py` manuell ausführen, müssen Sie das Programm möglicherweise automatisch im Backend ausführen, um Ressourcen freizugeben.

    > sudo killall python3
    > sudo python3 [RobotName]/server/webServer.py

- Wenn die `webServer.py` erfolgreich automatisch ausgeführt wird, öffnen Sie einen Webbrowser (hier Google Chrome), geben Sie die IP-Adresse des Raspberry Pi ein, mit `:5000` am Ende, und gehen Sie zum nächsten Schritt, Wie nachfolgend dargestellt:

    > 192.168.3.161:5000

- Wenn kein Bild angezeigt wird, versuchen Sie, `webServer.py` manuell auszuführen, wie im obigen Schritt beschrieben.

- Wenn ein Bild angezeigt wird, können Sie den Roboter jetzt so steuern, dass er sich bewegt. Sie können die Beschreibung der Tastenkombinationen 'Anweisung' unten überprüfen und den Roboter anhand seiner allgemeinen Funktionen mit der Tastatur steuern.

- Das `Video`-Fenster zeigt das von der Roboterkamera aufgenommene Bild in Echtzeit.

- Das Fenster "Move Control" dient zur Steuerung der Grundbewegungen des Roboters.

- Das Fenster "Arm Control" steuert die Servobewegung.
    - <kbd>GRAB</kbd> <kbd>LOOSE</kbd>: Steuern Sie die Klauen des Roboterarms zum Öffnen und Schließen
    - <kbd>HANDUP</kbd> <kbd>HANDDOWN</kbd>: Steuern Sie den Roboterarm, um sich nach oben und unten zu bewegen
    - <kbd>LEFT</kbd> <kbd>RIGHT</kbd>: Steuern Sie die Klauendrehung des Roboterarms

- Das Fenster "CVFL-Steuerung" dient zur Steuerung der Sichtlinienverfolgungsfunktion des Roboters. Hier wird nur eine Übersicht zur Funktion beschrieben; Weitere Details finden Sie im Abschnitt OpenCV:
    - <kbd>START</kbd>: Aktiviert oder deaktiviert die visuelle Linienverfolgungsfunktion.
    - <kbd>COLOR</kbd>: Umschalten zwischen weißer und schwarzer Linienführung. Standardmäßig folgt der Roboter weißen Linien; Klicken Sie auf die Schaltfläche, um zur schwarzen Linie zu wechseln.
    - Die Zeilenfolgefunktion analysiert zwei Pixel parallel und verwendet die erkannten Informationen; die Positionen dieser beiden Pixel sind "L1" und "L2".
    - `SP` ist die Schwelle des Abbiegebefehls basierend auf den Ergebnissen der visuellen Analyse. Ein größerer "SP"-Wert bedeutet eine große Abweichung; obwohl ein besonders kleiner `SP`-Wert den Roboter an der Bewegung hindern kann, da er das Ziel nicht anvisieren und die Richtung finden kann.
    - Wenn die visuelle Linienverfolgungsfunktion aktiviert ist, wird der Videobildschirm automatisch zu binarisierten Ergebnissen, wodurch die visuelle Analyse klarer wird.

- Das Fenster "Hardware" zeigt die CPU-Temperatur, die CPU-Auslastung und die Speichernutzung des Raspberry Pi an.

- `Aktionen`-Fenster steuert einzigartige Funktionen des Roboters:
    - <kbd>MOTION GET</kbd>: Bewegungserkennungsfunktion basierend auf OpenCV. Wenn sich Objekte im Blickfeld der Kamera bewegen, umkreist das Programm das Teil im 'Video'-Fenster und das LED-Licht am Roboter zeigt die entsprechenden Änderungen an.
    - <kbd>AUTO MATIC</kbd>: Hindernisvermeidungsfunktion basierend auf Ultraschall. Wenn das Ultraschallmodul des Roboters ein Hindernis erkennt, biegt er automatisch nach links ab und macht einen Schritt zurück, bevor er sich dreht, wenn er sich zu nahe am Hindernis befindet.
    - <kbd>POLICE LIGHT</kbd>: WS2812-LED Lichtsteuerung basierend auf Multithreading. Dadurch blinkt das WS2812-LED-Licht am Roboter abwechselnd rot und blau.
    - <kbd>TRACK LINE</kbd>: Linienverfolgungsfunktion durch Verwendung des 3-Kanal-Infrarotmoduls. Standardmäßig verfolgt es schwarze Linien auf einer weißen Oberfläche (einem weißen Hintergrund, der Infrarot reflektiert, und 1 cm breite schwarze Linien, die kein Infrarot reflektieren). Die Leistung der Linienverfolgung variiert von Oberflächen- und Linienmaterialien sowie der Höhe des Roboterchassis; Möglicherweise benötigen Sie einen Kreuzschraubendreher, um das Potentiometer am Linienverfolgungsmodul einzustellen.

- Das Fenster "FC Control" steuert die Farbsperrfunktion des Roboters:
    - <kbd>START</kbd>: Aktivieren oder deaktivieren Sie die Farbsuch- und -verfolgungsfunktion.
    - <kbd>COLOR</kbd>: Wählen Sie die zu verfolgende Farbe.
    - Wenn die Funktion aktiviert ist, sperrt der Roboter automatisch eine bestimmte Farbe in der Kameraansicht. Standardmäßig verfolgt es leuchtend gelbe Objekte. Sie können die Farbe nach Belieben ändern. Wenn ein Objekt gesperrt ist, leuchtet die LED am Roboter orange. Da sich der Kopf des Roboters nur auf und ab bewegen kann, beinhaltet das Programm keine horizontale Farbverfolgung. Wenn Sie Interesse an diesem Teil haben, können Sie die Motorsteuerung basierend auf dem openCV-Abschnitt hinzufügen, um die Wirkung zu erzielen.

![webControl](images/webControl.png)

## 6. Fragen und Antworten

- Wo finde ich die IP-Adresse des Raspberry Pi?

    > - Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen. Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.

    > Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse](https://www.raspberrypi.org/documentation/remote-access/ip-address.md)

- Fehler treten mit der Eingabeaufforderung "Berechtigung verweigert" auf, wenn ich "server.py" oder "webServer.py" manuell ausführe.

    > Der Raspberry Pi benötigt die Root-Berechtigung, um die abhängigen Bibliotheken für die WS2812 LED-Lichtsteuerung auszuführen.
    > Sie müssen `sudo` am Anfang von `server.py` oder `webServer.py` hinzufügen, um das Programm auszuführen.
    > sudo python3 [PFAD]/server.py
    > sudo python3 [PFAD]/webServer.py

- Ich kann den Hotspot für den Roboter nicht erstellen.

    > Sie müssen das Open-Source-Projekt create_ap verwenden, um den Hotspot des Roboters einzurichten. Trennen Sie vor der Verwendung das WLAN-Netzwerk, aber schalten Sie das WLAN-Modul NICHT aus, sonst zeigt create_ap einen Fehler an, dass die Hardware blockiert ist.

- Der Servo dreht sich ungewöhnlich stark.

    > Vor dem Zusammenbau von Kipphebel und Servo müssen Sie die Servozahnräder in die mittlere Position ihres Drehbereichs drehen lassen. Montieren Sie dann den Kipphebel gemäß dem in der Dokumentation angegebenen Winkel. Aufgrund des Aufbaus des Servos (Zähnezahl 20 bei den Servozahnrädern) kann es zu einer Abweichung von weniger als 9° kommen. Für eine bessere Leistung können Sie die Servosteuerungsdokumentation für die anfängliche Gradeinstellung nach Code lesen.

- Das Servo wackelt.

    > Wahrscheinlich ist das Servo-Untersetzungsgetriebe defekt.

- Raspberry Pi kann nicht booten.

    > Entfernen Sie alle Teile auf der Treiberplatine. Nur das Board an Raspberry Pi und Stromversorgung anschließen, neu starten.

- "Remote-Seite unerwartet geschlossene Netzwerkverbindung" wird in einem Popup-Fenster angezeigt.

    > Während der Installation kann es zu Fehlermeldungen kommen, da der Raspberry Pi nach der Installation automatisch neu gestartet wird, wodurch das Board getrennt wird.

- Programm stürzt nach Doppelklick auf client.py oder GUI.py ab.

    > Führen Sie das Skript mit `python client.py` oder `python GUI.py` in cmd aus und überprüfen Sie die Fehlerberichte.

- Wie initialisiere ich den Winkel des Servos?

    > Wenn Sie die Softwareinstallation auf dem Raspberry Pi abgeschlossen haben, booten Sie ihn einfach und das Servo wird initialisiert.

- Ich kann über SSH eine Verbindung zum Raspberry Pi-Terminal herstellen \ Raspberry Pi konnte keine WLAN-Verbindung herstellen.

    > Die Stromversorgungsmethoden haben keinen Einfluss auf die Steuerung durch SSH. Prüfen Sie, ob Sie die Datei `wpa_supplicant.conf` mehrmals erstellt haben. Wenn ja, verursacht dieses Problem SSH-Fehler.

- Kann ich Robot HAT und Raspberry Pi über USB versorgen?

    > Ein 2A-Ausgang wird für einen Raspberry Pi 3B benötigt, wenn mindestens 3A für einen Raspberry Pi 4 benötigt werden. Sie können die USB-Stromversorgung für Softwareinstallation und Test verwenden, aber sie ist nicht geeignet für Hochleistungsmodule wie Servo- oder Motoranpassungen wie dies kann zu einer niedrigen Spannung führen. Es wird empfohlen, hier eine Batterie zur Stromversorgung zu verwenden.

- Nach der Installation zeigt der Roboter beim Booten keine Reaktion.

    > Die Datei `server.py` oder `webServer.py` kann aus bestimmten Gründen nicht ausgeführt werden. Versuchen Sie, `server.py` oder `webServer.py` manuell auszuführen und prüfen Sie, ob eine Fehlermeldung angezeigt wird.

- Das Servo kehrt beim Anschluss an die Treiberplatine nicht in die Mittelstellung zurück.

    > Im Allgemeinen führt der Raspberry Pi beim Booten automatisch `webServer.py` aus und `webServer.py` wird laufen und die Servo-Ports steuern, um ein Signal zum Drehen in die Mittelposition zu senden. Beim Zusammenbau des Servos können Sie es jederzeit an einen beliebigen Servoanschluss anschließen. Nach dem Anschließen des Servos an den Port drehen sich die Zahnräder in die Mittelposition; Montieren Sie den Kipphebel am Servo, trennen Sie das Servo vom Anschluss und setzen Sie weitere Servos ein, um die Kipphebelmontage zu wiederholen (alle Servos befinden sich in der Mittelposition).

    > Wenn das Servo eingeschaltet ist, versuchen Sie, den Kipphebel zu bewegen. Wenn es nicht bewegt werden kann, zeigt es das Programm für die Servos an; andernfalls gibt es einen Fehler für das Servoprogramm. Führen Sie die Zeile `[RobotName]/initPosServos.py` aus (ersetzen Sie `[RobotName]` durch den Ordnernamen Ihres Roboterprogramms), um das Servo in die Mittelposition zu drehen.

    > Beim Booten (es kann 30-50s dauern) dauert es eine Weile, bis der Raspberry Pi PCA9685 steuert, um das Signal aller Servoports für die Mittelpositionsdrehung zu setzen.

- Der Fehler "no cv2" tritt auf, wenn ich `server.py` oder `webServer.py` manuell ausführe.

    > OpenCV ist nicht richtig installiert. Geben Sie den Befehl sudo pip3 install opencv-contrib-python in den Raspberry Pi ein, um OpenCV manuell zu installieren.