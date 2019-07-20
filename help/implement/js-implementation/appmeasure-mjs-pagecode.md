---
description: In diesem Abschnitt finden Sie Beispielcode für Ihre Core-JavaScript-Datei und die Seiten auf Ihrer Website.
keywords: Analytics-Implementierung; appmeasurement. js code; Beispiel-Seitencode
seo-description: In diesem Abschnitt finden Sie Beispielcode für Ihre Core-JavaScript-Datei und die Seiten auf Ihrer Website.
seo-title: Beispiel-Seitencode und globale Konfiguration
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Beispiel-Seitencode und globale Konfiguration
topic: Entwickler und Implementierung
uuid: e 8880 d 77-172 b -42 e 5-8187-ce 371 aa 9 sf 9
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Beispiel-Seitencode und globale Konfiguration

In diesem Abschnitt finden Sie Beispielcode für Ihre Core-JavaScript-Datei und die Seiten auf Ihrer Website.

>[!IMPORTANT]
>
>This example uses the visitor ID service, which is deployed as part of your [JavaScript Implementation](../../implement/js-implementation/javascript-implementation-overview.md). Wenn Sie den Besucher-ID-Service in AppMeasurement aktivieren, bevor Sie die Besucher-API-JavaScript-Datei auf allen Webseiten eingebunden haben, hat dies möglicherweise doppelte Besucherzählungen zur Folge. Um doppelte Besucherzählungen zu vermeiden, befolgen Sie den unter [Besucher-ID-Service](../../implement/js-implementation/c-unique-visitors/visid-service.md#concept_230F8759826E47789EA8DEE08FA09B07).

## Beispielcode für AppMeasurement.js {#section_4351543F2D6049218E18B48769D471E2}

>[!IMPORTANT]
>
>Configuration variables should be set above the *`doPlugins`* function.

Bei neuen Implementierungen können Sie zum Einstieg den folgenden globalen Konfigurationscode am Anfang von AppMeasurement.js einfügen:

```js
//initialize AppMeasurement 
var s_account="INSERT-RSID-HERE" 
var s=s_gi(s_account) 
 
/******** VISITOR ID SERVICE CONFIG - REQUIRES VisitorAPI.js ********/ 
s.visitor=Visitor.getInstance("INSERT-MCORG-ID-HERE") 
 
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
/* Link Tracking Config */ 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.trackInlineStats=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx" 
s.linkInternalFilters="javascript:" //optional: add your internal domain here 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
 
/* uncomment below to use doPlugins */ 
/* s.usePlugins=true 
function s_doPlugins(s) { 
 
// use implementation plug-ins that are defined below 
// in this section. For example, if you copied the append 
// list plug-in code below, you could call: 
// s.events=s.apl(s.events,"event1",",",1); 
 
} 
s.doPlugins=s_doPlugins */ 
 
/* WARNING: Changing any of the below variables will cause drastic 
changes to how your visitor data is collected.  Changes should only be 
made when instructed to do so by your account manager.*/ 
s.trackingServer="INSERT-TRACKING-SERVER-HERE" 
s.trackingServerSecure="INSERT-SECURE-TRACKING-SERVER-HERE" 
 
/************************** PLUGINS SECTION *************************/ 
 
// copy and paste implementation plug-ins here - See "Implementation Plug-ins" @ 
// https://marketing.adobe.com/resources/help/en_US/sc/implement/#Implementation_Plugins 
// Plug-ins can then be used in the s_doPlugins(s) function above  
 
/****************************** MODULES *****************************/ 
 
// copy and paste implementation modules (Media, Integrate) here 
// AppMeasurement_Module_Media.js - Media Module, included in AppMeasurement zip 
// AppMeasurement_Module_Integrate.js - Integrate Module, included in AppMeasurement zip 
 
/* ============== DO NOT ALTER ANYTHING BELOW THIS LINE ! ===============  
```

## Beispiel-Seiten-Code {#section_042412C29CC249E298F19B2BC2F43CE7}

Bei neuen Implementierungen können Sie den folgenden Seiten-Code direkt nach dem Öffnen einfügen. <body> -tag auf Seiten, die Sie verfolgen möchten:

```js
<script language="JavaScript" type="text/javascript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.channel="" 
s.pageType="" 
s.prop1="" 
s.prop2="" 
s.prop3="" 
s.prop4="" 
s.prop5="" 
/* Conversion Variables */ 
s.campaign="" 
s.state="" 
s.zip="" 
s.events="" 
s.products="" 
s.purchaseID="" 
s.eVar1="" 
s.eVar2="" 
s.eVar3="" 
s.eVar4="" 
s.eVar5="" 
var s_code=s.t();if(s_code)document.write(s_code)//--></script>
```

Stellen Sie sicher, dass Sie auf jeder Seite stets auf `AppMeasurement.js` und `VisitorAPI.js` verweisen. See [JavaScript Implementation](../../implement/js-implementation/javascript-implementation-overview.md) for instructions.
