---
description: JavaScript-Plug-ins werden in der Regel von der doPlugins-Funktion aufgerufen, die beim Aufruf der t()-Funktion im einzufügenden Code ausgeführt wird.
keywords: Analytics-Implementierung
seo-description: JavaScript-Plug-ins werden in der Regel von der doPlugins-Funktion aufgerufen, die beim Aufruf der t()-Funktion im einzufügenden Code ausgeführt wird.
seo-title: Aufruf von Plug-ins mit doplugins-Funktion
solution: Analytics
subtopic: Plug-ins
title: Aufruf von Plug-ins mit doplugins-Funktion
topic: Entwickler und Implementierung
uuid: 95 dd 01 de -8136-4 ec 9-aac 9-4 a 3 d 371 b 839
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Aufruf von Plug-ins mit doplugins-Funktion

JavaScript-Plug-ins werden in der Regel von der doPlugins-Funktion aufgerufen, die beim Aufruf der t()-Funktion im einzufügenden Code ausgeführt wird.

Consequently, if you set a variable in the *`doPlugins`* function, you can overwrite a variable you set on the HTML page. The only time the *`doPlugins`* function is not called is when the [!UICONTROL usePlugins] variable is set to 'false.'

## Codebeispiel {#section_6940FD16F2E94753A1C39694D0CF5FBA}

The code example below is what the *`doPlugins`* function looks like in your JavaScript file:

AppMeasurement für JavaScript:

```js
/* Plugin Config */ 
s.usePlugins=true 
s.doPlugins=function(s) { 
 /* Add calls to plugins here */ 
}
```

H-Code:

```js
/* Plugin Config */ 
s.usePlugins=true 
function s_doPlugins(s) { 
 /* Add calls to plugins here */ 
} 
s.doPlugins=s_doPlugins
```

>[!NOTE]
>
>H-Code und frühere Versionen verwenden eine andere Syntax, um einige sehr alte Browser zu unterstützen (z. B. IE 4 und 5).

## Renaming the doPlugins Function {#section_70B7D58E057B48058E25907AB3726725}

The *`doPlugins`* function is typically called *`s_doPlugins`*. In certain circumstances, (usually when more than one version of code may appear on a single page) the *`doPlugins`* function name may be changed. If the standard *`doPlugins`* function needs to be renamed to avoid conflicts, ensure that *`doPlugins`* is assigned the correct function name, as shown in the example below.

```js
/* Plugin Config */ 
s_mc.usePlugins=true 
function s_mc_doPlugins(s_mc) { 
 /* Add calls to plugins here */ 
} 
s_mc.doPlugins=s_mc_doPlugins 
```

## Verwenden von doPlugins {#section_FA5D901CC5214D54BCD08AB77BED7925}

The *`doPlugins`* function provides an easy way to give default values to variables or to take values from [!UICONTROL query string parameters] on any page of the site. Using *`doPlugins`* is often easier than populating the values in the HTML page because only one file must be updated. Denken Sie jedoch immer daran, dass Änderungen, die Sie in der JavaScript-Datei vornehmen, nicht immer sofort wirksam werden. Wiederkehrende Besucher verwenden häufig zwischengespeicherte Versionen der JavaScript-Datei aus ihren Webbrowsern. Das bedeutet, dass in der Datei vorgenommene Aktualisierungen nicht bei allen Besuchern sofort übernommen werden – in einigen Fällen kann das bis zu einem Monat dauern.

Das nächste Beispiel zeigt, wie mithilfe der *`doPlugins`*-Funktion ein Standardwert für eine Variable festgelegt und ein Wert aus der Abfragezeichenfolge abgerufen wird.

```js
/* Plugin Config */ 
s.usePlugins=true 
s.doPlugins=function(s) { 
 /* Add calls to plugins here */ 
 // if prop1 doesn't have a value, set it to "Default Value" 
 if(!s.prop1) 
s.prop1="Default Value" 
 
 // if campaign doesn't have a value, get cid from the query string 
 if(!s.campaign) 
s.campaign=s.getQueryParam('cid'); 
 
// Note: The code to read query parameters is different for  
// Appmeasurement for JavaScript since a plug-in is not required: 
// s.campaign=s.Util.getQueryParam('cid'); 
} 
```

## Installierte Plug-ins {#section_C5494347D85940A78670032199787CD0}

Wenn Sie wissen möchten, ob ein bestimmtes Plug-in in Ihrer JavaScript-Datei enthalten ist und verwendet werden kann, schauen Sie in den Abschnitt [!UICONTROL Plug-ins] der JavaScript-Datei. Das nächste Beispiel zeigt die [!UICONTROL getQueryParam]-Funktion.

```js
/************************** PLUGINS SECTION *************************/ 
/* You may insert any plugins you wish to use here.                 */ 
/* 
 * Plugin: getQueryParam 1.3 - Return query string parameter values 
 */ 
s.getQueryParam=new Function("qp","d","" 
+"var s=this,v='',i,t;d=d?d:'';while(qp){i=qp.indexOf(',');i=i<0?qp.l" 
// 
// ... more code below ... 
// 
```

