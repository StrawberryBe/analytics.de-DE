---
title: getTimeSinceLastVisit
description: Messen Sie den Zeitraum zwischen zwei Besuchen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getTimeSinceLastVisit

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getTimeSinceLastVisit` Plug-in können Sie verfolgen, wie lange ein Besucher nach dem letzten Besuch zu Ihrer Site zurückkehrt.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe Angebots ist eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Catalog] Schaltfläche
1. Installieren und Veröffentlichen der [!UICONTROL Common Analytics Plugins] Erweiterung
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung &quot;Plug-ins initialisieren&quot;mit der folgenden Konfiguration:
   * Bedingung: Keines
   * Ereignis: Core - Bibliothek geladen (Seitenanfang)
1. Hinzufügen Sie eine Aktion mit der folgenden Konfiguration auf die oben stehende Regel:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialize getTimeSinceLastVisit
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter der Adobe Analytics-Erweiterung.
1. Erweitern Sie das [!UICONTROL Configure tracking using custom code] Akkordeon, das die [!UICONTROL Open Editor] Schaltfläche einblendet.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getTimeSinceLastVisit v1.0 (Requires formatTime and inList plug-ins) */
s.getTimeSinceLastVisit=function(){var s=this,a=new Date,b=a.getTime(),c=s.c_r("s_tslv")||0,d=Math.round((b-c)/1E3);a.setTime(b+63072E6);s.c_w("s_tslv",b,a);return c?1800<d&&s.formatTime?s.formatTime(d):"":"New Visitor"};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0, ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
 /******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getTimeSinceLastVisit` Methode verwendet keine Argumente. Gibt den Zeitraum zurück, der seit dem letzten Besuch des Besuchers auf der Site verstrichen ist und im folgenden Format zusammengefasst wurde:

* Die Zeit zwischen 30 Minuten und einer Stunde seit dem letzten Besuch wird auf die nächste halbe Minute-Benchmark gesetzt. Beispiel, `"30.5 minutes"`, `"53 minutes"`
* Die Zeit zwischen einer Stunde und einem Tag wird auf die nächste viertelstündige Benchmark gerundet. Beispiel, `"2.25 hours"`, `"7.5 hours"`
* Die Zeit, die länger als ein Tag ist, wird auf den nächsten Tag gerundet. Beispiel, `"1 day"`, `"3 days"`, `"9 days"`, `"372 days"`
* Wenn ein Besucher vor oder nach Ablauf von zwei Jahren noch nicht besucht wurde, wird der Wert auf `"New Visitor"`festgelegt.

> [!NOTE] Dieses Plug-In gibt nur einen Wert beim ersten Treffer eines Besuchs zurück.

Dieses Plug-in erstellt ein Erstanbieter-Cookie, das auf einen Unix-Zeitstempel der aktuellen Zeit `"s_tslv"` gesetzt wird. Das Cookie läuft nach zwei Jahren Inaktivität ab.

## Beispielaufrufe

### Beispiel 1

Wenn ein brandneuer Besucher zur Site kommt und der folgende Code auf der ersten Seite des Besuchs ausgeführt wird ...

```javascript
s.prop1 = s.getTimeSinceLastVisit();
s.linkTrackVars = s.apl(s.linkTrackVars, "prop1") //ensures that prop1 will be included on the first hit of the visit
```

...Der Wert von s.prop1 wird gleich &quot;Neuer Besucher&quot;gesetzt.

Wenn derselbe Code nach 35 Minuten Inaktivität auf derselben Domäne ausgeführt wird, wird der Wert von s.prop1 auf &quot;35 Minuten&quot;eingestellt.

Wenn derselbe Code nach 4 Tagen weiterer Inaktivität auf derselben Domäne ausgeführt wird, wird der Wert von s.prop1 auf &quot;4 Tage&quot;gesetzt.

## Versionsverlauf

### 1.0 (16. April 2018)

* Point Release (neu kompilierter Code und kleinere Größe).
* Aus dem `getDaysSinceLastVisit` Plug-In abgeleiteter Code (jetzt nicht mehr unterstützt und umbenannt).
* Verwendet jetzt `formatTime` und `inList` Plug-ins als Rückgabewert.
