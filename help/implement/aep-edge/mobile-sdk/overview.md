---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK
description: Verwenden Sie die Mobile SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
source-git-commit: 97bff355a5d9bb737d510221b63ba1321aaf5812
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 30%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Mobile SDK

Mit dem Adobe Experience Platform Mobile SDK können Sie die Experience Cloud-Lösungen und -Services von Adobe in Ihren Mobile Apps nutzen. Es ist für Android™, iOS und verschiedene plattformübergreifende Entwicklungs-Frameworks verfügbar. Die Konfiguration erfolgt über die Datenerfassung von Adobe Experience Platform.
>[!IMPORTANT]
>
>Eine Adobe Analytics-Erweiterung ist ebenfalls in der Datenerfassung von Adobe Experience Platform verfügbar. Wenn Sie diese Erweiterung installieren, nutzen Sie weder XDM noch das Edge-Netzwerk.

## Adobe Experience Platform SDK

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Adobe Analytics mithilfe des Workflows für die Analytics-Erweiterung](../../assets/mobilesdk-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td>1</td>
<td>Stellen Sie sicher, dass <b>Report Suite definiert haben</b>.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Einrichten von Schemata und Datensätzen</b>. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe den offenen und öffentlich dokumentierten Standard Experience-Datenmodell (XDM) erstellt.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de">Übersicht über die Benutzeroberfläche von Schemas</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de">Übersicht über die Benutzeroberfläche von Datensätzen</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datastream stellt die serverseitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en">Konfigurieren eines Datenstroms<a></td> 
</tr>

<td>4</td>
<td><b>Hinzufügen eines Adobe Analytics-Dienstes</b> in Ihren Datastream. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics">Hinzufügen des Adobe Analytics-Dienstes zu einem Datenspeicher</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Erstellen einer mobilen Eigenschaft</b>. Eine Eigenschaft ist ein Container, den Sie mit Erweiterungen, Regeln, Datenelementen und Bibliotheken füllen.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/">Einrichten einer mobilen Eigenschaft</a></tr>

<tr>
<td>6</td>
<td><b>Installieren der Adobe Experience Platform Edge Network-Erweiterung</b> in der mobilen Tag-Eigenschaft und konfigurieren Sie den Datastream in der Erweiterung.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/edge-network/">Adobe Experience Platform Edge Network</a>
</tr>

<tr>
<td>7</td>
<td><b>Verwenden des Codes in Ihrer App</b> , um die erforderlichen Erweiterungen zu registrieren und Ihre Tag-Konfiguration zu laden.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration">Einrichten der Konfiguration</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Implementieren und Testen von Funktionen</b> Verwenden Sie eine Kombination aus den Datenelementen, Regeln, zusätzlichen Erweiterungen und SDK-API-Aufrufen des Tags in Ihrer App. Datenerfassung und Erlebnisse für Ihre Mobile App in Inspect validieren und debuggen.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application">Beispielanwendung verwenden</a>
</tr>

<tr>
<td>9</td>
<td><b>Mobile-App-Implementierung erweitern und validieren</b> bevor sie in die Produktion verschoben wird.</td>
<td></td> 
</tr>

</table>


## Adobe Analytics-Erweiterung.

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Adobe Analytics mithilfe des Workflows für die Analytics-Erweiterung](../../assets/mobilesdk-analytics-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td>1</td>
<td>Stellen Sie sicher, dass <b>Report Suite definiert haben</b>.</td>
<td><a href="../../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Einrichten von Schemata und Datensätzen</b>. Um die Datenerfassung für die Verwendung in allen Anwendungen zu standardisieren, die Adobe Experience Platform nutzen, hat Adobe den offenen und öffentlich dokumentierten Standard Experience-Datenmodell (XDM) erstellt.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de">Übersicht über die Benutzeroberfläche von Schemas</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de">Übersicht über die Benutzeroberfläche von Datensätzen</a></td>
</tr>

<tr>
<td>3</td>
<td><b>Installieren der Adobe Analytics-Erweiterung</b> in der mobilen Tag-Eigenschaft und konfigurieren Sie die Erweiterung so, dass sie auf Ihre Report Suite verweist.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/adobe-analytics/">Adobe Analytics-Erweiterung für mobile Eigenschaft</a>
</tr>

<tr>
<td>4</td>
<td><b>Verwenden des Codes in Ihrer App</b> , um die erforderlichen Erweiterungen zu registrieren und Ihre Tag-Konfiguration zu laden.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#set-up-the-configuration">Einrichten der Konfiguration</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Implementieren und Testen von Funktionen</b> Verwenden Sie eine Kombination aus den Datenelementen, Regeln, zusätzlichen Erweiterungen und SDK-API-Aufrufen des Tags in Ihrer App. Datenerfassung und Erlebnisse für Ihre Mobile App in Inspect validieren und debuggen.</td>
<td><a href="https://developer.adobe.com/client-sdks/documentation/user-guides/getting-started-with-platform/overview/#use-the-sample-application">Beispielanwendung verwenden</a>
</tr>

<tr>
<td>6</td>
<td><b>Mobile-App-Implementierung erweitern und validieren</b> bevor sie in die Produktion verschoben wird.</td>
<td></td> 
</tr>

</table>

## Zusätzliche Ressourcen

- [Dokumentation zu Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#)

- [Mobile-SDKs – Dokumentation](https://developer.adobe.com/client-sdks/documentation/)



