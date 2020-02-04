---
title: getTimeToComplete
description: Messen Sie die zum Abschließen einer Aufgabe benötigte Zeit.
translation-type: tm+mt
source-git-commit: 180ad544541f25d02b3a257559bc045abed7387b

---


# Adobe-Plug-in: getTimeToComplete

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `getTimeToComplete` Plug-In verfolgt die Zeit, die ein Benutzer zum Abschluss eines Prozesses auf einer Site benötigt. Die &quot;Uhr&quot;beginnt, wenn die `start` Aktion aufgerufen wird, und endet, wenn die `stop` Aktion aufgerufen wird. Adobe empfiehlt die Verwendung dieses Plug-Ins, wenn ein Workflow auf der Site einige Zeit in Anspruch nimmt und Sie wissen möchten, wie viel Zeit die Besucher benötigen, um das Plug-In abzuschließen. Es ist nicht erforderlich, dieses Plug-in zu verwenden, wenn der Workflow auf Ihrer Site einen kurzen Zeitraum (weniger als 3 Sekunden) in Anspruch nimmt, da die Granularität nur auf die volle Sekunde reduziert wird.

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
   * Aktionstyp: Initialize getTimeToComplete
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
/* Adobe Consulting Plugin: getTimeToComplete v3.1 (Requires formatTime and inList plug-ins) */
s.getTimeToComplete=function(sos,cn,exp){sos=sos?sos.toLowerCase():"start";if("stop"===sos||"start"===sos){cn=cn?cn:"s_gttc";exp=exp?exp:0;var s=this,d=s.c_r(cn),e=new Date;if("start"===sos&&!d)s.c_w(cn,e.getTime(),exp?new Date(e.getTime()+864E5*exp):0);else if("stop"===sos&&d)return sos=Math.round((e.getTime()-d)/1E3),s.c_w(cn,"",0),s.formatTime(sos)}};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0,ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getTimeToComplete` Methode verwendet die folgenden Argumente:

* **`sos`**(optional, Zeichenfolge): Legen Sie fest,`"start"`wann der Timer gestartet werden soll. Legen Sie fest,`"stop"`wann der Timer angehalten werden soll. Die Standardeinstellung ist`"start"`.
* **`cn`**(optional, Zeichenfolge): Der Name des Cookies, mit dem die Startzeit gespeichert werden soll. Die Standardeinstellung ist`"s_gttc"`.
* **`exp`**(optional, integer): Die Anzahl der Tage, in denen das Cookie (und der Timer) abläuft. Die Standardeinstellung ist`0`das Ende der Browsersitzung.

Beim Aufrufen dieser Methode wird eine Zeichenfolge zurückgegeben, die die Anzahl der Tage, Stunden, Minuten und/oder Sekunden zwischen der `"start"` und der `"stop"` Aktion enthält.

## Beispielaufrufe

### Beispiel 1

Verwenden Sie diese Aufrufe, um die Zeit zwischen dem Start des Kassengangprozesses durch einen Besucher und dem Kaufvorgang zu bestimmen.

Starten Sie den Timer, wenn der Besucher den Checkout startet:

```js
if(s.events.indexOf("scCheckout") > -1) s.getTimeToComplete("start");
```

Beenden Sie den Timer, wenn der Besucher den Einkauf tätigt, und setzen Sie prop1 auf den Zeitunterschied zwischen Stopp und Start:

```js
if(s.events.indexOf("purchase") > -1) s.prop1 = s.getTimeToComplete("stop");
```

s.prop1 erfasst die zum Abschluss des Kaufprozesses benötigte Zeit

### Beispiel 2

Wenn mehrere Timer gleichzeitig ausgeführt werden sollen (um verschiedene Prozesse zu messen), müssen Sie das cn-Cookie-Argument manuell festlegen.  Wenn Sie z. B. die für den Abschluss eines Kaufs erforderliche Zeit messen möchten, legen Sie den folgenden Code fest...

```javascript
if(s.inList(s.events, "scCheckout")) s.getTimeToComplete("start", "gttcpurchase");
if(s.inList(s.events, "purchase")) s.prop1 = s.getTimeToComplete("start", "gttcpurchase");
```

 ...Wenn Sie aber auch (gleichzeitig) messen möchten, wie lange ein Registrierungsformular ausgefüllt werden muss, führen Sie auch den folgenden Code aus:

```js
if(s.inList(s.events, "event1")) s.getTimeToComplete("start", "gttcregister", 7);
if(s.inList(s.events, "event2")) s.prop2 = s.getTimeToComplete("stop", "gttcregister", 7);
```

Im zweiten Beispiel soll event1 den Beginn eines Registrierungsprozesses erfassen, der - aus welchen Gründen auch immer - bis zu 7 Tagen dauern kann, und event2 soll den Abschluss der Registrierung erfassen.  s.prop2 erfasst die Zeit, die zum Abschluss des Registrierungsprozesses benötigt wird

## Versionsverlauf

### 3.1 (30. September 2019)

* Es wurde eine Logik hinzugefügt, die den Wert &quot;start&quot;oder &quot;stop&quot;im ersten Argument erfordert.  Alle anderen übergebenen Werte verhindern, dass das Plug-In ausgeführt wird.
* Aktualisierung des `inList 2.0` Plug-ins auf `inList 2.1`.

### 3.0 (23. August 2018)

* Aktualisierung des `formatTime v1.0` Plug-Ins auf `formatTime v1.1`.

### 3.0 (17. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße).
* Geringfügige Fehlerbehebungen.

### 2.0. Juni 216)

* Die Abhängigkeit vom `p_fo` Plug-In wurde beseitigt.
* Kompatibilität mit H-Code und AppMeasurement hinzugefügt.
* Konsolenprotokollierung hinzugefügt.
