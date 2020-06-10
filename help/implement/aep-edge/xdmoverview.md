---
title: Verwenden von XDM-Daten mit Analytics
description: 'Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics '
translation-type: tm+mt
source-git-commit: a28a05047e95d12343fd94f7b11e5cabf7fac070
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 4%

---


# Verwenden von Adobe Experience Platform Edge-Daten mit Analytics

Sie können das [Adobe Experience Platform (AEP) Web SDK](https://docs.adobe.com/content/help/de-DE/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html) verwenden, um Daten an Adobe Analytics zu senden. Dies funktioniert durch die Übersetzung des [Experience Data Model (XDM)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) in ein von Analytics verwendetes Format.

Analytics erfasst XDM-Daten auf zwei Arten:

* Automatische Zuordnung von XDM-Schemas
* Manuelle Zuordnung zu Kontextdaten

## Automatische Zuordnung

[Die automatische Zuordnung](xdm-manual.md) beruht auf einem Standard- [Schema](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) im XDM, mit dem automatisch JSON-Objekte gefüllt werden, die in der typischen Analytics-Datenerfassung enthalten sind. Für die Analytics-Variablen, die automatisch von XDM zu Ihren konfigurierten Report Suites zugeordnet werden, ist keine Entwicklerunterstützung erforderlich, um sie zu integrieren.

## Manuelle Zuordnung

Die manuelle Zuordnung von XDM-Daten zu Analytics beruht auf [Analytics-Kontextdatenvariablen](../vars/page-vars/contextdata.md) . Diese Variablen werden in JSON-Objekte eingefügt, die den entsprechenden Schemas entsprechen. In der Regel fügt Ihr Entwicklungsteam Kontextdaten bei der Implementierung hinzu und legt dann [Verarbeitungsregeln](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md) fest, um diese Daten auf bestimmte Report Suites anzuwenden.

## Einrichten

So richten Sie Analytics für den Empfang von XDM-Daten ein:

1. Installieren und [konfigurieren](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/configuring-the-sdk.html) Sie das [Adobe Experience Platform Web SDK](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. Stellen Sie sicher, dass die entsprechenden Report Suites den gewünschten Daten zugeordnet sind. XDM-Daten fließen automatisch von der Adobe Experience-Plattform in die Report Suite.
