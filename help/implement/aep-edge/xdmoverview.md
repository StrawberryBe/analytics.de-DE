---
title: Verwenden von XDM-Daten mit Analytics
description: 'Übersicht über die Verwendung von XDM-Daten aus Experience Platform in Adobe Analytics '
translation-type: tm+mt
source-git-commit: 31efa43043120b68de90e817a7980addbe2ded39

---




# Verwenden von Adobe Experience Platform Edge-Daten mit Analytics

>[!IMPORTANT]
>
>Das Adobe Experience Edge Web SDK wird nicht veröffentlicht und steht nur für Beta-Tests bei eingeladenen Kunden zur Verfügung. Diese Dokumentation ist nur für Beta-Benutzer gedacht und enthält keine vollständige Beschreibung aller Funktionen. Wenn Sie Interesse haben, die App als Beta-Benutzer zu verwenden, wenden Sie sich an die Adobe-[Kundenunterstützung](https://helpx.adobe.com/de/contact/enterprise-support.ec.html).


Sie können das [Adobe Experience Platform (AEP) Web SDK](https://docs.adobe.com/content/help/de-DE/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html) verwenden, um Daten an Adobe Analytics zu senden. Dies funktioniert durch die Übersetzung des [Experience Data Model (XDM)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) in ein von Analytics verwendetes Format.

Analytics erfasst XDM-Daten auf zwei Arten:

* Automatische Zuordnung von XDM-Schemas

* Manuelle Zuordnung zu Kontextdaten

## Automatische Zuordnung

Die automatische Zuordnung beruht auf einem Standard- [Schema](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) im XDM, mit dem JSON-Objekte automatisch gefüllt werden, die in der typischen Analytics-Datenerfassung enthalten sind. Die [Analytics-Variablen, die automatisch von den XDM](https://git.corp.adobe.com/analytics-data-collection/anedge/blob/master/XDM_Translator.md) zu Ihren konfigurierten Report Suites zugeordnet werden, benötigen keine Unterstützung von Entwicklern, um sie zu integrieren.

## Manuelle Zuordnung

Die manuelle Zuordnung von XDM-Daten zu Analytics beruht auf [Analytics-Kontextdatenvariablen](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) . Diese Variablen werden in JSON-Objekte eingefügt, die den entsprechenden Schemas entsprechen. In der Regel fügt Ihr Entwicklungsteam Kontextdaten bei der Implementierung hinzu und legt dann [Verarbeitungsregeln](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/processing-rules/processing-rules-configuration/t-processing-rules.html) fest, um diese Daten auf bestimmte Report Suites anzuwenden.


## Einrichten

So richten Sie Analytics für den Empfang von XDM-Daten ein:

1. Installieren und [konfigurieren](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/configuring-the-sdk.html) Sie das [Adobe Experience Platform Web SDK](https://docs.adobe.com/content/help/en/experience-platform/edge/fundamentals/installing-the-sdk.html).

2. Stellen Sie sicher, dass die entsprechenden Report Suites den gewünschten Daten zugeordnet sind. XDM-Daten fließen automatisch von der Adobe Experience-Plattform in die Report Suite.

