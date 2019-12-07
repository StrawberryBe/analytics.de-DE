---
description: Erfasst den Wert einer Analytics-Variablen beim nächsten Seitenaufruf. Sie können mit dem Plug-in zum Beispiel den s.pageName-Wert des vorherigen Seitenaufrufs in einer benutzerspezifischen Traffic-Variablen erfassen. Darüber hinaus verfügt es über die Option, einen vorherigen Wert nur dann zu erfassen, wenn bestimmte Erfolgsereignisse festgelegt sind.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getPreviousValue
topic: Developer and implementation
uuid: 20da7b4a-9820-4690-a1cc-d10b6dd627a7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getPreviousValue

Erfasst den Wert einer Analytics-Variablen beim nächsten Seitenaufruf. Sie können mit dem Plug-in zum Beispiel den s.pageName-Wert des vorherigen Seitenaufrufs in einer benutzerspezifischen Traffic-Variablen erfassen. Darüber hinaus verfügt es über die Option, einen vorherigen Wert nur dann zu erfassen, wenn bestimmte Erfolgsereignisse festgelegt sind.

> [!NOTE] Für die folgenden Anweisungen müssen Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Plug-in-Code und -Implementierung {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: Für diesen Abschnitt sind keine Änderungen erforderlich.

**Plug-in-Konfiguration**

Fügen Sie den folgenden Code innerhalb der Funktion *`s_doPlugins()`* ein, die sich in der Datei *`s_code.js`* im Abschnitt *Plugin Config* befindet. Wählen Sie eine benutzerspezifische Traffic-Variable (s.prop) oder eine benutzerspezifische Konversionsvariable (s.eVar), um diese für die Erfassung von Daten zu persistenten Werten zu verwenden. Dies muss eine Variable sein, die über die Admin Console aktiviert wurde, die jedoch aktuell nicht für einen anderen Zweck verwendet wird. Sie können das folgende Beispiel verwenden und an Ihre Anforderungen anpassen.

`s.prop1=s.getPreviousValue(s.pageName,'gpv_pn','event1');`

*`s.getPreviousValue`* hat drei Argumente:

1. Die Variable, die von der vorherigen Seite erfasst werden soll ( *`s.pageName`* oben).
1. Der Cookie-Name zum Speichern des Werts für den Abruf ( *`gpv_pn`* oben).
1. Das Ereignis, das für den Seitenaufruf festgelegt sein muss, damit das Abrufen des vorherigen Werts ausgelöst wird (*`event1`* oben). Wenn hierzu keine Angabe gemacht wird, erfasst das Plug-in den vorherigen Wert für alle Seitenaufrufe.

**Plug-ins SECTION**: Fügen Sie in der Datei [!DNL s_code.js] den folgenden Code im Abschnitt Plug-ins SECTION hinzu. Nehmen Sie an diesem Teil des Plug-in-Codes keine Änderungen vor.

```js
/* 
 * Plugin: getPreviousValue_v1.0 - return previous value of designated 
 * variable (requires split utility) 
 */ 
s.getPreviousValue=new Function("v","c","el","" 
+"var s=this,t=new Date,i,j,r='';t.setTime(t.getTime()+1800000);if(el" 
+"){if(s.events){i=s.split(el,',');j=s.split(s.events,',');for(x in i" 
+"){for(y in j){if(i[x]==j[y]){if(s.c_r(c)) r=s.c_r(c);v?s.c_w(c,v,t)" 
+":s.c_w(c,'no value',t);return r}}}}}else{if(s.c_r(c)) r=s.c_r(c);v?" 
+"s.c_w(c,v,t):s.c_w(c,'no value',t);return r}"); 
/* 
 * Utility Function: split v1.5 - split a string (JS 1.0 compatible) 
 */ 
s.split=new Function("l","d","" 
+"var i,x=0,a=new Array;while(l){i=l.indexOf(d);i=i>-1?i:l.length;a[x" 
+"++]=l.substring(0,i);l=l.substring(i+d.length);}return a"); 
```

**Hinweise**

* Testen Sie die Installation von Plug-ins stets ausführlich, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
* Wenn für die ausgewählte Variable auf keiner Seite ein Wert vorhanden ist, wird der Text *kein Wert* im Cookie gesetzt.
* Es ist nun für jedes Cookie eine feste Ablaufzeit von 30 Minuten festgelegt, die bei jedem Seitenladevorgang aktualisiert wird. Das Plug-in funktioniert für die Dauer des Besuchs.
* Da die Funktion als Teil des Abschnittcodes des Plug-ins aufgerufen werden muss, wird der Code jedes Mal dann ausgeführt, wenn *`s.t()`* oder *`s.tl()`* aufgerufen wird.

* Die ausgewählte Variable muss mit einem Wert ausgefüllt werden, bevor der Aufruf von *`s.getPreviousValue`*. Weil die Funktion *`s_doPlugins()`* nach dem Ausfüllen der Variablen auf der Seite ausgeführt wird, tritt dieses Problem selten auf. Dies sollte nur dann von Belang sein, wenn die mit diesem Plug-in verwendete Variable in der Funktion *`s_doPlugins()`* und nach dem Aufruf von *`s.getPreviousValue`* eingetragen wird.

