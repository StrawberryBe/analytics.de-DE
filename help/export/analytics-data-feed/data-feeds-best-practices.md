---
description: 'Nachstehend werden einige bewährte Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. Gehen Sie dazu folgendermaßen vor '
keywords: Data Feed;best practices;traffic spike;hourly;ftp
title: Bewährte Methoden und allgemeine Informationen
uuid: f2d6c13a-5d4e-4fc2-8baa-28c69f0cf5f6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Best Practices

Nachstehend werden einige bewährte Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt.

* Stellen Sie sicher, dass Sie erwartete Traffic-Spitzen frühzeitig kommunizieren. Latenz wirkt sich direkt auf die Verarbeitungszeit für Data Feeds aus. Siehe Traffic-Spitzen [planen](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) im Admin-Benutzerhandbuch.
* Datenfeeds enthalten keine Service-Level-Vereinbarung, es sei denn, in Ihrem Vertrag mit Adobe ist dies ausdrücklich festgelegt. Feeds werden in der Regel mehrere Stunden nach Ablauf des Berichtsfensters bereitgestellt, gelegentlich kann es jedoch bis zu 12 Stunden oder mehr dauern.
* Stellen Sie sicher, dass auf Ihrer FTP-Seite ausreichend Speicherplatz zur Verfügung steht. Entfernen Sie Dateien regelmäßig aus dem Ziel, damit Ihnen nicht versehentlich der Speicherplatz ausgeht.
* Stündliche Feeds werden mit der schnellsten Bereitstellung mehrerer Dateien bereitgestellt. Erwägen Sie die Verwendung stündlicher mehrfacher Dateifeeds, wenn eine rechtzeitige Bereitstellung für Ihr Unternehmen eine hohe Priorität hat.
* Bei Verwendung von sFTP sollten Sie keine Dateien mit einem `.part` Suffix lesen oder löschen. Das `.part` Suffix zeigt an, dass die Datei teilweise übertragen wurde. Sobald die Datei übertragen wurde, verschwindet das `.part` Suffix.
* Wenn Sie Ihren Feed-Erfassungsvorgang automatisieren, sollten Sie die Möglichkeit in Betracht ziehen, dass eine Datei mehrmals übertragen werden kann. Duplizierte Dateien können vom Benutzer oder selten von Adobe erneut gesendet werden.
