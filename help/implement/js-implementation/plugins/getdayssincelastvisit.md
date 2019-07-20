---
description: Ermittelt die Anzahl der Tage seit dem letzten Besuch eines Benutzers auf Ihrer Site und erfasst diese Daten in einer Analytics-Variablen.
keywords: Analytics-Implementierung
seo-description: Ermittelt die Anzahl der Tage seit dem letzten Besuch eines Benutzers auf Ihrer Site und erfasst diese Daten in einer Analytics-Variablen.
seo-title: getDaysSinceLastVisit
solution: Analytics
subtopic: Plug-ins
title: getDaysSinceLastVisit
topic: Entwickler und Implementierung
uuid: cad 95882-3 bd 0-4 f 94-a 0 c 3-4 e 7 b 6058 d 246
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getDaysSinceLastVisit

Ermittelt die Anzahl der Tage seit dem letzten Besuch eines Benutzers auf Ihrer Site und erfasst diese Daten in einer Analytics-Variablen.

>[!IMPORTANT]
>
>[Der Analysis Workspace](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/) enthält jetzt eine **[!UICONTROL Tage seit der letzten]** Besuchsdauer des Felds, wodurch dieses Plug-plugin nicht mehr benötigt wird.

Mit diesen Daten zur Rückkehrfrequenz können die folgenden Fragen beantwortet werden:

* Wie häufig rufen Benutzer meine Site erneut auf?
* Wie verhält sich die Rückkehrfrequenz zur Konversion? Besuchen Wiederholungskäufer die Site häufig oder weniger häufig?
* Kehren Benutzer, die sich durch meine Kampagnen klicken, häufiger zurück?

Das Plug-in kann auch Werte generieren, die zur Segmentierung dienen. Sie können zum Beispiel ein Segment erstellen, das die Anzeige der Daten nur für die Benutzer ermöglicht, deren letzte Besuche mindestens 30 Tage zurücklagen.

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Plug-in-Code und -Implementierung {#section_5600DBB819F143D59527A73BD94418DE}

**CONFIG SECTION**

Keine Änderungen erforderlich

**Plug-in-Konfiguration**

Place the following code within the `s_doPlugins()` function, which is located in the area of the [!DNL s_code.js] file labeled *Plugin Config*. Wählen Sie eine benutzerspezifische Traffic-Variable (s.prop) und/oder eine Custom Converesion-Variable (s.eVar), um diese für die Erfassung von Daten zur Rückkehrfrequenz zu verwenden. Dies muss eine Variable sein, die über die Admin Console aktiviert wurde, die jedoch aktuell nicht für einen anderen Zweck verwendet wird. Nachfolgend ist ein Beispiel aufgeführt, das Sie an Ihre Anforderungen anpassen können.

```js
s.prop1=s.getDaysSinceLastVisit(Cookie_Name);
```

**Plug-ins SECTION**
Fügen Sie in der Datei [!DNL s_code.js] im Abschnitt *Plug-ins SECTION* den folgenden Code hinzu. Nehmen Sie an diesem Teil des Plug-in-Codes keine Änderungen vor.

```js
/* 
 * Plugin: Days since last Visit 1.1 - capture time from last visit 
 */ 
s.getDaysSinceLastVisit=new Function("c","" 
+"var s=this,e=new Date(),es=new Date(),cval,cval_s,cval_ss,ct=e.getT" 
+"ime(),day=24*60*60*1000,f1,f2,f3,f4,f5;e.setTime(ct+3*365*day);es.s" 
+"etTime(ct+30*60*1000);f0='Cookies Not Supported';f1='First Visit';f" 
+"2='More than 30 days';f3='More than 7 days';f4='Less than 7 days';f" 
+"5='Less than 1 day';cval=s.c_r(c);if(cval.length==0){s.c_w(c,ct,e);" 
+"s.c_w(c+'_s',f1,es);}else{var d=ct-cval;if(d>30*60*1000){if(d>30*da" 
+"y){s.c_w(c,ct,e);s.c_w(c+'_s',f2,es);}else if(d<30*day+1 && d>7*day" 
+"){s.c_w(c,ct,e);s.c_w(c+'_s',f3,es);}else if(d<7*day+1 && d>day){s." 
+"c_w(c,ct,e);s.c_w(c+'_s',f4,es);}else if(d<day+1){s.c_w(c,ct,e);s.c" 
+"_w(c+'_s',f5,es);}}else{s.c_w(c,ct,e);cval_ss=s.c_r(c+'_s');s.c_w(c" 
+"+'_s',cval_ss,es);}}cval_s=s.c_r(c+'_s');if(cval_s.length==0) retur" 
+"n f0;else if(cval_s!=f1&&cval_s!=f2&&cval_s!=f3&&cval_s!=f4&&cval_s" 
+"!=f5) return '';else return cval_s;");
```

**Hinweise**

* Testen Sie die Installation von Plug-ins stets ausführlich, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
* Mit dem Plug-in werden die Benutzer nach Rückkehrfrequenz in die folgenden Gruppen eingeteilt:

   * Erster Besuch
   * Weniger als ein Tag
   * Weniger als sieben Tage
   * Mehr als sieben Tage
   * Mehr als 30 Tage

* Dieses Plug-in muss Cookies verwenden, um einen Benutzer als zurückkehrenden Besucher zu kennzeichnen. Wenn der Browser keine Cookies zulässt, gibt das Plug-In den Wert *Cookies nicht unterstützt* zurück.

