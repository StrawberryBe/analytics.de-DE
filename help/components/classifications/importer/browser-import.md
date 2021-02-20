---
description: Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.
subtopic: Classifications
title: Browser-Import
topic: Admin tools
uuid: 56dfbf4c-36e6-49f4-b5cb-8ab714432825
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 100%

---


# Browser-Import

Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

## Browser-Import {#concept_314FB3D5FD5A439B9CFEDE37A3337BA7}

Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**

## Browser-Import von Classifications – Feldbeschreibungen {#section_F628C47081DA4026A4D30E3D3454B1DA}

<table id="table_7FC7E510E7E74C2D9E8F316C5C6B66DB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Report Suite auswählen </td> 
   <td colname="col2"> <p>Wählen Sie die Report Suite aus, in die die Classification-Daten importiert werden sollen. Die Importdatendatei muss mit dem Format des Datensatzes in der Report Suite übereinstimmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Datensatz, der klassifiziert werden soll </td> 
   <td colname="col2"> <p>Datensatz, der die Classifications empfangen soll. Die Dropdown-Liste enthält alle Berichte aus Ihren Report Suites, die für Classifications konfiguriert sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Datei zum Import auswählen </td> 
   <td colname="col2"> <p>Navigieren Sie hier zur Importdatendatei, die hochgeladen werden soll. </p> <p>Hinweis: Für das Hochladen von Dateien gilt eine maximale Dateigröße von 1 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Daten bei Konflikten überschreiben </td> 
   <td colname="col2"> <p>Überschreibt automatisch vorhandene Daten, die mit den importierten Daten in Konflikt stehen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Automatisches Herunterladen der Classification-Datei nach Abschluss des Imports. </td> 
   <td colname="col2"> <p>Lädt automatisch eine mit Tabulatoren begrenzte Datei herunter, die den Datensatz mit den soeben hochgeladenen Classification-Daten darstellt. Adobe erzeugt diese Datei automatisch für Sie, wenn beim Import eindeutige Kennungen erstellt werden oder Fehler auftreten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Importieren von Classifications über Browser {#task_D7D51CB6FB35437AB68599B1B23FEAC1}

<!-- 

t_upload_a_saint_data_file_via_web_browser.xml

 -->

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]**.
1. Konfigurieren Sie die Felder **[!UICONTROL Browser-Import]**.
1. Klicken Sie auf **[!UICONTROL Datei importieren]**.
1. Behalten Sie das Statusfenster für Benachrichtigungen zum Stand der Verarbeitung im Auge.
1. (Bedingt) Wenn Sie die Option **[!UICONTROL Klassifizierungsdatei nach dem Hochladen automatisch herunterladen]** ausgewählt haben, geben Sie an, wo die entsprechende Datei nach Abschluss der Bearbeitung gespeichert werden soll.
>Bei einem erfolgreichen Import werden die entsprechenden Änderungen automatisch in einem Export angezeigt. Datenänderungen in Berichten können hingegen vier Stunden bei Verwendung der Browser-Methode und bis zu 24 Stunden bei einem FTP-Import in Anspruch nehmen.

