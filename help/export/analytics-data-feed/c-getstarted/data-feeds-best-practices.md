---
description: 'Nachstehend werden einige bewährte Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. Gehen Sie dazu folgendermaßen vor '
keywords: Data Feed;best practices;traffic spike;hourly;ftp
solution: Analytics
title: Bewährte Methoden und allgemeine Informationen
uuid: f2d6c13a-5d4e-4fc2-8baa-28c69f0cf5f6
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Bewährte Methoden und allgemeine Informationen

Nachstehend werden einige bewährte Methoden für die Verarbeitung und Bereitstellung von Datenfeeds aufgeführt. Gehen Sie dazu folgendermaßen vor:

* Gehen Sie davon aus, dass Datenfeeds innerhalb von 12 Stunden nach Ende eines bestimmten Zeitraums bereitgestellt werden (95 % der Zielzeit).

   Wenn es sich beispielsweise um einen stündlichen Feed handelt, sollte die Datenfeed-Anforderung für die Stunde zwischen 3:00 und 4:00 bis 4:00 bereitgestellt werden (95 % der Zielzeit). Die Verarbeitung und Bereitstellung von Datenfeeds für Report Suites mit hohem Datenverkehrvolumen kann mehr Zeit in Anspruch nehmen, insbesondere wenn sie nicht als stündliche Feeds, sondern als tägliche Feeds konfiguriert sind.
* Stellen Sie sicher, dass Sie [erwartete Traffic-Spitzen](https://marketing.adobe.com/resources/help/en_US/reference/t_traffic_schedule_spike.html) frühzeitig kommunizieren. Jede Upstream-Latenz hat einen direkten Einfluss darauf, wie schnell der Datenfeedprozess beginnt.
* Stellen Sie sicher, dass auf Ihrer FTP-Seite ausreichend Speicherplatz zur Verfügung steht. Reinigen Sie es regelmäßig, damit Ihnen nicht versehentlich der Speicherplatz ausgeht.
* Stellen Sie bei einer Änderung der FTP-Anmeldeinformationen sicher, dass die Anmeldeinformationen im Datenfeedsystem von Adobe aktuell sind.
* Nutzen Sie, wenn möglich, die stündliche Auslieferung. Dadurch werden die Dateien kleiner und können schneller erstellt und übertragen werden.
* Erwägen Sie die Verwendung der Bereitstellung mehrerer Dateien (üblicherweise mit großen täglichen Feeds). Bei Bereitstellung mehrerer Dateien wird eine einzelne monolithische Datei in kleinere Dateien aufgeteilt, die alle zur gleichen Zeit ausgeliefert werden. Auch hier können die kleineren Dateien schneller erstellt, gezippt/entzippt und übertragen werden.
* Wenn Sie sFTP als Bereitstellungsmethode verwenden, lesen und löschen Sie keine Dateien mit dem Suffix ".part". Das Suffix ".part"zeigt an, dass die Datei teilweise übertragen wurde, aber nicht vollständig ist. Nachdem die Datei übertragen wurde, wird sie ohne das Suffix ".part"umbenannt.
* Erstellen Sie den ETL-Prozess mit der Annahme, dass eine Datei gelegentlich mehrmals übertragen wird. Andernfalls können Daten doppelt vorliegen.
