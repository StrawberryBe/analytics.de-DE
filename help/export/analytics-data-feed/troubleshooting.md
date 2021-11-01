---
title: Fehlerbehebung bei Daten-Feeds
description: Erfahren Sie, wie Sie Probleme mit Daten-Feeds ermitteln und beheben können.
keywords: job;Fehlerbehebung;Fehler;ftp;chdir;connect;login;put
exl-id: c082bc95-cdae-448b-86b5-695660fb2352
source-git-commit: b81ffba2f1e021888dd1c4b016c9b451448f47bb
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 29%

---

# Fehlerbehebung bei Daten-Feeds

Ermitteln Sie potenzielle Gründe, aus denen ein Auftrag möglicherweise nicht verarbeitet oder bereitgestellt werden kann.

## Fehlerbehebung bei vorhandenen Daten-Feeds

Wenn Sie über einen Daten-Feed verfügen, der stündlich oder täglich funktioniert, aber kürzlich fehlschlägt, überprüfen Sie jeden der folgenden Punkte:

* Verwenden Sie die [Tool &quot;Adobe Status&quot;](https://status.adobe.com/en/experience_cloud) um festzustellen, ob geplante Wartungsfenster oder Verfügbarkeitsprobleme vorliegen. Wenn zu diesem Zeitpunkt ein bekanntes Problem vorliegt, verarbeitet Adobe automatisch geplante Daten-Feeds, sobald der Dienst wiederhergestellt wurde.
* Stellen Sie sicher, dass auf der FTP-Site ausreichend Speicherplatz zur Verfügung steht. Wenn der FTP-Site der Speicherplatz ausgeht, löschen Sie einige Dateien vom Server, um Platz für neue Dateien zu schaffen.
* Wenn keine bekannten Probleme vorliegen und die FTP-Site über ausreichend Speicherplatz verfügt, können Sie den Daten-Feed erneut senden.

   1. Melden Sie sich bei Adobe Analytics an und navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Datenfeeds]**.
   2. Suchen Sie die gewünschten Daten-Feeds und klicken Sie dann auf das Kontrollkästchen neben den anderen Feeds, die Sie erneut ausführen möchten.
   3. Klicken **[!UICONTROL Rerun]**.

   ![Rerun](assets/rerun.png)

Wenn Sie die Daten-Feed-Dateien nach der erneuten Ausführung immer noch nicht erhalten, wenden Sie sich an die Kundenunterstützung.

## Fehlerbehebung bei einem neuen Daten-Feed

Wenn ein neuer Daten-Feed einen Fehler ausgibt, beheben Sie das Problem, indem Sie manuell eine Testdatei auf die FTP-Site hochladen. In den meisten Fällen können Sie die Fehlerursache mithilfe dieser Schritte ermitteln.

1. Melden Sie sich mit dem Datei-Explorer (Windows) oder Finder (Mac) bei Ihrer FTP-Site an. Vergewissern Sie sich, dass Sie das FTP-Protokoll (`ftp://`) und dass Sie [IP-Adressen der Adobe](/help/technotes/ip-addresses.md) durch die Firewall Ihres Unternehmens. Wenn Sie die FTP-Site nicht erreichen können, wenden Sie sich an den Eigentümer der FTP-Site, um das richtige Ziel zu ermitteln.

   ![Datei-Explorer](assets/file_explorer.png)

2. Ein Fenster wird angezeigt, in dem Sie nach dem Benutzernamen und Kennwort gefragt werden. Geben Sie Ihre Authentifizierungsdaten ein. Wenn die Anmeldeinformationen akzeptiert werden, wird im Fenster der aktuelle Inhalt auf der FTP-Site angezeigt. Wenn die Anmeldeinformationen nicht akzeptiert werden, wenden Sie sich an den FTP-Eigentümer, um sicherzustellen, dass der Benutzername und das Kennwort korrekt sind. Bei Verwendung von SFTP müssen Sie jeden Schritt im Abschnitt [SFTP-Handbuch](../ftp-and-sftp/c-sftp/ftp-sftp.md). Beachten Sie, dass Adobe nicht alle SFTP-Anwendungsfälle unterstützt.
3. Laden Sie eine Datei auf die FTP-Site hoch, indem Sie sie in das authentifizierte Fenster ziehen. Dafür kann jedes Bild- oder Textdokument verwendet werden. Wenn Sie einen Fehler erhalten, wenn Sie versuchen, eine Datei auf die FTP-Site zu laden, erkundigen Sie sich beim FTP-Eigentümer, ob genügend Speicherplatz vorhanden ist und ob der Benutzername Schreibberechtigungen für die FTP-Site besitzt.
4. Nachdem Sie bestätigt haben, dass sich die Datei auf der FTP-Site befindet, können Sie die im vorherigen Schritt hochgeladene Datei löschen.

Wenn alle oben genannten Schritte funktionieren und dennoch ein FTP-Fehler auftritt, wenden Sie sich an die Kundenunterstützung.
