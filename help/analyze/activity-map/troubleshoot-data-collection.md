---
title: Fehlerbehebung bei der Activity Map-Datenerfassung
description: Bestimmen Sie, warum Activity Map-Daten in Bildanforderungen nicht angezeigt werden können.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 3%

---


# Fehlerbehebung bei der Activity Map-Datenerfassung

Wenn Sie keine Daten zu Activity Map-Dimensionen sehen, verwenden Sie diese Seite, um herauszufinden, warum.

## Datenerfassung mit dem Debugger bestätigen

Vergewissern Sie sich zunächst, dass AppMeasurement Activity Map-Daten richtig erfasst.

1. Download and install the [Adobe Experience Cloud Debugger Chrome Extension](https://docs.adobe.com/content/help/de-DE/debugger/using/experience-cloud-debugger.html).
2. Navigieren Sie zu Ihrer Webseite und klicken Sie dann auf einen Link.
3. Wenn die nachfolgende Seite geladen wird, öffnen Sie den Debugger. Überprüfen Sie, ob die Activity Map Kontextdatenvariablen angezeigt werden, die zwischen `activitymap.` und `.activitymap`:

![Debugging-Daten](assets/debugger.png)

## Mögliche Gründe, warum keine Activity Map-Daten vorhanden sind

Überprüfen Sie, ob Activity Map-Komponenten vorhanden sind:

* **AppMeasurement-Version**: Activity Map wird ab Version 1.6 unterstützt. Bei der Aktualisierung auf die neueste stabile Version von AppMeasurement wurden zahlreiche Fallfehler behoben.
* **Activity Map-Modul**: Überprüfen Sie, ob das `AppMeasurement_Module_Activity_Map` Modul in Ihrer `AppMeasurement.js` Datei vorhanden ist. Wenn Ihre Implementierung Adobe Experience Platform Launch verwendet, vergewissern Sie sich, dass bei der Konfiguration der Analytics-Erweiterung unter &quot; **[!UICONTROL Link-Verfolgung]** &quot;die Option &quot;ClickMap **** aktivieren&quot;aktiviert ist.
* **Das`s_sq`Cookie**: Activity Map hängt von dem `s_sq` Cookie für die Datenerfassung ab.
   * Achten Sie darauf, dass die `cookieDomainPeriods` Variable korrekt eingestellt ist, insbesondere für regionale Domänen wie `*.co.uk` oder `*.co.jp`.
   * Stellen Sie sicher, dass die `linkInternalFilters` Variable auf die gewünschten Werte eingestellt ist. Wenn ein angeklickter Link nicht mit internen Filtern übereinstimmt, betrachtet Activity Map ihn als Ausstiegslink und erfasst keine Daten.
* **Activity Map-Überlagerung ausgeführt**: AppMeasurement verfolgt keine Klickdaten für Ihre Webseite, wenn die Activity Map-Überlagerung aktiviert ist.
