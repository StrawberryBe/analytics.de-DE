---
description: Sie können Berichte entsprechend der von Ihnen festgelegten Datums- und Dateiformate planen.
seo-description: Sie können Berichte entsprechend der von Ihnen festgelegten Datums- und Dateiformate planen.
seo-title: Datenanforderung planen
solution: Analytics
title: Datenanforderung planen
topic: ReportBuilder
uuid: f 6 d 8 c 90 f-e 185-4 d 60-8035-f 20 f 74 bfcd 89
translation-type: tm+mt
source-git-commit: 6a70b32b576cc7b5b6a6f0037d98e35b3f8c1426

---


# Datenanforderung planen

Sie können Berichte entsprechend der von Ihnen festgelegten Datums- und Dateiformate planen.

**So planen Sie eine Datenanforderung**

1. Erzeugen Sie einen Bericht und speichern Sie ihn.
1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]**.

   Die Registerkarte „[!UICONTROL Terminierte Berichte]“ enthält eine Zusammenfassung aller von Ihnen erstellten Aufgaben sowie die Anzahl der verbleibenden Aufgaben.
1. Klicken Sie auf de Registerkarte **** Geplante Berichte auf **[!UICONTROL Neu]**.
1. Das Fenster „Planungs-Assistent – Grundlegend“ wird angezeigt:

   ![](assets/simple-schedule-wizard.png)

1. Konfigurieren Sie im Fenster [!UICONTROL Planungs-Assistent – Grundlegend] die folgenden Optionen:

* **Bericht auswählen**: Der Name des Berichts. Bei neuen terminierten Berichten erscheint in diesem Feld automatisch der Name der aktiven Arbeitsmappe.

<table id="table_6D5B1B832EB0451293F1902E2A1D1068"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feld </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bericht auswählen </p> </td> 
   <td colname="col2"> <p>Den Namen des Berichts. Bei neuen terminierten Berichten erscheint in diesem Feld automatisch der Name der aktiven Arbeitsmappe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Auswählen </p> </td> 
   <td colname="col2"> <p>Hierdurch wird die Seite <span class="wintitle">Bericht auswählen</span> angezeigt. Sie können einen Bericht vom Server (wo alle früher geplanten Arbeitsmappen gespeichert sind) oder von Ihrem lokalen Computer auswählen. Wenn Sie einen Arbeitsmappe von der lokalen Festplatte im <span class="filepath">.xls</span>-Format auswählen, wandelt das System sie in eine <span class="filepath">.xlsx</span>-Datei um. Im Rahmen der Konversion wird die Datei in Excel geöffnet und aktiviert. Wenn die für den terminierten Bericht ausgewählte Arbeitsmappe denselben Dateinamen wie die derzeit in Excel geöffnete Arbeitsmappe hat, wählt das System statt der vorher hochgeladenen Datei die lokale Datei. Wenn Sie einen Bericht aus dem Repository der terminierten Berichte wählen, wird eine Kopie der Arbeitsmappe auf dem Server erstellt und deren Dateiname um „1“ erweitert, und der neu terminierte Bericht verwendet die kopierte Arbeitmappe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anpassen </p> </td> 
   <td colname="col2"> <p>Ermöglicht Ihnen, das Datumsformat anzupassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>An </p> </td> 
   <td colname="col2"> <p>Zeigt Ihr gegebenenfalls vorhandenes Outlook-Adressbuch an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Senden an: E-Mail </p> </td> 
   <td colname="col2"> <p>Die E-Mail-Adresse des Berichtempfängers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Senden an: Veröffentlichungsliste </p> </td> 
   <td colname="col2"> <p>Hiermit zeigen Sie eine Liste der in Ihrem Unternehmen verfügbaren Veröffentlichungslisten an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Power BI </p> </td> 
   <td colname="col2"> <p>Weitere Informationen finden Sie unter <a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_BA137EA92A46483F83BB5C1C40FBA002" format="dita" scope="local">Arbeitsmappe in Microsoft Power BI veröffentlichen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Betreff </p> </td> 
   <td colname="col2"> <p>Eine benutzerdefinierte Beschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zeitplan </p> </td> 
   <td colname="col2"> <p>  Hier können Sie angeben, wann der Bericht gesendet werden soll (sofort, stündlich, täglich, wöchentlich oder jährlich). </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Click **[!UICONTROL Advanced Delivery Options]** to configure file and publishing options:

<table id="table_1BA8A5600DE94A33B83B096E69CE15F3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feld </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Registerkarte <b>Zeitplan</b> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zeitpunkt der Bereitstellung </p> </td> 
   <td colname="col2"> <p>Hier können Sie eine sofortige oder spätere Auslieferung des Berichts planen. Die Uhrzeit entspricht der Zeitzoneneinstellung auf Ihrem Computer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wiederholungsmuster </p> </td> 
   <td colname="col2"> <p>Hiermit wird der Bericht entsprechend Ihrer Auswahl gesendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bereich der Wiederholung </p> </td> 
   <td colname="col2"> <p>Hier geben Sie an, wann der Empfang des Berichts beginnen und enden soll. </p> <p> <p>Hinweis: Wenn Sie einen Bericht für den ersten Tag eines bestimmten Zeitraums (Woche, Monat, Quartal oder Jahr) planen, werden nur Daten für den ersten Tag zurückgegeben. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Registerkarte <b>Dateioptionen</b> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dateiformat </p> </td> 
   <td colname="col2"> <p>Hier können Sie als Bereitstellungsformat Excel 2007 <span class="filepath">(.xlsx)</span> oder 2003 <span class="filepath">(.xls)</span>, <span class="filepath">.pdf</span>, <span class="filepath">.csv</span>, <span class="filepath">.mht</span>, <span class="filepath">.txt</span> oder <span class="filepath">.xml</span> auswählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dateiziel </p> </td> 
   <td colname="col2"> <p> Hier wird die E-Mail- oder FTP-Adresse angegeben. Die verfügbaren Optionen wechseln ja nach der bisherigen Auswahl. Für FTP müssen Sie sicherstellen, dass der Host extern verfügbar ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Veröffentlichungsliste </p> </td> 
   <td colname="col2"> <p> Wenn Sie den terminierten Bericht an mehrere Veröffentlichungslisten gleichzeitig senden, wird der Bericht jeweils einmal pro Liste ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sprache des Dateiinhalts </p> </td> 
   <td colname="col2"> <p>Gibt die Sprache an, die für das Anschreiben verwendet werden soll. Zur Auswahl stehen Chinesisch (vereinfacht oder traditionell), Deutsch, Französisch, Japanisch, Koreanisch, Portugiesisch (Brasilien) oder Spanisch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Registerkarte <b>Veröffentlichungsoptionen</b> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>In Power BI veröffentlichen </p> </td> 
   <td colname="col2"> 
    <ul id="ul_40697E4FB2CE4F34B857FBF153D6D6D5"> 
     <li id="li_023E4750814D415EBC899269C9EA5D46"><a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_BA137EA92A46483F83BB5C1C40FBA002" format="dita" scope="local"> Arbeitsmappe in Power BI veröffentlichen</a> </li> 
     <li id="li_9B684BE22AF94ABC903405EE83951A80"><a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_E48148793E794169B766C73995897B9F" format="dita" scope="local"> Alle ReportBuilder-Anforderungen als Power BI-Datensätze veröffentlichen</a> </li> 
     <li id="li_7B0BD285BC1749D1B2C65759CA97877B"><a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#section_6F8422B90D3F4F7EB5D4C97BFFA807AD" format="dita" scope="local"> Alle formatierten Tabellen als Power BI-Datensätze veröffentlichen</a> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Diesen Power BI-Bericht bezeichnen als </p> </td> 
   <td colname="col2"> <p>Bezeichnungsdetails </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Click **[!UICONTROL OK]**, then click **[!UICONTROL Exit]**.

   ReportBuilder zeigt den terminierten Bericht im [Manager für geplante Aufgaben](../../analyze/report-builder/r-arb-scheduled-reports.md#section_69306B8D833F4DF7BBFA53753B0E6C31) an.
