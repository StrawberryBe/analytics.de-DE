---
title: Fehlerbehebung bei der Activity Map-Datenerfassung
description: Ermitteln Sie, warum in Bildanforderungen keine Activity Map-Daten angezeigt werden.
feature: Activity Map
role: User, Admin
exl-id: 7f9e06ba-4040-483b-b18b-cdfe85bca486
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# Fehlerbehebung bei der Activity Map-Datenerfassung

Wenn keine Daten für Activity Map-Dimensionen angezeigt werden, können Sie auf dieser Seite anhand der Gründe ermitteln.

## Bestätigen der Datenerfassung mit dem Debugger

Stellen Sie zunächst sicher, dass AppMeasurement Activity Map-Daten korrekt erfasst.

1. Laden Sie die [Adobe Experience Cloud Debugger Chrome-Erweiterung](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de).
2. Navigieren Sie zu Ihrer Webseite und klicken Sie auf einen Link.
3. Wenn die nachfolgende Seite geladen wird, öffnen Sie den Debugger. Überprüfen Sie, ob Sie Activity Map-Kontextdatenvariablen sehen, die zwischen `activitymap.` und `.activitymap`:

![Debugger-Daten](assets/debugger.png)

## Mögliche Gründe, warum keine Activity Map-Daten vorhanden sind

Überprüfen Sie alle folgenden Punkte, um sicherzustellen, dass Activity Map-Komponenten vorhanden sind:

* **AppMeasurement-Version**: Activity Map wird ab Version 1.6 unterstützt. Bei einem Upgrade auf die neueste stabile Version von AppMeasurement werden viele Probleme mit den Randfällen behoben.
* **Activity Map-Modul**: Überprüfen Sie, ob die `AppMeasurement_Module_Activity_Map` -Modul in Ihrer `AppMeasurement.js` -Datei. Wenn Ihre Implementierung zur Datenerfassung mit Adobe Experience Platform arbeitet, stellen Sie sicher, dass **[!UICONTROL ClickMap aktivieren]** wird bei der Konfiguration der Analytics-Erweiterung unter **[!UICONTROL Linktracking]**.
* **Die `s_sq` Cookie**: Activity Map hängt von der `s_sq` Cookie für die Datenerfassung.
   * Stellen Sie sicher, dass die Variable `cookieDomainPeriods` korrekt festgelegt ist, insbesondere für regionale Domänen wie `*.co.uk` oder `*.co.jp`.
   * Stellen Sie sicher, dass die Variable `linkInternalFilters` auf die gewünschten Werte eingestellt ist. Wenn ein angeklickter Link nicht mit internen Filtern übereinstimmt, betrachtet Activity Map ihn als Exitlink und erfasst keine Daten.
* **Activity Map-Overlay wird ausgeführt**: AppMeasurement verfolgt keine Klickdaten für Ihre Webseite, wenn die Activity Map-Überlagerung aktiviert ist.
