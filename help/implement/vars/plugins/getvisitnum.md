---
title: getVisitNum
description: Verfolgen Sie die aktuelle Besuchsnummer eines Besuchers.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 100%

---


# Adobe-Plug-in: getVisitNum

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getVisitNum`-Plug-in gibt die Besuchsnummer für alle Besucher zurück, die innerhalb der gewünschten Anzahl von Tagen auf die Website kommen. Analysis Workspace bietet die Dimension „Besuchsnummer“, die ähnliche Funktionen bietet. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie mehr Kontrolle darüber haben möchten, wie die Besuchsnummer inkrementiert wird. Dieses Plug-in ist nicht erforderlich, wenn die integrierte Dimension „Besuchsnummer“ in Analysis Workspace für Ihre Berichtsanforderungen ausreicht.

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
   * Aktionstyp: getVisitNum initialisieren
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
/* Adobe Consulting Plugin: getVisitNum v4.11 (Requires endOfDatePeriod plug-in) */
s.getVisitNum=function(rp,erp){var s=this,c=function(rp){return isNaN(rp)?!1:(parseFloat(rp)|0)===parseFloat(rp)};rp=rp?rp:365;erp= "undefined"!==typeof erp?!!erp:c(rp)?!0:!1;var e=(new Date).getTime(),b=endOfDatePeriod(rp);if(s.c_r("s_vnc"+rp))var g=s.c_r("s_vnc"+rp).split("&vn="),d=g[1];if(s.c_r("s_ivc"))return d?(b.setTime(e+18E5),s.c_w("s_ivc",!0,b),d):"unknown visit number";if("undefined"!==typeof d)return d++,c=erp&&c(rp)?e+864E5*rp:g[0],b.setTime(c),s.c_w("s_vnc"+rp,c+"&vn="+d,b),b.setTime(e+ 18E5),s.c_w("s_ivc",!0,b),d;c=c(rp)?e+864E5*rp:endOfDatePeriod(rp).getTime();s.c_w("s_vnc"+rp,c+"&vn=1",b);b.setTime(e+18E5); s.c_w("s_ivc",!0,b);return"1"};

/* Adobe Consulting Plugin: endOfDatePeriod v1.1 */
var endOfDatePeriod=function(dp){var a=new Date,b=isNaN(dp)?0:Math.floor(dp);a.setHours(23);a.setMinutes(59);a.setSeconds(59); "w"===dp&&(b=6-a.getDay());if("m"===dp){b=a.getMonth()+1;var d=a.getFullYear();b=(new Date(d?d:1970,b?b:1,0)).getDate()-a.getDate()}a.setDate(a.getDate()+b);"y"===dp&&(a.setMonth(11),a.setDate(31));return a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getVisitNum`-Methode verwendet die folgenden Argumente:

* **`rp`** (optional, Ganzzahl ODER Zeichenfolge): Die Anzahl der Tage, bevor der Besuchsnummerzähler zurückgesetzt wird.  Die Standardeinstellung ist `365`, wenn nicht festgelegt.
   * Wenn dieses Argument `"w"` ist, wird der Zähler am Ende der Woche (an diesem Samstag um 23:59 Uhr) zurückgesetzt
   * Wenn dieses Argument `"m"` ist, wird der Zähler am Ende des Monats (am letzten Tag dieses Monats) zurückgesetzt
   * Wenn dieses Argument `"y"` ist, wird der Zähler am Ende des Jahres (am 31. Dezember) zurückgesetzt
* **`erp`** (optional, boolesch): Wenn das `rp`-Argument eine Zahl ist, bestimmt dieses Argument, ob die Gültigkeit der Besuchsnummer verlängert werden soll. Wenn der Wert auf `true` gesetzt wird, wird der Besuchsnummernzähler durch nachfolgende Treffer auf Ihrer Website zurückgesetzt. Wenn der Wert auf `false` gesetzt wird, werden nachfolgende Treffer auf Ihrer Website nicht verlängert, wenn der Zähler für die Besuchsnummer zurückgesetzt wird. Die Standardeinstellung ist `true`. Dieses Argument ist nicht gültig, wenn das `rp`-Argument eine Zeichenfolge ist.

Die Anzahl der Besuche wird erhöht, wenn der Besucher nach 30 Minuten Inaktivität zu Ihrer Website zurückkehrt. Der Aufruf dieser Methode gibt eine Ganzzahl zurück, die die aktuelle Besuchsnummer des Besuchers angibt.

Dieses Plug-in setzt ein Erstanbieter-Cookie mit dem Namen `"s_vnc[LENGTH]"`, wobei `[LENGTH]` der Wert ist, der an das `rp`-Argument übergeben wird. Beispiele: `"s_vncw"`, `"s_vncm"` oder `"s_vnc365"`. Der Wert des Cookies ist eine Kombination aus einem Unix-Zeitstempel, der angibt, wann die Besuchsanzahl zurückgesetzt wird, z. B. Ende der Woche, Ende des Monats oder nach 365 Tagen Inaktivität. Er enthält auch die aktuelle Besuchsnummer. Dieses Plug-in setzt ein weiteres Cookie mit dem Namen `"s_ivc"`, das auf `true` gesetzt ist und nach 30 Minuten Inaktivität abläuft.

## Beispielaufrufe

### Beispiel 1

Für einen Besucher, der innerhalb der letzten 365 Tage nicht auf der Website war, setzt der folgende Code s.prop1 auf den Wert „1“:

```js
s.prop1=s.getVisitNum();
```

### Beispiel 2

Für einen Besucher, der innerhalb von 364 Tagen nach seinem ersten Besuch auf die Website zurückkehrt, setzt der folgende Code s.prop1 auf „2“:

```js
s.prop1=s.getVisitNum(365);
```

Wenn dieser Besucher innerhalb von 364 Tagen nach seinem zweiten Besuch auf die Website zurückkehrt, setzt der folgende Code s.prop1 auf „3“:

```js
s.prop1=s.getVisitNum(365);
```

### Beispiel 3

Für einen Besucher, der innerhalb von 179 Tagen nach seinem ersten Besuch auf die Website zurückkehrt, setzt der folgende Code s.prop1 auf „2“:

```js
s.prop1=s.getVisitNum(180,false);
```

Wenn dieser Besucher jedoch 1 oder mehrere Tage nach seinem zweiten Besuch auf die Website zurückkehrt, setzt der folgende Code s.prop1 auf „1“:

```js
s.prop1=s.getVisitNum(180,false);
```

Wenn das zweite Argument im Aufruf gleich „false“ ist, wird die Routine, die bestimmt, wann die Besuchsnummer auf „1“ „zurückgesetzt“ werden soll, dies „x“ Tage – in diesem Beispiel 365 Tage – nach dem ersten Besuch des Besuchers auf der Website tun.

Wenn das zweite Argument gleich „true“ (oder nicht gesetzt) ist, setzt das Plug-in die Besuchsnummer erst nach „x“ Tagen – in diesem Beispiel 365 Tage – der Besucherinaktivität auf „1“ zurück.

### Beispiel 4

Für alle Besucher, die während der laufenden Woche – beginnend am Sonntag – zum ersten Mal auf die Website kommen, setzt der folgende Code s.prop1 auf „1“:

```js
s.prop1=s.getVisitNum("w");
```

### Beispiel 5

Für alle Besucher, die im laufenden Monat zum ersten Mal auf die Website kommen – beginnend mit dem ersten Tag jedes Monats – setzt der folgende Code s.prop1 auf „1“:

```js
s.prop1=s.getVisitNum("m");
```

Denken Sie daran, dass das getVisitNum-Plug-in Retail-basierte Kalender (d. h. 4-5-4, 4-4-5 usw.) nicht berücksichtigt.

### Beispiel 6

Für alle Besucher, die während des laufenden Jahres – beginnend am 1. Januar – zum ersten Mal auf die Website kommen, setzt der folgende Code s.prop1 auf „1“:

```js
s.prop1=s.getVisitNum("y");
```

### Beispiel 7

Wenn Sie die Besuchsnummer eines Besuchers für die Woche, die Besuchsnummer des Besuchers für den Monat und die Besuchsnummer des Besuchers für das Jahr – alle innerhalb verschiedener Analytics-Variablen – verfolgen möchten, sollten Sie Code verwenden, der dem Folgenden ähnelt:

```js
s.prop1=s.getVisitNum("w");
s.prop2=s.getVisitNum("m");
s.prop3=s.getVisitNum("y");
```

In diesem Fall erstellt das Plug-in drei verschiedene Cookies – eines für jeden der verschiedenen Zeiträume, um die individuelle Besuchsnummer pro Zeitraum zu verfolgen.

## Versionsverlauf

### 4.11 (30. September 2019)

* Ein Problem wurde behoben, bei dem das `erp`-Argument explizit auf `false` gesetzt wurde.

### 4.1 (21. Mai 2018)

* `endOfDatePeriod`-Plug-in auf v1.1 aktualisiert.

### 4.0 (17. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe).
* Cookie-Argumente wurden entfernt, da das Plug-in jetzt dynamisch Cookies basierend auf dem `rp`-Argument generiert.

### 3.0 (5. Juni 2016)

* Vollständige Überarbeitung.
* Alle vorherigen Lösungen, die in verschiedenen Versionen des `getVisitNum`-Plug-ins verfügbar sind, wurden zusammengeführt.
