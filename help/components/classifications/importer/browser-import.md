---
description: Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.
title: Browser-Import
feature: Classifications
exl-id: 5bef1f6d-9b27-464d-8343-472f300a7437
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '351'
ht-degree: 100%

---

# Browser-Import

Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

## Browser-Import {#concept_314FB3D5FD5A439B9CFEDE37A3337BA7}

Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**

## Browser-Import von Classifications – Feldbeschreibungen {#section_F628C47081DA4026A4D30E3D3454B1DA}

| Element | Beschreibung |
| --- | --- |
| Report Suite auswählen | Wählen Sie die Report Suite aus, in die die Classification-Daten importiert werden sollen. Die Importdatendatei muss mit dem Format des Datensatzes in der Report Suite übereinstimmen. |
| Datensatz, der klassifiziert werden soll | Datensatz, der die Classifications empfangen soll. Die Dropdown-Liste enthält alle Berichte aus Ihren Report Suites, die für Classifications konfiguriert sind. |
| Datei zum Import auswählen | Navigieren Sie hier zur Importdatendatei, die hochgeladen werden soll.  Hinweis: Für das Hochladen von Dateien gilt eine maximale Dateigröße von 1 MB. |
| Daten bei Konflikten überschreiben | Überschreibt automatisch vorhandene Daten, die mit den importierten Daten in Konflikt stehen.<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |
| Automatisches Herunterladen der Classification-Datei nach Abschluss des Imports. | Lädt automatisch eine mit Tabulatoren begrenzte Datei herunter, die den Datensatz mit den soeben hochgeladenen Classification-Daten darstellt. Adobe erzeugt diese Datei automatisch für Sie, wenn beim Import eindeutige Kennungen erstellt werden oder Fehler auftreten.<br>**Wichtig**: Diese Option ist nicht für Report Suites verfügbar, die für die neue Klassifizierungsarchitektur aktiviert sind. |


## Importieren von Classifications über Browser {#task_D7D51CB6FB35437AB68599B1B23FEAC1}

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]**.
1. Konfigurieren Sie die Felder **[!UICONTROL Browser-Import]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]**.
1. Behalten Sie das Statusfenster für Benachrichtigungen zum Stand der Verarbeitung im Auge.
1. (Bedingt) Wenn Sie die Option **[!UICONTROL Klassifizierungsdatei nach dem Hochladen automatisch herunterladen]** ausgewählt haben, geben Sie an, wo die entsprechende Datei nach Abschluss der Bearbeitung gespeichert werden soll. Beachten Sie, dass diese Option nicht für Report Suites verfügbar ist, die für die neue Klassifizierungsarchitektur aktiviert sind.

>Bei einem erfolgreichen Import werden die entsprechenden Änderungen automatisch in einem Export angezeigt. Datenänderungen in Berichten können hingegen vier Stunden bei Verwendung der Browser-Methode und bis zu 24 Stunden bei einem FTP-Import in Anspruch nehmen.
