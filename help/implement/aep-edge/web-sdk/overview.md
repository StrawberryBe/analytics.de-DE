---
title: Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK
description: Verwenden Sie die Web SDK-Erweiterung in der Adobe Experience Platform-Datenerfassung, um Daten an Adobe Analytics zu senden.
exl-id: 97f8d650-247f-4386-b4d2-699f3dab0467
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: 9d9212313f54e4b44c5341754942ac0e0c78b84c
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 76%

---

# Implementieren von Adobe Analytics mit dem Adobe Experience Platform Web SDK

Sie können das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=de) verwenden, um Daten an Adobe Analytics zu senden. Bei dieser Implementierungsmethode wird das [Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) in ein von Analytics verwendetes Format übersetzt.

Sie können Daten direkt mit der [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/overview.html?lang=en)oder über die Web SDK-Erweiterung in Tags.

## Web SDK

Ein allgemeiner Überblick über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mit dem Web SDK-Workflow, wie in diesem Abschnitt beschrieben.](../../assets/websdk-annotated.png)

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
<td><b>Erstellen Sie eine Datenschicht</b>, um das Tracking der Daten auf Ihrer Website zu verwalten.</td>
<td><a href="../../prepare/data-layer.md">Datenschicht erstellen</a></td>
</tr>

<tr>
<td> 4</td>
<td><b>Installieren Sie die vordefinierte eigenständige Version</b>. Sie können direkt auf Ihrer Seite auf die Bibliothek (<code>alloy.js</code>) im CDN verweisen oder sie herunterladen und in Ihrer eigenen Infrastruktur hosten. Alternativ können Sie das NPM-Paket verwenden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=de#option-2%3A-installing-the-prebuilt-standalone-version">Installieren der vordefinierten eigenständigen Version</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=de#option-3%3A-using-the-npm-package">Verwenden des NPM-Pakets</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datenstrom stellt die Server-seitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de">Konfigurieren eines Datenstroms<a></td> 
</tr>

<td>6</td>
<td><b>Fügen Sie einen Adobe Analytics-Service</b> in Ihrem Datenstrom hinzu. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden und an welche Report Suite(s) speziell.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de#analytics">Hinzufügen des Adobe Analytics-Service zu einem Datenstrom</a></td>
</tr>

<tr>
<td>7</td>
<td><b>Konfigurieren des Web SDKs</b>. Stellen Sie sicher, dass die Bibliothek, die Sie in Schritt 4 installiert haben, ordnungsgemäß mit der Datastraam-ID konfiguriert ist (ehemals Edge-Konfigurations-ID (<code>edgeConfigId</code>), Organisations-ID (<code>orgId</code>) und anderen verfügbaren Optionen. Stellen Sie sicher, dass Variablen ordnungsgemäß zugeordnet werden. </td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de">Web SDK konfigurieren</a><br/><a href="https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=en">Analytics-Variablenzuordnung</a><br/><a href="https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html?lang=en">Manuelles Zuordnen von Variablen</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Führen Sie Befehle aus</b> und/oder <b>verfolgen Sie Ereignisse</b>. Nachdem der Basis-Code auf Ihrer Web-Seite implementiert wurde, können Sie mit der Ausführung von Befehlen und dem Nachverfolgen von Ereignissen mit dem SDK beginnen.
</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/executing-commands.html?lang=de">Ausführen von Befehlen</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/tracking-events.html?lang=de">Nachverfolgen von Ereignissen</a></td>
</tr>

<tr>
<td>9</td><td><b>Erweitern und validieren Sie die Implementierung</b>, bevor Sie sie in die Produktion verschieben.</td><td></td> 
</tr>
</table>


## Web SDK-Erweiterung

Ein allgemeiner Überblick über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mithilfe des Workflows Web SDK-Erweiterung , wie in diesem Abschnitt beschrieben.](../../assets/websdk-extension-annotated.png)

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
<td><b>Erstellen Sie eine Datenschicht</b>, um das Tracking der Daten auf Ihrer Website zu verwalten.</td>
<td><a href="../../prepare/data-layer.md">Datenschicht erstellen</a></td>
</tr>

<tr>
<td>4</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datenstrom stellt die Server-seitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de">Konfigurieren eines Datenstroms<a></td> 
</tr>

<tr>
<td>5</td> 
<td><b>Fügen Sie einen Adobe Analytics-Service</b> in Ihrem Datenstrom hinzu. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden und an welche Report Suite(s) speziell.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de#analytics">Hinzufügen des Adobe Analytics-Service zu einem Datenstrom</a></td>
</tr>

<tr>
<td>6</td>
<td><b>Erstellen Sie eine Tag-Eigenschaft</b>. Eigenschaften sind übergreifende Container, die zum Verweisen auf Tag-Management-Daten verwendet werden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=de#for-web">Erstellen oder Konfigurieren einer Tag-Eigenschaft für das Web</a></td>
</tr>

<tr>
<td>7</td> 
<td><b>Installieren und konfigurieren Sie die Web SDK-Erweiterung</b> in Ihrer Tag-Eigenschaft. Konfigurieren Sie die Web SDK-Erweiterung, um Daten an den in Schritt 4 konfigurierten Datenstrom zu senden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/sdk/overview.html?lang=de">Adobe Experience Platform Web SDK-Erweiterung – Übersicht</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Iterieren, validieren und veröffentlichen Sie</b> in der Produktionsumgebung. Betten Sie Code ein, um Ihre Tag-Eigenschaft in die Seiten Ihrer Website aufzunehmen. Verwenden Sie dann Datenelemente, Regeln usw., um Ihre Implementierung anzupassen.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?lang=en#embed-code">Einbettungscode</a><br/><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=de">Veröffentlichungsübersicht</a></td>
</tr>

</table>


## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Adobe Experience Platform Web SDK-Dokumentation](https://experienceleague.adobe.com/docs/web-sdk.html?lang=de)
