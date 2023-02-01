---
title: Implementieren von Adobe Analytics mit der Analytics-Erweiterung
description: Erfahren Sie, wie Sie Adobe Analytics mithilfe von Tags und der Analytics-Erweiterung implementieren
feature: Launch Implementation
source-git-commit: aef1d613437688b7eed704b227c41e4fbe4677dd
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 58%

---

# Implementieren von Adobe Analytics mit der Analytics-Erweiterung

Während der gesamten Lebensdauer von Adobe Analytics hat Adobe verschiedene Methoden zur Implementierung von Code für die Datenerfassung auf Ihrer Website angeboten. Die derzeit empfohlene Methode von Adobe erfolgt über -Tags in Adobe Experience Platform.

Tags in Adobe Experience Platform ist eine Tag-Management-Lösung, mit der Sie Analytics-Code bereitstellen und weitere Tagging-Vorgaben erfüllen können. Adobe bietet Integrationen mit anderen Lösungen und Produkten und ermöglicht die Bereitstellung von benutzerdefiniertem Code. Alle diese Aufgaben können ausgeführt werden, ohne dass Entwicklungsteams in Ihrer Organisation Code auf Ihrer Website aktualisieren müssen.

Alle Kunden mit einem aktiven Adobe Experience Cloud-Vertrag können Tags verwenden. Wenn Sie sich nicht sicher sind, ob Sie Zugriff haben, wenden Sie sich an einen Experience Cloud-Systemadministrator Ihres Unternehmens.

Eine allgemeine Übersicht über die Implementierungsaufgaben:



![Adobe Analytics mithilfe des Workflows für die Analytics-Erweiterung](../assets/analytics-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td> 1</td>
<td>Stellen Sie sicher, dass <b>Report Suite definiert haben</b>.</td>
<td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Erstellen einer Datenschicht</b>um das Tracking der Daten auf Ihrer Website zu verwalten.</td>
<td>
<a href="../prepare/data-layer.md">Datenschicht erstellen</a>
</td>
</tr>

<tr>
<td>3</td>
<td><b><b>Tag-Eigenschaft erstellen</b>. Eigenschaften sind übergreifende Container, die zum Verweisen auf Tag Management-Daten verwendet werden.</td>
<td><a ref="../launch/create-analytics-property.md">Erstellen einer Tag-Eigenschaft in Adobe Analytics</a></td>
</tr>

<tr>
<td>4</td><td><b>Installieren der Analytics-Erweiterung</b> in der Tag-Eigenschaft. Konfigurieren Sie die Analytics-Erweiterung, um Daten an Adobe Analytics zu senden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=en">Adobe Analytics-Erweiterung – Übersicht</a></td>
</tr>

<tr>
<td>5</td>
<td><b>In einer Entwicklungsumgebung bereitstellen</b>. Verwenden Sie eine Umgebung, in der Sie die Entwicklung von Tags iterieren können.</td>
<td><a href="./deploy-dev.md">Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen</td>
</tr>

<tr>
<td>6</td> 
<td><b>Validieren und Veröffentlichen in der Produktionsumgebung</b>. Fügen Sie die Tag-Eigenschaft Ihrer Website hinzu. Verwenden Sie dann Datenelemente, Regeln usw., um Ihre Implementierung anzupassen.</td>
<td><a href="./validate-publish-prod.md">Entwicklungsimplementierung validieren und in der Produktion veröffentlichen</a></td>
</tr>

</table>

## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Implementierungsvariablen](../vars/overview.md): Legen Sie fest, welche Variablen Sie an Datenerfassungs-Server senden möchten.
