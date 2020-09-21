---
description: 'Nachstehend sind einige Best-Practice-Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. Gehen Sie dazu folgendermaßen vor '
keywords: Data Feed;best practices;traffic spike;hourly;ftp
title: Best Practice und allgemeine Informationen
uuid: f2d6c13a-5d4e-4fc2-8baa-28c69f0cf5f6
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '211'
ht-degree: 100%

---


# Best Practices

Nachstehend sind einige Best-Practice-Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. 

* Stellen Sie sicher, dass Sie erwartete Traffic-Spitzen frühzeitig kommunizieren. Latenz wirkt sich direkt auf die Verarbeitungszeit für Daten-Feeds aus. Siehe [Planen von Traffic-Spitzen](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) im Admin-Benutzerhandbuch.
* Daten-Feeds enthalten kein Service-Level-Agreement, es sei denn, in Ihrem Vertrag mit Adobe ist dies ausdrücklich festgelegt. Feeds werden in der Regel mehrere Stunden nach Ablauf des Berichtsfensters bereitgestellt, gelegentlich kann es jedoch bis zu 12 Stunden oder mehr dauern.
* Stellen Sie sicher, dass auf Ihrer FTP-Seite ausreichend Speicherplatz zur Verfügung steht. Entfernen Sie Dateien regelmäßig aus dem Ziel, damit Ihnen nicht versehentlich der Speicherplatz ausgeht.
* Stündliche Feeds mit der Bereitstellung mehrerer Dateien werden am schnellsten verarbeitet. Erwägen Sie die Verwendung stündlicher Feeds mit mehreren Dateien, wenn eine rechtzeitige Bereitstellung für Ihre Organisation hohe Priorität hat.
* Bei Verwendung von sFTP sollten Sie keine Dateien mit `.part`-Suffix lesen oder löschen. Das `.part`-Suffix zeigt an, dass die Datei teilweise übertragen wurde. Sobald die Datei übertragen wurde, verschwindet das `.part`-Suffix.
* Wenn Sie Ihren Feed-Erfassungsvorgang automatisieren, sollten Sie die Möglichkeit in Betracht ziehen, dass eine Datei mehrmals übertragen werden kann. Duplizierte Dateien können vom Benutzer oder in seltenen Fällen von Adobe erneut gesendet werden.
