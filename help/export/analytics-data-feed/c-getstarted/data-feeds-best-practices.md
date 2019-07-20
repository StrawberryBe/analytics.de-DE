---
description: 'Nachstehend werden einige bewährte Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. Gehen Sie dazu folgendermaßen vor '
keywords: Datenfeed; Best Practices; Traffic-Spitze; stündlich; ftp
seo-description: 'Nachstehend werden einige bewährte Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. Gehen Sie dazu folgendermaßen vor '
seo-title: Bewährte Methoden und allgemeine Informationen
solution: Analytics
title: Bewährte Methoden und allgemeine Informationen
uuid: f 2 d 6 c 13 a -5 d 4 e -4 fc 2-8 baa -28 c 69 f 0 cf 5 f 6
translation-type: tm+mt
source-git-commit: d8f2458e7bae596dbabc8dab33ea5d2881047566

---


# Bewährte Methoden und allgemeine Informationen

Nachstehend werden einige bewährte Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. Gehen Sie dazu folgendermaßen vor:

* Gehen Sie davon aus, dass Datenfeeds innerhalb von 12 Stunden nach Ende eines bestimmten Zeitraums bereitgestellt werden (95 % der Zielzeit).

   Wenn es sich beispielsweise um einen stündlichen Feed handelt, sollte die Datenfeed-Anforderung für die Stunde zwischen 3:00 und 4:00 bis 4:00 bereitgestellt werden (95 % der Zielzeit). Die Verarbeitung und Bereitstellung von Datenfeeds für Report Suites mit hohem Datenverkehrvolumen kann mehr Zeit in Anspruch nehmen, insbesondere wenn sie nicht als stündliche Feeds, sondern als tägliche Feeds konfiguriert sind.
* Stellen Sie sicher, dass Sie [erwartete Traffic-Spitzen](https://marketing.adobe.com/resources/help/en_US/reference/t_traffic_schedule_spike.html) frühzeitig kommunizieren. Jede Upstream-Latenz hat einen direkten Einfluss darauf, wie schnell der Datenfeedprozess beginnt.
* Stellen Sie sicher, dass auf Ihrer FTP-Seite ausreichend Speicherplatz zur Verfügung steht. Führen Sie regelmäßig eine Bereinigung durch, sodass keine Gefahr besteht, dass Ihnen versehentlich der Speicherplatz ausgeht.
* Stellen Sie bei einer Änderung der FTP-Anmeldeinformationen sicher, dass die Anmeldeinformationen im Datenfeedsystem von Adobe aktuell sind.
* Nutzen Sie, wenn möglich, die stündliche Auslieferung. Dadurch werden die Dateien kleiner und können schneller erstellt und übertragen werden.
* Nutzen Sie gegebenenfalls die Option „Bereitstellung mehrerer Dateien“ (wird normalerweise für große tägliche Feeds verwendet). Bei Bereitstellung mehrerer Dateien wird eine einzelne monolithische Datei in kleinere Dateien aufgeteilt, die alle zur gleichen Zeit ausgeliefert werden. Auch hier können die kleineren Dateien schneller erstellt, gezippt/entzippt und übertragen werden.
* Wenn Sie sFTP als Bereitstellungsmethode nutzen, lesen und löschen Sie keine Dateien mit dem Suffix „.part“. Das Suffix „.part“ gibt an, dass die Datei teilweise übertragen wurde und dass sie nicht vollständig ist. Nachdem die Datei übertragen wurde, wird sie umbenannt, sodass sie das Suffix „.part“ nicht mehr enthält.
* Erstellen Sie den ETL-Prozess mit der Annahme, dass eine Datei gelegentlich mehrmals übertragen wird. Andernfalls können Daten doppelt vorliegen.
