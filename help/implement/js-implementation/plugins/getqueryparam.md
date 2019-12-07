---
description: Gibt den Wert des Parameters einer bestimmten Abfragezeichenfolge zurück, wenn er in der URL der aktuellen Seite vorhanden ist. Da in der Abfragezeichenfolge einer Seite wichtige Daten enthalten sind (Kampagnen-Trackingcodes, interne Keywords usw.), kann „getQueryParam“ dabei helfen, die Daten in Analytics-Variablen zu überführen.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getQueryParam
topic: Developer and implementation
uuid: ba202756-c728-4ebc-8fd9-5bc29a9f673b
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getQueryParam

Gibt den Wert des Parameters einer bestimmten Abfragezeichenfolge zurück, wenn er in der URL der aktuellen Seite vorhanden ist. Da in der Abfragezeichenfolge einer Seite wichtige Daten enthalten sind (Kampagnen-Trackingcodes, interne Keywords usw.), kann „getQueryParam“ dabei helfen, die Daten in Analytics-Variablen zu erfassen.

>[!IMPORTANT]
>
>Dieses Plug-in wird nur von H-Code verwendet. [AppMeasurement für JavaScript](/help/implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md) bietet diese Funktionalität nativ mit [Util.getQueryParam](/help/implement/js-implementation/util-getqueryparam.md).

Nachdem das Plug-in im [!DNL AppMeasurement] für JavaScript-Code installiert wurde, wird es konfiguriert. Dazu wird eine [!DNL Analytics]-Variable ausgewählt, die mit den in der Abfragezeichenfolge gefundenen Daten aufgefüllt werden soll, und es wird angegeben, welche Werte der Abfragezeichenfolge erfasst werden sollen. Das Plug-in erkennt die angegebene Abfragezeichenfolge, soweit vorhanden, und erfasst den Wert in der ausgewählten Variablen. Wenn kein Abfragezeichenfolgen-Parameter mit diesem Wert gefunden wird, wird eine leere Zeichenfolge zurückgegeben. Wenn ein Abfragezeichenfolgenparameter vorhanden ist, aber keinen Wert hat (z. B. param1 in `?param1&param2=value`), wird das Wort *`true`* ausgegeben.

> [!NOTE] Damit die unten aufgeführten Beispiele funktionieren, müssen Sie den Basis-Code für das Plug-in in den [!DNL AppMeasurement] für den JavaScript-Code installieren.

Wenn Sie mit *`s.campaign`* Kampagnen-Trackingcodes erfassen möchten, die als Werte des Abfrageparameters *`cid`* verfügbar sind, geben Sie Folgendes in die Funktion *`doPlugins()`* in [!DNL AppMeasurement] für JavaScript-Code ein:

`s.campaign=s.getQueryParam('cid')`

Wenn in diesem Beispiel der Benutzer auf eine Landingpage Ihrer Website gelangt ist, auf der die URL [!DNL https://www.yoursite.com/index.html?cid=123456] war, würde *`s.campaign`* einen Wert von *123456* erhalten. Mit dem [!DNL DigitalPulse][!UICONTROL  Debugger] kann dies sichtbar gemacht werden, in dem *v0=123456* als Teil der Bildanforderung angezeigt werden sollte.

> [!NOTE] Der Parameter *`cid`* und andere werden hier als Beispiele verwendet. Sie können sie durch beliebige Zeichenfolgenparameter ersetzen, die in Ihrer Site vorhanden sind.

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

Ab der Version 2.0 von *`getQueryParam`* 2.0 von akzeptiert das Plug-in auch ein optionales drittes Argument, *u*, mit dem Sie die URL angeben können, aus der Sie Abfragezeichenfolgen-Parameter extrahieren möchten. Das Plug-in verwendet standardmäßig (das heißt, wenn dieses dritte Argument nicht spezifiziert wird) die Seiten-URL. Wenn Sie zum Beispiel eine Abfragezeichenfolge vom Referrer extrahieren möchten, können Sie den folgenden Code verwenden:

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

> [!NOTE] Für die folgenden Anweisungen müssen Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

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

