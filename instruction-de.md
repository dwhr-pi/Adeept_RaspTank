Zunächst sollte das Programm auf der SD-Karte erstellt werden, einschließlich des Schreibens des Raspberry Pi-Systems,
Herunterladen und Installieren des Rasptank-Programms.

Achten Sie auf die Groß-/Kleinschreibung während des Prozesses von git clone . Der spezifische Operationsprozess
steht im Dokument und Handbuch. Es wird automatisch beim Booten gestartet, nachdem das Programm erfolgreich installiert wurde.

Sie müssen die Treiberplatine und den Raspberry Pi verbinden und vor dem Einschalten das Servo mit der Treiberplatine verbinden.
Warten Sie, bis sich das Servo zum Zusammenbau in die angegebene Position dreht.

Das Servo hat 20 Zähne und wird während des Installationsvorgangs einen Fehler von weniger als 9° haben, was normal ist.

----------------------------------------------------------------------------------------------------------------------------

Das Programm .py im Ordner client ist das auf dem PC benötigte Programm.
Das .py-Programm im Ordner server ist das auf dem Roboter erforderliche Programm.

Diese Anweisung konzentriert sich auf die Programme im Ordnerserver. Wenn Probleme auftreten, können Sie diese Beschreibung verwenden, um das Problem zu lösen.


1. Was soll ich tun, wenn der Roboter das Programm beim Einschalten nicht automatisch ausführt?
Erste Ursache: Das Programm ist nicht vollständig installiert, wahrscheinlich weil die Serververbindung der benötigten abhängigen Bibliotheken instabil ist, was zu einem unvollständigen Download der abhängigen Bibliotheken führt. Die Vollversion des Programms muss die entsprechenden Abhängigkeiten installieren, um ordnungsgemäß ausgeführt zu werden.
Zweite Ursache: Linux unterscheidet zwischen Groß- und Kleinschreibung. Die Groß-/Kleinschreibung des Namens beim Klonen von Github unterscheidet sich von der der Autostart-Datei des Standardpfads.

Lösung: Versuchen Sie das Beta-Programm - ein Programm namens serverTest.py im Ordner server.
Wenn das Beta-Programm bei jedem Booten automatisch ausgeführt werden soll, führen Sie autorun.py aus - geben Sie "2" ein, um die Autorun-Beta auszuwählen - geben Sie ein.
Wenn Sie bei jedem Booten zur Vollversion des Autorun-Programms wechseln müssen, führen Sie autorun.py aus - geben Sie "1" ein, um die Vollversion von Autorun auszuwählen - geben Sie ein.


2. Was soll ich tun, wenn sich das Servo in die entgegengesetzte Richtung bewegt?
Ursache: Die Servos wurden in verschiedenen Chargen hergestellt, die Bewegungsrichtung kann unterschiedlich sein.

Lösung: Wir haben im Programm eine Schnittstelle zum Einstellen der Richtung des Servos reserviert, was das Debuggen erheblich erleichtert.
Der gesamte bewegungsbezogene Code wird in den Programmserver/move.py geschrieben.
Geben Sie den folgenden Befehl ein, um move.py zu öffnen (beachten Sie, dass er nicht ausgeführt werden soll) und bearbeiten Sie:
sudo nano (Pfad)/move.py
(Der Pfad variiert je nach gekauftem Produkt. Nehmen Sie RaspClaws als Beispiel. Der Pfad von move.py lautet //home/pi/adeept_raspclaws/server/move.py)
Ändern Sie nach dem Öffnen von move.py den Wert von Set_Direction auf 0 (der Standardwert ist 1), drücken Sie dann Strg+x zum Beenden, drücken Sie Y zum Speichern der Änderung und drücken Sie zur Bestätigung die Eingabetaste.


3. Was soll ich tun, wenn es keine gute Selbststabilisierung realisiert?
Ursache: Der IPD-Controller dient zur Selbststabilisierung. Sie müssen die entsprechenden PID-Parameter eingeben, um eine perfekte Stabilisierung zu erreichen. Die PID-Parameter jedes Roboters sind unterschiedlich.

Lösung: Wenn die Reaktion langsam ist, können Sie den P-Wert entsprechend erhöhen (die Zeile 75 von move.py). Wenn die Reaktion zu schnell ist (oder hin und her schwingt), können Sie den P-Wert entsprechend reduzieren.
Wenn die Reaktionsgeschwindigkeit normal ist, aber ein Überschwingen auftritt, müssen Sie den I-Wert entsprechend erhöhen.
Der D-Wert ist differentiell und muss für dieses Produkt normalerweise nicht geändert werden.

Der Spaß am Schaffen liegt im Lösen von Problemen
Wenn Sie weitere Fragen haben, senden Sie uns bitte eine E-Mail an support@adeept.com