---
description: Auftretende Fehler werden in der Spalte „Auftragsstatus“ aufgeführt.
keywords: Data Feed;job;troubleshooting;error;ftp;chdir;connect;login;put
title: Fehlerbehebung bei Aufträgen
uuid: 8fbb914e-03db-434e-b4d3-8594144ff2b7
translation-type: ht
source-git-commit: 322e2e87ab532d5e8a864dc06613a9b275c71df5
workflow-type: ht
source-wordcount: '454'
ht-degree: 100%

---


# Fehlerbehebung bei Aufträgen

Auf dieser Seite finden Sie mögliche Ursachen für Probleme beim Anzeigen von Daten-Feeds auf Ihrer FTP-Site.

## Fehlercodes

Auftretende Fehler werden in der Spalte „Auftragsstatus“ aufgeführt.

### FTP-chdir-Fehler

Der Feed kann nicht zum angegebenen Ordner navigieren oder darin schreiben. Stellen Sie sicher, dass der Zielordner auf der FTP-Site vorhanden ist und die angegebenen Anmeldeinformationen über die erforderlichen Lese-/Schreibberechtigungen für diesen Ordner verfügen.

### FTP-Verbindungsfehler

Der Feed kann keine Verbindung zum FTP-Ziel herstellen. Vergewissern Sie sich, dass das FTP-Ziel korrekt und gültig ist.

### FTP-Fehler

Ein generischer Fehler, bei dem der Feed die Datei nicht auf die FTP-Site schreiben kann. Dieser Fehler kann möglicherweise von der Festplatte des FTP-Servers verursacht werden, wenn das Kontingent überschritten wurde. Der Fehler kann auch von einem Netzwerk- oder Zielserverfehler verursacht werden.

### FTP-Anmeldefehler

Der Feed kann sich nicht mit den angegebenen Anmeldeinformationen anmelden. Vergewissern Sie sich, dass der FTP-Benutzername und das Kennwort korrekt sind.

### FTP-Put-Fehler

Der Feed kann keine Dateien auf die FTP-Site schreiben. Vergewissern Sie sich, dass die FTP-Anmeldung über die richtigen Berechtigungen zum Lesen und Schreiben von Daten auf Ihrer FTP-Site verfügt. Dieser Fehler kann möglicherweise auch von einer vollen Festplatte oder von einem überschrittenen Datenträgerkontingent auf dem FTP-Server stammen.

## Schritte zur Fehlerbehebung

Melden Sie sich bei Ihrer FTP-Site an und laden Sie eine beliebige Datei hoch. In den meisten Fällen können Sie die Fehlerursache mithilfe dieser Schritte ermitteln.

1. Melden Sie sich mit dem Datei-Explorer (Windows) oder Finder (Mac) bei Ihrer FTP-Site an. Achten Sie darauf, das FTP-Protokoll zu verwenden (`ftp://`). Wenn Sie die FTP-Site nicht erreichen können, kontaktieren Sie den Eigentümer der FTP-Site, um das richtige Ziel einzugeben.

   ![Datei-Explorer](assets/file_explorer.png)

2. Ein Fenster wird angezeigt, in dem Sie nach dem Benutzernamen und Kennwort gefragt werden. Geben Sie Ihre Authentifizierungsdaten ein. Wenn die Anmeldeinformationen akzeptiert werden, wird im Fenster der aktuelle Inhalt auf der FTP-Site angezeigt. Wenn die Anmeldeinformationen nicht akzeptiert werden, konsultieren Sie den FTP-Eigentümer, um zu prüfen, ob der Benutzername und das Kennwort korrekt sind.
3. Laden Sie eine Datei auf die FTP-Site hoch, indem Sie sie in das authentifizierte Fenster ziehen. Dafür kann jedes Bild- oder Textdokument verwendet werden. Wenn Sie einen Fehler erhalten, wenn Sie versuchen, eine Datei auf die FTP-Site zu laden, erkundigen Sie sich beim FTP-Eigentümer, ob genügend Speicherplatz vorhanden ist und ob der Benutzername Schreibberechtigungen für die FTP-Site besitzt.
4. Nachdem Sie bestätigt haben, dass sich die Datei auf der FTP-Site befindet, können Sie die im vorherigen Schritt hochgeladene Datei löschen.
5. Wenn alle oben genannten Schritte funktionieren und Sie dennoch einen FTP-Fehler erhalten, ersuchen Sie einen Support-Mitarbeiter, sich an die Kundenunterstützung zu wenden.
