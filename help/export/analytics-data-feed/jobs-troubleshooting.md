---
description: Wenn ein Fehler auftritt, wird in der Spalte „Auftragsstatus“ ein Fehler gemeldet.
keywords: Data Feed;job;troubleshooting;error;ftp;chdir;connect;login;put
title: Fehlerbehebung bei Aufträgen
uuid: 8fbb914e-03db-434e-b4d3-8594144ff2b7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Fehlerbehebung bei Aufträgen

Wenn Sie Probleme haben, einen Datenfeed auf Ihrer FTP-Site anzuzeigen, verwenden Sie diese Seite, um zu verstehen, warum.

## Fehlercodes

Wenn ein Fehler auftritt, wird in der Spalte „Auftragsstatus“ ein Fehler gemeldet.

### FTP-Chdir-Fehler

Der Feed kann nicht in den angegebenen Ordner navigieren oder darin schreiben. Stellen Sie sicher, dass der Zielordner auf der FTP-Site vorhanden ist und dass die angegebenen Anmeldeinformationen über die richtigen Lese-/Schreibberechtigungen für diesen Ordner verfügen.

### FTP-Verbindungsfehler

Der Feed kann keine Verbindung zum FTP-Ziel herstellen. Vergewissern Sie sich, dass das FTP-Ziel korrekt und gültig ist.

### FTP-Fehler

Ein generischer Fehler, bei dem der Feed die Datei letztendlich nicht auf die FTP-Site schreiben kann. Dieser Fehler kann möglicherweise von der Festplatte des FTP-Servers verursacht werden, wenn die Quote überschritten wurde. Der Fehler kann auch von einem Netzwerk- oder Zielserverfehler verursacht werden.

### FTP-Anmeldefehler

Der Feed kann sich nicht mit den angegebenen Anmeldeinformationen anmelden. Vergewissern Sie sich, dass der FTP-Benutzername und das Kennwort korrekt sind.

### FTP-Put-Fehler

Der Feed kann keine Dateien auf die FTP-Site schreiben. Vergewissern Sie sich, dass die FTP-Anmeldung über die richtigen Berechtigungen zum Lesen und Schreiben von Daten auf Ihrer FTP-Site verfügt. Dieser Fehler kann möglicherweise auch von einer vollständigen Festplatte oder einem überschritten Datenträgerkontingent auf dem FTP-Server stammen.

## Schritte zur Fehlerbehebung

Melden Sie sich bei Ihrer FTP-Site an und laden Sie eine beliebige Datei hoch. In den meisten Fällen können Sie den Fehlerpunkt mithilfe dieser Schritte ermitteln.

1. Melden Sie sich mit dem File Explorer (Windows) oder Finder (Mac) bei Ihrer FTP-Site an. Vergewissern Sie sich, dass Sie das FTP-Protokoll (`ftp://`) verwenden. Wenn Sie die FTP-Site nicht erreichen können, können Sie mit dem Eigentümer der FTP-Site das richtige Ziel ermitteln.

   ![Datei-Explorer](assets/file_explorer.png)

2. Es wird ein Popup angezeigt, in dem Sie nach einem Benutzernamen und einem Kennwort gefragt werden. Geben Sie Ihre Authentifizierungsdaten ein. Wenn die Anmeldeinformationen akzeptiert werden, zeigt das Fenster den aktuellen Inhalt auf der FTP-Site an. Wenn die Anmeldeinformationen nicht akzeptiert werden, können Sie mit dem FTP-Eigentümer zusammenarbeiten, um sicherzustellen, dass Benutzername und Kennwort korrekt sind.
3. Laden Sie eine Datei auf die FTP-Site hoch, indem Sie sie in das authentifizierte Fenster ziehen. Jedes Bild- oder Textdokument ist ausreichend. Wenn Sie einen Fehler beim Versuch erhalten, eine Datei auf die FTP-Site zu setzen, überprüfen Sie mit dem FTP-Eigentümer, ob genügend Speicherplatz vorhanden ist und ob der Benutzername Schreibberechtigungen für die FTP-Site besitzt.
4. Nachdem Sie bestätigt haben, dass sich die Datei auf der FTP-Site befindet, können Sie die im vorherigen Schritt hochgeladene Datei löschen.
5. Wenn alle oben genannten Schritte funktionieren und Sie dennoch einen FTP-Fehler erhalten, bitten Sie einen Kundendienstmitarbeiter, sich an den Kundendienst zu wenden.
