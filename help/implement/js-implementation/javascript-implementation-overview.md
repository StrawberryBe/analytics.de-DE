---
description: Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.
keywords: Analytics-Implementierung; javascript; Javascript-Implementierung; appmeasurement; Appmeasurement herunterladen; Identitätsdienst; visitorapi. js; caching; Appmeasurement-Komprimierung
seo-description: Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.
seo-title: Übersicht über javascript-Implementierung
solution: Analytics
title: Übersicht über javascript-Implementierung
topic: Entwickler und Implementierung
uuid: bb 661 d 8 c-faf 9-4454-ac 3 c -0 c 1 a 4 c 0 a 9336
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Übersicht über javascript-Implementierung

Damit Analytics mit der Arbeit beginnen kann, müssen Daten, die in Berichten angezeigt werden sollen, an eine Report Suite gesendet werden.

The easiest and recommended way to send data to [!DNL Analytics] is by using [Dynamic Tag Management](../../implement/c-implement-with-dtm/dtm-implementation-overview.md). In einigen Fällen bevorzugen Sie eventuell die ältere JavaScript-Methode zur Implementierung von Analytics.

>[!NOTE]
>
>In diesem Abschnitt wird die alte Methode zur Implementierung von Analytics beschrieben. Alle Analytics-Kunden haben Zugriff auf das [Dynamic Tag Management](https://marketing.adobe.com/resources/help/en_US/dtm/), wobei es sich um die Standardmethode für das Bereitstellen von Experience Cloud-Tags handelt.

## Implementierungsschritte {#section_73961BAD5BB4430A95E073DE5C026277}

Um eine Seite mit Code zur Erfassung von Daten erfolgreich zu implementieren, müssen Sie über Zugriff auf Ihre Hostingserver verfügen, um neue Inhalte auf Ihre Website hochladen zu können. Außerdem ist es auch nützlich, wenn für die Implementierung von Code bereits eine Site vorhanden ist. 

Anhand der folgenden Schritte werden Sie durch eine grundlegende Analytics-Implementierung geführt.

<table id="table_1683413EA0E34DBC9291832647B68E96"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Schritt </th> 
   <th colname="col1" class="entry"> Aufgabe </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <img  src="assets/step1_icon.png" id="image_21F30BBFC0A249F8B0E1A50EBBEED77D" /> </td> 
   <td colname="col1"> Laden Sie AppMeasurement für JavaScript und den Besucher-ID-Service herunter. </td> 
   <td colname="col2"> <p>Der Download ist im <a href="https://marketing.adobe.com/resources/help/en_US/reference/?f=code_manager_admin" format="http" scope="external"> Code-Manager </a> verfügbar. </p> <p>Die ZIP-Datei zum Download enthält mehrere Dateien. <code> AppMeasurement.js </code> und <code> VisitorAPI.js </code> sind zum Implementieren von Analytics relevant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step2_icon.png" id="image_02CFDC007BF1486AA312698EBFFA79F7" /> </td> 
   <td colname="col1"> Richten Sie den Identitätsdienst ein. </td> 
   <td colname="col2"> <p>(Formerly <span class="term"> Visitor ID service </span>.) See <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html" format="https" scope="external"> Set Up the Identity Service for Analytics </a>. </p> 
    <draft-comment> 
     <p>Fügen Sie am Anfang der Datei <code> VisitorAPI.js </code> den folgenden Besucher-ID-Initialisierungscode hinzu: </p> 
     <code class="syntax javascript">
     var visitor = Visitor.getinstance("INSERT-MCORG-ID-HERE");
     visitor.trackingServer = "INSERT-TRACKING-SERVER-HERE"; // gleichen wie s.trackingServer visitor.trackingServerSecure = "INSERT-SECURE-TRACKING-SERVER-HERE"; //same as s.trackingServerSecure /* == DO NOT ALTER ANYTHING BELOW THIS LINE ==
     </code> 
     <ul id="ul_769BA118CC244308A805079C2CBECC12"> 
      <li id="li_D366EBDE24CB433EA523DB228CB2FAF1"> <code> " INSERT-MCORG-ID-HERE " </code> - (Erforderlich) Diese Adobe Experience Cloud-Organisations-ID wird an Ihren Administrator gesendet, wenn Ihr Unternehmen für die Adobe Experience Cloud bereitgestellt wird. </li> 
      <li id="li_4F9704A6A6EA4334A3758F99B8D67C9D"> <code> "INSERT-TRACKING-SERVER-HERE" </code> - (Erforderlich) Ihr Analytics-Trackingserver. </li> 
      <li id="li_C578420458D649228E54D9809AF62627"> <code> "INSERT-SECURE-TRACKING-SERVER-HERE" </code> – (Erforderlich, wenn SSL aktiviert ist) Ihr sicherer Analytics-Trackingserver. </li> 
     </ul> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step3_icon.png" id="image_76B61DEABE3849CCB39135FDD7399EAA" /> </td> 
   <td colname="col1"> Aktualisieren Sie <code> AppMeasurement.js </code>. </td> 
   <td colname="col2"> <p>Kopieren Sie den <a href="../../implement/js-implementation/appmeasure-mjs-pagecode.md#section_4351543F2D6049218E18B48769D471E2" format="dita" scope="local"> Beispielcode für AppMeasurement.js</a>, und fügen Sie ihn am Anfang der Datei <code> AppMeasurement.js </code> ein. Aktualisieren Sie mindestens die folgenden Variablen: </p> 
    <ul id="ul_62FA640BD2604E589650A92158272615"> 
     <li id="li_54E56B483B3A416EA27D7B540D60E39F"> <code> s.account="INSERT-RSID-HERE" </code> </li> 
     <li id="li_00A958289BB045379B436F13287E03D5"> <code> s.trackingServer="INSERT-TRACKING-SERVER-HERE" </code> </li> 
     <li id="li_C0779ADF780440ED876236AEB1FB5DCC"> <code> s.visitorNamespace = "INSERT-NAMESPACE-HERE" </code> </li> 
     <li id="li_93072B656C134D8C89195B7F2D7D8F05"> <code> s.visitor = Visitor.getInstance("INSERT-MCORG-ID-HERE") </code> </li> 
    </ul> <p> See <a href="https://helpx.adobe.com/analytics/kb/determining-data-center.html" format="https" scope="external"> Correctly populate the trackingServer and trackingServerSecure variable </a> or contact Client Care if you are unsure about any of these values. Wenn diese nicht korrekt eingestellt sind, werden Daten nicht von Ihrer Implementierung erfasst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step4_icon.png" id="image_B255E5EAE7BB43FC946D0E9DFCA83003" /> </td> 
   <td colname="col1"> Definieren Sie einen Host für <code> AppMeasurement.js </code> und <code> VisitorAPI.js </code>. </td> 
   <td colname="col2"> <p>Diese Core-JavaScript-Dateien müssen auf einem Webserver gehostet werden, der für alle Seiten Ihrer Website zugänglich ist. Für den nächsten Schritt benötigen Sie den Pfad zu den Dateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step5_icon.png" id="image_844E896941E2489A943BE10AD710ED36" /> </td> 
   <td colname="col1"> Verweisen Sie auf allen Seiten der Website auf <code> AppMeasurement.js </code> und <code> VisitorAPI.js </code>. </td> 
   <td colname="col2"> <p> Integrieren Sie den Besucher-ID-Service, indem Sie dem Tag <code> &lt;head&gt; </code> oder &lt;body&gt; auf jeder Seite die folgende Codezeile hinzufügen. <code> VisitorAPI.js </code> muss vor <code> AppMeasurement.js </code> integriert werden : </p> 
    <code class="syntax html"> &lt;script language="javascript" type="text/javascript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/VisitorAPI.js"&gt;&lt;/script &gt; </code>
  <p> Integrieren Sie den AppMeasurement für JavaScript, in dem Sie dem Tag <code> &lt;head&gt; </code> oder <code> &lt;body&gt; </code> auf jeder Seite die folgende Codezeile hinzufügen: </p> 
    <code class="syntax html"> &lt;script language="javascript" type="text/javascript" src="https://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/AppMeasurement.js"&gt;&lt;/script&gt; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step6_icon.png" id="image_1C4293CA98F04EE2ADA69EAB95BDE8B1" /> </td> 
   <td colname="col1"> Aktualisieren Sie den Seiten-Code, und stellen Sie ihn bereit. </td> 
   <td colname="col2"> <p>Kopieren Sie den <a href="../../implement/js-implementation/appmeasure-mjs-pagecode.md#section_042412C29CC249E298F19B2BC2F43CE7" format="dita" scope="local">Beispiel-Seiten-Code</a>, und fügen Sie ihn auf den nachzuverfolgenden Seiten direkt nach dem öffnenden <code> &lt;body&gt; </code> -Tag ein. Aktualisieren Sie mindestens die folgenden Variablen: </p> 
    <ul id="ul_29200A6E8DA14386BDA242AD8B270FEB"> 
     <li id="li_FB24D2CB9241401A83BD13EE342A7810"> <code> var s=s_gi("INSERT-RSID-HERE") </code> </li> 
     <li id="li_463A35BA06CC4618B4AF17CD7E83AED5"> <code> s.pageName="INSERT-NAME-HERE" // for example, s.pageName=document.title </code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step7_icon.png" id="image_A423CBF386AF4E5986E8CBB6E31CD3E5" /> </td> 
   <td colname="col1"> Prüfen Sie mit dem DigitalPulse-Debugger, ob Daten gesendet werden. </td> 
   <td colname="col2"> <p>Installieren Sie das   <a href="../../implement/impl-testing/debugger.md#concept_B26FFE005EDD4E0FACB3117AE3E95AA2" format="dita" scope="local"> Adobe Debugger</a>-Bookmarklet. Laden Sie anschließend eine Seite, auf der Sie den Seiten-Code bereitgestellt haben, und öffnen Sie den Debugger. Der Debugger zeigt Information darüber an, welche erfassten Daten gesendet wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zwischenspeicherung {#section_4E2D1D962DF046418134C43CFC49AD4A}

Die JavaScript-Datei wird nach dem ersten Laden im Browser des Besuchers zwischengespeichert und in der Regel nur ein Mal pro Sitzung heruntergeladen. Die Datei wird nicht für jede Seite erneut heruntergeladen, selbst wenn sie auf jeder Seite der Website verwendet wird. Auf den meisten Websites rufen Benutzer im Durchschnitt mehr als nur ein paar Seitenansichten pro Sitzung auf. Somit kann durch die Übertragung von mehrfach verwendetem JavaScript in diese Datei die insgesamt heruntergeladene Datenmenge reduziert werden.

## Komprimierung bei JavaScript für AppMeasurement {#section_C10BBC84C81C414088F97363D29E021B}

Wenn Sie die Seitengröße mit H-Code reduzieren möchten(AppMeasurement für JavaScript 1.0 ist vorkomprimiert), empfiehlt Adobe, die Datei mittels GZIP zu komprimieren. GZIP wird in allen gängigen Browsern unterstützt und bietet beim Packen und Entpacken der JavaScript-Hauptdatei [!DNL s_code.js] eine höhere Performance als die JavaScript-Komprimierung.

Unter den folgenden Links wird erklärt, wie Sie die Komprimierung des [!DNL s_code.js]-JavaScript-Codes auf Ihrer Website per GZIP durchführen können:

[Apache Module mod_deflate](https://httpd.apache.org/docs/2.0/mod/mod_deflate.html) (in englischer Sprache)

[Enabling gzip compression with Tomcat and Flex](https://www.cubicleman.com/2007/04/06/enabling-gzip-compression-with-tomcat-and-flex/) (in englischer Sprache)
