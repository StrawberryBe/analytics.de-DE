---
description: Erstellen, verwalten und zeigen Sie die Nutzung von Datenquellen in einer Report Suite an.
subtopic: Data sources
title: Data Sources Manager
topic-fix: Developer and implementation
uuid: ccfa4a1c-7c56-421b-8ee6-a42b334659b1
exl-id: a63137b8-deeb-4865-9be9-322416b00186
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 98%

---

# Data Sources Manager

Erstellen, verwalten und zeigen Sie die Nutzung von Datenquellen in einer Report Suite an.

**[!UICONTROL Analytics]** >  **[!UICONTROL Admin]** >  **[!UICONTROL Alle Admin]** >  **[!UICONTROL Datenquellen]**.

## Registerkarte „Erstellen“  {#section_74603FDA3D8842E49F1A51624A06DE20}

Über die Registerkarte [!UICONTROL Erstellen] können Sie eine neue Datenquelle für die aktuell ausgewählte Report Suite konfigurieren. Wenn Sie eine Datenquelle aktivieren, führt Sie der [!UICONTROL Data Sources-Assistent] durch den Erstellungsvorgang einer Data Sources-Vorlage und legt einen FTP-Speicherort zum Hochladen der Daten an.

Die anfänglich in der erstellten Vorlage angezeigten Felder sind von der Auswahl auf der Registerkarte „Erstellen“ abhängig. Siehe   [Erstellen einer Importdatei-Vorlage](/help/import/c-data-sources/datasrc-template/t-datasrc-creating-data-sources-file.md).

## Registerkarte „Verwalten“  {#section_DD559A6701CA45F1A85E56F840F48DBE}

<table id="table_F74696EC855441328CFE0BF49C20D9B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Option </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verarbeitung neu starten </p> </td> 
   <td colname="col2"> <p>Startet die Verarbeitung der Datenquelle neu, die zuvor aufgrund von Fehlern oder Warnungen angehalten wurde. Die Verarbeitung wird fortgesetzt, bis der nächste Fehler erkannt wird. Data Sources stoppt die Verarbeitung einer Data Sources-Datei nur, wenn Sie die Option <span class="uicontrol">Verarbeitung bei Fehler stoppen</span> auswählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verarbeitung abschließen </p> </td> 
   <td colname="col2"> <p>Weist Data Sources an, offene Besuche in der Datei zu schließen und die Verarbeitung der Data Sources-Datei abzuschließen, als wäre sie vollständig. Dies ist nützlich, wenn Sie Besuche haben, die sich über mehrere Data Sources-Dateien erstrecken. Dies gilt nur für   <a href="/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md"   > Vollständige Verarbeitung</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deaktivieren </p> </td> 
   <td colname="col2"> <p> Durch Deaktivieren einer Datenquelle wird sie gelöscht. Wenn die Verarbeitung von Dateien auf dem Server begonnen hat, wird diese Verarbeitung fortgesetzt, bis sie abgeschlossen ist. Dateien, deren Verarbeitung noch nicht begonnen hat, werden nicht verarbeitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verarbeitung bei Fehler/Warnung stoppen </p> </td> 
   <td colname="col2"> <p> Weist die Verarbeitungs-Engine von Data Sources an, die Verarbeitung zu stoppen, sobald ein Fehler auftritt. Die Verarbeitung der Datenquelle wird erst fortgesetzt, nachdem Sie „Verarbeitung neu starten“ gewählt haben. Die Option „Verarbeitung bei Fehler/Warnung stoppen“ gilt nur für   <a href="/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md"   > Vollständige Verarbeitung</a>. </p> <p>Wenn in Data Sources ein Dateifehler auftritt, wird eine Fehlermeldung ausgegeben. Das System verschiebt die Data Sources-Datei mit dem Fehler in einen Ordner mit dem Namen <span class="filepath">files_with_errors</span> auf dem FTP-Server. Sobald Sie das Problem gelöst haben, können Sie die Data Sources-Datei erneut für die Verarbeitung einreichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Konfigurieren </p> </td> 
   <td colname="col2"> <p>Ermöglicht es Ihnen, die Datenquellen-Vorlage oder andere für diese Datenquelle spezifische Einstellungen zu ändern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FTP-Info </p> </td> 
   <td colname="col2"> <p>Zeigt die FTP-Informationen für diese Datenquelle an. Verwenden Sie diese Informationen, um auf die Datenquellen-Vorlage zuzugreifen und die Datenquelle-Daten zu senden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dateiname </p> </td> 
   <td colname="col2"> <p>Der Name der hochgeladenen Datei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> <p> Der aktuelle Status der Datei. Mögliche Statuswerte: </p> 
    <ul id="ul_56A0BF8C1BE249F6BB39B0D11DA3997F"> 
     <li id="li_BAB359E08EDE4E0298C0362258789603">In Warteschlange (Schritt 1 von 3): Die Datei existiert, aber die Verarbeitung hat noch nicht begonnen. Wenn die Datei nicht innerhalb von 30 Minuten angezeigt wird, überprüfen Sie, ob die zugehörige <span class="filepath">.fin</span>-Datei vorliegt. </li> 
     <li id="li_A09A14F42CB74F01B694799740B3DA17">Vorbereitung (Schritt 2 von 3): Die Datei wird auf Fehler oder Warnungen geprüft. </li> 
     <li id="li_793FDCDB64CF434D82CAF5B6E9BDE557">Verarbeitung (Schritt 3 von 3): Die Datei wird verarbeitet. </li> 
     <li id="li_1D8C4B241FF0453EAF7DDFD8354C5573">Fehlgeschlagen: Die Datei wurde aufgrund von Fehlern nicht verarbeitet. </li> 
     <li id="li_A52507602FB4492B83A70AF6449A539A">Erfolg: Die Datei wurde vollständig verarbeitet. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Registerkarte „Dateiprotokoll“   {#section_B7AC7EE8CAD740A59DD53CF1919373F0}

Das Dateiprotokoll enthält eine Suchfunktion, mit der Sie anhand von Datenquelle-Name, Datenquelle-Typ, Dateiname, Empfangsdatum oder Status nach Informationen suchen können.
