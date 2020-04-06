---
description: Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.
title: Neue Report Suite – Einstellungen
topic: Admin tools
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Neue Report Suite – Einstellungen

Sie können eine neue Report Suite erstellen, indem Sie eine vordefinierte Vorlage auswählen oder eine Ihrer vorhandenen Report Suites als Modell verwenden.

Beschreibung der verwendeten Elemente beim [Erstellen einer Report Suite](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md).

>[!NOTE] In der [Dokumentation zur Virtual Report Suite](/help/components/vrs/c-workflow-vrs/vrs-create.md) erfahren Sie, wie Sie Virtual Report Suites erstellen.

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
   <td colname="col2"> <p>Gibt eine eindeutige ID an, die nur alphanumerische Zeichen enthalten darf. Diese ID kann nach der Erstellung nicht mehr geändert werden. Adobe legt das erforderliche ID-Präfix fest und kann auch nicht geändert werden. </p> <p>Stellen Sie beim Erstellen mehrerer Report Suites sicher, dass die von Ihnen verwendete Benennungsregel eindeutige Report Suite-IDs gewährleistet. </p> </td> 
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
   <td colname="col2"> (Optional) Definiert die Basisdomäne für die Report Suite. Diese URL fungiert als interner URL-Filter, wenn Sie für die Report Suite keine expliziten internen URL-Filter definieren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Standardseite</span> </td> 
   <td colname="col2"> <p>(Optional) Bereinigt Vorkommnisse des Werts <span class="wintitle">Standardseite</span> von den dabei auftretenden URL-Adressen. Wenn der Bericht <span class="wintitle">Bevorzugte Seiten</span> URLs statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Webseite mehrere URLs angegeben werden. </p> <p>Beispielsweise sind die URLs <span class="filepath">https://meinsesite.com</span> und <span class="filepath">https://meinesite.com/index.html</span> normalerweise dieselben Seiten. Sie können irrelevante Dateinamen entfernen, sodass beide URL-Adressen in den Berichten als <span class="filepath">https://meinesite.com</span> angezeigt werden. </p> <p>Wenn Sie diesen Wert nicht angeben, entfernt Analytics automatisch die folgenden Dateinamen aus den URLs: <span class="filepath">index.htm</span>, <span class="filepath">index.html</span>, <span class="filepath">index.cgi</span>, <span class="filepath">index.asp</span>, <span class="filepath">default.htm</span>, <span class="filepath">default.html</span>, <span class="filepath">default.cgi</span>, <span class="filepath">default.asp</span>, <span class="filepath">home.htm</span>, <span class="filepath">home.html</span>, <span class="filepath">home.cgi</span> und <span class="filepath">home.asp</span>. </p> <p>Um das Entfernen von Dateinamen zu deaktivieren, geben Sie einen Wert für die Standardseite an, der in Ihren URLs nicht vorkommt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aufschaltdatum </p> </td> 
   <td colname="col2">Informiert Adobe über das Datum, ab dem diese Report Suite aktiv sein soll. Wenn sich der Implementierungsplan ändert, müssen Sie mithilfe des Tools <span class="wintitle">Dauerhaft erwarteter Traffic</span> in <a href="/help/admin/c-traffic-management/traffic-management.md">Traffic-Management</a> eine aktualisierte Traffic-Schätzung eingeben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Geschätzte Seitenansichten pro Tag</span> </td> 
   <td colname="col2"> Identifiziert die geschätzte Anzahl der Seitenzahlen, die diese Report Suite pro Tag unterstützen soll. Große Traffic-Volumes erfordern einen längeren Genehmigungsprozess. Um Verzögerungen bei der Verarbeitung zu vermeiden, sollten Sie bei dieser Schätzung so genau wie möglich sein. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Basiswährung</span> </td> 
   <td colname="col2"> <p>Gibt die Standardwährung an, in der alle Währungsdaten gespeichert werden. Analytics Berichte konvertiert Transaktionen in anderen Währungen in die Basiswährung, wobei der aktuelle Konversionsrate zum Zeitpunkt des Eingangs der Daten verwendet wird. </p> <p> Die Analytics-Berichterstellung verwendet die <span class="varname"> currencyCode</span>-JavaScript-Variable, um die Währung einer Transaktion zu bestimmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Multibytezeichenunterstützung deaktivieren </span> </td> 
   <td colname="col2"> <p>Deaktiviert die Multibyte-Zeichenunterstützung für die Report Suite. Wenn Sie die Multibyte-Zeichenunterstützung deaktivieren, geht das System davon aus, dass die Daten im ISO-8859-1-Format vorliegen. Auf Webseiten muss der Zeichensatz in der JavaScript-Variablen <span class="varname"> „charSet“</span> angeben. </p> <p>Die Multibyte-Zeichenunterstützung speichert Zeichen in der Report Suite mit UTF-8. Nach Eingang konvertiert das System Daten aus dem Zeichensatz Ihrer Webseite in den UTF-8-Zeichensatz, damit Sie in Ihren Marketing-Berichten jede Sprache verwenden können. </p> <p>Wenden Sie sich an Ihren Kundenbetreuer oder die Kundenunterstützung, um die Multibyte-Zeichenunterstützung für eine Report Suite zu ändern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="wintitle"> Ad Hoc Analysis für diese Suite aktivieren</span> </td> 
   <td colname="col2"> Aktiviert die Anzeige dieser Report Suite, wenn Sie Ad Hoc Analysis durchführen. </td> 
  </tr> 
 </tbody> 
</table>

