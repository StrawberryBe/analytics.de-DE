---
description: Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.
seo-description: Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.
seo-title: Neue Report Suite - Einstellungen
solution: Analytics
title: Neue Report Suite - Einstellungen
topic: Admin Tools
uuid: 3508 f 684-11 a 3-4 c 8 f-a 233-bea 6 bafd 57 c 0
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Neue Report Suite - Einstellungen

Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.

Beschreibung der verwendeten Elemente beim [Erstellen einer Report Suite](../../../admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md#task_67033B9710CB49F9B71A4DE374A538A0).

>[!NOTE]
>
>The [Virtual Report Suite documentation](/help/components/vrs/c-workflow-vrs/vrs-create.md) shows you how to create virtual report suites.

<table id="table_F739FBD8DB8D409E916F12F61C5953D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Report Suite-ID </span> </td> 
   <td colname="col2"> <p>Gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach dem Erstellen nicht mehr geändert werden. Adobe legt das erforderliche ID-Präfix fest, das ebenfalls nicht geändert werden kann. </p> <p>Achten Sie beim Erstellen mehrerer Report Suites darauf, dass die von Ihnen verwendeten Benennungsregeln eindeutige Report Suite-IDs ergeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Site-Titel</span> </td> 
   <td colname="col2">Gibt die Report Suite in den <span class="wintitle">Admin Tools</span> an. Der Titel wird ebenfalls in der Dropdownliste <span class="wintitle">„Report Suite“</span> im Suite-Header verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Zeitzone</span> </td> 
   <td colname="col2"> Wird zur Planung von Ereignissen und für Zeitstempeldaten verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basis-URL</span> </td> 
   <td colname="col2"> (Optional) Definiert die Basisdomäne für die Report Suite. Diese URL-Adresse fungiert als interner URL-Filter, wenn Sie nicht explizit interne URL-Filter für die Report Suite definiert haben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Standardseite</span> </td> 
   <td colname="col2"> <p>(Optional) Bereinigt Vorkommnisse des Werts <span class="wintitle">Standardseite</span> von den dabei auftretenden URL-Adressen. Wenn der Bericht <span class="wintitle">Bevorzugte Seiten</span> URLs statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Webseite mehrere URLs angegeben werden. </p> <p>For example, the URLs<span class="filepath"> https://mysite.com</span> and <span class="filepath"> https://mysite.com/index.html</span> are typically the same page. You can remove extraneous filenames so that both these URLs show up as <span class="filepath"> https://mysite.com</span> in your reports. </p> <p>Wenn Sie diesen Wert nicht angeben, entfernt Analytics automatisch die folgenden Dateinamen aus den URLs: <span class="filepath">index.htm</span>, <span class="filepath">index.html</span>, <span class="filepath">index.cgi</span>, <span class="filepath">index.asp</span>, <span class="filepath">default.htm</span>, <span class="filepath">default.html</span>, <span class="filepath">default.cgi</span>, <span class="filepath">default.asp</span>, <span class="filepath">home.htm</span>, <span class="filepath">home.html</span>, <span class="filepath">home.cgi</span> und <span class="filepath">home.asp</span>. </p> <p>Wenn Sie die Bereinigung von Dateinamen deaktivieren möchten, geben Sie einen Wert für „Standardseite“ an, der in keiner URL-Adresse vorkommt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aufschaltdatum </p> </td> 
   <td colname="col2">Informiert Adobe über das Datum, ab dem diese Report Suite aktiv sein soll. If your deployment schedule changes, provide an updated traffic estimate using the <span class="wintitle"> Permanent Expected Traffic</span> tool in <a href="../../../admin/c-traffic-management/traffic-management.md#concept_8BD651EE8B84434CB4D6308BC6C01B79" format="dita" scope="local"> Traffic Management</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Geschätzte Seitenansichten pro Tag</span> </td> 
   <td colname="col2"> Gibt an, wie viele Seitenaufrufe diese Report Suite pro Tag unterstützen soll. Ein großes Traffic-Volumen beansprucht mehr Zeit im Genehmigungsprozess. Die Schätzung sollte möglichst genau ausfallen, damit es nicht zu Verzögerungen bei der Verarbeitung kommt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basiswährung</span> </td> 
   <td colname="col2"> <p>Gibt die Standardwährung für die Speicherung sämtlicher Beträge an. In der Analytics-Berichterstellung werden Transaktionen in anderen Währungen zum aktuellen Konversionskurs (d. h. zum Zeitpunkt des Eingangs der Daten) in die Basiswährung umgerechnet. </p> <p> Die Analytics-Berichterstellung verwendet die <span class="varname"> Currencycode</span> -javascript-Variable zur Identifizierung der Währung einer Transaktion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Multibytezeichenunterstützung deaktivieren </span> </td> 
   <td colname="col2"> <p>Deaktiviert die Multibytezeichenunterstützung für die Report Suite. Wenn Sie die Multibytezeichenunterstützung deaktivieren, geht das System davon aus, dass die Daten im ISO-8859-1-Format vorliegen. Auf Webseiten muss der Zeichensatz in der JavaScript-Variablen <span class="varname"> Javascript-Variable</span> "charset" . </p> <p>Bei der Multibytezeichenunterstützung werden Zeichen der Report Suite als UTF-8 gespeichert. Beim Empfang der Daten konvertiert das System die Daten aus dem Zeichensatz der Webseite in den UTF-8-Zeichensatz, damit Sie in Ihren Marketing-Berichten eine beliebige Sprache verwenden können. </p> <p>Wenden Sie sich an Ihren Kundenbetreuer oder an den Kundendienst, wenn die Multibytezeichenunterstützung für eine Report Suite geändert werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Ad Hoc Analysis für diese Suite aktivieren</span> </td> 
   <td colname="col2"> Aktiviert die Anzeige dieser Report Suite, wenn Sie Ad Hoc Analysis durchführen. </td> 
  </tr> 
 </tbody> 
</table>

