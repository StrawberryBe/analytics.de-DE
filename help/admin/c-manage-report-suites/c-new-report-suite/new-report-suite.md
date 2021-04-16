---
description: Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.
title: Neue Report Suite – Einstellungen
feature: Admin Tools
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
exl-id: ea5f8543-058d-4e08-bc66-575e3a7460c2
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 93%

---

# Neue Report Suite – Einstellungen

Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.

Beschreibung der verwendeten Elemente beim  [Erstellen einer Report Suite](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md).

>[!NOTE]
>
>In der [Dokumentation zur Virtual Report Suite](/help/components/vrs/c-workflow-vrs/vrs-create.md) erfahren Sie, wie Sie Virtual Report Suites erstellen.

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
   <td colname="col2">Gibt die Report Suite in den <span class="wintitle">Admin Tools</span> an. Der Titel wird ebenfalls in der Dropdown-Liste <span class="wintitle">Report Suite</span> in der Kopfzeile der Suite verwendet. </td> 
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
   <td colname="col2"> <p>(Optional) Bereinigt Vorkommnisse des Werts <span class="wintitle">Standardseite</span> von den dabei auftretenden URL-Adressen. Wenn der Bericht <span class="wintitle">Bevorzugte Seiten</span> URLs statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Webseite mehrere URLs angegeben werden. </p> <p>Beispielsweise sind die URLs<span class="filepath"> https://example.com</span> und <span class="filepath"> https://example.com/index.html</span> normalerweise dieselbe Seite. Sie können externe Dateinamen entfernen, damit beide URLs in Ihren Berichten als <span class="filepath"> https://example.com</span> angezeigt werden. </p> <p>Wenn Sie diesen Wert nicht angeben, entfernt Analytics automatisch die folgenden Dateinamen aus den URLs: <span class="filepath">index.htm</span>, <span class="filepath">index.html</span>, <span class="filepath">index.cgi</span>, <span class="filepath">index.asp</span>, <span class="filepath">default.htm</span>, <span class="filepath">default.html</span>, <span class="filepath">default.cgi</span>, <span class="filepath">default.asp</span>, <span class="filepath">home.htm</span>, <span class="filepath">home.html</span>, <span class="filepath">home.cgi</span> und <span class="filepath">home.asp</span>. </p> <p>Wenn Sie die Bereinigung von Dateinamen deaktivieren möchten, geben Sie einen Wert für „Standardseite“ an, der in keiner URL-Adresse vorkommt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aufschaltdatum </p> </td> 
   <td colname="col2">Informiert Adobe über das Datum, ab dem diese Report Suite aktiv sein soll. Wenn sich der Implementierungsplan ändert, müssen Sie mithilfe des Tools <span class="wintitle">Dauerhaft erwarteter Traffic</span> in <a href="/help/admin/c-traffic-management/traffic-management.md">Traffic-Management</a> eine aktualisierte Traffic-Schätzung eingeben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Geschätzte Seitenansichten pro Tag</span> </td> 
   <td colname="col2"> Gibt an, wie viele Seitenaufrufe diese Report Suite pro Tag unterstützen soll. Ein großes Traffic-Volumen beansprucht mehr Zeit im Genehmigungsprozess. Die Schätzung sollte möglichst genau ausfallen, damit es nicht zu Verzögerungen bei der Verarbeitung kommt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basiswährung</span> </td> 
   <td colname="col2"> <p>Gibt die Standardwährung für die Speicherung sämtlicher Beträge an. In der Analytics-Berichterstellung werden Transaktionen in anderen Währungen zum aktuellen Konversionskurs (d. h. zum Zeitpunkt des Eingangs der Daten) in die Basiswährung umgerechnet. </p> <p> Die Analytics-Berichterstellung verwendet die  <span class="varname"> currencyCode</span>-JavaScript-Variable, um die Währung einer Transaktion zu bestimmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Multibytezeichenunterstützung deaktivieren </span> </td> 
   <td colname="col2"> <p>Deaktiviert die Multibytezeichenunterstützung für die Report Suite. Wenn Sie die Multibytezeichenunterstützung deaktivieren, geht das System davon aus, dass die Daten im ISO-8859-1-Format vorliegen. Auf Webseiten muss der Zeichensatz in der JavaScript-Variablen  <span class="varname"> „charSet“</span> angeben. </p> <p>Bei der Multibytezeichenunterstützung werden Zeichen der Report Suite als UTF-8 gespeichert. Beim Empfang der Daten konvertiert das System die Daten aus dem Zeichensatz der Webseite in den UTF-8-Zeichensatz, damit Sie in Ihren Marketing-Berichten eine beliebige Sprache verwenden können. </p> <p>Wenden Sie sich an Ihren Kundenbetreuer oder an den Kundendienst, wenn die Multibytezeichenunterstützung für eine Report Suite geändert werden soll. </p> </td> 
  </tr>  
 </tbody> 
</table>
