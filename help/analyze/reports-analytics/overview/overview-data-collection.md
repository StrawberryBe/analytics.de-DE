---
description: Erfahren Sie, wie Daten für Adobe Analytics gesammelt werden.
seo-description: Erfahren Sie, wie Daten für Adobe Analytics gesammelt werden.
seo-title: Über die Datenkollektion
solution: Analytics
subtopic: Erste Schritte
title: Über die Datenkollektion
topic: Reports and Analytics
uuid: 4 dd 9 a 23 d-ad 49-4841-8 f 4 c -32 c 3993851 f 2
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Über die Datenkollektion{#about-data-collection}

Erfahren Sie, wie Daten für Adobe Analytics gesammelt werden.

Jede von Adobe verfolgte Seite enthält einen kleinen Abschnitt aus JavaScript-Code, der von Adobe autorisiert wurde. Ihr Kundenbetreuer stellt diesen Code bereit.

Im Detail verläuft der Datenkollektionsprozess wie folgt:

![](assets/data_collection.png)

1. Ein Besucher besucht eine Webseite, die den Datenkollektionscode enthält.
1. Während die Seite geladen wird, sendet der Datenkollektionscode eine Image-Anforderung (als Web-Beacon bezeichnet) an die Adobe-Datenkollektionsserver. Die Image-Anforderung enthält die Daten zur Interaktion des Besuchers mit Ihrer Webseite, die Sie erfassen möchten.
1. Adobe speichert die Daten in Report Suites. Sie können sich anmelden, um auf Report Suite-Daten zuzugreifen und Berichte zur Benutzeraktivität auf Ihrer Website zu erstellen.

Die Datenkollektion erfolgt sehr schnell und beeinträchtigt die Seitenladezeiten nicht merklich. Zu den erfassten Daten zählen Seitenansichten, die durch Klicken auf die **Aktualisieren**- oder **Zurück**-Schaltflächen im Browser zustande gekommen sind. Der JavaScript-Code wird ausgeführt, selbst wenn die Seite aus dem Cache-Speicher geladen wird.

See [Data Collection in Analytics](https://marketing.adobe.com/resources/help/en_US/reference/usecase_sending_data_to_sc.html).
