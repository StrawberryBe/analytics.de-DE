---
title: Betriebssystem
description: Das Betriebssystem des Besuchers.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
source-git-commit: 26de81f090cebb45473a04a2edbe281f1c8591a4
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 29%

---

# Betriebssystem

Die Dimension „Betriebssystem“ zeigt das Betriebssystem und die Version an, die der Besucher verwendet hat. Wenn Sie in Ihrer Web-Eigenschaft Funktionen haben, die betriebssystemspezifisch sind, hilft Ihnen diese Dimension zu verstehen, welche Betriebssysteme am häufigsten verwendet werden.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören die Betriebssysteme, die Besucher verwenden. Beispiele sind `"Windows 10"`, `"OS X 10.15"` und `"Android 9"`.

## Änderungen der Kennzeichnung und Definition

Nachstehend finden Sie eine Liste spezifischer Probleme mit der Darstellung des Betriebssystems im Benutzeragenten und in der Adobe Analytics-Berichterstellung.

### Änderung der Namenskonvention für das Apple-Betriebssystem:

Ab Version 11 verwenden wir OS X anstelle von Mac OS, um auf das Apple-Betriebssystem zu verweisen.

Beispiele:

* macOS-Version 10.15.7 (siehe Hinweis unten zu Version 10.15.7 über die Darstellung in UA-Zeichenfolgen).
* OS X Version 11.0.0

### Mac OS-Version ist im Benutzeragenten nach Version 10.15.7 falsch 

Ab Januar 2023 zeigt der Benutzeragent in allen Browsern die Mac OS-Version als 10.15.7 an, auch für neuere Versionen. Dies geschah, weil die Aufnahme von Version 11 in die UA anscheinend Probleme mit einigen Websites verursacht hat. Apple stellt außerdem fest, dass die Aufnahme einer falschen Betriebssystemversion in die Benutzeroberfläche einige Datenschutzvorteile bietet.

Beachten Sie, dass Client-Hinweise die richtige Version im Hinweis zur Plattformversion enthalten (&quot;Sec-CH-UA-Platform-Version&quot;). Dies ist ein Hinweis mit hoher Entropie, sodass nicht automatisch von Adobe erfasst wird. Siehe [Häufig gestellte Fragen zu Adobe Analytics-Hinweisen](https://experienceleague.adobe.com/docs/analytics/technotes/client-hints.html?lang=en) für Details zur Erfassung von Hinweisen zur Entropie mit hoher Entropie.

### Die Windows-Version ist im Benutzeragenten ab Windows 11 falsch

Ab Januar 2023 stellt der Benutzeragent in allen Browsern Windows 11 als Windows 10 dar.

Beachten Sie, dass Client-Hinweise die richtige Version im Hinweis zur Plattformversion enthalten (&quot;Sec-CH-UA-Platform-Version&quot;). Dies ist ein Hinweis mit hoher Entropie, sodass nicht automatisch von Adobe erfasst wird. Siehe [Häufig gestellte Fragen zu Adobe Analytics-Hinweisen](https://experienceleague.adobe.com/docs/analytics/technotes/client-hints.html?lang=en) für Details zur Erfassung von Hinweisen zur Entropie mit hoher Entropie.
