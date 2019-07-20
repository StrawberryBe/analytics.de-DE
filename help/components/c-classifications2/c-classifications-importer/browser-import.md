---
description: Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.
seo-description: Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.
seo-title: Browser-Import
solution: Analytics
subtopic: Classifications
title: Browser-Import
topic: Admin Tools
uuid: 56 dfbf 4 c -36 e 6-49 f 4-b 5 cb -8 ab 714432825
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Browser-Import

Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

## Browser import {#concept_314FB3D5FD5A439B9CFEDE37A3337BA7}

Sie können Classification-Daten über den Browser importieren (hochladen). Diese Methode beschränkt Ihre heruntergeladenen Classification-Daten auf eine einzige Report Suite.

**[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**

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

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Click **[!UICONTROL Import File]**.
1. Configure the **[!UICONTROL Browser Import]** fields.
1. Click **[!UICONTROL Import File]**.
1.  Behalten Sie das Statusfenster für Benachrichtigungen zum Stand der Verarbeitung im Auge.
1. (Conditional) If you selected **[!UICONTROL Automatically Download Classification File After Upload is Complete]**, specify where you want to store the resulting file when processing completes.
>Bei einem erfolgreichen Import werden die entsprechenden Änderungen automatisch in einem Export angezeigt. Datenänderungen in Berichten können hingegen vier Stunden bei Verwendung der Browser-Methode und bis zu 24 Stunden bei einem FTP-Import in Anspruch nehmen.

