---
description: Sie können den Zeitplan für Versand für Berichte anpassen. Sie können den Versand zu einem bestimmten Zeitpunkt beenden oder angeben, wie oft Sie einen Bericht senden möchten. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und die tägliche Ausführung planen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht.
title: Zeitplan-Manager
topic: Ad hoc analysis
uuid: 82a054ef-109d-414d-a6e1-e09ee57c163f
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Zeitplan-Manager

Sie können den Zeitplan für Versand für Berichte anpassen. Sie können den Versand zu einem bestimmten Zeitpunkt beenden oder angeben, wie oft Sie einen Bericht senden möchten. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und die tägliche Ausführung planen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht.

## Zeitplan-Manager {#concept_A1CDE14B72A54DD6AE17B816092CAB8B}

Sie können den Zeitplan für Versand für Berichte anpassen. Sie können den Versand zu einem bestimmten Zeitpunkt beenden oder angeben, wie oft Sie einen Bericht senden möchten. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und die tägliche Ausführung planen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht.

>[!NOTE] Bei Deaktivierung eines Benutzerkontos werden terminierte Berichtbereitstellungen dieses Benutzers ausgesetzt.

To ensure that line items in a breakdown are persistent in saved and scheduled reports, use the **[!UICONTROL Edit Items]** feature in the [Table Builder](/help/analyze/ad-hoc-analysis/c-tablebuilder.md) to create fixed dimension lists in breakdowns.

>[!IMPORTANT]
>
>Mithilfe von Ad Hoc Analysis können Sie schnell und einfach Berichte für spezielle, zeitnahe Ad-hoc-Berichtsanforderungen erstellen. Es ist nicht für den vollständigen Export von Daten mit einer großen Anzahl von Zeilen, Spalten, Metrikbewertungen oder umfangreichen Aufschlüsselungen mithilfe von Datenextrahierungen konzipiert.
>
>Die praktischen Einschränkungen für geplante Berichte in Ad-hoc-Analysen basieren auf diesem Prinzip: Wenn Ihr Bericht nicht innerhalb von zehn Minuten erstellt wird (Timeout für Ad-hoc-Analysen), ist Ihr Bericht höchstwahrscheinlich zu komplex.
>
>Wahrscheinlich enthält Ihr Bericht zu viele Metriken, zu viele Aufschlüsselungen von Dimensionselementen, zu viele Zeilen oder Spalten oder andere Extreme, die die Erstellung eines Berichts für Ad-hoc-Analysen zu lange dauern lassen. Dieser Berichtstyp muss in Data Warehouse ausgeführt werden, einer Adobe Analytics-Funktion, die für die Offline-Extraktion der vollständigen Daten mit Berichtgenerierung ausgelegt ist, die viele Stunden oder Tage dauern kann.
>
>Beispielsweise kann die Ad-hoc-Analyse 50.000 Datenzeilen verarbeiten, aber eine Aufschlüsselung dieser Daten für zehn Browsertypen bedeutet 50.000 mal 10, eine exponentielle Zunahme, die für ein Ad-hoc-Berichte-Tool möglicherweise zu komplex ist. Zusätzliche Aufschlüsselungen erhöhen die Datenzeilen exponentiell. Die Definition der tatsächlichen Anzahl bzw. der Zeilen, Spalten und Aufschlüsselungen, die für Ad-hoc-Analysen-Berichte eingeschränkt werden sollen, kann nicht mit eindeutigen Begriffen definiert werden, sondern stellt eine Kombination aus all diesen Faktoren dar.

## Bereitstellung eines Berichts planen {#task_7A3165C8C5C349718FE3B2B0C727ACFD}

Die folgenden Schritte beschreiben, wie Sie die Bereitstellung eines Berichts planen.

<!-- 

t_schedule_delivery.xml

 -->

1. Klicken Sie auf **[!UICONTROL Tools]** und dann auf **[!UICONTROL Schedule Manager]**.
1. Klicken Sie im [!UICONTROL Schedule Manager]Fenster auf **[!UICONTROL New.]**

## Bereitstellungsoptionen – Definitionen {#reference_CA49AC560258471AAE959BCA243F170C}

Definitionen für die Einstellungen unter &quot;Versand-Optionen&quot;.

<!-- 

r_delivery_options.xml

 -->

Sie können Ihre Informationen, wie im aktuell ausgewählten Bericht angezeigt, an das von Ihnen ausgewählte Format senden. Sie können die Datei einmalig versenden oder einen Zeitplan für den Versand einrichten und das gewünschte Dateiformat angeben. Sie können eine digitale Signatur erstellen und senden, um dem Empfänger der Datei zu versichern, dass sie authentisch ist. Sie können die Datei an eine E-Mail-Adresse senden oder auf einen FTP-Server hochladen.

<table id="table_C18A0F1C9E214EB585A29801BA2400F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Feld </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Name </p> </td> 
   <td colname="col2"> <p> Der konfigurierbare Name dieses Berichts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID </p> </td> 
   <td colname="col2"> <p>Zeigt die Bericht-ID an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dateiformat </p> </td> 
   <td colname="col2"> 
    <ul id="ul_711C2D9B216C48359F7B42521D927872"> 
     <li id="li_36E8DEFDA1B84890A4204A6DFF4E0267">Excel: Gibt Ihren Bericht einschließlich aller Bilder in einer Tabelle aus. Bearbeitbar in Microsoft Excel. </li> 
     <li id="li_C918FA3AE8194BD2B59E554DAC7CBBE2">CSV: Gibt Ihren Bericht in kommagetrennten Werten aus. Sie können in einem einfachen Texteditor (z. B. Notepad) oder einem Tabelleneditor (z. B. Excel) bearbeitet werden. Enthält keine Bilder. </li> 
     <li id="li_B7C8C098C5264B349C21077A0DEFE059">PDF: Gibt Ihren Bericht im Portable Dokument Format aus. Nicht bearbeitbar und in Adobe Acrobat oder Adobe Reader sichtbar. </li> 
     <li id="li_B1183DB25DE34B689FBD0E5B44691F49">HTML: Gibt Ihren Bericht in einem Hypertext Markup Language-Anhang aus. Aus diesem Format bestehen die meisten Websites. Nicht bearbeitbar, wenn Sie mit HTML-Code vertraut sind. </li> 
     <li id="li_5ED5F1862AB1490A9FF5695FF9F52C5E">Word: Gibt Ihren Bericht einschließlich aller Bilder im Rich Text Format aus. Bearbeitbar in Microsoft Word oder WordPad. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Erweitert </p> </td> 
   <td colname="col2"> <p> Weitere Informationen finden Sie unter <a href="/help/analyze/ad-hoc-analysis/c-schedule.md"   >Erweiterte Formateinstellungen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dateiziel </p> </td> 
   <td colname="col2"> <p>E-Mail: Einstellungen, die per E-Mail gesendet werden sollen. </p> <p>FTP: Einstellungen zum Hochladen auf einen FTP-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berichtsbereich und Zeitplan für Versand </p> </td> 
   <td colname="col2"> <p>Gibt an, wann der Bericht bereitgestellt werden soll. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und die tägliche Ausführung planen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Erweiterte Formateinstellungen – Definitionen {#reference_F99B65BF7C9746638D8147EED147015B}

Definitionen für die Einstellungen unter Erweiterte Formateinstellungen.

<!-- 

r_advanced_format_settings_dsc.xml

 -->

<table id="table_CD0888E8390745F4B83DF6AC69CB0854"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Feld </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dateiname </p> </td> 
   <td colname="col2"> <p>Ein benutzerdefinierter Dateiname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID an Dateinamen anhängen </p> </td> 
   <td colname="col2"> <p>Hängt automatisch die Bericht-ID an den Dateinamen an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Datum an Dateinamen anhängen </p> </td> 
   <td colname="col2"> <p> Hängt automatisch das Datum des Berichts an den Dateinamen an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sprache </p> </td> 
   <td colname="col2"> <p> Hier können Sie eine Sprache für den Bericht auswählen. Sie können den Bericht unabhängig von der verwendeten Sprache in einer der folgenden Sprachen senden </p> 
    <ul id="ul_BD3D331B0D6146F79A6D254136E43920"> 
     <li id="li_0EE6A371B1BB4627BD3F64BD0EF07E44">Englisch </li> 
     <li id="li_5EF76261928543FDB36D99E4C89DE994">spanisch </li> 
     <li id="li_FABF47E8CD64486BA1567E02460422C5">Vereinfachtes Chinesisch </li> 
     <li id="li_8A6BC2DE92DB47DA9397B8931D8DCC6E">Traditionelles Chinesisch </li> 
     <li id="li_EDA24D700BE040E8B839B82E31DABC28">Französisch </li> 
     <li id="li_A8D41DCCC91542BB8D0A522EC99575E8">Deutsch </li> 
     <li id="li_E9F73C93C94A46B78BCE85A7261CEDD4">Japanisch </li> 
     <li id="li_699B97050AA54D818659C191F4594E4E">portugiesisch </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kodierung </p> </td> 
   <td colname="col2"> <p>Gibt einen Kodierungstyp an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Bericht als komprimierte Datei senden </p> </td> 
   <td colname="col2"> <p> Komprimiert die Datei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Digitalsignaturdatei senden </p> </td> 
   <td colname="col2"> <p>Erstellt eine digitale Signatur, die mit der E-Mail gesendet werden soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

