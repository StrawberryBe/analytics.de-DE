---
description: Gibt den Wert des Parameters einer bestimmten Abfragezeichenfolge zurück, wenn er in der URL der aktuellen Seite vorhanden ist. Da in der Abfragezeichenfolge einer Seite wichtige Daten enthalten sind (Kampagnen-Trackingcodes, interne Keywords usw.), in der Abfragezeichenfolge einer Seite verfügbar sind, kann  „getQueryParam“ dabei helfen, die Daten in Analytics-Variablen zu erfassen.
keywords: Analytics-Implementierung
seo-description: Gibt den Wert des Parameters einer bestimmten Abfragezeichenfolge zurück, wenn er in der URL der aktuellen Seite vorhanden ist. Da in der Abfragezeichenfolge einer Seite wichtige Daten enthalten sind (Kampagnen-Trackingcodes, interne Keywords usw.), in der Abfragezeichenfolge einer Seite verfügbar sind, kann  "getQueryParam" dabei helfen, die Daten in Analytics-Variablen zu überführen.
seo-title: getQueryParam
solution: Analytics
subtopic: Plug-ins
title: getQueryParam
topic: Entwickler und Implementierung
uuid: ba 202756-c 728-4 ebc -8 fd 9-5 bc 29 a 9 f 673 b
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getQueryParam

Gibt den Wert des Parameters einer bestimmten Abfragezeichenfolge zurück, wenn er in der URL der aktuellen Seite vorhanden ist. Da in der Abfragezeichenfolge einer Seite wichtige Daten enthalten sind (Kampagnen-Trackingcodes, interne Keywords usw.), in der Abfragezeichenfolge einer Seite verfügbar sind, kann  „getQueryParam“ dabei helfen, die Daten in Analytics-Variablen zu erfassen.

>[!IMPORTANT]
>
>Dieses Plug-In wird nur von H-Code verwendet. [Appmeasurement for javascript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8) verwendet diese Funktion nativ unter Verwendung von [Util. getqueryparam](../../../implement/js-implementation/util-getqueryparam.md#concept_763AD2621BB44A3990204BE72D3C9FA5).

Once installed in your [!DNL AppMeasurement] for JavaScript code, the plug-in is configured by selecting a [!DNL Analytics] variable to populate using data found in the query string, and specifying which query string values to capture. Das Plug-in erkennt die angegebene Abfragezeichenfolge, soweit vorhanden, und erfasst den Wert in der ausgewählten Variablen. Wenn kein Abfragezeichenfolgen-Parameter mit diesem Wert gefunden wird, wird eine leere Zeichenfolge zurückgegeben. If a query string parameter exists but does not have a value (such as param1 in `?param1&param2=value`), the word *`true`* is returned.

>[!NOTE]
>
>The base code for the plug-in must be installed in your [!DNL AppMeasurement] for JavaScript code before the examples below will work.

If you wanted to use *`s.campaign`* to capture campaign tracking codes available as values of the *`cid`* query parameter, you would enter the following in the *`doPlugins()`* function in your [!DNL AppMeasurement] for JavaScript code:

`s.campaign=s.getQueryParam('cid')`

In this example, if the user arrived at a landing page on your site where the URL was [!DNL https://www.yoursite.com/index.html?cid=123456], then *`s.campaign`* would receive a value of *123456*. Mit dem [!DNL DigitalPulse] Debugger kann dies sichtbar gemacht werden, in dem *v0=123456* als Teil der Bildanforderung angezeigt werden sollte.

>[!NOTE]
>
>The parameter *`cid`* and others are used here as examples. Sie können sie durch beliebige Zeichenfolgenparameter ersetzen, die in Ihrer Site vorhanden sind.

Die Variable *`getQueryParam`* verfügt über zwei weitere (optionale) Argumente, die zum Erfassen von Daten in Analytics-Variablen verwendet werden können.

```js
s.getQueryParam('p','d','u') 
 
where: 
p = comma-separated list of query parameters to locate (can also be a single value with no comma) 
d = delimiter for list of values (in case more than one specified parameter is found) 
u = where to search for value (e.g., document.referrer); set to current page URL by default
```

Wenn *p* eine Liste von Abfragezeichenfolgen-Parametern ist und mehr als ein Abfragezeichenfolgen-Parameter in der URL vorhanden ist, werden alle Werte in einer Liste mit dem Trennzeichen *d* zurückgegeben, wobei es sich um ein einzelnes Zeichen oder eine Zeichenfolge handeln kann, z. B. „ : “ (Leerzeichen-Doppelpunkt-Leerzeichen). Wenn *d* ausgelassen wird, werden die Werte nicht durch ein Trennzeichen voneinander getrennt. Wenn ein Abfragezeichenfolge-Parameter Vorrang vor einem anderen haben soll und beide vorhanden sind, verwenden Sie eine *if*-Anweisung, wie nachfolgend dargestellt.

```js
// cid takes precedence over iid if both exist in the query string 
s.campaign=s.getQueryParam('cid'); 
 if(!s.campaign) 
 s.campaign=s.getQueryParam('iid'); 
```

Ab der Version 2.0 von *`getQueryParam`* akzeptiert das Plug-in auch ein optionales drittes Argument, *u*, mit dem Sie die URL angeben können, aus der Sie Abfragezeichenfolgen-Parameter extrahieren möchten. Das Plug-in verwendet standardmäßig (das heißt, wenn dieses dritte Argument nicht spezifiziert wird) die Seiten-URL. Wenn Sie zum Beispiel eine Abfragezeichenfolge vom Referrer extrahieren möchten, können Sie den folgenden Code verwenden:

```js
// take the query string from the referrer 
 s.eVar1=s.getQueryParam('pid','',document.referrer); 
```

Der Kennzeichner „f“ muss in diesem dritten Argument mit Bildfeldern verwendet werden, wenn der notwendige Abfragezeichenfolgen-Parameter in der Adressleiste anstatt in der URL des aktuellen Bildfeldes gefunden wird.

```js
// take the query string from the parent frame 
 s.eVar1=s.getQueryParam('pid','',f); 
```

Wenn Sie Bildfelder und den Parameter *f* verwenden, wird empfohlen, das Plug-in *`getValOnce`* zu verwenden, um zu verhindern, dass der Kampagnen-Trackingcode bei jedem Seitenaufruf gesendet wird.

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

**Plug-in-Code**

```js
/******************************************************************** 
 * 
 * Main Plug-in code (should be in Plug-ins section) 
 * 
 *******************************************************************/ 
/* 
 * Plugin: getQueryParam 2.3 
 */ 
s.getQueryParam=new Function("p","d","u","" 
+"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" 
+"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" 
+".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" 
+"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" 
+"=p.length?i:i+1)}return v"); 
s.p_gpv=new Function("k","u","" 
+"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" 
+"=s.pt(q,'&','p_gvf',k)}return v"); 
s.p_gvf=new Function("t","k","" 
+"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" 
+"rue':t.substring(i+1);if(p.toLowerCase()==k.toLowerCase())return s." 
+"epa(v)}return ''"); 
 
/******************************************************************** 
 * 
 * Commented example of how to use this is doPlugins function 
 * 
 *******************************************************************/ 
 /* Plugin Example: getQueryParam 2.3 
 //single parameter 
 s.campaign=s.getQueryParam('cid'); 
 
 //multiple parameters 
 s.campaign=s.getQueryParam('cid,sid',':'); 
 
 //non-page URL example 
 s.campaign=s.getQueryParam('cid','',document.referrer); 
 
 //parent frame example 
 s.campaign=s.getQueryParam('cid','','f'); 
 
 */ 
 
/******************************************************************** 
 * 
 * Config variables (should be above doPlugins section) 
 * 
 *******************************************************************/ 
 
 None 
 
/******************************************************************** 
 * 
 * Utility functions that may be shared between plug-ins (name only) 
 * 
 *******************************************************************/ 
  
 None
```

