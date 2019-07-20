---
description: Das getVisitNum-Plug-in ermittelt, wie oft ein Benutzer Ihre Site besucht hat, und erfasst diese Anzahl in einer Analytics-Variablen.
keywords: Analytics-Implementierung
seo-description: Das getVisitNum-Plug-in ermittelt, wie oft ein Benutzer Ihre Site besucht hat, und erfasst diese Anzahl in einer Analytics-Variablen.
seo-title: getVisitNum
solution: Analytics
subtopic: Plug-ins
title: getVisitNum
topic: Entwickler und Implementierung
uuid: 27 d 57 f 92-fffb -44 d 0-b 9 ca -9 da 93323 f 64 c
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getVisitNum

Das getVisitNum-Plug-in ermittelt, wie oft ein Benutzer Ihre Site besucht hat, und erfasst diese Anzahl in einer Analytics-Variablen.

## Plug-in-Code und -Implementierung {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: Für diesen Abschnitt sind keine Änderungen erforderlich.

**Plug-in-Konfiguration**

Place the following code within the *`s_doPlugins()`* function, which is located in the area of the *`s_code.js`* file labeled *Plugin Config*. Wählen Sie eine benutzerspezifische Traffic-Variable (s.prop) oder eine benutzerspezifische Konversionsvariable (s.eVar), um diese für die Erfassung von Daten zur Anzahl von Besuchen zu verwenden. Dies muss eine Variable sein, die über die Admin Console aktiviert wurde, die jedoch aktuell nicht für einen anderen Zweck verwendet wird. Sie können das folgende Beispiel verwenden und an Ihre Anforderungen anpassen.

`s.prop1=s.getVisitNum();`

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

**Plug-ins SECTION**: Fügen Sie in der Datei [!DNL s_code.js] den folgenden Code im Abschnitt Plug-ins SECTION hinzu. Nehmen Sie an diesem Teil des Plug-in-Codes keine Änderungen vor.

```js
/* 
* Plugin: getVisitNum - version 3.0 
*/ 
s.getVisitNum=new Function("tp","c","c2","" 
+"var s=this,e=new Date,cval,cvisit,ct=e.getTime(),d;if(!tp){tp='m';}" 
+"if(tp=='m'||tp=='w'||tp=='d'){eo=s.endof(tp),y=eo.getTime();e.setTi" 
+"me(y);}else {d=tp*86400000;e.setTime(ct+d);}if(!c){c='s_vnum';}if(!" 
+"c2){c2='s_invisit';}cval=s.c_r(c);if(cval){var i=cval.indexOf('&vn=" 
+"'),str=cval.substring(i+4,cval.length),k;}cvisit=s.c_r(c2);if(cvisi" 
+"t){if(str){e.setTime(ct+1800000);s.c_w(c2,'true',e);return str;}els" 
+"e {return 'unknown visit number';}}else {if(str){str++;k=cval.substri" 
+"ng(0,i);e.setTime(k);s.c_w(c,k+'&vn='+str,e);e.setTime(ct+1800000);" 
+"s.c_w(c2,'true',e);return str;}else {s.c_w(c,e.getTime()+'&vn=1',e)" 
+";e.setTime(ct+1800000);s.c_w(c2,'true',e);return 1;}}"); 
s.dimo=new Function("m","y","" 
+"var d=new Date(y,m+1,0);return d.getDate();"); 
s.endof=new Function("x","" 
+"var t=new Date;t.setHours(0);t.setMinutes(0);t.setSeconds(0);if(x==" 
+"'m'){d=s.dimo(t.getMonth(),t.getFullYear())-t.getDate()+1;}else if(" 
+"x=='w'){d=7-t.getDay();}else {d=1;}t.setDate(t.getDate()+d);return " 
+"t;");
```

**Parameter**

* tp = (Zeichenfolge, optional) Verfolgungszeitraum. Verwenden Sie „d“ für Tag, „w“ für Woche, „m“ für Monat oder eine Zahl für eine benutzerdefinierte Anzahl von Tagen.

   * Wenn Sie einen Tag, eine Woche oder einen Monat auswählen, wird die Besuchszahl am Ende des Tages/der Woche/des Monats zurückgesetzt.
   * Wenn Sie eine benutzerdefinierte Anzahl von Tagen auswählen, wird die Besuchszahl nach dieser Anzahl an Tagen zurückgesetzt.
   * Wenn Sie keinen Wert angeben, wird „m“ verwendet.

* c = (Zeichenfolge, optional) Geben Sie den Namen des beständigen Cookies an. Der Standardwert ist „s_vnum“.
* c2 = (Zeichenfolge, optional) Geben Sie den Sitzungs-Cookie-Namen an. Der Standardwert ist „s_invisit“.

**Rückgabe**

* Gibt die Besuchsnummer (1, 2, 3 usw.) des Besuchs zurück. Diese Nummer wird nur auf der ersten Seite jedes Besuchs erhöht.
* Gibt „unknown visit number“ zurück, wenn das Plug-in die Besuchsnummer nicht ermitteln kann (Cookies sind blockiert).

**Beispiele**

```js
s.prop1=s.getVisitNum(365); //custom length, 365 days. Default cookie names 
s.prop1=s.getVisitNum('w'); //resets weekly 
s.prop1=s.getVisitNum('m','s_vmonthnum','s_monthinvisit'); //resets montly, custom cookie names 
s.prop1=s.getVisitNum('d'); //resets daily
```

**Hinweise**

* Testen Sie die Installation von Plug-ins stets ausführlich, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
* Für dieses Plug-in müssen im Webbrowser des Benutzer Cookies gesetzt werden. Wenn der Benutzer keine Cookies zulässt, erscheinen alle Besuche als erste Besuche.

