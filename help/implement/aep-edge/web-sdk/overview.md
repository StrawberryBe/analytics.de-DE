---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK
description: Verwenden Sie die Web SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
source-git-commit: 97bff355a5d9bb737d510221b63ba1321aaf5812
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 31%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK

Sie können das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html) verwenden, um Daten an Adobe Analytics zu senden. Bei dieser Implementierungsmethode wird das [Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) in ein von Analytics verwendetes Format übersetzt.

Sie können Daten direkt mit dem Web SDK oder über die Web SDK-Erweiterung in Tags an Experience Edge senden.

## Web SDK

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mit dem Web SDK-Workflow](../../assets/websdk-annotated.png)

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
<td><b>Erstellen einer Datenschicht</b> um das Tracking der Daten auf Ihrer Website zu verwalten.</td>
<td><a href="../../prepare/data-layer.md">Datenschicht erstellen</a></td>
</tr>

<tr>
<td> 4</td>
<td><b>Installieren der vordefinierten eigenständigen Version</b>. Sie können auf die Bibliothek verweisen (<code>alloy.js</code>) direkt auf Ihrer Seite platzieren oder herunterladen und in Ihrer eigenen Infrastruktur hosten. Alternativ können Sie das NPM-Paket verwenden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-2%3A-installing-the-prebuilt-standalone-version">Installieren der vordefinierten eigenständigen Version</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en#option-3%3A-using-the-npm-package">Verwenden des NPM-Pakets</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datastream stellt die serverseitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en">Konfigurieren eines Datenstroms<a></td> 
</tr>

<td>6</td>
<td><b>Hinzufügen eines Adobe Analytics-Dienstes</b> in Ihren Datastream. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics">Hinzufügen des Adobe Analytics-Dienstes zu einem Datenspeicher</a></td>
</tr>

<tr>
<td>7</td>
<td><b>Konfigurieren des Web SDKs</b>. Stellen Sie sicher, dass die Bibliothek, die Sie in Schritt 4 installiert haben, ordnungsgemäß mit der Datastraam-ID konfiguriert ist (ehemals Edge-Konfigurations-ID (<code>edgeConfigId</code>), Organisations-ID (<code>orgId</code>) und anderen verfügbaren Optionen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de">Konfigurieren des Web SDKs</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Ausführen von Befehlen</b> und/oder <b>Ereignisse verfolgen</b>. Nachdem der Basis-Code auf Ihrer Webseite implementiert wurde, können Sie mit der Ausführung von Befehlen und Tracking-Ereignissen mit dem SDK beginnen.
</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/executing-commands.html?lang=en">Ausführen von Befehlen</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=en">Ereignisse verfolgen</a></td>
</tr>

<tr>
<td>9</td><td><b>Implementierung erweitern und validieren</b> bevor sie in die Produktion verschoben wird.</td><td></td> 
</tr>
</table>


## Web SDK-Erweiterung

Eine allgemeine Übersicht über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mithilfe des Workflows Web SDK-Erweiterung](../../assets/websdk-extension-annotated.png)

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
<td><b>Erstellen einer Datenschicht</b> um das Tracking der Daten auf Ihrer Website zu verwalten.</td>
<td><a href="../../prepare/data-layer.md">Datenschicht erstellen</a></td>
</tr>

<tr>
<td>4</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datastream stellt die serverseitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en">Konfigurieren eines Datenstroms<a></td> 
</tr>

<tr>
<td>5</td> 
<td><b>Hinzufügen eines Adobe Analytics-Dienstes</b> in Ihren Datastream. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en#analytics">Hinzufügen des Adobe Analytics-Dienstes zu einem Datenspeicher</a></td>
</tr>

<tr>
<td>6</td>
<td><b>Tag-Eigenschaft erstellen</b>. Eigenschaften sind übergreifende Container, die zum Verweisen auf Tag Management-Daten verwendet werden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en#for-web">Erstellen oder Konfigurieren einer Tag-Eigenschaft für das Web</a></td>
</tr>

<tr>
<td>7</td> 
<td><b>Installieren und Konfigurieren der Web SDK-Erweiterung</b> in Ihrer Tag-Eigenschaft. Konfigurieren Sie die Web SDK-Erweiterung, um Daten an den in Schritt 4 konfigurierten Datastream zu senden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=en">Adobe Experience Platform Web SDK-Erweiterung – Übersicht</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Iterieren, Validieren und Veröffentlichen</b> zur Produktion. Fügen Sie die Tag-Eigenschaft Ihrer Website hinzu. Verwenden Sie dann Datenelemente, Regeln usw., um Ihre Implementierung anzupassen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=de">Veröffentlichungsübersicht</a></td>
</tr>

</table>


## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Dokumentation zum Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/web-sdk.html?lang=de)
