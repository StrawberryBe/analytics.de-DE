---
title: Verwenden von XDM-Daten mit Analytics
description: Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics
feature: AEP Edge
exl-id: 6f1282fb-8d4a-4d88-9be0-1c939c22cb92
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 100%

---

# Verwenden von Adobe Experience Platform Edge-Daten mit Analytics

Sie können das [Adobe Experience Platform (AEP) Web SDK](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html?lang=de) verwenden, um Daten an Adobe Analytics zu senden. Dies funktioniert durch die Übersetzung des [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de) in ein von Analytics verwendetes Format.

Analytics erfasst XDM-Daten auf zwei Arten:

* Automatische Zuordnung von XDM-Schemas
* Manuelle Zuordnung zu Kontextdaten

## Automatische Zuordnung

Die automatische Zuordnung beruht auf einem Standard-[Schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de) in XDM, mit dem JSON-Objekte automatisch befüllt werden, die normalerweise in der Analytics-Datenerfassung enthalten sind. Die Analytics-Variablen, die automatisch von XDM Ihren konfigurierten Report Suites zugeordnet werden, benötigen zur Integration keine Hilfe von Entwicklern. Siehe [Automatisch zugeordnete Variablen in Analytics](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/adobe-analytics/automatically-mapped-vars.html?lang=de) im Platform Web SDK-Benutzerhandbuch.

## Manuelle Zuordnung

[Die manuelle Zuordnung von XDM-Daten](xdm-manual.md) zu Analytics beruht auf [Analytics-Kontextdatenvariablen](../vars/page-vars/contextdata.md). Diese Variablen werden in JSON-Objekte eingefügt, die den jeweiligen Schemas entsprechen. In der Regel fügt Ihr Entwicklungsteam Kontextdaten bei der Implementierung hinzu und die Administratoren legen dann [Verarbeitungsregeln](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) fest, um diese Daten auf bestimmte Report Suites anzuwenden.

## Einrichten

So richten Sie Analytics für den Empfang von XDM-Daten ein:

1. Installieren und [konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=de).

2. Stellen Sie sicher, dass die entsprechenden Report Suites den gewünschten Daten zugeordnet sind. XDM-Daten werden automatisch von der Adobe Experience-Plattform in die Report Suite übertragen.
