[Robotername]: Adeept_Rasptank
[RobotURL]: https://github.com/adeept/adeept_rasptank
[RobotGit]: https://github.com/adeept/adeept_rasptank.git
[Offizielle Raspberry Pi-Website]: https://www.raspberrypi.org/downloads/
[Image-Datei für den Raspberry Pi Robot]: https://adeept-my.sharepoint.com/personal/tomsun_adeept_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ftomsun%5Fadeept%5Fonmicrosoft%5Fcom%2FDocuments%2FadeeptRaspTank&amp ; originalPath = aHR0cHM6Ly9hZGVlcHQtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvdG9tc3VuX2FkZWVwdF9vbm1pY3Jvc29mdF9jb20vRXZCZmhES1dJVEJLb1ZLejFJTThta01CaWc5SHRiZG9sMXdLQU83WTk5cFJWdz9ydGltZT1rUWxJeE9EMjEwZw
[Offizielle Website]: https://www.adeept.com/
[GitHub]: https://github.com/adeept/adeept_rasptank/
[Dokumentation zur Strukturmontage]: https://www.adeept.com/learn/
Erste Schritte mit Raspberry Pi Robot und Python
----
* [Erste Schritte mit Raspberry Pi Robot und Python](#getting-started-with-raspberry-pi-robot-and-python)
    * [1. Prämisse](#1-Prämisse)
       * [1.1 STEAM und Raspberry Pi] (#11-steam-and-raspberry-pi)
       * [1.2 Über die Dokumentation](#12-über-die-dokumentation)
    * [2. Erste Schritte mit dem Raspberry Pi](#2-Getting-to-use-the-raspberry-pi)
       * [2.1 Das Raspberry Pi-Image auf eine SD-Karte schreiben](#21-write-the-raspberry-pi-image-to-an-sd-card)
          * [2.1.1 Methode A: 'Raspbian' mit Raspberry Pi Imager auf die SD-Karte schreiben](#211-method-a-write-raspbian-to-the-sd-card-by-raspberry-pi-imager)
          * [2.1.2 Methode B: Laden Sie die Image-Datei Raspbian herunter und schreiben Sie sie manuell auf die SD-Karte](#212-method-b-download-the-image-file-raspbian-and-write-it-to-the- SD-Karte-manuell)
          * [2.1.3 Methode C: Laden Sie die von uns bereitgestellte Bilddatei manuell herunter und schreiben Sie sie auf die SD-Karte (nicht empfohlen)](#213-method-c-manually-download-the-image-file-provided-by- uns-und-schreiben-es-auf-die-sd-karte-nicht-empfohlen)
       * [2.2 SSH-Server von Raspberry Pi aktivieren](#22-enable-ssh-server-of-raspberry-pi)
          * [2.2.1 Methode A: SSH mit Peripheriegeräten aktivieren](#221-method-a-enable-ssh-with-peripherals)
          * [2.2.2 Methode A: SSH ohne Peripheriegeräte aktivieren](#222-method-a-enable-ssh-ohne-peripheriegeräte)
       * [2.3 WLAN auf Raspberry Pi konfigurieren] (#23-configure-wifi-on-raspberry-pi)
          * [2.3.1 Methode A: WiFi-Verbindung mit Peripheriegeräten](#231-Methode-eine-WLAN-Verbindung-mit-Peripheriegeräten)
          * [2.3.2 Methode A: WiFi-Verbindung ohne Peripheriegeräte](#232-Methode-eine-WLAN-Verbindung-ohne-Peripheriegeräte)
    * [3. Softwareinstallation &amp; Betrieb auf Raspberry Pi](#3-software-installation--operation-on-raspberry-pi)
       * [3.1 Bei Raspberry Pi anmelden (Windows 10)](#31-log-in-raspberry-pi-windows-10)
       * [3.2 Anmelden bei Raspberry Pi (Linux oder Mac OS)](#32-log-in-raspberry-pi-linux-or-mac-os)
       * [3.3 Einloggen in Raspberry Pi (Windows)](#33-log-in-raspberry-pi-windows)
       * [3.4 Download-Programm des Raspberry Pi-Roboters](#34-download-program-of-the-raspberry-pi-robot)
       * [3.5 Entsprechende abhängige Bibliotheken installieren](#35-installieren-entsprechende-abhängige-Bibliotheken)
       * [3.6 Führen Sie das Programm des Raspberry Pi Robots aus] (#36-run-the-raspberry-pi-robots-program)
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



## 2. Wie Sie den Raspberry Pi verwenden

### 2.1 Das Raspberry Pi-Image auf eine SD-Karte schreiben


#### 2.1.1 Methode A: 'Raspbian' mit 'Raspberry Pi Imager' auf die SD-Karte schreiben
"Raspberry Pi Imager" ist ein von der Raspberry Pi Organization entwickeltes Tool zum Schreiben von Bildern auf eine SD-Karte. Es wird mit vielen Versionen geliefert, die auf verschiedenen Systemen funktionieren, und es ist ziemlich einfach zu bedienen; Sie müssen lediglich das Betriebssystem und die SD-Karte auswählen, Raspberry Pi Imager lädt die entsprechende Image-Datei für das System herunter und installiert sie auf der SD-Karte.

**Schritt-für-Schritt-Übersicht**

1. Bereiten Sie eine SD-Karte (16 GB oder größer) und einen SD-Kartenleser vor
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen)
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen")
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen")
3. Installieren Sie den `Raspberry Pi Imager`
4. Schreiben Sie das Betriebssystem für Raspberry Pi auf die SD-Karte mit `Raspberry Pi Imager` `Raspbian Full - Eine Portierung von Debian mit Desktop und empfohlener Anwendung`
5. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/), suchen Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem und laden Sie ihn herunter. oder klicken Sie auf die obigen Links für das entsprechende System, um es direkt herunterzuladen und zu installieren.

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
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen)
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen")
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen")
3. Installieren Sie den `Raspberry Pi Imager`
4. Laden Sie die Bilddatei `Raspbian` . herunter
    - Torrent-Datei:
    [Raspbian - Raspbian Buster mit Desktop und empfohlener Software](https://downloads.raspberrypi.org/raspbian_full_latest.torrent "Link zum Download der Torrent-Datei für Bild")
    - Zip-Datei: [Raspbian - Raspbian Buster mit Desktop und empfohlener Software](https://downloads.raspberrypi.org/raspbian_full_latest "Link zum Download der Zip-Datei für das Bild")
5. Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
6. Schreiben Sie die auf die SD-Karte heruntergeladene Bilddatei `Raspbian` mit `Raspberry Pi Imager`
7. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website], suchen und laden Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem herunter oder klicken Sie auf die obigen Links, um das entsprechende System direkt herunterzuladen und Installieren.

  ![imagerDownload](images/imagerDownload.png)

- Wählen Sie auf der Raspberry Pi-Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/ ) über `Downloads` -> `Raspbian` -> `Raspbian Buster mit Desktop und empfohlener Software` und Klicken Sie zum Herunterladen auf die Torrent- oder ZIP-Datei. Entpacken Sie die Datei nach dem Download, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt; andernfalls öffnet `Raspberry Pi Imager` die `.img`-Datei möglicherweise nicht. Es wird empfohlen, die Datei `.img` im Stammverzeichnis der Festplatte `C:\` oder `D:\` zu speichern, **aber `.img` nicht auf der SD-Karte zu speichern**.

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
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen")
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen")
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen")
3. Installieren Sie den `Raspberry Pi Imager`
4. Laden Sie die Bilddatei `Raspbian` . herunter
    - [Image-Datei für den Raspberry Pi-Roboter](https://adeept-my.sharepoint.com/personal/tomsun_adeept_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ftomsun%5Fadeept%5Fonmicrosoft%5Fcom%2FDocuments% 2FadeeptRaspTank & originalPath = aHR0cHM6Ly9hZGVlcHQtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvdG9tc3VuX2FkZWVwdF9vbm1pY3Jvc29mdF9jb20vRXZCZmhES1dJVEJLb1ZLejFJTThta01CaWc5SHRiZG9sMXdLQU83WTk5cFJWdz9ydGltZT1rUWxJeE9EMjEwZw)
5. Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
6. Schreiben Sie die auf die SD-Karte heruntergeladene Bilddatei `Raspbian` mit `Raspberry Pi Imager`
7. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/), suchen Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem und laden Sie ihn herunter. oder klicken Sie auf die obigen Links für das entsprechende System, um es direkt herunterzuladen und zu installieren.

  ![imagerDownload](images/imagerDownload.png)

- Gehen Sie zu unserer [offiziellen Website](https://www.adeept.com/ ), suchen Sie die Image-Datei und laden Sie sie herunter - [Image-Datei für den Raspberry Pi-Roboter](https://adeept-my.sharepoint.com/ persönlich / tomsun_adeept_onmicrosoft_com / _layouts / 15 / onedrive.aspx? id =% 2Fpersonal% 2Ftomsun% 5Fadeept% 5Fonmicrosoft% 5Fcom% 2FDocuments% 2FadeeptRaspTank & originalPath = aHR0cHM6Ly9hZGVlcHQtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvdG9tc3VuX2FkZWVwdF9vbm1pY3Jvc29mdF9jb20vRXZCZmhES1dJVEJLb1ZLejFJTThta01CaWc5SHRiZG9sMXdLQU83WTk5cFJWdz9ydGltZT1rUWxJeE9EMjEwZw). Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt. andernfalls öffnet `Raspberry Pi Imager` die `.img`-Datei möglicherweise nicht. Es wird empfohlen, die Datei `.img` im Stammverzeichnis der Festplatte `C:\` oder `D:\` zu speichern, **aber `.img` nicht auf der SD-Karte zu speichern**.

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
    country=Geben Sie hier den Ländercode ein
    Netzwerk={
     ssid="Name Ihres WLANs"
     psk="Passwort für Ihr WLAN"
    }
    ```

    4. Geben Sie Ihre eigenen Informationen für `Ländercode hier einfügen`, `Name Ihres WLANs` und `Passwort für Ihr WLAN` ein. Achten Sie auf die Groß-/Kleinschreibung. Siehe folgendes Beispiel:

    ```
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    Land=USA
    Netzwerk={
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

- Bei niedrigeren Versionen des Windows-Betriebssystems ist SSH nicht integriert, und Sie können sich in der offiziellen Dokumentation [SSH using Windows] (https://www.raspberrypi.org/documentation/remote-access/) beim Raspberry Pi anmelden. ssh/windows.md).

- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen. Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.

- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse] (https://www.raspberrypi.org/documentation/remote-access/ip-address.md)

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

- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse] (https://www.raspberrypi.org/documentation/remote-access/ip-address.md)

- Öffnen Sie das Terminalfenster (oder die Befehlszeile)

- Der Standardnutzer ist "pi" und das Passwort ist "raspberry".

- Geben Sie `ssh pi@<IP>` in die Befehlszeile ein, ersetzen Sie `<IP>` durch die IP-Adresse Ihres Raspberry Pi wie unten gezeigt:

    >ssh pi@192.168.3.161

- Drücken Sie die Eingabetaste und eine Eingabeaufforderung wird angezeigt: `Sind Sie sicher, dass Sie die Verbindung fortsetzen möchten (ja/nein)?`

- Geben Sie `yes` ein, drücken Sie die Eingabetaste und es wird `pi@192.168.3.161's password:` angezeigt, geben Sie das anfängliche Passwort des Raspberry Pi ein, `raspberry` (achten Sie auf die Groß-/Kleinschreibung). Während der Eingabe ändert sich der Bildschirm nicht, aber das bedeutet nicht, dass Sie die Informationen nicht eingeben. Drücken Sie die <kbd>Eingabetaste</kbd>, nachdem Sie mit der Eingabe fertig sind.

- Jetzt haben Sie sich also beim Raspberry Pi angemeldet.

### 3.3 Bei Raspberry Pi anmelden (Windows)
- Für niedrigere Versionen des Windows-Betriebssystems ist SSH nicht integriert, und Sie können sich beim Raspberry Pi anmelden, indem Sie sich auf die offizielle Dokumentation Raspberry Pi [SSH using Windows] (https://www.raspberrypi.org/documentation/remote- access/ssh/windows.md).
- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen. Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.
- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse] (https://www.raspberrypi.org/documentation/remote-access/ip-address.md)
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

- If the program is not run when the robot is booted, try to connect Raspberry Pi via SSH, manually run `webServer.py` with code and check the errors. Refer to the **Q&A** below or email us for help (before manually running `webServer.py`, you need to end the program possibly auto run in the backend to release resources. 

    > sudo killall python3  
    > sudo python3 [RobotName]/server/webServer.py

- If the `webServer.py` is auto run successfully, open a web browser (here Google Chrome), type in the IP address of the Raspberry Pi, with `:5000` added to the end, and go to the next step, as shown below:   

    > 192.168.3.161:5000  

- If no image is displayed, try manual running `webServer.py` as described in the step above.  

- If image is shown, you can control the robot to move now. You may check the description for keyboard shortcuts `Instruction` at the bottom and control the robot based on its general functions with the keyboard.   

- `Video` window shows the image captured by the robot's camera in real time.  

- `Move Control` window is to control the basic movements of the robot.   

- `Arm Control` window controls the servo movement. 
    - <kbd>GRAB</kbd>   <kbd>LOOSE</kbd>: Control the claws of the robotic arm to open and close
    - <kbd>HANDUP</kbd> <kbd>HANDDOWN</kbd>: Control the robotic arm to move up and down 
    - <kbd>LEFT</kbd>   <kbd>RIGHT</kbd>: Control the claws rotation of the robotic arm 

- `CVFL Control` window is to control the visual line following function of the robot. Here only an overview for the function is described; more details will be provided in the OpenCV section: 
    - <kbd>START</kbd>: Enable or disable the visual line following function. 
    - <kbd>COLOR</kbd>: Switch between white and black line following. By default the robot follows white lines; click the button to switch to black line following.
    - The line following function analyzes two pixels in parallel and utilizes the information detected; the positions of these two pixels are `L1` and `L2`.
    - `SP` is the threshold of the turning command based on the visual analysis results. A bigger `SP` value means a big deviation; though a particularly small `SP` value may stop the robot from moving as it can't aim the target and find the direction. 
    - When the visual line following function is enabled, the video screen will automatically become binarized results, making the visual analysis clearer.  

- `Hard Ware` window displays CPU temperature, CPU occupancy rate, and memory usage of the Raspberry Pi.  

- `Actions`window control unique functions of the robot: 
    - <kbd>MOTION GET</kbd>: Motion detection function based on OpenCV. When objects move in the view of the camera, the program will circle the part in the `Video` window, and the LED light on the robot will show respective changes. 
    - <kbd>AUTO MATIC</kbd>: Obstacle avoidance function based on ultrasonic. When the ultrasonic module on the robot detects an obstacle, it will automatically turn left, and take a step backward before turning if it's too close to the obstacle. 
    - <kbd>POLICE LIGHT</kbd>: WS2812-LED light control based on multithreading. It makes the WS2812-LED light on the robot blink red and blue alternately.
    - <kbd>TRACK LINE</kbd>: Line tracking function by using the 3-channel infrared module. By default it tracks black lines on a white surface (a white background that reflects infrared, and 1-cm wide black lines that do not reflects infrared). Performance of the line tracking varies from surface and line materials as well as the height of the robot chassis; you may need a cross screwdriver to adjust the potentiometer on the line tracking module.  

- `FC Control` window controls the color lock function of the robot:
    - <kbd>START</kbd>: Enable or disable color searching and tracking function.
    - <kbd>COLOR</kbd>: Select the color to track.
    - When the function is on, the robot will automatically lock one particular color in the camera view. By default it tracks bright yellow objects. You can change the color as you want. When an object is locked, the LED on the robot will turn orange. As the robot's head can only move up and down, the program does not involve tracking colors horizontally. If you have interest in this part, you may add the motor control based on the openCV section to realize effect.   

![webControl](images/webControl.png)

## 6. Q&A

- Where to find the IP address of the Raspberry Pi?

    > - Before connecting the Raspberry Pi via SSH, you need to know the IP address of the Raspberry Pi. Check the Management interface for your router, or download the app `Network Scanner` -> search for a device named `RASPBERRY` or `Raspberry Pi Foundation` to get the IP address.  

    > For other methods of obtaining the IP address of Raspberry Pi, refer to the official documentation [IP Address](https://www.raspberrypi.org/documentation/remote-access/ip-address.md) 

- Errors occur with `permission denied` prompt when I manually run `server.py` or `webServer.py`.

    > The Raspberry Pi needs the root permission to run the dependent libraries for WS2812 LED lights control.
    > You need to add `sudo` to the beginning of `server.py` or `webServer.py` to run the program. 
    > sudo python3 [PATH]/server.py
    > sudo python3 [PATH]/webServer.py

- I can't create the hotspot for the robot. 

    > You need to use the open source project create_ap to setup the robot's hotspot. Prior to use, disconnect WiFi network but DO NOT turn the WiFi module off, or the create_ap will show an error of hardware being blocked. 

- The servo rotates to an abnormal degree. 

    > Before assembling the rocker arm and servo, you need to make the servo gears rotate to the central position of its rotating range. Then assemble the rocker arm based on the angle instructed in the documentation. There can be a deviation of less than 9° due to the structure of the servo (number of teeth is 20 for the servo gears). For better performance, you may refer to the servo control documentation for initial degree adjustment by code. 

- The servo is shaking. 

    > Probably the servo reducing gear is broken. 

- Raspberry Pi can't boot. 

    > Remove all parts on the driver board. Only connect the board to Raspberry Pi and power supply, reboot. 

- "Remote side unexpectedly closed network connection" shows on a popup window. 

    > There can be error prompts during installation because the Raspberry Pi will auto reboot after the installation, which will disconnect the board. 

- Program crashes after double clicking on client.py or GUI.py.

    > Run the script by `python client.py` or `python GUI.py` in cmd and check the error reports.

- How to initialize the servo's angle?

    > If you've finished software installation on the Raspberry Pi, just boot it up and the servo will be initialized. 

- I can connect to the Raspberry Pi terminal via SSH \ Raspberry Pi failed to connect a WiFi.

    > The power supply methods will not influence control by SSH. Check whether you've created the file `wpa_supplicant.conf` for multiple times. If yes, that's problem causing SSH errors. 

- Can I supply the Robot HAT and Raspberry Pi via USB? 

    > A 2A output is required for a Raspberry Pi 3B, when at least 3A is needed for a Raspberry Pi 4. You can use the USB power for software installation and testing, but it's not suitable for high power module like servo or motor adjustment as it may result in low voltage. It's recommended to use battery for power here.

- After installation, the robot shows no response when booting. 

    > The `server.py` or `webServer.py` may not run due to some reasons. Try to manually run `server.py` or `webServer.py` and check whether there's any error prompt.

- The servo doesn't return to the central position when connected to the driver board. 

    > In general, the Raspberry Pi will auto run `webServer.py` when booting, and `webServer.py` will run and control the servo ports to send a signal of rotating to the central position. When assembling the servo, you can connect it to any servo port anytime. After connecting the servo to the port, the gears will rotate to the central position; assemble the rocker arm to the servo, disconnect the servo from the port, and insert more servos to repeat rocker arm assembly (all servos will be in the central position). 

    > When the servo is powered on, try moving the rocker arm. If it can't be moved, it indicates the program for the servo works; otherwise there's error for the servo program. Run the line `[RobotName]/initPosServos.py` (replace `[RobotName]` with the folder name of your robot's program) to make the servo rotate to the central position.  

    > When booting (it may take 30-50s), it takes a while for the Raspberry Pi to control PCA9685 to set signal of all servo ports for central position rotating. 

- “no cv2" error occurs when I manually run `server.py` or `webServer.py`. 

    > OpenCV is not installed correctly. Type in the command sudo pip3 install opencv-contrib-python in the Raspberry Pi to manually install OpenCV.