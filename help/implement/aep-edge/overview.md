---
title: Implementieren von Adobe Analytics mit Adobe Experience Platform Edge
description: Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 9d9212313f54e4b44c5341754942ac0e0c78b84c
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 35%

---

# Implementieren von Adobe Analytics mit Adobe Experience Platform Edge

Mit Adobe Experience Platform Edge können Sie Daten, die für mehrere Produkte bestimmt sind, an einen zentralen Ort senden. Experience Edge leitet die entsprechenden Informationen an die gewünschten Produkte weiter. Mit diesem Konzept können Sie Implementierungsaufgaben zusammenfassen, insbesondere, wenn mehrere Datenlösungen vorhanden sind.

Adobe bietet drei Methoden zum Senden von Daten an Experience Edge:

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Verwenden Sie die Web SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, um Daten an Edge zu senden.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Verwenden Sie die Mobile SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, um Daten an Edge zu senden.
* **[Adobe Experience Platform Edge Network Server-API](server-api/overview.md)**: Senden Sie Daten mit einer API direkt an Edge.



## Verarbeitung von Experience Edge-Daten durch Adobe Analytics

Daten, die an Experience Edge gesendet werden, müssen Schemas entsprechen, die auf [XDM (Experience-Datenmodell)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de). Mit XDM können Sie flexibel bestimmen, welche Felder als Teil von Ereignissen definiert werden. Wenn Ereignisse Adobe Analytics erreichen, werden diese Ereignisse in strukturiertere Daten übersetzt, die Adobe Analytics verarbeiten kann: Seitenansichten oder Verknüpfungsereignisse.

XDM schreibt selbst nicht vor, wie Seitenansichten oder Verknüpfungsereignisse definiert werden, und weist Adobe Analytics auch nicht an, wie seine Payload zu behandeln ist. Zum Beispiel bestimmte vordefinierte XDM-Felder, die scheinbar mit Seitenansichten oder Link-Ereignissen verbunden sind, wie `eventType`, `web.webPageDetails.pageViews`oder `web.webInteraction.linkEvents` sind vollständig unabhängig von der Implementierung und haben keine Relevanz für Adobe Analytics.

Um Seitenansichten und Verknüpfungsereignisse ordnungsgemäß zu verarbeiten, wird die folgende Logik auf Daten angewendet, die an das Adobe Experience Edge-Netzwerk gesendet und an Adobe Analytics weitergeleitet werden.

| XDM-Payload enthält ... | Adobe Analytics... |
|---|---|
| `web.webPageDetails.name` oder `web.webPageDetails.URL` und `web.webInteraction.type` | berücksichtigt Nutzdaten einer **Seitenansicht** |
| `web.webInteraction.type` und (`web.webInteraction.name` oder `web.webInteraction.url`) | berücksichtigt Nutzdaten einer **Linkereignis** |
| `web.webInteraction.type` und (`web.webPageDetails.name` oder `web.webPageDetails.url`) | berücksichtigt Nutzdaten einer **Linkereignis** <br/>`web.webPageDetails.name` und `web.webPageDetails.URL` auf `null` |
| no `web.webInteraction.type` und `webPageDetails.name` und `web.webPageDetails.URL`) | die Payload entfernt und die Daten ignoriert |

{style="table-layout:auto"}

Siehe [Feldergruppe Adobe Analytics ExperienceEvent Full Extension](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html?lang=en) für weitere Informationen.
