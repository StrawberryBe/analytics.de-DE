---
description: Bei AppMeasurement für JavaScript-Plug-ins handelt es sich um Programme oder Funktionen, die verschiedene erweiterte Funktionen durchführen.
keywords: Analytics Implementation
subtopic: Plug-ins
title: Plug-ins für Implementierungen verwenden
topic: Developer and implementation
uuid: 7ffcfe89-b7e2-45e4-b771-942d5ae07c39
translation-type: tm+mt
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# Plug-ins für Implementierungen verwenden

Plug-ins sind Codefragmente, die mehrere erweiterte Funktionen ausführen, um Ihre Analytics-Implementierung zu unterstützen.

Diese Plug-ins erweitern den Funktionsumfang Ihrer JavaScript-Datei um Funktionen, die bei einer Basisimplementierung nicht vorhanden sind. Im Rahmen erweiterter Lösungen bietet Adobe noch andere Plug-ins an. Wenn Sie mit JavaScript Daten erfassen möchten, aber nicht genau wissen, wie Sie dabei vorgehen sollen, wenden Sie sich an Ihren Kundenbetreuer.

JavaScript plug-ins are usually called by the doPlugins function, which is executed when the `t` method is called in the Code to Paste.

Wenn Sie eine Variable in der Funktion *`doPlugins`*festlegen, überschreiben Sie daher möglicherweise eine Variable, die Sie auf der HTML-Seite festgelegt haben. Die Funktion*`doPlugins`* wird nur dann nicht aufgerufen, wenn in der Variable [!UICONTROL usePlugins] der Wert „false“ festgelegt ist.

## Codebeispiel {#section_6940FD16F2E94753A1C39694D0CF5FBA}

Das folgende Codebeispiel zeigt, wie die Funktion *`doPlugins`*in Ihrer JavaScript-Datei aussieht:

AppMeasurement für JavaScript:

```js
/* Plugin Config */
s.usePlugins=true
s.doPlugins=function(s) {
 /* Add calls to plug-ins here */
}
```

H-Code:

```js
/* Plugin Config */
s.usePlugins=true
function s_doPlugins(s) {
 /* Add calls to plug-ins here */
}
s.doPlugins=s_doPlugins
```

> [!NOTE] H-Code und frühere Versionen verwenden eine andere Syntax, um Unterstützung für einige sehr alte Browser zu bieten (z. B. IE 4 und 5).

## Umbenennen der doPlugins-Funktion {#section_70B7D58E057B48058E25907AB3726725}

Die Funktion *`doPlugins`*heißt in der Regel*`s_doPlugins`*. Unter bestimmten Umständen (normalerweise, wenn mehr als eine Codeversion auf einer Seite angezeigt wird), kann der Name der Funktion *`doPlugins`*geändert werden. Wenn die standardmäßige Funktion*`doPlugins`* zur Vermeidung von Konflikten umbenannt werden muss, weisen Sie *`doPlugins`*den richtigen Funktionsnamen zu, wie im Beispiel unten aufgeführt.

```js
/* Plugin Config */
s_mc.usePlugins=true
function s_mc_doPlugins(s_mc) {
 /* Add calls to plug-ins here */
}
s_mc.doPlugins=s_mc_doPlugins
```

## Verwenden von doPlugins {#section_FA5D901CC5214D54BCD08AB77BED7925}

Die Funktion *`doPlugins`*bietet einen einfachen Weg, um Variablen Standardwerte zuzuweisen oder um aus[!UICONTROL Abfragezeichenfolgenparametern]einer beliebigen Website-Seite Werte zu entnehmen. Das Verwenden von*`doPlugins`* ist oftmals bequemer, als die Werte in der HTML-Seite einzutragen, da so nur eine Datei aktualisiert werden muss. Denken Sie jedoch immer daran, dass Änderungen, die Sie in der JavaScript-Datei vornehmen, nicht immer sofort wirksam werden. Wiederkehrende Besucher verwenden häufig zwischengespeicherte Versionen der JavaScript-Datei aus ihren Webbrowsern. Das bedeutet, dass in der Datei vorgenommene Aktualisierungen nicht bei allen Besuchern sofort übernommen werden – in einigen Fällen kann das bis zu einem Monat dauern.

Das nächste Beispiel zeigt, wie mithilfe der *`doPlugins`*-Funktion ein Standardwert für eine Variable festgelegt und ein Wert aus der Abfragezeichenfolge abgerufen wird.

```js
/* Plugin Config */
s.usePlugins=true
s.doPlugins=function(s) {
 /* Add calls to plug-ins here */
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
/* You may insert any plug-ins you wish to use here.                 */
/*
 * Plugin: getQueryParam 1.3 - Return query string parameter values
 */
s.getQueryParam=new Function("qp","d",""
+"var s=this,v='',i,t;d=d?d:'';while(qp){i=qp.indexOf(',');i=i<0?qp.l"
//
// ... more code below ...
//
```

