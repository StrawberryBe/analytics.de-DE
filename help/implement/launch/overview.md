---
title: Implementieren von Adobe Analytics mit der Analytics-Erweiterung
description: Erfahren Sie, wie Sie Adobe Analytics mithilfe von Tags und der Analytics-Erweiterung implementieren
feature: Launch Implementation
source-git-commit: aef1d613437688b7eed704b227c41e4fbe4677dd
workflow-type: ht
source-wordcount: '364'
ht-degree: 100%

---

# Implementieren von Adobe Analytics mit der Analytics-Erweiterung

Seit dem Bestehen von Adobe Analytics hat Adobe verschiedene Methoden zur Implementierung von Code für die Datenerfassung auf Ihrer Website angeboten. Die derzeit von Adobe empfohlene Methode verwendet Tags in Adobe Experience Platform.

Tags in Adobe Experience Platform ist eine Tag-Management-Lösung, mit der Sie Analytics-Code bereitstellen und weitere Tagging-Vorgaben erfüllen können. Adobe bietet Integrationen mit anderen Lösungen und Produkten und ermöglicht die Bereitstellung von benutzerdefiniertem Code. Alle diese Aufgaben können ausgeführt werden, ohne dass Entwicklungsteams in Ihrer Organisation Code auf Ihrer Website aktualisieren müssen.

Alle Kunden mit einem aktiven Adobe Experience Cloud-Vertrag können Tags verwenden. Wenn Sie sich wissen, ob Sie Zugriff haben, wenden Sie sich an einen Systemadministrator bzw. eine Systemadministratorin für Experience Cloud in Ihrem Unternehmen.

Ein allgemeiner Überblick über die Implementierungsaufgaben:



![Workflow von Adobe Analytics mit der Analytics-Erweiterung](../assets/analytics-extension-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td> 1</td>
<td>Stellen Sie sicher, dass Sie <b>eine Report Suite definiert haben</b>.</td>
<td><a href="../../admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
</tr>

<tr>
<td>2</td>
<td><b>Erstellen Sie eine Datenschicht</b>, um das Tracking der Daten auf Ihrer Website zu verwalten</td>
<td>
<a href="../prepare/data-layer.md">Datenschicht erstellen</a>
</td>
</tr>

<tr>
<td>3</td>
<td><b><b>Erstellen Sie eine Tag-Eigenschaft</b>. Eigenschaften sind übergreifende Container, die für Verweise auf Tag-Management-Daten verwendet werden.</td>
<td><a ref="../launch/create-analytics-property.md">Erstellen einer Tag-Eigenschaft in Adobe Analytics</a></td>
</tr>

<tr>
<td>4</td><td><b>Installieren Sie die Analytics-Erweiterung</b> in der Tag-Eigenschaft. Konfigurieren Sie die Analytics-Erweiterung, um Daten an Adobe Analytics zu senden.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=de">Adobe Analytics-Erweiterung – Übersicht</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Implementierung in einer Entwicklungsumgebung</b>. Verwenden Sie eine Umgebung, in der Sie die Entwicklung von Tags iterieren können.</td>
<td><a href="./deploy-dev.md">Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen</td>
</tr>

<tr>
<td>6</td> 
<td><b>Validieren und Veröffentlichen in der Produktionsumgebung</b>. Fügen Sie die Tag-Eigenschaft zu Ihrer Website hinzu. Verwenden Sie dann Datenelemente, Regeln usw., um Ihre Implementierung anzupassen.</td>
<td><a href="./validate-publish-prod.md">Entwicklungsimplementierung validieren und in der Produktionsumgebung veröffentlichen</a></td>
</tr>

</table>

## Zusätzliche Ressourcen

Tags können in hohem Maße angepasst werden. Erfahren Sie, wie Sie Adobe Analytics optimal nutzen können, indem Sie die richtigen Daten in Ihre Implementierung aufnehmen.

- [Tags-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de#): Hier erfahren Sie, wie die Benutzeroberfläche funktioniert und welche Erweiterungen verfügbar sind.

- [Implementierungsvariablen](../vars/overview.md): Legen Sie fest, welche Variablen Sie an Datenerfassungs-Server senden möchten.
