---
description: Das Plug-in „s.hitGovernor“ verfolgt die Gesamtzahl der Analytics-Bildanforderungen, die während eines vordefinierten rollierenden Zeitrahmens gesendet wurden, und kann bei Bedarf zusätzliche Logik ausführen, wenn diese Gesamtzahl einen bestimmten Schwellenwert überschreitet.
seo-description: Das Plug-in „s.hitGovernor“ verfolgt die Gesamtzahl der Analytics-Bildanforderungen, die während eines vordefinierten rollierenden Zeitrahmens gesendet wurden, und kann bei Bedarf zusätzliche Logik ausführen, wenn diese Gesamtzahl einen bestimmten Schwellenwert überschreitet.
seo-title: hitGovernor
title: hitGovernor
uuid: d 0991 eae -005 a -43 c 2-b 419-980 b 795 bc 2 a 9
translation-type: tm+mt
source-git-commit: 4d3fdf9d90afab9d899a93561105a589742d838e

---


# hitGovernor

Das Plug-in „s.hitGovernor“ verfolgt die Gesamtzahl der Analytics-Bildanforderungen, die während eines vordefinierten rollierenden Zeitrahmens gesendet wurden, und kann bei Bedarf zusätzliche Logik ausführen, wenn diese Gesamtzahl einen bestimmten Schwellenwert überschreitet.

Obwohl Traffic von Bots, Spiders, bestimmten Benutzeragenten oder einer bestimmten Liste von IP-Adressen als Bot-Traffic erkannt oder anderweitig vom Reporting ausgeschlossen werden kann, enthalten Ihre Report Suites möglicherweise Traffic, der nicht berücksichtigt werden sollte. Zum Beispiel könnte eine unangemessen hohe Anzahl von Klicks oder Seitenaufrufen in einem sehr kurzen Zeitraum (d. h. ungefähr eine Anfrage pro Sekunde) ein Anzeichen für verfälschten Traffic sein.

Mit diesem Plug-in wird dieser Traffic für den Rest der Besucherlebensdauer automatisch blockiert und kann auch dynamisch in Berichten identifiziert werden.

## Funktionsweise des Plug-ins „hitGovernor“ {#section_541BC639E31442D09B1C85A2FFCDC02C}

Das Plug-in erhöht bei jeder Bildanforderung an Ihre Tracking-Server einen Cookie-Wert und verfolgt diesen über einen rollierenden Zeitrahmen hinweg. Der Standardzeitrahmen beträgt eine Minute, kann jedoch überschrieben werden. (Weitere Informationen finden Sie unter [Implementierung](../../../implement/js-implementation/plugins/hitgovernor.md#task_D4BDB524AA294C139AFCAE2B61FEA3F2) weiter unten.) If the total number of hits during that time frame exceeds the default hit threshold (60), a final custom link image request is sent to set the *`exceptionFlag`* context data variable. Dieser standardmäßige Schwellenwert für Treffer kann auch überschrieben werden. 

Bei Bedarf kann die Erfassung von Traffic für diesen bestimmten Besucher von diesem Zeitpunkt an für einen Standardzeitraum von 60 Tagen verhindert werden. Das Blockieren des Datenverkehrs erfordert eine zusätzliche Codezeile in Ihrer doPlugins-Funktion, wie unten beschrieben. Der Zeitrahmen kann ebenfalls angepasst werden. The logic allows time to either include that visitor's IP address, User Agent, or [!DNL Experience Cloud] Visitor ID in the proper permanent exception logic, or to reset the timeout period after the sixty days have elapsed. Wenn dieser Traffic nach 60 Tagen vom Plug-in als betrügerisch identifiziert wird, wird der Traffic erneut als Ausnahme gekennzeichnet und für weitere 60 Tage nicht erfasst.

## Berichterstellung {#section_E742F19B528041808454744DB2C7007C}

Es müssen keine Standardvariablen oder Ereignisse eingerichtet werden. Es wird jedoch dringend empfohlen, dass Sie Logik für Verarbeitungsregeln einrichten, um Variablen und Ereignisse entsprechend einzustellen. Diese benutzerspezifischen Variablen und Ereignisse können Folgendes enthalten:

* [!DNL Experience Cloud] Visitor ID
* IP-Adresse
* Benutzeragent
* Gekennzeichnetes Ausnahmeereignis

Durch das Erstellen von Segmenten für diese Variablen können Sie dann Segmente und virtuelle Report Suites anlegen, um die Auswirkungen dieser mehrdeutigen Treffer auf die Website insgesamt anzuzeigen.

Es wird empfohlen, mithilfe der erfassten Reporting-Werte die Bot-Regeln, DB VISTA-Regeln oder Firmen-IP-Ausschlüsse zu aktualisieren.

## Implementierung {#task_D4BDB524AA294C139AFCAE2B61FEA3F2}

Implementieren des Plug-ins „hitGovernor“:

1. Ändern Sie die AppMeasurement-Bibliothek.

   Um das Plug-in zu initialisieren, fügen Sie diese Codezeile (fettgedruckt) innerhalb der Funktion `registerPostTrackCallback` in den Code der AppMeasurement-Bibliothek ein.

   >[!NOTE]
   >
   >Although the `registerPostTrackCallback` functionality is included in AppMeasurement libraries 1.8.0+, it is not included in any custom code configuration by default. Sie wird im Anschluss an die doPlugins-Funktion und *außerhalb* von ihr aufgenommen.

   ```
    s.registerPostTrackCallback(function(){ 
    s.governor();
   }); 
   ```

   Fügen Sie unterhalb des Abschnitts „doPlugins“ in Ihrer AppMeasurement-Datei den Plug-in-Code ein, der in dem folgenden [Plug-in-Quellcode](../../../implement/js-implementation/plugins/hitgovernor.md#reference_76423C81A7A342B2AC4BE41490B27DE0) enthalten ist.

   Die Schwellenwerte für Treffer, Trefferzeitpunkt und die Zeitrahmen für den Traffic-Ausschluss können überschrieben werden, indem Sie diese Variablen außerhalb des Plug-ins selbst einstellen und vorzugsweise Ihre anderen Konfigurationsvariablen verwenden:

<table id="table_9959A40F5F0B40B39DB86E21D03E25FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variable </th> 
   <th colname="col2" class="entry"> Syntax </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Schwellenwert für Treffer </p> </td> 
   <td colname="col2"> <p> <code> s.hl = 60; </code> </p> </td> 
   <td colname="col3"> <p>Die Gesamtzahl der Treffer, die während eines bestimmten Zeitraums nicht überschritten werden sollten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Schwellenwert für Trefferzeitpunkt </p> </td> 
   <td colname="col2"> <p> <code> s.ht = 10; </code> </p> </td> 
   <td colname="col3"> <p>Das Zeitfenster für die Erfassung von Treffern in Sekunden. Diese Zahl wird durch sechs dividiert, um die rollierenden Zeitfenster zu bestimmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ausschlussschwellenwert </p> </td> 
   <td colname="col2"> <p> <code> s.he = 60; </code> </p> </td> 
   <td colname="col3"> <p>Anzahl der Tage, in denen das Ausschluss-Cookie für diesen Besucher festgelegt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ihre Implementierung verwendet möglicherweise einen anderen Objektnamen als das standardmäßige "Objekt" von Analytics. Aktualisieren Sie in diesem Fall den Objektnamen entsprechend.

1. Konfigurieren Sie Verarbeitungsregeln.

   Dieses Plug-in zeichnet gekennzeichnete Ausnahmen als Kontextdaten in einer Linktracking-Bildanforderung auf. Verarbeitungsregeln müssen so konfiguriert werden, dass sie diesen gekennzeichneten Ausnahmen geeignete Variablen wie die nachstehenden für das Tracking zuweisen.

   ![](assets/hitgov-config.png)

1. (Optional) Schließen Sie Code zum Blockieren von Traffic in doPlugins ein.

   Nachdem der Traffic als Ausnahme erkannt wurde, können alle nachfolgenden Treffer von diesem Besucher vollständig blockiert werden, indem dieser Code in die `doPlugins`-Funktion eingefügt wird:

   ```
   //Check for hit governor flag 
         if(s.Util.cookieRead('s_hg')==9)s.abort=true;
   ```

   Wenn dieser Code nicht enthalten ist, wird der Traffic von diesem Besucher gekennzeichnet, jedoch nicht blockiert.

## Plug-in-Quellcode {#reference_76423C81A7A342B2AC4BE41490B27DE0}

Dieser Code sollte unterhalb des Abschnitts „doPlugins“ in Ihrer AppMeasurement-Bibliothek hinzugefügt werden.

```
//Hit Governor (Version 0.1 BETA, 11-13-17) 
s.governor=new Function("","" 
+"var s=this;if(typeof s.hl=='undefined'){s.hl=60;}if(typeof s.ht=='u" 
+"ndefined'){s.ht=60;}if(typeof s.he=='undefined'){s.he=60;}if(s.Util" 
+".cookieRead('s_hg')==8){var i=new Date(),y=i.getFullYear(),m=i.getM" 
+"onth(),d=i.getDate(),i=new Date(y,m,d+s.he);s.Util.cookieWrite('s_h" 
+"g',9,i);return;}var f=s.Util.cookieRead('s_hc'),g=Number(s.Util.coo" 
+"kieRead('s_ht')),h=Math.floor((new Date()).getTime()),ha=f!=''?f.sp" 
+"lit('|').map(Number):[0,0,0,0,0],i=ha.reduce(function(ha,b){return " 
+"ha+b;},0),j=g==0?0:Math.floor(((h-g)/(s.ht/6))/1000);if(g==0)s.Util" 
+".cookieWrite('s_ht',h);if(i<s.hl){if(j>=1){if(j>=6){ha=[0,0,0,0,0];" 
+"}else{for(var k=0;k<j;k++){ha.unshift(0);ha.pop();}}s.Util.cookieWr" 
+"ite('s_ht',h);}}else{s.Util.cookieWrite('s_hg',8);s.linkTrackVars+=" 
+"',contextData.exceptionFlag';s.contextData['exceptionFlag']='true';" 
+"s.tl(this,'o','exceptionFlag');}ha[0]++;s.Util.cookieWrite('s_hc',h" 
+"a.join('|'));"); 
```

