---
title: getVisitNum
description: Verfolgen Sie die aktuelle Besuchsnummer eines Besuchers.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-Plug-in: getVisitNum

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `getVisitNum` Plugin gibt die Besuchsnummer für alle Besucher zurück, die innerhalb der gewünschten Anzahl von Tagen zur Site gelangen. Der Arbeitsbereich für Analysen bietet die Dimension &quot;Besuchsnummer&quot;, die ähnliche Funktionen bietet. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie mehr Kontrolle darüber haben möchten, wie die Besuchsnummer inkrementiert wird. Dieses Plug-in ist nicht erforderlich, wenn die integrierte Dimension &quot;Besuch-Nr.&quot;im Analysis Workspace für Ihre Berichtsanforderungen ausreicht.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog]
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins]
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung &quot;Plug-ins initialisieren&quot;mit der folgenden Konfiguration:
   * Bedingung: Keines
   * Ereignis: Core - Bibliothek geladen (Seitenanfang)
1. Fügen Sie der oben stehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialisieren von getVisitNum
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
1. Erweitern Sie die [!UICONTROL Verfolgung mithilfe eines benutzerdefinierten Code] -Akkordeons, das die Schaltfläche zum [!UICONTROL Öffnen des Editors] anzeigt.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung `s_gi`). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getVisitNum v4.11 (Requires endOfDatePeriod plug-in) */
s.getVisitNum=function(rp,erp){var s=this,c=function(rp){return isNaN(rp)?!1:(parseFloat(rp)|0)===parseFloat(rp)};rp=rp?rp:365;erp= "undefined"!==typeof erp?!!erp:c(rp)?!0:!1;var e=(new Date).getTime(),b=endOfDatePeriod(rp);if(s.c_r("s_vnc"+rp))var g=s.c_r("s_vnc"+rp).split("&vn="),d=g[1];if(s.c_r("s_ivc"))return d?(b.setTime(e+18E5),s.c_w("s_ivc",!0,b),d):"unknown visit number";if("undefined"!==typeof d)return d++,c=erp&&c(rp)?e+864E5*rp:g[0],b.setTime(c),s.c_w("s_vnc"+rp,c+"&vn="+d,b),b.setTime(e+ 18E5),s.c_w("s_ivc",!0,b),d;c=c(rp)?e+864E5*rp:endOfDatePeriod(rp).getTime();s.c_w("s_vnc"+rp,c+"&vn=1",b);b.setTime(e+18E5); s.c_w("s_ivc",!0,b);return"1"};

/* Adobe Consulting Plugin: endOfDatePeriod v1.1 */
var endOfDatePeriod=function(dp){var a=new Date,b=isNaN(dp)?0:Math.floor(dp);a.setHours(23);a.setMinutes(59);a.setSeconds(59); "w"===dp&&(b=6-a.getDay());if("m"===dp){b=a.getMonth()+1;var d=a.getFullYear();b=(new Date(d?d:1970,b?b:1,0)).getDate()-a.getDate()}a.setDate(a.getDate()+b);"y"===dp&&(a.setMonth(11),a.setDate(31));return a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getVisitNum` Methode verwendet die folgenden Argumente:

* **`rp`**(optional, Ganzzahl-ODER-Zeichenfolge): Die Anzahl der Tage vor dem Zurücksetzen des Zählers für die Besuchnummer.  Die Standardeinstellung ist`365`nicht festgelegt.
   * Wenn dieses Argument verwendet wird, `"w"`wird der Zähler am Ende der Woche (Samstag um 23:59 Uhr) zurückgesetzt
   * Wenn dieses Argument `"m"`verwendet wird, wird der Zähler am Ende des Monats (dem letzten Tag dieses Monats) zurückgesetzt.
   * Wenn dieses Argument verwendet wird `"y"`, wird der Zähler am Ende des Jahres (31. Dezember) zurückgesetzt.
* **`erp`**(optional, boolean): Wenn das`rp`Argument eine Zahl ist, bestimmt dieses Argument, ob der Ablauf der Besuchsnummer verlängert werden soll. Bei Festlegung auf`true`wird der Zähler für die Besuchsnummer bei nachfolgenden Treffern auf Ihrer Site zurückgesetzt. Bei Festlegung auf`false`verlängern sich nachfolgende Treffer auf Ihrer Site nicht, wenn der Zähler für die Besuchsnummer zurückgesetzt wird. Die Standardeinstellung ist`true`. Dieses Argument ist nicht gültig, wenn das`rp`Argument eine Zeichenfolge ist.

Die Anzahl der Besuche wird erhöht, wenn der Besucher nach 30 Minuten Inaktivität zu Ihrer Site zurückkehrt. Der Aufruf dieser Methode gibt eine Ganzzahl zurück, die die aktuelle Besuchsnummer des Besuchers angibt.

Dieses Plug-in setzt ein Erstanbieter-Cookie, das heißt, `"s_vnc[LENGTH]"` wobei `[LENGTH]` der Wert, der an das `rp` Argument übergeben wird, angegeben wird. Beispiel: `"s_vncw"`, `"s_vncm"`oder `"s_vnc365"`. Der Wert des Cookies ist eine Kombination aus einem Unix-Zeitstempel, der angibt, wann der Besuchszähler zurückgesetzt wird, z. B. Ende der Woche, Ende des Monats oder nach 365 Tagen Inaktivität. Er enthält auch die aktuelle Besuchsnummer. Dieses Plug-in setzt ein weiteres Cookie namens `"s_ivc"` , das nach 30 Minuten Inaktivität auf `true` und abläuft.

## Beispielaufrufe

### Beispiel 1

Für Besucher, die innerhalb der letzten 365 Tage nicht zur Site gegangen sind, setzt der folgende Code s.prop1 auf den Wert 1:

```js
s.prop1=s.getVisitNum();
```

### Beispiel 2

Für Besucher, die innerhalb von 364 Tagen nach ihrem ersten Besuch zur Site zurückkehren, setzt der folgende Code s.prop1 auf 2:

```js
s.prop1=s.getVisitNum(365);
```

Wenn der Besucher innerhalb von 364 Tagen nach seinem zweiten Besuch zur Site zurückkehrt, setzt der folgende Code s.prop1 auf 3:

```js
s.prop1=s.getVisitNum(365);
```

### Beispiel 3

Für Besucher, die innerhalb von 179 Tagen nach ihrem ersten Besuch zur Site zurückkehren, setzt der folgende Code s.prop1 auf 2:

```js
s.prop1=s.getVisitNum(180,false);
```

Wenn dieser Besucher jedoch 1 oder mehr Tage nach seinem zweiten Besuch zur Site zurückkehrt, setzt der folgende Code s.prop1 gleich 1:

```js
s.prop1=s.getVisitNum(180,false);
```

Wenn das zweite Argument im Aufruf mit &quot;false&quot;identisch ist, legt die Routine fest, wann die Besuchsnummer auf &quot;1&quot;zurückgesetzt werden soll, dies mit &quot;x&quot;der Anzahl der Tage - in diesem Beispiel 365 Tage - nach dem ersten Besuch des Besuchers auf der Site vor.

Wenn das zweite Argument &quot;true&quot;ist (oder gar nicht festgelegt ist), setzt das Plug-in die Besuchsnummer erst dann auf 1 zurück, wenn die Anzahl der Tage - in diesem Beispiel 365 Tage - der Besucherinaktivität &quot;x&quot;erreicht ist.

### Beispiel 4

Für alle Besucher, die die Site zum ersten Mal in der aktuellen Woche - beginnend am Sonntag - aufrufen, setzt der folgende Code s.prop1 gleich 1:

```js
s.prop1=s.getVisitNum("w");
```

### Beispiel 5

Für alle Besucher, die die Site zum ersten Mal im aktuellen Monat aufrufen - beginnend am ersten Tag jedes Monats - setzt der folgende Code s.prop1 auf 1:

```js
s.prop1=s.getVisitNum("m");
```

Denken Sie daran, dass das getVisitNum-Plug-in nicht auf den Handel bezogene Kalender berücksichtigt (d. h. 4-5-4, 4-4-5 usw.)

### Beispiel 6

Für alle Besucher, die die Site zum ersten Mal im aktuellen Jahr - beginnend am 1. Januar - aufrufen, setzt der folgende Code s.prop1 gleich 1:

```js
s.prop1=s.getVisitNum("y");
```

### Beispiel 7

Wenn Sie die Besuchsnummer eines Besuchers für die Woche, die Besuchsnummer des Besuchers für den Monat und die Besuchsnummer des Besuchers für das Jahr - alle innerhalb verschiedener Analytics-Variablen - verfolgen möchten, sollten Sie Code verwenden, der dem Folgenden ähnelt:

```js
s.prop1=s.getVisitNum("w");
s.prop2=s.getVisitNum("m");
s.prop3=s.getVisitNum("y");
```

In diesem Fall erstellt das Plug-in drei verschiedene Cookies - eines für jeden der verschiedenen Zeiträume -, um die individuelle Besuchsnummer pro Zeitraum zu verfolgen.

## Versionsverlauf

### 4.11 (30. September 2019)

* Es wurde ein Problem behoben, bei dem das `erp` Argument explizit auf `false`eingestellt war.

### 4.1 (21. Mai 2018)

* Das `endOfDatePeriod` Plug-In wurde auf Version 1.1 aktualisiert.

### 4.0 (17. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße).
* Cookie-Argumente wurden entfernt, da das Plug-In nun dynamisch Cookies basierend auf dem `rp` Argument generiert)

### 3.0 (5. Juni 2016)

* Vollständige Überarbeitung
* Alle vorherigen Lösungen, die in verschiedenen Versionen des `getVisitNum` Plug-Ins verfügbar sind, wurden kombiniert.
