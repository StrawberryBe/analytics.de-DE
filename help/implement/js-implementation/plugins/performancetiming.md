---
description: Bei diesem Plug-in wird die Navigation Timing JavaScript API zur präzisen Messung der Leistung im Web verwendet. Dies stellt eine native Methode dar, um präzise und detaillierte Zeitstatistiken zu Seitenladeereignissen und Assetladezeiten abzurufen. Zuvor verwendeten Messungen dieser Sorte entweder das JavaScript Date-Objekt für Zeitmetriken oder eine rudimentäre Weiterführung der Metriken für die Navigationszeit. Beide Methoden sind unzuverlässig, obwohl sie einige Trenddaten für die Seitenladezeit bereitstellen.
keywords: Analytics-Implementierung
seo-description: Bei diesem Plug-in wird die Navigation Timing JavaScript API zur präzisen Messung der Leistung im Web verwendet. Dies stellt eine native Methode dar, um präzise und detaillierte Zeitstatistiken zu Seitenladeereignissen und Assetladezeiten abzurufen. Zuvor verwendeten Messungen dieser Sorte entweder das JavaScript Date-Objekt für Zeitmetriken oder eine rudimentäre Weiterführung der Metriken für die Navigationszeit. Beide Methoden sind unzuverlässig, obwohl sie einige Trenddaten für die Seitenladezeit bereitstellen.
seo-title: performanceTiming
solution: Analytics
title: performanceTiming
topic: Entwickler und Implementierung
uuid: ab 2 a 6 c 51-8791-41 e 7-9 bea-c 1 ce 8 d 312 de 8
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# performanceTiming

Bei diesem Plug-in wird die Navigation Timing JavaScript API zur präzisen Messung der Leistung im Web verwendet. Dies stellt eine native Methode dar, um präzise und detaillierte Zeitstatistiken zu Seitenladeereignissen und Assetladezeiten abzurufen. Zuvor verwendeten Messungen dieser Sorte entweder das JavaScript Date-Objekt für Zeitmetriken oder eine rudimentäre Weiterführung der Metriken für die Navigationszeit. Beide Methoden sind unzuverlässig, obwohl sie einige Trenddaten für die Seitenladezeit bereitstellen.

## Aufgaben dieses Plug-ins {#section_4E0771B959FD4F86B4B91BD18CA01DF1}

>[!IMPORTANT]
>
>Hierbei handelt es sich um eine Betaversion des Plugins. Möglicherweise werden weitere Updates vorgenommen.

Dieses Plug-in nutzt die folgenden detaillierten Ereignisse zum Tracking der einzelnen Zeitkomponenten einer Seitenladung:

| Ereignis | Name | Berechnet aus |
|---|---|---|
| 1 | Umleitungszeit | fetchStart - navigationStart |
| 2 | App-Cache-Zeit | domainLookupStart - fetchStart |
| 3 | DNS-Zeit | domainLookupEnd - domainLookupStart |
| 4 | TCP-Zeit | connectEnd - connectStart |
| 5 | Abfragezeit | responseStart - connectEnd |
| 6 | Reaktionszeit | responseEnd - responseStart |
| 7 | Verarbeitungszeit | loadEventStart - domLoading |
| 8 | onLoad-Zeit | loadEventEnd - loadEventStart |
| 9 | Gesamte Seitenladezeit | loadEventEnd - navigationStart |
| 10 | Leistungsinstanzen | Zähler |

Das folgende Diagramm veranschaulicht die von der PerformanceTiming-Schnittstelle und der PerformanceNavigation-Schnittstelle mit bzw. ohne Umleitung definierten Zeitattribute.

![](assets/timing-attributes.png)

Sämtliche Details zum Navigation Timing-Objekt finden Sie hier:

[https://www.w3.org/TR/navigation-timing/#sec-navigation-timing-interface](https://www.w3.org/TR/navigation-timing/#sec-navigation-timing-interface)

Optional kann das Plug-in zudem das performanceEntries-Objekt zum Aufzeichnen des Asset-Namens, der Startzeit der Asset-Ladezeit und der Details zur Dauer der Ladezeit für jeden einzelnen Asset auf einer bestimmten Seite verwenden. Mit diesem Plug-in wird eine große Menge an Informationen aufgezeichnet. Daher muss das DOM-Speicherobjekt aktiviert werden, um die Seitenladeinformationen zwischen Seitenaufrufen zu speichern. Stellen Sie sicher, dass die Datenschutzrichtlinien Ihres Unternehmens die Verwendung des DOM-Speicherobjekts zulassen, bevor Sie die Funktion aktivieren. Zudem benötigen Sie eine listVar für das Tracking aller Assets.

## Erforderliche unterstützende Plug-ins {#section_B6447EB6548942EFBC219AEFDC245639}

* appendList
* getPreviousValue

## Plug-in-Code und -Implementierung {#section_564D77E1CF0E445586D95AD9769CE57D}

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von Adobe Analytics verfügt. This plugin is compatible only with [!DNL AppMeasurement] tracking libraries.

**Config-Abschnitt (vor doPlugins):**

`s.pte`: Kommagetrennte Liste von Ereignissen mit den 10 Ereignissen, die Sie in dieser Reihenfolge verwenden möchten – die individuellen Zeitereigniskomponenten (Ereignisse 1-8), die gesamte Seitenladezeit (Ereignis 9) und die gesamten Leistungsinstanzen (Ereignis 10).

`s.ptc`: Hiermit können Sie festlegen, ob das Plugin mit doPlugins ausgeführt werden soll oder nicht. Stets als ungültig festgelegt.

*Beispielaufrufe*

```
s.pte = 'event10,event11,event12,event13,event14,event15,event16,event17,event18,event19' 
//[--------------------------- 1 to 8 ---------------------------][-- 9 --][- 10 -] 
s.ptc = false; 
```

**doPlugins-Bereich:**

Um das Plug-in zu initialisieren, ist eine Zeile Code im Bereich `doPlugins` Ihres s_code erforderlich, vorzugsweise nach der Zuweisung der `s.pageName`-Variablen. Wenn Sie die Asset-Ladezeitfunktion im Plug-in nutzen möchten, müssen Sie den Namen der zu verwendenden Listenvariablen weitergeben. Andernfalls werden nicht nur die Leistungszeiteinträge in den Ereignissen verfolgt, die Sie zuvor in der `s.pte`-Variablen angegeben haben.

>[!NOTE]
>
>In order to correlate performance timing entries with pages on your site, you must also initialize the `getPreviousValue` plug-in. Wir empfehlen, diese Leistungseinträge mit dem vorherigen Seitennamen oder dem vorherigen Seiten-URL-Wert zu vergleichen.

*Beispielaufrufe*

```
/* Performance Timing */ 
s.eVar9 = s.getPreviousValue(s.pageName,'gpv_v9','');  //Record the previous page name in the designated eVar of your choice 
s.performanceTiming('list2')  
```

**Plug-ins-Abschnitt:**

Fügen Sie Ihrer JavaScript-Implementierung zuletzt das Plug-in selbst hinzu.

```
/* Plugin: Performance Timing Tracking - 0.11 BETA */ 
s.performanceTiming=new Function("v","" 
+"var s=this;if(v)s.ptv=v;if(typeof performance!='undefined'){if(perf" 
+"ormance.timing.loadEventEnd==0){s.pi=setInterval(function(){s.perfo" 
+"rmanceWrite()},250);}if(!s.ptc||s.linkType=='e'){s.performanceRead(" 
+");}else{s.rfe();s[s.ptv]='';}}"); 
s.performanceWrite=new Function("","" 
+"var s=this;if(performance.timing.loadEventEnd>0)clearInterval(s.pi)" 
+";try{if(s.c_r('s_ptc')==''&&performance.timing.loadEventEnd>0){try{" 
+"var pt=performance.timing;var pta='';pta=s.performanceCheck(pt.fetc" 
+"hStart,pt.navigationStart);pta+='^^'+s.performanceCheck(pt.domainLo" 
+"okupStart,pt.fetchStart);pta+='^^'+s.performanceCheck(pt.domainLook" 
+"upEnd,pt.domainLookupStart);pta+='^^'+s.performanceCheck(pt.connect" 
+"End,pt.connectStart);pta+='^^'+s.performanceCheck(pt.responseStart," 
+"pt.connectEnd);pta+='^^'+s.performanceCheck(pt.responseEnd,pt.respo" 
+"nseStart);pta+='^^'+s.performanceCheck(pt.loadEventStart,pt.domLoad" 
+"ing);pta+='^^'+s.performanceCheck(pt.loadEventEnd,pt.loadEventStart" 
+");pta+='^^'+s.performanceCheck(pt.loadEventEnd,pt.navigationStart);" 
+"s.c_w('s_ptc',pta);if(sessionStorage&&navigator.cookieEnabled&&s.pt" 
+"v!='undefined'){var pe=performance.getEntries();var tempPe='';for(v" 
+"ar i=0;i<pe.length;i++){tempPe+='!';tempPe+=pe[i].name.indexOf('?')" 
+">-1?pe[i].name.split('?')[0]:pe[i].name;tempPe+='|'+(Math.round(pe[" 
+"i].startTime)/1000).toFixed(1)+'|'+(Math.round(pe[i].duration)/1000" 
+").toFixed(1)+'|'+pe[i].initiatorType;}sessionStorage.setItem('s_pec" 
+"',tempPe);}}catch(err){return;}}}catch(err){return;}"); 
s.performanceCheck=new Function("a","b","" 
+"if(a>=0&&b>=0){if((a-b)<60000&&((a-b)>=0)){return((a-b)/1000).toFix" 
+"ed(2);}else{return 600;}}"); 
s.performanceRead=new Function("","" 
+"var s=this;if(performance.timing.loadEventEnd>0)clearInterval(s.pi)" 
+";var cv=s.c_r('s_ptc');if(s.pte){var ela=s.pte.split(',');}if(cv!='" 
+"'){var cva=s.split(cv,'^^');if(cva[1]!=''){for(var x=0;x<(ela.lengt" 
+"h-1);x++){s.events=s.apl(s.events,ela[x]+'='+cva[x],',',2);}}s.even" 
+"ts=s.apl(s.events,ela[ela.length-1],',',2);}s.linkTrackEvents=s.apl" 
+"(s.linkTrackEvents,s.pte,',',2);s.c_w('s_ptc','',0);if(sessionStora" 
+"ge&&navigator.cookieEnabled&&s.ptv!='undefined'){s[s.ptv]=sessionSt" 
+"orage.getItem('s_pec');sessionStorage.setItem('s_pec','',0);}else{s" 
+"[s.ptv]='sessionStorage Unavailable';}s.ptc=true;"); 
/* Remove from Events 0.1 - Performance Specific,  
removes all performance events from s.events once being tracked. */ 
s.rfe=new Function("","" 
+"var s=this;var ea=s.split(s.events,',');var pta=s.split(s.pte,',');" 
+"try{for(x in pta){s.events=s.rfl(s.events,pta[x]);s.contextData['ev" 
+"ents']=s.events;}}catch(e){return;}"); 
/* Plugin Utility - RFL (remove from list) 1.0*/ 
s.rfl=new Function("l","v","d1","d2","ku","" 
+"var s=this,R=new Array(),C='',d1=!d1?',':d1,d2=!d2?',':d2,ku=!ku?0:" 
+"1;if(!l)return'';L=l.split(d1);for(i=0;i<L.length;i++){if(L[i].inde" 
+"xOf(':')>-1){C=L[i].split(':');C[1]=C[0]+':'+C[1];L[i]=C[0];}if(L[i" 
+"].indexOf('=')>-1){C=L[i].split('=');C[1]=C[0]+'='+C[1];L[i]=C[0];}" 
+"if(L[i]!=v&&C)R.push(C[1]);else if(L[i]!=v)R.push(L[i]);else if(L[i" 
+"]==v&&ku){ku=0;if(C)R.push(C[1]);else R.push(L[i]);}C='';}return s." 
+"join(R,{delim:d2})"); 
```

## Hinweise {#section_131C5D97A0094880AFC3A2BBE0BC9DE4}

* Testen Sie stets die Installation des Plug-ins, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
* Da das Plug-in die Leistungsdaten in Verbindung mit der vorherigen Seite weitergibt, werden keine Daten für die finale Seitenanzeige des Besuchs erfasst.
* Beim Tracking der Asset-Zeit verlässt sich dieses Plug-in auf die Fähigkeit, DOM-Speicherwerte im Webbrowser des Benutzers festzulegen. Wenn der Benutzer Cookies nicht akzeptiert und den DOM-Speicher nicht aktiviert hat, wird das Plug-in keine Daten an Analytics weitergeben.
* Ein sehr kleiner Prozentsatz an Benutzern übermittelt aufgrund von Browserbeschränkungen keine Navigationszeitdaten, und Logik ist im Plugin enthalten, um sicherzustellen, dass die Daten nicht als Ergebnis verfälscht werden - insbesondere bei einem kleinen Teil der mobilen Browser. Dieses Plug-in wurde jedoch in IE, Firefox, Chrome und Safari erfolgreich getestet.
* [!UICONTROL Es sollten berechnete Metriken] erstellt werden, um die Zusammenfassung und das Verständnis des Besucherverhaltens mit diesen Metriken zu unterstützen:

   * Durchschnittliche Umleitungszeit (Umleitungszeit/Leistungszeitinstanzen)
   * Durchschnittliche App-Cache-Zeit (App-Cache-Zeit/Leistungszeitinstanzen)
   * Durchschnittliche DNS-Zeit (Umleitungszeit/Leistungszeitinstanzen)
   * Durchschnittliche TCP-Zeit (Umleitungszeit/Leistungszeitinstanzen)
   * Durchschnittliche Abfragezeit (Umleitungszeit/Leistungszeitinstanzen)
   * Durchschnittliche Reaktionszeit (Umleitungszeit/Leistungszeitinstanzen)
   * Durchschnittliche Verarbeitungszeit (Umleitungszeit/Leistungszeitinstanzen)
   * Durchschnittliche onLoad-Zeit (onLoad-Zeit/Leistungszeitinstanzen)
   * Durchschnittliche gesamte Seitenladezeit (Gesamte Seitenladezeit/Leistungszeitinstanzen)

