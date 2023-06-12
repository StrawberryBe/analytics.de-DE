---
description: Nachstehend sind einige Best-Practice-Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt.
keywords: Daten-Feed;Best Practices;Traffic-Spitze;stündlich;FTP
title: Best Practice und allgemeine Informationen
feature: Data Feeds
exl-id: 5f6fbc13-b176-4f69-8f2d-7accc6e6ac2d
source-git-commit: 6b42fc4a383b05a3630cbba7c5bce6b4561a9419
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 88%

---

# Best Practices für Datenfeeds

Nachstehend sind einige Best-Practice-Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt.

* Stellen Sie sicher, dass Sie erwartete Traffic-Spitzen frühzeitig kommunizieren. Latenz wirkt sich direkt auf die Verarbeitungszeit für Daten-Feeds aus. Siehe [Planen von Traffic-Spitzen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md) im Admin-Benutzerhandbuch.

* Daten-Feeds enthalten kein Service-Level-Agreement, es sei denn, in Ihrem Vertrag mit Adobe ist dies ausdrücklich festgelegt. Feeds werden in der Regel mehrere Stunden nach Ablauf des Berichtsfensters bereitgestellt, gelegentlich kann es jedoch bis zu 12 Stunden oder mehr dauern.

* Stündliche Feeds mit der Bereitstellung mehrerer Dateien werden am schnellsten verarbeitet. Erwägen Sie die Verwendung stündlicher Feeds mit mehreren Dateien, wenn eine rechtzeitige Bereitstellung für Ihre Organisation hohe Priorität hat.

* Wenn Sie Ihren Feed-Erfassungsvorgang automatisieren, sollten Sie die Möglichkeit in Betracht ziehen, dass Treffer und Dateien mehrmals übertragen werden können. Ihr Feed-Erfassungsvorgang muss doppelte Treffer und doppelte Dateien verarbeiten, ohne Fehler zu verursachen oder Daten zu duplizieren. Es wird empfohlen, die Spalten `hitid_high` und `hitid_low` zur eindeutigen Identifizierung eines Treffers zu verwenden.

  In seltenen Fällen werden möglicherweise doppelte Werte für `hitid_high` und `hitid_low` angezeigt. Bestätigen Sie in diesem Fall, dass die Datei noch nicht gesendet und verarbeitet wurde. Wenn nur einige Zeilen in einer Datei dupliziert sind, sollten Sie `visit_num` und `visit_page_num` hinzufügen, um die Eindeutigkeit zu ermitteln.

* Wenn Sie FTP verwenden (nicht empfohlen), stellen Sie sicher, dass auf Ihrer FTP-Site genügend Platz vorhanden ist. Entfernen Sie Dateien regelmäßig aus dem Ziel, damit Ihnen nicht versehentlich der Speicherplatz ausgeht.

* Bei Verwendung von sFTP (nicht empfohlen) sollten Sie keine Dateien mit einer `.part` Suffix. Das `.part`-Suffix zeigt an, dass die Datei teilweise übertragen wurde. Sobald die Datei übertragen wurde, verschwindet das `.part`-Suffix.