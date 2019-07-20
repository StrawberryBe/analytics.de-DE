---
description: Erfasst die Zeitspanne in Sekunden, während der Ihre Seite die aktive Registerkarte im Browser war. Dieser Wert wird auf der nächsten Seite in Form einer Kennzahl angezeigt.
keywords: Analytics-Implementierung
seo-description: Erfasst die Zeitspanne in Sekunden, während der Ihre Seite die aktive Registerkarte im Browser war. Dieser Wert wird auf der nächsten Seite in Form einer Kennzahl angezeigt.
seo-title: getPageVisibility
solution: Analytics
title: getPageVisibility
topic: Entwickler und Implementierung
uuid: 3891 e 2 aa-d 5 c 1-4 a 2 b -8522-eb 2 bae 39 ea 2 e
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getPageVisibility

Erfasst die Zeitspanne in Sekunden, während der Ihre Seite die aktive Registerkarte im Browser war. Dieser Wert wird auf der nächsten Seite in Form einer Kennzahl angezeigt.

>[!NOTE]
>
>Hierbei handelt es sich um eine Betaversion des Plugins. Möglicherweise werden weitere Updates vorgenommen.

This plug-in requires [getVisitStart](../../../implement/js-implementation/plugins/getvisitstart.md#concept_1C3CD25A87094A498A1D8A455963FBD8).

Dieses Plug-in erfasst auch die Zeitspanne, während der die Seite im Browser geöffnet war (sowohl aktiv als auch inaktiv). Das getPreviousValue-Plug-in muss verwendet werden, um den Namen der vorherigen Seite in Verbindung mit der Anzeige der Seite nachzuverfolgen. Anhand dieser Werte können Sie die Interaktionen Ihrer Besucher nachvollziehen und das Verhalten der Besucher Ihrer Seiten verfolgen.

Sie müssen das getPreviousValue-Plug-in verwenden, um den Namen der vorherigen Seite in Verbindung mit der Anzeige der Seite nachzuverfolgen. Anhand dieser Werte können Sie die Interaktionen Ihrer Besucher nachvollziehen und das Verhalten der Besucher Ihrer Seiten verfolgen.

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von Analytics verfügt. This plug-in is compatible only with [!DNL AppMeasurement] tracking libraries.

## Erforderliche unterstützende Plug-ins {#section_0CA7624F4A7B4B5F851A4300937887AD}

* appendList
* getPreviousValue
* getVisitStart

## Plug-in-Code und -Implementierung {#section_543ABD8B3E6A48A5AFD86CFEDE144696}

**Config Section**

Die `s.pvel`-Variable sollte die drei Ereignisse verwenden, die Sie verwenden möchten:

| Ereignis | Definition |
|---|---|
| Gesamtdauer der Anzeige der Seite in Sekunden (numerisch) | Die Zeitdauer, während der die Seite aktiv im Browser angezeigt wurde |
| Gesamtdauer der Seite (numerisch) | Die Zeitdauer, während der die Seite im Browser geöffnet war, unabhängig vom Anzeigestatus |
| Gesamtanzahl der Anzeigeinstanzen der Seite (Zähler) | Gesamtanzahl der für die vorherigen beiden Ereignisse erfassten Werte |

**Beispielaufrufe**

```
//Page Visibility Event List (total page visibility seconds, total page seconds, total page visibility instances) 
s.pvel='event7,event8,event9' 
```

**doPlugins-Bereich**

Um das Plug-in zu initialisieren, sind zwei Zeilen Code im Bereich `doPlugins` Ihres s__Code erforderlich, vorzugsweise nach der Zuweisung der `s.pageName`-Variablen.

**Beispielaufrufe**

```
/* Page Visibility */ 
s.eVar9 = s.getPreviousValue(s.pageName,'gpv_v9','');  //Record the previous page name in the designated eVar of your choice 
s.getPageVisibility(); 
```

**Plug-in-Bereich**

```
/* Page Visibility Plugin 0.1 (BETA) */ 
s.getPageVisibility=new Function("","" 
+"var s=this;if(s.getVisitStart()){s.Util.cookieWrite('s_pvs','');s.U" 
+"til.cookieWrite('s_tps','');}if(s.Util.cookieRead('s_pvs')&&s.pvt<1" 
+"){if(parseInt(s.Util.cookieRead('s_pvs'))<=parseInt(s.Util.cookieRe" 
+"ad('s_tps'))){s.pve=s.pvel.split(',');s.events=s.apl(s.events,s.pve" 
+"[0]+'='+(parseInt(s.Util.cookieRead('s_pvs'))),',',2);s.Util.cookie" 
+"Write('s_pvs','');s.events=s.apl(s.events,s.pve[1]+'='+(parseInt(s." 
+"Util.cookieRead('s_tps'))),',',2);s.Util.cookieWrite('s_tps','');s." 
+"events=s.apl(s.events,s.pve[2],',',2);}}s.pvi=setInterval(s.pvx,100" 
+"0);s.wpvi=setInterval(s.wpvc,5000);"); 
s.gbp=new Function("","" 
+"if('hidden'in document){return null;}var bp=['moz','ms','o','webkit" 
+"'];for(var i=0;i<bp.length;i++){var p=bp[i]+'Hidden';if(p in docume" 
+"nt){return bp[i];}}return null;"); 
s.hp=new Function("p","" 
+"if(p){return p+'Hidden';}else{return'hidden';}"); 
s.vs=new Function("p","" 
+"if(p){return p+'VisibilityState';}else{return'visibilityState';}"); 
s.ve=new Function("p","" 
+"if(p){return p+'visibilitychange';}else{return'visibilitychange';}"); 
s.pvx=new Function("","" 
+"s.pvt+=1;"); 
s.wpvc = function(){var tempDate = Date.now();s.Util.cookieWrite('s_tps', 
Math.ceil((tempDate - s.totalTime)/1000));s.Util.cookieWrite('s_pvs', s.pvt)} 
document.addEventListener('visibilitychange',function(event){if(document.hidden){s.visibility = false;clearTimeout(s.pvi);}else{s.visibility=true;s.pvi=setInterval(s.pvx,1000);}});s.totalTime=new Date();s.pvt=0;s.prefix=s.gbp;s.hidden=s.hp(s.prefix);s.visibility=true;s.visibilityState=s.vs(s.prefix);s.visibilityEvent=s.ve(s.prefix); 
```

## Hinweise {#section_47964BB9D0A24BFEB4B2498A41D8B017}

* Testen Sie stets die Installation des Plug-ins, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
* Da das Plug-in die Seitenanzeige in Sekunden und die Gesamtdauer in Verbindung mit der vorherigen Seite weitergibt, werden keine Daten für die finale Seitenanzeige des Besuchs erfasst.
* Für dieses Plug-in müssen im Webbrowser des Benutzers Cookies gesetzt werden. Wenn der Benutzer keine Erstanbieter-Cookies akzeptiert, übergibt das Plug-in auch keine Daten an Analytics.
* The plug-in creates its own first-party cookies named `s_tps` and `s_pvs`.

* Nur wenige Benutzer werden den prozentualen Anteil an auf der Seite angezeigten Daten aufgrund von Browserbeschränkungen nicht weitergeben. Und im Plug-in ist Logik enthalten, um sicherzustellen, dass die Daten deshalb nicht schwanken. Dieses Plug-in wurde jedoch in IE, Firefox, Chrome und Safari erfolgreich getestet.
* Aufgrund der Messweise des Plug-ins für die Gesamtdauer in Sekunden und der Zuweisung dieses Werts zum Namen der vorherigen Seite kommt es zu Abweichungen zwischen den Kennzahlen für die Standardzeit, während der die Seite geöffnet war, und den Kennzahlen für die Gesamtdauer in Sekunden.
* [!UICONTROL Es können berechnete Metriken] erstellt werden, um die Zusammenfassung und das Verständnis des Besucherverhaltens mit diesen Metriken zu unterstützen:

   * ** Seitensichtbarkeitsverhältnis** (Gesamtdauer der Seitenanzeige in Sekunden/Gesamtdauer der Seite in Sekunden)
   * ** Ausgeblendete Sekunden insgesamt** (Gesamtdauer der Seite in Sekunden - Gesamtdauer der Seitenanzeige in Sekunden)
   * ** Durchschnittliche Seitensichtbarkeit Sekunden** (Gesamtdauer der Seitenanzeige in Sekunden/Gesamtanzahl der Anzeigeinstanzen der Seite)
   * **Durchschnittliche Dauer des Verbergens der Seite in Sekunden** ((Gesamtdauer der Seite in Sekunden – Gesamtdauer der Anzeige der Seite in Sekunden)/Gesamtanzahl der Anzeigeinstanzen der Seite)

* Aufgrund der Aufrundungsweise des Plug-ins kann es zu einer Differenz von 1–2 Sekunden zwischen der Gesamtdauer der Anzeige der Seite in Sekunden und der Gesamtdauer in Sekunden kommen, wobei die Gesamtdauer in Sekunden höher ist. (Problem wird in einem zukünftigen Update behoben.)
* Die Verwendung des getVisitStart-Plug-ins erfasst Besucher, die einen neuen Besuch nach einer Inaktivität von mindestens 30 Minuten gestartet haben. Dies funktioniert nicht wie geplant. Aber wahrscheinlich wird dieses Problem behoben sein, wenn wir die „Aktive Gesamtdauer in Sekunden“ in eine zukünftige Version des Plug-ins integrieren.

## Häufig gestellte Fragen {#section_1ED9391D3BAA4208817F0DF69ABBB25E}

**Wird dieses Plug-in zusätzliche Server-Aufrufe durchführen? **

Das Plug-in erfasst nur die Werte für die Seitenanzeige auf nachfolgenden Server-Aufrufen für Seitenanzeigen. Es werden in Verbindung damit keine zusätzlichen Server-Aufrufe verwendet.

**Wenn ich die Gesamtdauer der Seite oder die Gesamtanzahl der Anzeigeinstanzen der Seite nicht erfassen möchte, kann ich diese dann aus der Ereignisliste ausschließen? **

Ja, die Gesamtdauer der Seite und die Gesamtanzahl der Anzeigeinstanzen der Seite sind optionale Ereignisse und können auf Wunsch aus der Liste ausgeschlossen werden.

**Ergeben die erfassten Ereignisse Sinn, wenn ich sie in anderen Berichten als dem Bericht „Vorheriger Seitenname“ verwende? **

Da das Plug-in nur Werte zur nachfolgenden Bildanforderung erfasst, könnten andere eVars, die im Kontext einer vorherigen Seite erfasst wurden, angewendet werden, z. B. „Vorherige Seiten-URL“.

**Sendet das Plug-in die Anzeigezeit über einen s.tl()-Aufruf oder einen s.t()-Aufruf?**

Die Anzeigezeit wird nur mit s.t()-Aufrufen erfasst.
