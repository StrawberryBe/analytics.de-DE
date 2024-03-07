---
title: Implementieren von Adobe Analytics mit Adobe Experience Platform Edge
description: Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 914b822aae659d1d0f0b8a98480090ead99e102a
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 23%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Edge Network

Mit dem Adobe Experience Platform Edge Network können Sie Daten an mehrere Produkte an einen zentralen Ort senden. Das Edge-Netzwerk leitet die entsprechenden Informationen an die gewünschten Produkte weiter. Mit diesem Konzept können Sie Implementierungsaufgaben zusammenfassen, insbesondere, wenn mehrere Datenlösungen vorhanden sind.

Adobe bietet drei Hauptmethoden zum Senden von Daten an das Edge-Netzwerk:

* **[Adobe Experience Platform Web SDK](web-sdk/overview.md)**: Verwenden Sie die Web SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, um Daten an Edge zu senden.
* **[Adobe Experience Platform Mobile SDK](mobile-sdk/overview.md)**: Verwenden Sie die Mobile SDK-Erweiterung in der Datenerfassung von Adobe Experience Platform, um Daten an Edge zu senden.
* **[Adobe Experience Platform Edge Network Server-API](server-api/overview.md)**: Senden Sie Daten mit einer API direkt an Edge.



## Verarbeitung von Edge-Netzwerkdaten durch Adobe Analytics

An das Adobe Experience Platform Edge Network gesendete Daten können zwei Formate aufweisen:

* XDM-Objekt: Mit Schemas konform basierend auf [XDM (Experience-Datenmodell)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de). Mit XDM können Sie flexibel bestimmen, welche Felder als Teil von Ereignissen definiert werden. Wenn Ereignisse Adobe Analytics erreichen, werden sie in ein Format übersetzt, das von Adobe Analytics verarbeitet werden kann.
* Datenobjekt: Senden Sie Daten mithilfe bestimmter, Adobe Analytics zugewiesener Felder an das Edge-Netzwerk. Das Edge-Netzwerk erkennt das Vorhandensein dieser Felder und leitet sie an Adobe Analytics weiter, ohne dass ein Schema konform sein muss.


Das Edge-Netzwerk verwendet die folgende Logik, um die Seitenansichten und Verknüpfungsereignisse in Adobe Analytics zu bestimmen

| XDM-Payload enthält ... | Adobe Analytics... |
|---|---|
| `web.webPageDetails.name` oder `web.webPageDetails.URL` und `web.webInteraction.type` | berücksichtigt Nutzdaten einer **Seitenansicht** |
| `web.webInteraction.type` und (`web.webInteraction.name` oder `web.webInteraction.url`) | berücksichtigt Nutzdaten einer **Linkereignis** |
| `web.webInteraction.type` und (`web.webPageDetails.name` oder `web.webPageDetails.url`) | berücksichtigt Nutzdaten einer **Linkereignis** <br/>`web.webPageDetails.name` und `web.webPageDetails.URL` auf `null` |
| no `web.webInteraction.type` und `webPageDetails.name` und `web.webPageDetails.URL`) | die Payload entfernt und die Daten ignoriert |

{style="table-layout:auto"}

Siehe [Feldergruppe Adobe Analytics ExperienceEvent Full Extension](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html) für weitere Informationen.
