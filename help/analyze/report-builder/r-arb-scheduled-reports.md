---
description: Feldbeschreibungen für den Manager für geplante Aufgaben.
seo-description: Feldbeschreibungen für den Manager für geplante Aufgaben.
seo-title: Manager für geplante Aufgaben
solution: Analytics
title: Manager für geplante Aufgaben
topic: ReportBuilder
uuid: dec 259 f 0-2 a 04-4 c 94-abbc -5008 cf 2 f 1 cb 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Manager für geplante Aufgaben

Feldbeschreibungen für den Manager für geplante Aufgaben.

Im Manager für geplante Aufgaben können Sie eine Liste mit den vorhandenen terminierten Berichten, ihren Empfängern, Zeitplandetails und Dateiformaten sehen. Sie können außerdem geplante Arbeitsmappen, deren Ausführung fehlgeschlagen ist, reaktivieren.

<table id="table_21B07A0B5F1D4435A4E882E45A7A6B6E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feld </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Registerkarte <b>Terminierte Berichte </b> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berichtname </p> </td> 
   <td colname="col2"> <p>Dies ist der Name des terminierten Berichts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> E-Mail/FTP </p> </td> 
   <td colname="col2"> <p>Die E-Mail- oder FTP-Adresse des Empfängers. </p> <p>Hinweis: Wenn E-Mail ausgewählt ist, werden Berichte, die größer als 1 MB sind, automatisch als ZIP-Datei an die E-Mail angehängt. Dank dieser Funktion bleibt die Größe des Anhangs gering und Anhänge werden nicht deaktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Veröffentlichungsoptionen </p> </td> 
   <td colname="col2"> <p>Diese Spalte enthält Power BI, wenn eine der <a href="../../analyze/report-builder/c-publish-power-bi/integration-power-bi.md#concept_0C4105AA10F9460A872C2489C9CD7945" format="dita" scope="local"> Power BI-Veröffentlichungsoptionen</a> ausgewählt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plan </p> </td> 
   <td colname="col2"> <p>Der Typ der geplanten Bereitstellung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dateiformat </p> </td> 
   <td colname="col2"> <p> Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reaktivieren </p> </td> 
   <td colname="col2"> <p>Wenn eine geplante Arbeitsmappe nicht ausgeführt werden kann, unternimmt ReportBuilder in jeweils 15 Minuten Abstand zwei weitere Ausführungsversuche. Nach drei fehlgeschlagenen Versuchen deaktiviert ReportBuilder den Plan und zeigt die Schaltfläche <span class="wintitle">Reaktivieren</span> an. Wenn Sie eine Arbeitsmappe reaktivieren, wird die geplante Bereitstellung ab dem Zeitpunkt wiederaufgenommen, an dem die Deaktivierung erfolgte. </p> <p>Wenn eine geplante Arbeitsmappe beispielsweise vor 14 Tagen deaktiviert wurde und Sie sie heute reaktivieren, wird sie für jeden fehlenden Tag, also 14-mal ausgeliefert. Wenn die Arbeitsmappe für die fehlenden Tage nicht ausgeliefert werden soll, können Sie die geplante Arbeitsmappe löschen und eine neue geplante Arbeitsmappe unter Verwendung derselben Planungsparameter erstellen. </p> <p> <p>Hinweis: Sie sollten eine Arbeitsmappe nicht reaktivieren, bevor Sie die Ursache der Deaktivierung durch das System kennen. Eine Möglichkeit der Fehlerbehebung besteht darin, die deaktivierte Arbeitsmappe herunterzuladen und sie auf der Clientseite aktualisieren. Wenn keine Fehlermeldung erfolgt, sollte die Arbeitsmappe reaktiviert werden können. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zuletzt gesendet </p> </td> 
   <td colname="col2"> <p>Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Registerkarte <b>Empfänger </b> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E-Mail-Adresse des Empfängers </p> </td> 
   <td colname="col2"> Die E-Mail-Adresse des Berichtempfängers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berichte </p> </td> 
   <td colname="col2"> Die Berichte, die an die einzelnen Empfänger gesendet wurden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Registerkarte <b>Berichte – Verlauf</b> </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dateiname </p> </td> 
   <td colname="col2"> Dies ist der Name des terminierten Berichts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datums </p> </td> 
   <td colname="col2"> Das Datum und die Uhrzeit, an denen der Bericht zuletzt gesendet wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> Der Status gibt an, ob der Bericht gesendet oder nicht gesendet wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>E-Mail/FTP </p> </td> 
   <td colname="col2"> Die E-Mail- oder FTP-Adresse für den Empfänger des Berichts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dateiformat </p> </td> 
   <td colname="col2"> Das Bereitstellungsformat des Berichts, z. B. Excel, PDF, HTML usw. </td> 
  </tr> 
 </tbody> 
</table>
