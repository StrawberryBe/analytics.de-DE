---
title: Implementieren von Adobe Analytics mit der Adobe Experience Platform Edge Network Server-API
description: Verwenden Sie die Adobe Experience Platform Edge Network Server-API, um Daten an Adobe Analytics zu senden.
exl-id: 1ede95b7-4f17-4d69-aba6-62b253b6693a
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 35%

---

# Implementieren von Adobe Analytics mit der Adobe Experience Platform Edge Network Server-API

Normalerweise verwenden Sie die Experience Platform Edge Network Server-API, um Daten von Geräten wie IoT-Geräten, Set-Top-Boxen und Desktop-Anwendungen zu erfassen. Senden Sie diese Daten dann an das Edge-Netzwerk und dann an Dienste wie Adobe Analytics.

Beachten Sie auch die Edge Network Server-API, wenn vertrauliche Daten sicher erfasst und im Netzwerk authentifiziert werden müssen. Siehe [Authentifizierung](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/authentication.html?lang=en) für weitere Informationen.

Ein allgemeiner Überblick über die Implementierungsaufgaben:

![Workflow von Adobe Analytics mit der Analytics-Erweiterung](../../assets/edge-network-server-api.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td>1</td>
<td>Stellen Sie sicher, dass Sie <b>eine Report Suite definiert haben</b>.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Schemas einrichten</b>. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe das offene und öffentlich dokumentierte Standard Experience-Datenmodell (XDM) erstellt.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de">Übersicht über die Benutzeroberfläche von Schemas</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datastream stellt die serverseitige Konfiguration bei Verwendung der APIs aus der Adobe Experience Platform Edge Network-API dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de">Konfigurieren eines Datenstroms<a></td> 
</tr>

<tr>
<td>4</td>
<td><b>Implementieren und Testen der Datenerfassung</b> Verwendung der Datenerfassungs-APIs für Einzelereignisse und Batch-Ereignisse.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=en">Datenerfassung mit einem Ereignis</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/non-interactive-data-collection.html?lang=en">Datenerfassung für Batch-Ereignisse</a>
</tr>

<td>5</td>
<td><b>Fügen Sie einen Adobe Analytics-Service</b> in Ihrem Datenstrom hinzu. Mit diesem Service wird gesteuert, ob und wie Daten an Adobe Analytics gesendet werden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html?lang=ens">Interagieren mit Adobe Analytics</a></td>
</tr>


</table>

Siehe [Dokumentation zur Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=de)und ein Beispiel [Integration mit Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/interacting-other-adobe-solutions/interacting-adobe-analytics.html?lang=de) für weitere Informationen.

