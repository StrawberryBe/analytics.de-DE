---
title: getTimeSinceLastVisit
description: Messen Sie den Zeitraum zwischen zwei Besuchen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-Plug-in: getTimeSinceLastVisit

>[!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getTimeSinceLastVisit`-Plug-in können Sie verfolgen, wie lange ein Besucher nach seinem letzten Besuch gebraucht hat, um zu Ihrer Website zurückzukehren.

## Installieren des Plug-ins mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: getTimeSinceLastVisit initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

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

## Verwenden des Plug-ins

Die `getTimeSinceLastVisit`-Methode verwendet keine Argumente. Sie gibt die seit dem letzten Website-Besuch des Besuchers verstrichene Zeit in folgendem Format zurück:

* Eine Zeit zwischen 30 Minuten und einer Stunde seit dem letzten Besuch wird auf den nächsten halbminütigen Benchmark gesetzt. Beispiel: `"30.5 minutes"`, `"53 minutes"`.
* Eine Zeit zwischen einer Stunde und einem wird auf den nächsten viertelstündigen Benchmark gerundet. Beispiel: `"2.25 hours"`, `"7.5 hours"`.
* Eine Zeit, die länger als ein Tag ist, wird auf den nächsten Tages-Benchmark gerundet. Beispiel: `"1 day"`, `"3 days"`, `"9 days"`, `"372 days"`.
* Wenn ein Besucher noch nie zuvor einen Besuch gemacht hat oder die verstrichene Zeit größer als zwei Jahre ist, wird der Wert auf `"New Visitor"` gesetzt.

>[!NOTE] Dieses Plug-in gibt nur einen Wert beim ersten Treffer eines Besuchs zurück.

Dieses Plug-in erzeugt ein First-Party-Cookie namens `"s_tslv"`, das auf einen Unix-Zeitstempel der aktuellen Zeit gesetzt wird. Das Cookie läuft nach zwei Jahren Inaktivität ab.

## Beispielaufrufe

### Beispiel 1

Wenn ein brandneuer Besucher zur Website kommt und der folgende Code auf der ersten Seite des Besuchs ausgeführt wird ...

```javascript
s.prop1 = s.getTimeSinceLastVisit();
s.linkTrackVars = s.apl(s.linkTrackVars, "prop1") //ensures that prop1 will be included on the first hit of the visit
```

... wird der Wert von s.prop1 auf „Neuer Besucher“ gesetzt.

Wenn derselbe Code nach 35 Minuten Inaktivität auf derselben Domäne ausgeführt wird, wird der Wert von s.prop1 auf „35 Minuten“ eingestellt.

Wenn derselbe Code nach 4 Tagen weiterer Inaktivität auf derselben Domäne ausgeführt wird, wird der Wert von s.prop1 auf „4 Tage“ gesetzt.

## Versionsverlauf

### 1.0 (16. April 2018)

* Zwischenversion (neu kompilierter Code und kleinere Code-Größe).
* Aus dem Plug-in `getDaysSinceLastVisit` abgeleiteter Code (jetzt veraltet und umbenannt).
* Verwendet jetzt die Plug-ins `formatTime` und `inList` für den Rückgabewert.
