---
title: Tage seit dem letzten Besuch
description: Die Anzahl der Tage zwischen dem aktuellen Treffer und dem letzten Besuch.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 74%

---


# Tage seit dem letzten Besuch

Die Dimension „Tage seit dem letzten Besuch“ misst die Zeitdauer, die zwischen dem aktuellen Treffer des Besuchers und seinem vorherigen Besuch verstrichen ist (sofern vorhanden). Diese Dimension hilft Ihnen, das Verhalten der Besucher nach dem Besuch Ihrer Website zu verstehen. Beispiele hierfür sind:

* Wie häufig rufen Benutzer die Site erneut auf?
* Wie verhält sich die Rückkehrfrequenz zur Konversion? Besuchen Wiederholungskäufer die Site häufig oder weniger häufig?
* Kehren Benutzer, die sich durch Kampagnen klicken, häufiger zurück?

Erstmalige Besucher sind in dieser Dimension nicht enthalten.

## Füllen dieser Dimension mit Daten

Diese Dimension ist bei allen Implementierungen vorkonfiguriert. Wenn eine Report Suite Daten enthält, funktioniert diese Dimension.

## Dimensionen

Zu den Elementen der Dimension gehören die Tage zwischen dem letzten Besuch eines Besuchers und dem aktuellen Treffer. Each number of days is a separate dimension item, with `"Same day"` occurring where a visitor&#39;s last visit and the current hit happened on the same day.
