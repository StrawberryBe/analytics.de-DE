---
description: Beim Migrieren von Besuchern wird das Besucher-ID-Cookie von einer Domäne zu einer anderen migriert.
keywords: Analytics Implementation
title: Besuchermigration
topic: Developer and implementation
uuid: af31928c-85d7-407f-a583-0c8f2852ceb3
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# Besuchermigration

Beim Migrieren von Besuchern wird das Besucher-ID-Cookie von einer Domäne zu einer anderen migriert.

Besuchermigration lässt Sie die Cookies zur Identifizierung von Besuchern beibehalten, wenn Sie die Datenerfassungsdomänen ändern. Das Ändern von Datenerfassungsdomänen kann die folgenden Gründe haben:

* Wechsel von `2o7.net` auf `omtrdc.net` ([regionale Datenerfassung](https://marketing.adobe.com/resources/help/de_DE/whitepapers/rdc/)).

* Sie implementieren den [Experience Cloud-Besucher-ID-Dienst](https://marketing.adobe.com/resources/help/de_DE/mcvid/) und wechseln von einer Datenerfassungsdomäne mit CNAME-Eintrag/Erstanbieterkontext zu `2o7.net` oder `omtrdc.net` ([regionale Datenerfassung](https://marketing.adobe.com/resources/help/de_DE/whitepapers/rdc/)).

* Wechsel von `2o7.net` oder `omtrdc.net` zu einer Datenerfassungsdomäne mit CNAME-Eintrag/Erstanbieterkontext ([Erstanbieter-Cookies](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-first-party.translate.html)).

* Wechsel von einem CNAME zu einem anderen (Domänenwechsel).

Nach der Konfiguration der Migration von Besuchern leitet der Server, wenn ein Benutzer die neue Domäne ohne Besucher-ID-Cookie besucht, zum vorherigen Datenerfassungshostnamen um, ruft alle verfügbaren Besucher-ID-Cookies ab und leitet dann zur neuen Domäne zurück. Wenn für den vorherigen Hostnamen keine Besucher-ID gefunden wird, wird eine neue ID generiert. Dies geschieht nur einmal pro Besucher.

## Migrieren von Besuchern {#section_FF0C5C5CAEF343FFA1892B29311F7160}

In der folgenden Tabelle werden die für die Migration von Besuchern erforderlichen Aufgaben Liste:

<table id="table_7B2535FC3E264216A299686415C6B21C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Aufgabe </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Zu Beginn:</b> <a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html"  >Wenden Sie sich an den Kundendienst</a>, und teilen Sie die Domäne(n) mit, die migriert werden sollen, sowie den Migrationszeitraum, der aktiviert werden soll (30, 60 oder 90 Tage). Stellen Sie sicher, dass die nicht sicheren Domänen einbezogen werden. </p> </td> 
   <td colname="col3"> <p>Erstellen Sie eine Liste mit der <i>exakten</i> Syntax für die Domänen, zu denen Sie migrieren und von denen Sie migrieren möchten. </p> 
    <ul id="ul_067EC5C7619141A6BDFBC209C9FD47E2"> 
     <li id="li_0723D948465A49C1871B81207AEDC4DC">example.112.2o7.net &gt; metrics.example.com </li> 
     <li id="li_B0CA15A593BD4AB9802E33A3FF037C7A">example.102.112.2o7.net &gt; smetrics.example.com </li> 
    </ul> <p>Die Hostnamen für die Migration werden auf dem Adobe-Datenerfassungsserver konfiguriert. Die Kundenunterstützung informiert Sie darüber, wann die Änderung vorgenommen wurde, damit Sie den nächsten Schritt planen können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>6 und mehr Stunden nach dem Konfigurationswechsel</b>: Aktualisieren Sie die Variablen <code> s.trackingServer</code> und <code> s.trackingServerSecure</code> in Ihrem Analytics JavaScript-Code, um die neuen Datenerfassungsserver zu verwenden. </p> </td> 
   <td colname="col3"> <p>After you make this change, use a <a href="../implement/validate/packet-monitor.md"> packet monitor</a> to verify that the Analtyics image request is going to the updated data collection server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Sofort nach Aktualisierung Ihres Analytics-Codes</b>: Testen Sie Ihre Site, um sicherzustellen, dass die Umleitung zur vorherigen Datenerfassungsdomäne erfolgt. </p> </td> 
   <td colname="col3"> <p>Use a <a href="../implement/validate/packet-monitor.md"> packet monitor</a> to verify that when you access your site for the first time, or after clearing cookies, you see two 302 (redirect) HTTP status codes before the 200 (OK) HTTP status code. Wenn eine dieser Umleitungen fehlschlägt, wenden Sie sich sofort an den Kundendienst, um sicherzustellen, dass die Migration korrekt konfiguriert ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Für den gesamten Migrationszeitraum</b>: Lassen Sie den DNS-Datensatz für den vorherigen Hostnamen aktiv. </p> </td> 
   <td colname="col3"> <p>Der vorherige Hostname muss über DNS aufgelöst werden, sonst tritt keine Cookie-Migration auf. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Variablen „visitorMigrationKey“ und „visitorMigrationServer“ veraltet {#section_32FCEE2575944D039EA0FEBFB5814259}

Ab März 2013 wird die Verwendung der Datenerfassungsvariablen `visitorMigrationServer`, `visitorMigrationKey` und `visitorMigrationServerSecure` eingestellt. Die bisher in diesen Variablen enthaltenen Daten werden aus Sicherheitsgründen auf Servern von Adobe gespeichert.
