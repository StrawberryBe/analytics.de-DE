---
description: Erfahren Sie, wie Daten für Adobe Analytics gesammelt werden.
subtopic: Get started
title: Über die Datenerfassung
uuid: 4dd9a23d-ad49-4841-8f4c-32c3993851f2
feature: Grundlagen zu Reports & Analysen
role: Business Practitioner, Administrator
exl-id: 34a7be55-519a-4e04-95a3-99b0f6e04b3e
translation-type: tm+mt
source-git-commit: cddf2a76ca36914f133379959b7cbb5246bdd695
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 98%

---

# Über die Datenerfassung

Erfahren Sie, wie Daten für Adobe Analytics gesammelt werden.

Jede von Adobe verfolgte Seite enthält einen kleinen Abschnitt aus JavaScript-Code, der von Adobe autorisiert wurde. Ihr Kundenbetreuer stellt diesen Code bereit.

Im Detail verläuft der Datenkollektionsprozess wie folgt:

![](assets/data_collection.png)

1. Ein Besucher besucht eine Webseite, die den Datenkollektionscode enthält.
1. Während die Seite geladen wird, sendet der Datenkollektionscode eine Image-Anforderung (als Web-Beacon bezeichnet) an die Adobe-Datenkollektionsserver. Die Image-Anforderung enthält die Daten zur Interaktion des Besuchers mit Ihrer Webseite, die Sie erfassen möchten.
1. Adobe speichert die Daten in Report Suites. Sie können sich anmelden, um auf Report Suite-Daten zuzugreifen und Berichte zur Benutzeraktivität auf Ihrer Website zu erstellen.

Die Datenkollektion erfolgt sehr schnell und beeinträchtigt die Seitenladezeiten nicht merklich. Zu den erfassten Daten zählen Seitenansichten, die durch Klicken auf die **Aktualisieren**- oder **Zurück**-Schaltflächen im Browser zustande gekommen sind. Der JavaScript-Code wird ausgeführt, selbst wenn die Seite aus dem Cache-Speicher geladen wird.

Siehe [Datenerfassung in Analytics](/help/import/home.md).
