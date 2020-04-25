---
description: Zeigt die Links, die die Besucher Ihrer Site gern aufrufen. Die Homepage Ihrer Website hat vermutlich mehrere Links, die zur selben Seite führen. Möglicherweise gibt es einen Grafik- und Text-Link, die beide zur selben Seite führen. Dieser Bericht zeigt den Prozentsatz der Besucher, die den Grafik-Link im Vergleich zum Text-Link verwenden.
title: Benutzerspezifischer Link
topic: Reports
uuid: 2e0d0175-d5e4-4919-b601-3f488ef3e090
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Benutzerspezifischer Link

Zeigt die Links, die die Besucher Ihrer Site gern aufrufen. Die Homepage Ihrer Website hat vermutlich mehrere Links, die zur selben Seite führen. Möglicherweise gibt es einen Grafik- und Text-Link, die beide zur selben Seite führen. Dieser Bericht zeigt den Prozentsatz der Besucher, die den Grafik-Link im Vergleich zum Text-Link verwenden.

Die spezifischen Links, die verfolgt werden sollen, müssen mit speziellen Tags modifiziert werden, siehe [Linktracking](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/variables-analytics-reporting/config-var/s-linktrackvars.html).

Den [!UICONTROL Bericht „Benutzerspezifische Links] können Sie zu folgenden Zwecken einsetzen:

* Ihren Site-Entwurf zu optimieren, durch die Erkenntnis, welche Links von Besuchern bevorzugt werden
* den Bedarf an redundanten Links zu Einzelseiten zu bestätigen

## Mobile SDK-Link-Namen  {#section_70C91FE794104B5FBF289B19CC02EA8E}

Die [Mobile SDKs](https://marketing.adobe.com/resources/help/de_DE/mobile/home.html) verwenden benutzerspezifische Links, um Aktionen und Lebenszyklusmetriken zu verfolgen. In Report Suites, die verwendet werden, um mobile Anwendungen zu messen, werden möglicherweise die folgenden vom SDK festgelegten Link-Namen angezeigt:

| ADBINTERNAL:Lifecycle | Gesendet vom Lebenszyklus-Aufruf in den 4.x SDKs. |
|---|---|
| AMACTION:[Aktionsname] | Gesendet von der Methode trackAction() in den 4.x SDKs, wobei „Aktionsname“ der bei Aufruf der Methode festgelegte Name ist. |
| ADMS BP-Ereignis | Gesendet vom Lebenszyklus-Aufruf in den 3.x SDKs. |

