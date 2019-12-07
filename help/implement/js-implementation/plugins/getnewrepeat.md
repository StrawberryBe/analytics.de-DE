---
description: Ermittelt, ob es sich bei einem Besucher um einen neuen Besucher oder einen wiederholten Besucher handelt, und erfasst diese Informationen in einer Analytics-Variablen.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getNewRepeat
topic: Developer and implementation
uuid: e3e9f362-e0b1-4a2b-bb5b-98eddaa0a7f4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getNewRepeat

Ermittelt, ob es sich bei einem Besucher um einen neuen Besucher oder einen wiederholten Besucher handelt, und erfasst diese Informationen in einer Analytics-Variablen.

Mithilfe dieses Plug-ins können Sie die folgenden Fragen beantworten:

* Wie hoch ist der Prozentsatz der neuen Besucher (im Vergleich zu zurückkehrenden Besuchern)?
* Generieren wiederkehrende Besucher eine höhere Konversion pro Kopf als neue Besucher? Wie stellt sich dieses Verhältnis dar?
* Führen meine Marketing-Kampagnen über mehrere Besuche hinweg zu einer Persistenz? Kehren zum Beispiel Benutzer, die sich durch meine Kampagnen klicken, auch wieder zurück?

> [!NOTE] Für die folgenden Anweisungen müssen Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Plug-in-Code und -Implementierung {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: Für diesen Abschnitt sind keine Änderungen erforderlich.

**Plug-in-Konfiguration**

Fügen Sie den folgenden Code innerhalb der Funktion *`s_doPlugins()`* ein, die sich in der Datei *`s_code.js`* im Abschnitt *Plugin Config* befindet. Wählen Sie eine benutzerspezifische Traffic-Variable (s.prop) oder eine benutzerspezifische Konversionsvariable (s.eVar), um diese für die Erfassung von Daten zu persistenten Werten zu verwenden. Dies muss eine Variable sein, die über die Admin Console aktiviert wurde, die jedoch aktuell nicht für einen anderen Zweck verwendet wird. Sie können das folgende Beispiel verwenden und an Ihre Anforderungen anpassen.

`s.prop1=s.getNewRepeat(30,'s_getNewRepeat');`

*`s.getNewRepeat`* hat zwei optionale Argumente:

1. Das erste optionale Argument ist die Anzahl der Tage, die das Cookie beibehalten wird. Wenn dieses Argument nicht festgelegt wird, ist die Standardeinstellung 30 Tage.
1. Das zweite optionale Argument ist der Cookiename. Wenn dieses Argument nicht festgelegt wird, wird ein Standardwert verwendet.

**Plug-ins SECTION**: Fügen Sie in der Datei [!DNL s_code.js] den folgenden Code im Abschnitt Plug-ins SECTION hinzu. Nehmen Sie an diesem Teil des Plug-in-Codes keine Änderungen vor.

```js
/* 
 * Plugin: getNewRepeat 1.2 - Returns whether user is new or repeat 
 */ 
s.getNewRepeat=new Function("d","cn","" 
+"var s=this,e=new Date(),cval,sval,ct=e.getTime();d=d?d:30;cn=cn?cn:" 
+"'s_nr';e.setTime(ct+d*24*60*60*1000);cval=s.c_r(cn);if(cval.length=" 
+"=0){s.c_w(cn,ct+'-New',e);return'New';}sval=s.split(cval,'-');if(ct" 
+"-sval[0]<30*60*1000&&sval[1]=='New'){s.c_w(cn,ct+'-New',e);return'N" 
+"ew';}else{s.c_w(cn,ct+'-Repeat',e);return'Repeat';}"); 
/* 
* Utility Function: split v1.5 (JS 1.0 compatible) 
*/ 
s.split=new Function("l","d","" 
+"var i,x=0,a=new Array;while(l){i=l.indexOf(d);i=i>-1?i:l.length;a[x" 
+"++]=l.substring(0,i);l=l.substring(i+d.length);}return a");
```

Testen Sie die Installation von Plug-Ins stets ausführlich, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
