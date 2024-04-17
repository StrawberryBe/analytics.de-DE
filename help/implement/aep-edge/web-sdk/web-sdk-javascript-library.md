---
title: Senden von Daten an Adobe Analytics mithilfe der Web SDK-JavaScript-Bibliothek
description: Beginnen Sie mit einer sauberen Web SDK-Implementierung, um mithilfe der JavaScript-Bibliothek Daten an Adobe Analytics zu senden.
hide: true
hidefromtoc: true
source-git-commit: d6c16d8841110e3382248f4c9ce3c2f2e32fe454
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 18%

---

# Senden von Daten an Adobe Analytics mithilfe der Web SDK-JavaScript-Bibliothek

Dieser Implementierungspfad umfasst eine neue Web SDK-Installation unter Verwendung der Web SDK JavaScript-Bibliothek. Andere Implementierungspfade werden auf separaten Seiten behandelt:

* [Web SDK-Tag-Erweiterung](web-sdk-tag-extension.md): Eine neue Web SDK-Installation mit der Web SDK-Tag-Erweiterung. Ähnlich wie der JavaScript-Bibliotheksansatz des Web SDK (diese Seite), mit dem Unterschied, dass Sie die Implementierung mit Tags in der Adobe Experience Platform-Datenerfassung verwalten. Dazu ist die Adobe Analytics ExperienceEvent-Feldergruppe erforderlich, die typische Analytics-Variablen enthält, die in Ihr XDM-Schema aufgenommen werden sollen.
* [Analytics-Erweiterung auf Web SDK-Erweiterung](analytics-extension-to-web-sdk.md): Verwenden Sie einen reibungslosen und methodischen Ansatz, um von der Adobe Analytics-Tag-Erweiterung zur Web SDK-Tag-Erweiterung zu wechseln. Dieser Ansatz unterdrückt die Notwendigkeit, XDM zu verwenden, bis Ihr Unternehmen für die Verwendung von Adobe Experience Platform-Diensten wie Customer Journey Analytics bereit ist. Verwenden Sie die `data` -Objekt anstelle des `xdm` -Objekt zum Senden von Daten an Adobe.
* [AppMeasurement zur JavaScript-Bibliothek des Web SDK](appmeasurement-to-web-sdk.md): Ein reibungsloser und methodischer Ansatz für die Migration zum Web SDK, mit der Ausnahme, dass keine Tags verwendet werden. Stattdessen können Sie die Adobe Analytics-Datenerfassungsbibliothek (`AppMeasurement.js`) und ersetzen Sie sie durch die JavaScript-Bibliothek des Web SDK (`alloy.js`).

## Vorteile und Nachteile dieses Implementierungspfads

Die Verwendung der JavaScript-Bibliothek des Web SDK zum Senden von Daten an Adobe Analytics hat sowohl Vor- als auch Nachteile. Legen Sie bei jeder Option sorgfältig ab, welcher Ansatz für Ihr Unternehmen am besten geeignet ist.

| Vorteile | Nachteile |
| --- | --- |
| <ul><li>**Direkter Ansatz**: Dieser Implementierungspfad ist einfacher als Ansätze, die vorhandene Adobe Analytics-Implementierungen verschieben. Wenn Sie keine aktuelle Adobe Analytics-Implementierung haben, um die Sie sich Sorgen machen müssen, füllen Sie die entsprechenden Web SDK-XDM-Felder aus.</li><li>**Vordefiniertes Schema**: Wenn Ihr Unternehmen kein eigenes Schema benötigt, können Sie einfach das für Adobe Analytics geeignete Schema verwenden. Dieses Konzept gilt auch bei der Umstellung auf Customer Journey Analytics. Das Konzept der Props und eVars gilt nicht für Customer Journey Analytics, Sie können aber Props und eVars weiterhin als einfache benutzerdefinierte Dimensionen verwenden.</li></ul> | <ul><li>**Implementierungsänderungen erfordern eine Intervention von Entwicklern**: Wenn Sie Änderungen an Ihrer Web SDK-Implementierung vornehmen möchten, müssen Sie sich an Ihr Entwicklungsteam wenden, um den Code auf Ihrer Site zu bearbeiten. Der Ansatz, der die [Web SDK-Tag-Erweiterung](web-sdk-tag-extension.md) vermeidet diesen Nachteil.</li><li>**Verwendung eines bestimmten Schemas blockiert**: Wenn Ihr Unternehmen zu Customer Journey Analytics wechselt, müssen Sie das Adobe Analytics-Schema weiterhin verwenden oder zum Schema Ihres eigenen Unternehmens migrieren (bei dem es sich um einen separaten Datensatz handelt). Wenn Ihr Unternehmen beim Wechsel zu Customer Journey Analytics sowohl das Adobe Analytics-Schema als auch die Migration zu einem separaten Datensatz vermeiden möchte, empfiehlt Adobe eine der beiden folgenden Methoden:</li><ul><li>Verwenden Sie die `data` -Objekt: Die `data` -Objekt können Sie Daten an Adobe Analytics senden, ohne ein XDM-Schema zu erfüllen. Nachdem das Schema Ihres Unternehmens erstellt wurde, können Sie die Zuordnung mithilfe der Datastream-Zuordnung vornehmen `data` -Objektfelder in XDM. Beide [Analytics-Erweiterung auf Web SDK-Erweiterung](analytics-extension-to-web-sdk.md) und [AppMeasurement zur JavaScript-Bibliothek des Web SDK](appmeasurement-to-web-sdk.md) Verwenden Sie diese `data` -Objekt.</li><li>Adobe Analytics vollständig überspringen: Wenn Sie das Web SDK implementieren, können Sie diese Daten zur Verwendung in Customer Journey Analytics an einen Datensatz in Adobe Experience Platform senden. Sie können ein beliebiges Schema verwenden. Adobe Analytics ist an diesem Workflow überhaupt nicht beteiligt und benötigt daher keine Adobe Analytics ExperienceEvent-Feldergruppe. Bei dieser Methode entsteht der geringste technische Schuldenstand, aber auch Adobe Analytics wird vollständig ausgeschlossen.</li></ul></ul> |

>[!CAUTION]
>
>Für diese Implementierungsmethode müssen Sie ein für Adobe Analytics konfiguriertes Schema verwenden. Wenn Ihr Unternehmen in Zukunft Ihr eigenes Schema mit Customer Journey Analytics verwenden möchte, kann die Verwendung des Adobe Analytics-Schemas für Datenadministratoren oder Architekten Verwirrung stiften. Es gibt mehrere Möglichkeiten, dieses Hindernis zu beheben:
>
>* Sie können das Adobe Analytics-Schema in CJA verwenden. Beachten Sie, dass CJA kein Konzept von Props oder eVars hat. Sie werden wie jedes andere Schemafeld behandelt. Beachten Sie außerdem, dass die Verwendung des Adobe Analytics-Schemas in CJA die Verwendung anderer Plattformdienste wie Adobe Journey Optimizer oder Real-time Customer Data Platform erschweren kann.
>* Sie können das Datenobjekt ähnlich einem Migrations-Workflow verwenden. Beachten Sie, dass die Verwendung des Datenobjekts erfordert, dass Sie jedes Datenobjektfeld einem XDM-Schemafeld zuordnen.
>* Sie können die Adobe Analytics-Implementierung vollständig überspringen und Daten mithilfe Ihres eigenen Schemas an Adobe Experience Platform senden. Dieser Ansatz ist langfristig ideal und ermöglicht es Ihrem Unternehmen, mit der Verwendung von Customer Journey Analytics zu beginnen.

## Schritte, die zur Implementierung der Web SDK-JavaScript-Bibliothek erforderlich sind

Ein allgemeiner Überblick über die Implementierungsaufgaben:

![Implementieren von Adobe Analytics mit dem Web SDK-Workflow, wie in diesem Abschnitt beschrieben.](../../assets/websdk-annotated.png)

<table style="width:100%">

<tr>
<th style="width:5%"></th><th style="width:60%"><b>Aufgabe</b></th><th style="width:35%"><b>Weitere Informationen</b></th>
</tr>

<tr>
<td>1</td>
<td>Stellen Sie sicher, dass Sie <b>eine Report Suite definiert haben</b>.</td>
<td><a href="/help/admin/admin/c-manage-report-suites/report-suites-admin.md">Report Suite Manager</a></td>
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
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/library.html">Installieren der vordefinierten eigenständigen Version</a> und <a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/install/npm.html">Verwenden des NPM-Pakets</a></td>
</tr>

<tr>
<td>5</td>
<td><b>Konfigurieren eines Datenstroms</b>. Ein Datenstrom stellt die Server-seitige Konfiguration bei der Implementierung des Adobe Experience Platform Web SDK dar.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de">Konfigurieren eines Datenstroms<a></td> 
</tr>

<td>6</td>
<td><b>Fügen Sie einen Adobe Analytics-Service</b> in Ihrem Datenstrom hinzu. Dieser Dienst steuert, ob und wie Daten an Adobe Analytics gesendet werden und an welche Report Suite(s) speziell.</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html#analytics">Hinzufügen des Adobe Analytics-Service zu einem Datenstrom</a></td>
</tr>

<tr>
<td>7</td>
<td><b>Konfigurieren des Web SDKs</b>. Stellen Sie sicher, dass die Bibliothek, die Sie in Schritt 4 installiert haben, ordnungsgemäß mit der Datastraam-ID konfiguriert ist (ehemals Edge-Konfigurations-ID (<code>edgeConfigId</code>), Organisations-ID (<code>orgId</code>) und anderen verfügbaren Optionen. Stellen Sie sicher, dass Variablen ordnungsgemäß zugeordnet werden. </td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/configure/overview.html">Web SDK konfigurieren</a><br/><a href="../xdm-var-mapping.md">XDM-Objektvariablenzuordnung</a></td>
</tr>

<tr>
<td>8</td>
<td><b>Führen Sie Befehle aus</b> und/oder <b>verfolgen Sie Ereignisse</b>. Nachdem der Basis-Code auf Ihrer Web-Seite implementiert wurde, können Sie mit der Ausführung von Befehlen und dem Nachverfolgen von Ereignissen mit dem SDK beginnen.
</td>
<td><a href="https://experienceleague.adobe.com/docs/experience-platform/web-sdk/commands/sendevent/overview.html">Ereignisse senden</a></td>
</tr>

<tr>
<td>9</td><td><b>Erweitern und validieren Sie die Implementierung</b>, bevor Sie sie in die Produktion verschieben.</td><td></td> 
</tr>
</table>