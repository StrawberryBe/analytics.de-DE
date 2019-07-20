---
description: JavaScript-Plug-ins werden in der Regel von der doPlugins-Funktion aufgerufen, die beim Aufruf der t()-Funktion im einzufügenden Code ausgeführt wird.
keywords: Analytics-Implementierung
seo-description: JavaScript-Plug-ins werden in der Regel von der doPlugins-Funktion aufgerufen, die beim Aufruf der t()-Funktion im einzufügenden Code ausgeführt wird.
seo-title: doPlug-Ins-Funktion
solution: Analytics
subtopic: Plug-ins
title: doPlugins-Funktion
topic: Entwickler und Implementierung
uuid: 367 d 5550-f 8 e 2-477 d -8681-18 ae 9665 d 699
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# doPlugins-Funktion

JavaScript-Plug-ins werden in der Regel von der doPlugins-Funktion aufgerufen, die beim Aufruf der t()-Funktion im einzufügenden Code ausgeführt wird.

Wenn Sie eine Variable in der `doPlugins`-Funktion festlegen, überschreiben Sie daher möglicherweise eine Variable, die Sie auf der HTML-Seite festgelegt haben. The only time the `doPlugins` function is not called is when the *`usePlugins`* variable is set to `false`.

**Codebeispiel**

The `doPlugins` function is typically called `s_doPlugins`. Unter bestimmten Umständen (meist, wenn sich auf einer Seite mehrere Versionen von [!DNL Analytics]-Code befinden) können Sie den Namen der `doPlugins`-Funktion jedoch ändern. Wenn die standardmäßige `doPlugins`-Funktion zur Vermeidung von Konflikten umbenannt werden muss, weisen Sie `doPlugins` den richtigen Funktionsnamen zu, wie im Beispiel unten aufgeführt.

```js
/* Plugin Config */ 
s_mc.usePlugins=true 
function  
<b>s_mc_doPlugins</b>(s_mc) { 
/* Add calls to plugins here */ 
} 
s_mc.doPlugins= 
<b>s_mc_doPlugins</b>
```

**Verwenden von doPlugins**

Mit dieser Funktion können Variablen auf einfache Weise Standardwerte zugewiesen werden oder Werte aus Abfrage-Zeichenfolgenparametern auf einer Seite der Site abgerufen werden. Die Verwendung von `doPlugins` kann einfacher sein, als die Werte auf der HTML-Seite auszufüllen, da nur eine Datei aktualisiert werden muss. Änderungen an der JavaScript-Datei werden nicht immer sofort wirksam. Wiederkehrende Besucher verwenden häufig zwischengespeicherte Versionen der JavaScript-Datei aus ihren Webbrowsern. Das heißt, dass Aktualisierungen der Datei möglicherweise für einige Besucher erst einen Monat nach der Änderung übernommen werden.

Die folgenden Beispiele stellen dar, wie Sie mit der `doPlugins`-Funktion einen Standardwert für eine Variable festlegen und einen Wert von der Abfragezeichenfolge abrufen können.

```js
/* Plugin Config */ 
s.usePlugins=true 
function s_doPlugins(s) { 
/* Add calls to plugins here */ 
// if prop1 doesn't have a value, set it to "Default Value" 
if(!s.prop1) 
s.prop1="Default Value" 
 
// if campaign doesn't have a value, get cid from the query string 
if(!s.campaign) 
s.campaign=getQueryParam('cid'); 
} 
s.doPlugins=s_doPlugins
```

**Installierte Plug-ins**

Um zu ermitteln, ob ein Plug-in in Ihrer JavaScript-Datei enthalten und für die Verwendung bereit ist, sehen Sie sich den Abschnitt [!UICONTROL Plug-ins Section] der JavaScript-Datei an. Im folgenden Beispiel ist dargestellt, wie die `getQueryParam`-Funktion im Abschnitt [!UICONTROL Plug-ins Section] aussieht.

```js
/************************** PLUGINS SECTION *************************/ 
 
/* You may insert any plugins you wish to use here. */ 
/* 
* Plugin: getQueryParam 1.3 - Return query string parameter values 
*/ 
s.getQueryParam=new Function("qp","d","" 
+"vars=this,v='',i,t;d=d?d:'';while(qp){i=qp.indexOf(',');i=i<0?qp.l" 
// 
// ... more code below ... 
// 
```

