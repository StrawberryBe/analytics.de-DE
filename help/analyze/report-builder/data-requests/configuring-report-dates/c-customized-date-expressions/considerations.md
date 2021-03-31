---
description: 'Bei der Verwendung von „Ausdruck anpassen“ für die Festlegung eines Datumsbereichs sind zwei Umstände besonders zu beachten '
title: Überlegungen zum benutzerdefinierten Datum
uuid: a3bb3a63-0f15-4292-ade7-4ea852fe68c8
feature: Report Builder
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 99%

---


# Überlegungen zum benutzerdefinierten Datum

Bei der Verwendung von „Ausdruck anpassen“ für die Festlegung eines Datumsbereichs sind zwei Umstände besonders zu beachten:

* Der Tag der Ausführung des Berichts bzw. der Aktualisierung von Anforderungen („Ausführungsdatum“) legt fest, welche Daten verfügbar sind.
* Die Verschiebung von Start- und Enddatumswerten für den Bericht hat Auswirkungen darauf, welcher Datumsbereich von dem Bericht abgedeckt wird.

Da die Verfügbarkeit von Daten sowohl vom zeitlichen Rahmen des Berichts als auch vom Datum der Aktualisierung von Anforderungen in dem Bericht abhängt, müssen Sie sicherstellen, dass der Bericht an Tagen ausgeführt wird, die dafür geeignet sind, die gewünschten Informationen zu erhalten. Die nachstehenden Beispiele illustrieren die beiden besonders zu berücksichtigenden Umstände.

Angenommen, Sie fordern die Zahl der [!UICONTROL Seitenaufrufe] mit einer Granularität von „Aggregiert“ an. In Nordamerika beginnt die Woche am Sonntag. Um aktualisierte Berichte für die Zeit von Sonntag bis Samstag (z. B. 23.–29. November 2008) zu erhalten, führen Sie den Bericht (bzw. die Aktualisierungsanforderung) am Sonntag, den 30. November für die vergangene Woche (23.11.–29.11.) aus.

Verwenden Sie dazu diesen benutzerdefinierten Ausdruck:

*Von:* cw-1w *Bis:* cw-1d

Eine Analyse des benutzerdefinierten Ausdrucks, wenn das einschließliche [!UICONTROL Enddatum] für die Anforderung der 30.11. ist:

*Von:* cw-1w

der aktuelle Tag in der am Sonntag, dem 30. November beginnenden Woche minus sieben Tage = der Tag der am Sonntag, dem 23. November beginnenden vergangenen Woche

*Bis:* cw-1d

der Tag in der am Sonntag, dem 30. November beginnenden aktuellen Woche minus ein Tag = Samstag, der 29. November

Ordnen Sie den benutzerdefinierten Ausdruck dem Arbeitsblatt zu und aktualisieren Sie dann die Anforderung mit Sonntag, dem 30. November 2008 als einschließlichem [!UICONTROL Enddatum] für die gleitende Anforderung. Die Daten beziehen sich nur auf den wöchentlichen Zeitraum.

Wenn Sie stattdessen den Ausdruck aktualisieren und dabei Samstag, den 29. November als [!UICONTROL Enddatum] für die gleitende Anforderung angeben, beziehen sich die Daten auf die Woche vom 16.11. bis zum 22.11. Dies liegt daran, dass das Referenzdatum für die Aktualisierungsanforderung einen Tag früher liegt.

Hier sind die Unterschiede, wenn das einschließliche [!UICONTROL Enddatum] der Anforderung der 29.11. ist.

*Von:* cw-1w

der aktuelle Tag in der am Sonntag, dem 23. November beginnenden Woche minus sieben Tage = der Tag der am Sonntag, dem 16. November beginnenden vergangenen Woche

*Bis:* cw-1d

der Tag in der am Sonntag, dem 23. November beginnenden aktuellen Woche minus ein Tag = Samstag, der 22. November

In Europa und einigen anderen Ländern beginnt die Woche am Montag, nicht am Sonntag. In diesem Fall können Sie den Kalender anpassen, um das Startdatum zu ändern. (Siehe [Benutzerdefinierter Kalender](/help/analyze/report-builder/data-requests/configuring-report-dates/custom-calendar.md).)
