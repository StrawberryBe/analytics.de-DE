---
description: Sie können die Bereitstellung von Berichten planen. Sie können die Bereitstellung zu einem bestimmten Zeitpunkt stoppen oder die Häufigkeit des Berichtversands festlegen. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und eine tägliche Ausführung ansetzen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht.
title: Zeitplan-Manager
topic: Ad hoc analysis
uuid: 82a054ef-109d-414d-a6e1-e09ee57c163f
translation-type: tm+mt
source-git-commit: d4cb2acb4ecaecce3644a2f3cf29913440e5cd6a
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 98%

---


# Zeitplan-Manager

>[!IMPORTANT]
>
>Die Adobe bringt Ad Hoc Analysis am 1. März 2021 in den Status als lebensbedrohlich. [Weitere Infos...](https://adobe.ly/discoverworkspace).

Sie können die Bereitstellung von Berichten planen. Sie können die Bereitstellung zu einem bestimmten Zeitpunkt stoppen oder die Häufigkeit des Berichtversands festlegen. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und eine tägliche Ausführung ansetzen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht.

## Zeitplan-Manager {#concept_A1CDE14B72A54DD6AE17B816092CAB8B}

Sie können die Bereitstellung von Berichten planen. Sie können die Bereitstellung zu einem bestimmten Zeitpunkt stoppen oder die Häufigkeit des Berichtversands festlegen. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und eine tägliche Ausführung ansetzen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht.

>[!NOTE]
>
>Bei Deaktivierung eines Benutzerkontos werden terminierte Berichtbereitstellungen dieses Benutzers ausgesetzt.

Um sicherzustellen, dass Zeileneinträge in einer Aufschlüsselung in gespeicherten und terminierten Berichten persistent sind, verwenden Sie die Funktion **[!UICONTROL Elemente bearbeiten]** im [Tabellenaufbau](/help/analyze/ad-hoc-analysis/c-tablebuilder.md), um in Aufschlüsselungen feste Dimensionslisten zu erstellen.

>[!IMPORTANT]
>
>Mithilfe von Ad Hoc Analysis können Sie schnell und einfach Berichte für spezielle, zeitnahe Ad-hoc-Berichtsanforderungen erstellen. Die Anwendung ist nicht für den vollständigen Datenexport mit einer hohen Anzahl Zeilen, Werte, Metrik-Auswertungen oder umfangreiche Aufschlüsselungen mittels Datenextraktion ausgelegt.
>
>Praktische Beschränkungen der terminierten Berichtsfunktion bei Ad Hoc Analysis basieren auf diesem Prinzip: Wenn der Bericht nicht innerhalb von 10 Minuten erstellt wird (Timeout für Ad Hoc Analysis), dann ist der Bericht wahrscheinlich zu komplex.
>
>Wahrscheinlich enthält der Bericht zu viele Kennzahlen, zu viele Aufschlüsselungen nach Dimensionselementen, zu viele Zeilen oder Spalten oder andere Extreme, die den Bericht für die Erstellung mit Ad Hoc Analysis zu komplex machen. Derartige Berichte müssen im Data Warehouse erstellt werden, einer Adobe Analytics-Funktion, die für die umfassende Offline-Datenextraktion entwickelt wurde und Berichte erstellen kann, für die Stunden oder gar Tage erforderlich sind.
>
>Ad Hoc Analysis können z. B. 50.000 Zeilen mit Daten verarbeiten. Wenn diese Daten aber für 10 verschiedene Browser aufgeschlüsselt werden sollten, bedeutet das zehnmal 50.000, und dieses exponentielle Wachstum ist für das Berichterstellungswerkzeug der Ad Hoc Analysis wahrscheinlich zu komplex. Weitere Aufschlüsselungen erhöhen die Datenmenge exponentiell. Die tatsächliche Anzahl Zeilen, Spalten und Aufschlüsselungen, die von der Berichtfunktion von Ad Hoc Analysis bewältigt werden können, lässt sich nicht genau festlegen. Die Kombination dieser Faktoren schränkt die Leistungsfähigkeit aber zunehmend ein.

## Bereitstellung eines Berichts planen {#task_7A3165C8C5C349718FE3B2B0C727ACFD}

Die folgenden Schritte beschreiben, wie Sie die Bereitstellung eines Berichts planen.

<!-- 

t_schedule_delivery.xml

 -->

1. Klicken Sie auf **[!UICONTROL Tools]** und dann auf **[!UICONTROL Zeitplan-Manager]**.
1. Klicken Sie im [!UICONTROL Zeitplan-Manager] auf **[!UICONTROL Neu]**. 

## Bereitstellungsoptionen – Definitionen {#reference_CA49AC560258471AAE959BCA243F170C}

Definitionen für die Einstellungen der Bereitstellungsoptionen.

<!-- 

r_delivery_options.xml

 -->

Sie können die derzeit im Bericht angezeigten Informationen an das Format Ihrer Wahl senden. Der Versand kann einmal oder nach einem Lieferungszeitplan erfolgen und Sie können das bevorzugte Dateiformat angeben. Wenn Sie dem Empfänger die Echtheit der Datei zusichern möchten, können Sie eine Digitalsignatur erstellen und mitsenden. Sie können die Datei an eine E-Mail-Adresse senden oder auf einen FTP-Server laden.

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
   <td colname="col2"> <p>Hiermit rufen Sie die Bericht-ID ab. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dateiformat </p> </td> 
   <td colname="col2"> 
    <ul id="ul_711C2D9B216C48359F7B42521D927872"> 
     <li id="li_36E8DEFDA1B84890A4204A6DFF4E0267">Excel: Der Bericht wird mit allen Bildern in Tabellenform ausgegeben. Er kann in Microsoft Excel bearbeitet werden. </li> 
     <li id="li_C918FA3AE8194BD2B59E554DAC7CBBE2">CSV: Ihr Bericht wird in einer Datei mit kommagetrennten Werten ausgegeben. Diese kann in einem einfachen Texteditor oder einem Tabellenkalkulationsprogramm (z. B. Excel) bearbeitet werden. Sie enthält keine Bilder. </li> 
     <li id="li_B7C8C098C5264B349C21077A0DEFE059">PDF: Ihr Bericht wird im PDF-Format ausgegeben. Diese Dateien sind nicht editierbar und können im Adobe Acrobat oder Adobe Reader angezeigt werden. </li> 
     <li id="li_B1183DB25DE34B689FBD0E5B44691F49">HTML: Ihr Bericht wird als HTML-Anhang ausgegeben. Dieses Format (Hypertext Markup Language) liegt den meisten Webseiten zugrunde. Sie sollten es nur editieren, wenn Sie sich mit HTML-Code auskennen. </li> 
     <li id="li_5ED5F1862AB1490A9FF5695FF9F52C5E">Word: Ihr Bericht wird inklusive aller Bilder im Rich Text Format ausgegeben. Er kann in Microsoft Word oder WordPad bearbeitet werden. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Erweitert </p> </td> 
   <td colname="col2"> <p> Weitere Informationen finden Sie unter <a href="/help/analyze/ad-hoc-analysis/c-schedule.md"   >Erweiterte Formateinstellungen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dateiziel </p> </td> 
   <td colname="col2"> <p>E-Mail: Einstellungen für den E-Mail-Versand. </p> <p>FTP: Einstellungen für den Upload auf einen FTP-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berichtsbereich und Bereitstellungsplan </p> </td> 
   <td colname="col2"> <p>Legt fest, wann der Bericht bereitgestellt wird. Neue Zeitpläne verwenden den im Bericht definierten Datumsbereich. Wenn Sie beispielsweise einen Bericht für die letzten 90 Tage erstellen und eine tägliche Ausführung ansetzen, erhalten Sie jeden Tag einen Bericht für die letzten 90 Tage. Wenn Sie einen Bericht mit einem statischen Datumsbereich aus dem Kalender erstellen, sehen Sie jedes Mal, wenn der Bericht versendet wird, denselben Bericht. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Erweiterte Formateinstellungen – Definitionen {#reference_F99B65BF7C9746638D8147EED147015B}

Definitionen für die Einstellungen der erweiterten Formateinstellungen.

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
   <td colname="col2"> <p> Hängt automatisch das Berichtdatum an den Dateinamen an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sprache </p> </td> 
   <td colname="col2"> <p> Hier können Sie eine Sprache für den Bericht auswählen. Sie können den Bericht unabhängig von Ihrer bevorzugten Sprache in einer der folgenden Sprachen senden </p> 
    <ul id="ul_BD3D331B0D6146F79A6D254136E43920"> 
     <li id="li_0EE6A371B1BB4627BD3F64BD0EF07E44">Englisch </li> 
     <li id="li_5EF76261928543FDB36D99E4C89DE994">Spanisch </li> 
     <li id="li_FABF47E8CD64486BA1567E02460422C5">Vereinfachtes Chinesisch </li> 
     <li id="li_8A6BC2DE92DB47DA9397B8931D8DCC6E">Traditionelles Chinesisch </li> 
     <li id="li_EDA24D700BE040E8B839B82E31DABC28">Französisch </li> 
     <li id="li_A8D41DCCC91542BB8D0A522EC99575E8">Deutsch </li> 
     <li id="li_E9F73C93C94A46B78BCE85A7261CEDD4">Japanisch </li> 
     <li id="li_699B97050AA54D818659C191F4594E4E">Portugiesisch </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kodierung </p> </td> 
   <td colname="col2"> <p>Hier wird der Kodierungstyp festgelegt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Bericht als komprimierte Datei senden </p> </td> 
   <td colname="col2"> <p> Komprimiert die Datei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Digitalsignaturdatei senden </p> </td> 
   <td colname="col2"> <p>Erstellt eine digitale Signatur, die mit der E-Mail gesendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

