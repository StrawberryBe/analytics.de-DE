---
title: Fehlerbehebung bei der Activity Map-Datenerfassung
description: Ermitteln Sie, warum in Bildanforderungen keine Activity Map-Daten angezeigt werden.
feature: Activity Map
role: User, Admin
exl-id: 7f9e06ba-4040-483b-b18b-cdfe85bca486
source-git-commit: e6f3beadfba340cea07f5fd2694105ad31de9751
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---

# Fehlerbehebung bei der Activity Map-Datenerfassung

Wenn keine Daten für Activity Map-Dimensionen angezeigt werden, können Sie auf dieser Seite anhand der Gründe ermitteln.

## Bestätigen der Datenerfassung mit dem Debugger

Stellen Sie zunächst sicher, dass AppMeasurement Activity Map-Daten korrekt erfasst.

1. Laden Sie die Chrome-Erweiterung [Adobe Experience Cloud Debugger ](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de) herunter und installieren Sie sie.
2. Navigieren Sie zu Ihrer Webseite und klicken Sie auf einen Link.
3. Wenn die nachfolgende Seite geladen wird, öffnen Sie den Debugger. Überprüfen Sie, ob Sie Activity Map-Kontextdatenvariablen sehen, die zwischen `activitymap.` und `.activitymap` unterteilt sind:

![Debugger-Daten](assets/debugger.png)

## Mögliche Gründe, warum keine Activity Map-Daten vorhanden sind

Überprüfen Sie alle folgenden Punkte, um sicherzustellen, dass Activity Map-Komponenten vorhanden sind:

* **AppMeasurement-Version**: Activity Map wird ab Version 1.6 unterstützt. Bei einem Upgrade auf die neueste stabile Version von AppMeasurement werden viele Probleme mit den Randfällen behoben.
* **Activity Map-Modul**: Überprüfen Sie, ob das  `AppMeasurement_Module_Activity_Map` Modul in Ihrer  `AppMeasurement.js` Datei vorhanden ist. Wenn Ihre Implementierung die Adobe Experience Platform-Datenerfassung (Launch) verwendet, stellen Sie sicher, dass **[!UICONTROL Enable ClickMap]** bei der Konfiguration der Analytics-Erweiterung unter **[!UICONTROL Linktracking]** aktiviert ist.
* **Das  `s_sq` Cookie**: Activity Map hängt von dem  `s_sq` Cookie für die Datenerfassung ab.
   * Stellen Sie sicher, dass die Variable `cookieDomainPeriods` richtig eingestellt ist, insbesondere für regionale Domänen wie `*.co.uk` oder `*.co.jp`.
   * Stellen Sie sicher, dass die Variable `linkInternalFilters` auf die gewünschten Werte eingestellt ist. Wenn ein angeklickter Link nicht mit internen Filtern übereinstimmt, betrachtet Activity Map ihn als Exitlink und erfasst keine Daten.
* **Activity Map-Overlay wird ausgeführt**: AppMeasurement verfolgt keine Klickdaten für Ihre Webseite, wenn die Activity Map-Überlagerung aktiviert ist.
