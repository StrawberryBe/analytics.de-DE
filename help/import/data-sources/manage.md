---
title: Datenquellen verwalten
description: Navigieren Sie zur Benutzeroberfläche zum Verwalten von Datenquellen .
source-git-commit: e32a7c85e2f0629c04bcd7ed0fa80ec1593bb6e8
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 2%

---

# Datenquellen verwalten

Verwenden Sie den Datenquellen-Manager, um Datenquellen zu erstellen, zu bearbeiten oder zu deaktivieren. Sie können diese Benutzeroberfläche auch verwenden, um den Status von Dateien zu verfolgen, die an FTP-Speicherorte für Datenquellen hochgeladen wurden.

**[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenquellen]**

Verwenden Sie die Report Suite-Auswahl oben rechts, um zwischen Report Suites in Ihrer Organisation zu wechseln.

Diese Benutzeroberfläche verfügt über drei Hauptregisterkarten. **[!UICONTROL Verwalten]**, **[!UICONTROL Erstellen]** und **[!UICONTROL Dateiprotokoll]**.

## Verwalten

Die **[!UICONTROL Verwalten]** -Registerkarte verarbeitet alle Datenquellen, die Ihr Unternehmen erstellt hat. Sie können FTP-Informationen anzeigen, Änderungen an Variablen vornehmen, die in Vorlagendateien verwendet werden, oder Datenquellen vollständig deaktivieren.

![Verwalten](assets/manage.png)

Die oberste Datenquelle ist immer [!UICONTROL Webbeacon]. Diese Datenquelle wird für die typische Datenerfassung über AppMeasurement verwendet. Sie kann nicht bearbeitet oder deaktiviert werden.

Jede Datenquelle verfügt über die folgenden Optionen:

* **[!UICONTROL Verarbeitung neu starten]**: Startet die Verarbeitung der Datenquelle neu, die zuvor aufgrund von Fehlern angehalten wurde. Die Verarbeitung wird fortgesetzt, bis der nächste Fehler erkannt wird. Data Sources stoppt die Verarbeitung einer Data Sources-Datei nur bei Auswahl von **[!UICONTROL Verarbeitung von Fehlern stoppen]**.
* **[!UICONTROL Verarbeitung abschließen]**: Wird nicht mehr verwendet - diese Schaltfläche wird nur für [Datenquellen mit vollständiger Verarbeitung](full-processing-eol.md).
* **[!UICONTROL Verarbeitung von Fehlern stoppen]**: Ein Kontrollkästchen, das den Verarbeitungsserver anweist, bei einem Fehler anzuhalten. Die Verarbeitung der Datenquelle wird erst fortgesetzt, wenn Sie **[!UICONTROL Verarbeitung neu starten]**. Wenn bei einer Datenquelle ein Dateifehler auftritt, werden Sie über den Fehler benachrichtigt. Adobe verschiebt die Datei mit dem Fehler in einen Ordner namens `files_with_errors` auf dem FTP-Server. Nachdem Sie das Problem behoben haben, senden Sie die Datei erneut zur Verarbeitung.
* **[!UICONTROL Konfigurieren]**: Ein Link, der Sie durch den Erstellungsassistenten für Datenquellen für diese Datenquelle führt. Mit diesem Assistenten können Sie die Datenquelle umbenennen oder die automatisch beim Herunterladen einer Vorlagendatei eingeschlossenen Variablen neu konfigurieren.
* **[!UICONTROL FTP-Info]**: Ein Link, der Sie zum letzten Schritt des Datenquellen-Erstellungsassistenten führt, in dem FTP-Anmeldeinformationen angezeigt werden.

Sobald eine Datenquelle Daten erhält, wird eine Tabelle mit mehreren Spalten für die hochgeladenen Dateien angezeigt.

* **[!UICONTROL Dateien in der Verarbeitungswarteschlange]**: Der Name der Datei.
* **[!UICONTROL Zeilen]**: Die Gesamtanzahl der Zeilen in der Datei.
* **[!UICONTROL Fehler]**: Die Anzahl der Zeilen, die Fehler enthielten und nicht erfasst werden konnten.
* **[!UICONTROL Warnungen]**: Die Anzahl der Zeilen, die Warnungen enthielten.
* **[!UICONTROL Erhalten]**: Der Zeitstempel, mit dem die Datei in der Zeitzone der Report Suite empfangen wurde.
* **[!UICONTROL Status]**: Der Status der Datei (`Success` oder `Failed`).

## Erstellen

Die **[!UICONTROL Erstellen]** -Tab bietet Ihnen einen Ausgangspunkt für den Assistenten zur Datenquellen-Erstellung.

![Erstellen](assets/create.png)

Die Kategorie und der Typ der Datenquelle waren in früheren Versionen von Adobe Analytics wertvoller. Sie haben jedoch weiterhin nur eingeschränkte Verwendung:

* Der Datenquellentyp wird auf der Seite [Verwalten](#manage) für die Datenquelle selbst und die [Dateiprotokoll](#file-log) für jede einzelne Datei.
* Einige Datenquellentypen enthalten beim Herunterladen der Vorlagendatei automatisch Variablen. Sie können jedoch jede verfügbare Dimension oder Metrik einbeziehen, sofern sie der festgelegten [Dateiformat](file-format.md).

Über diese Gründe hinaus sind alle Datenquellen-Kategorien und -Typen, die Sie auswählen können, effektiv identisch. Wählen Sie die Kategorie und den Typ aus, die Ihren Zweck für die Verwendung von Datenquellen am besten widerspiegeln.

Mit dem Ausscheiden aus dem [Datenquellen mit vollständiger Verarbeitung](full-processing-eol.md), können mehrere Kategorien und Typen nicht ausgewählt werden. Wenn Sie einen Datenquellentyp mit vollständiger Verarbeitung auswählen, wird die **[!UICONTROL Aktivieren]** Schaltfläche ausgegraut ist.

## Dateiprotokoll

Die **[!UICONTROL Dateiprotokoll]** bietet eine aggregierte Ansicht aller Datenquellendateien, die für die jeweilige Report Suite hochgeladen wurden.

![Dateiprotokoll](assets/file-log.png)

Es steht eine Suchleiste zur Verfügung, die Ihnen beim Suchen nach einer bestimmten Datenquelle hilft. Die Tabelle enthält die folgenden Spalten:

* **[!UICONTROL Datenquellenname]**: Der Name der Datenquelle.
* **[!UICONTROL Typ]**: Der Typ der Datenquelle.
* **[!UICONTROL Dateiname]**: Der Name der hochgeladenen Datei.
* **[!UICONTROL Zeilen]**: Die Gesamtanzahl der Zeilen in der Datei.
* **[!UICONTROL Fehler]**: Die Anzahl der Zeilen, die Fehler enthielten.
* **[!UICONTROL Warnungen]**: Wird nicht mehr verwendet. Die Anzahl der Zeilen, die Warnungen enthielten.
* **[!UICONTROL Erhalten]**: Datum und Uhrzeit des Zeitpunkts, zu dem die Dateiverarbeitung durch die Adobe gestartet wurde.
* **[!UICONTROL Status]**: Der Dateistatus (`Success` oder `Failed`).
