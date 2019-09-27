---
description: 'null'
seo-description: 'null'
seo-title: Implementierungs-Roadmap
title: Implementierungs-Roadmap
uuid: 988bcca5-67ae-4e3f-97e6-6a42030b1962
translation-type: tm+mt
source-git-commit: 3c5cc9275c9978caf57e4e29704e23405ac24b65

---


# Implementierungs-Roadmap

## Neue Benutzer {#section_77433E4FC5ED4C6BAFC1E72EB61C4503}

Wenn Sie mit Adobe Analytics noch nicht vertraut sind, können Sie mithilfe des Leitfadens [Erste Schritte – Adobe Analytics](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/) schnell Ihre erste Analytics Report Suite (Datenrepository) erstellen. Then, you can deploy Analytics code using [Experience Platform Launch](https://docs.adobelaunch.com/).

## Implementierungs-Roadmap {#section_E3DD8D199B744FFB9E9B386A44220206}

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
   <td colname="col1"> Implementierungsmethode auswählen. </td> 
   <td colname="col2"> <p>Zu den verbreiteten Methoden der Implementierung von Analytics gehören: </p> <p> 
     <ul id="ul_A7475867861540EFBD77AEE8C6DAD418"> 
      <li id="li_035E2619670F4D04A7F708625A9C01EF"> <a href="https://docs.adobelaunch.com/" format="https" scope="external"> Experience Platform Launch </a> (Recommended) <p>In diesem Leitfaden erfahren Sie alles, was Sie über die Verwendung der Adobe-Verwaltungsfunktionen für Website-Tags und mobile SDKs wissen müssen, und wie Sie diese implementieren können. </p> </li> 
      <li id="li_996FA2F5B0E149399CED391AB5235D8A"> <a href="../../implement/c-implement-with-dtm/dtm-implementation-overview.md" format="dita" scope="local"> Dynamic Tag Management </a> <p>Dieser Leitfaden enthält spezifische Informationen zu Analytics, um Sie durch eine Implementierung des Dynamic Tag Managements zu führen. </p> </li> 
      <li id="li_18E6AD6D864246D0BA26DAA1D91DD811"> <a href="../../implement/js-implementation/javascript-implementation-overview.md" format="dita" scope="local"> JavaScript </a> <p>Dieser Leitfaden enthält eine Beschreibung der Datenerfassungsvariablen und Details zur Implementierung von Code zur Datenerfassung in JavaScript, einschließlich <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/video/video_js.html" format="https" scope="external">Video </a>. </p> </li> 
      <li id="li_85EC7A0AC5E04EE6981ED72A88C5D1FD"> <a href="https://marketing.adobe.com/resources/help/en_US/reference/developer.html" format="html" scope="external"> Analytics-SDKs </a> <p>Verwenden Sie Analytics-SDKs zur Verwaltung von: </p> <p> 
        <ul id="ul_F67F2E1964724800A84445A36DFB8E86"> 
         <li id="li_9C43F051EB5B4EA7A4C14EC1513DB824"> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/ios/analytics_main.html" format="html" scope="external"> Mobilen Apps auf iOS </a> </li> 
         <li id="li_4354E44EB8B3494A88578C1621EF5BAC"> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/android/analytics_main.html" format="html" scope="external"> Mobilen Apps auf Android </a> </li> 
        </ul> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step2_icon.png" id="image_02CFDC007BF1486AA312698EBFFA79F7" /> </td> 
   <td colname="col1"> Set up the Identity Service. </td> 
   <td colname="col2"> <p>(Formerly <span class="term"> Visitor ID service </span>.) See  Set Up the Identity Service for Analytics .<a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html" format="https" scope="external"></a> </p> 
    <draft-comment> 
     <p>Fügen Sie am Anfang der Datei <code>VisitorAPI.js</code> den folgenden Besucher-ID-Initialisierungscode hinzu: </p> 
     <code class="syntax javascript">
       var visitor = Visitor.getInstance("INSERT-MCORG-ID-HERE"); 
      visitor.trackingServer = "INSERT-TRACKING-SERVER-HERE"; // same as s.trackingServer 
      visitor.trackingServerSecure = "INSERT-SECURE-TRACKING-SERVER-HERE"; //same as s.trackingServerSecure 
      /* 
       ============== DO NOT ALTER ANYTHING BELOW THIS LINE ! ============
     </code> 
     <ul id="ul_769BA118CC244308A805079C2CBECC12"> 
      <li id="li_D366EBDE24CB433EA523DB228CB2FAF1"> <code> "INSERT-MCORG-ID-HERE" </code> - (Erforderlich) Diese Adobe Experience Cloud-Organisations-ID wird an Ihren Administrator gesendet, wenn Ihr Unternehmen für die Adobe Experience Cloud bereitgestellt wird. </li> 
      <li id="li_4F9704A6A6EA4334A3758F99B8D67C9D"> <code> "INSERT-TRACKING-SERVER-HERE"</code> (Erforderlich): Ihr Analytics-Trackingserver. </li> 
      <li id="li_C578420458D649228E54D9809AF62627"> <code> "INSERT-SECURE-TRACKING-SERVER-HERE"</code> – (Erforderlich, wenn SSL aktiviert ist) Ihr sicherer Analytics-Trackingserver. </li> 
     </ul> 
    </draft-comment> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step3_icon.png" id="image_76B61DEABE3849CCB39135FDD7399EAA" /> </td> 
   <td colname="col1"> Verwenden Sie die ausgewählte Implementierungsmethode zum Aktualisieren und Bereitstellen von Seiten-Code. </td> 
   <td colname="col2"> <p>Fügen Sie den Seiten-Code auf jeder nachzuverfolgenden Seite direkt nach dem öffnenden <code>&lt;body&gt;</code>-Tag ein. Aktualisieren Sie mindestens die folgenden Variablen: </p> 
    <ul id="ul_29200A6E8DA14386BDA242AD8B270FEB"> 
     <li id="li_FB24D2CB9241401A83BD13EE342A7810"> <code> var s=s_gi("INSERT-RSID-HERE") </code> </li> 
     <li id="li_463A35BA06CC4618B4AF17CD7E83AED5"> <code> s.pageName="INSERT-NAME-HERE" // for example, s.pageName=document.title </code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step4_icon.png" id="image_B255E5EAE7BB43FC946D0E9DFCA83003" /> </td> 
   <td colname="col1"> Validieren Sie die Implementierung. </td> 
   <td colname="col2"> <p>  Unter <a href="../../implement/impl-testing/impl-validation/impl-validation.md" format="dita" scope="local">Test und Validierung</a> erhalten Sie Informationen zur Validierung Ihrer Implementierung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <img  src="assets/step5_icon.png" id="image_844E896941E2489A943BE10AD710ED36" /> </td> 
   <td colname="col1"> Prüfen Sie mit dem Adobe Experience Cloud-Debugger, ob Daten gesendet werden. </td> 
   <td colname="col2"> <p>Install the <a href="../../implement/impl-testing/debugger.md#topic_E05CEAF0682E483A9AB147D774CF2188" format="dita" scope="local"> Experience Cloud Debugger </a>. Laden Sie anschließend eine Seite, auf der Sie den Seiten-Code bereitgestellt haben, und öffnen Sie den Debugger. Der Debugger zeigt Information darüber an, welche erfassten Daten gesendet wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Weitere Info {#section_64B6A948DF4A4B5E9E1D22549F8C508B}

For information about the differences between Experience Platform Launch, Dynamic Tag Management, and JavaScript methods, see Choose an Implementation Method.[](../../implement/c-implementation-methods/choose-implementation-method.md#concept_97CE27B16410422EB28B4B9CE3B9529B)

Einen kurzen Überblick über die ersten Schritte und die schnelle Einrichtung Ihrer ersten Analytics-Report Suite finden Sie unter [Erste Schritte mit der Analytics-Implementierung](https://marketing.adobe.com/resources/help/en_US/dtm/get_started.html) im Leitfaden zu den ersten Schritten mit Analytics.
