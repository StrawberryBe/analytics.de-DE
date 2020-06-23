---
title: getTimeToComplete
description: Messen Sie die Zeit, die zum Ausführen einer Aufgabe benötigt wird.
translation-type: ht
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe-Plug-in: getTimeToComplete

>[!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getTimeToComplete`-Plug-in verfolgt die Zeit, die ein Benutzer zum Ausführen eines Prozesses auf einer Website benötigt. Die Zeiterfassung beginnt mit dem Aufruf der `start`-Aktion und endet mit dem Aufruf der `stop`-Aktion. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn es auf der Website einen Workflow gibt, der einige Zeit in Anspruch nimmt, und Sie wissen möchten, wie viel Zeit die Besucher benötigen, um ihn abzuschließen. Es ist nicht erforderlich, dieses Plug-in zu verwenden, wenn der Arbeitsablauf auf Ihrer Website eine kurze Zeitspanne (weniger als 3 Sekunden) in Anspruch nimmt, da die Granularität auf die volle Sekunde begrenzt ist.

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
   * Aktionstyp: getTimeToComplete initialisieren
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
/* Adobe Consulting Plugin: getTimeToComplete v3.1 (Requires formatTime and inList plug-ins) */
s.getTimeToComplete=function(sos,cn,exp){sos=sos?sos.toLowerCase():"start";if("stop"===sos||"start"===sos){cn=cn?cn:"s_gttc";exp=exp?exp:0;var s=this,d=s.c_r(cn),e=new Date;if("start"===sos&&!d)s.c_w(cn,e.getTime(),exp?new Date(e.getTime()+864E5*exp):0);else if("stop"===sos&&d)return sos=Math.round((e.getTime()-d)/1E3),s.c_w(cn,"",0),s.formatTime(sos)}};

/* Adobe Consulting Plugin: formatTime v1.1 (Requires inList plug-in) */
s.formatTime=function(ns,tf,bml){var s=this;if(!("undefined"===typeof ns||isNaN(ns)||0>Number(ns))){if("string"===typeof tf&&"d"===tf||("string"!==typeof tf||!s.inList("h,m,s",tf))&&86400<=ns){tf=86400;var d="days";bml=isNaN(bml)?1:tf/(bml*tf)} else"string"===typeof tf&&"h"===tf||("string"!==typeof tf||!s.inList("m,s",tf))&&3600<=ns?(tf=3600,d="hours", bml=isNaN(bml)?4: tf/(bml*tf)):"string"===typeof tf&&"m"===tf||("string"!==typeof tf||!s.inList("s",tf))&&60<=ns?(tf=60,d="minutes",bml=isNaN(bml)?2: tf/(bml*tf)):(tf=1,d="seconds",bml=isNaN(bml)?.2:tf/bml);ns=Math.round(ns*bml/tf)/bml+" "+d;0===ns.indexOf("1 ")&&(ns=ns.substring(0,ns.length-1));return ns}};

/* Adobe Consulting Plugin: inList v2.1 */
s.inList=function(lv,vtc,d,cc){if("string"!==typeof vtc)return!1;if("string"===typeof lv)lv=lv.split(d||",");else if("object"!== typeof lv)return!1;d=0;for(var e=lv.length;d<e;d++)if(1==cc&&vtc===lv[d]||vtc.toLowerCase()===lv[d].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getTimeToComplete`-Methode verwendet die folgenden Argumente:

* **`sos`** (optional, Zeichenfolge): Stellen Sie `"start"` ein, wenn Sie den Timer starten möchten. Stellen Sie `"stop"` ein, wenn Sie den Timer anhalten möchten. Die Standardeinstellung ist `"start"`.
* **`cn`** (optional, Zeichenfolge): Der Name des Cookies, in dem der Startzeit gespeichert werden soll. Die Standardeinstellung ist `"s_gttc"`.
* **`exp`** (optional, Ganzzahl): Die Anzahl der Tage, in denen das Cookie (und der Timer) abläuft. Die Standardeinstellung ist `0`, was das Ende der Browser-Sitzung darstellt.

Beim Aufrufen dieser Methode wird eine Zeichenfolge zurückgegeben, die die Anzahl der Tage, Stunden, Minuten und/oder Sekunden zwischen der `"start"`- und der `"stop"`-Aktion enthält.

## Beispielaufrufe

### Beispiel 1

Verwenden Sie diese Anrufe, um die Zeit zwischen dem Beginn des Checkout-Prozesses und dem Kauf zu bestimmen.

Starten Sie den Timer, wenn der Besucher den Checkout startet:

```js
if(s.events.indexOf("scCheckout") > -1) s.getTimeToComplete("start");
```

Beenden Sie den Timer, wenn der Besucher den Kauf tätigt, und setzen Sie prop1 auf den Zeitunterschied zwischen Stopp und Start:

```js
if(s.events.indexOf("purchase") > -1) s.prop1 = s.getTimeToComplete("stop");
```

s.prop1 erfasst die zum Abschluss des Kaufprozesses benötigte Zeit

### Beispiel 2

Wenn mehrere Timer gleichzeitig ausgeführt werden sollen (um verschiedene Prozesse zu messen), müssen Sie das cn-Cookie-Argument manuell festlegen.  Wenn Sie z. B. die Zeit messen möchten, die für den Abschluss eines Kaufs benötigt wird, würden Sie den folgenden Code festlegen ...

```javascript
if(s.inList(s.events, "scCheckout")) s.getTimeToComplete("start", "gttcpurchase");
if(s.inList(s.events, "purchase")) s.prop1 = s.getTimeToComplete("start", "gttcpurchase");
```

... aber wenn Sie auch (gleichzeitig) die Zeit messen wollten, die für das Ausfüllen eines Anmeldeformulars benötigt wird, würden Sie auch den folgenden Code ausführen:

```js
if(s.inList(s.events, "event1")) s.getTimeToComplete("start", "gttcregister", 7);
if(s.inList(s.events, "event2")) s.prop2 = s.getTimeToComplete("stop", "gttcregister", 7);
```

Im zweiten Beispiel soll event1 den Beginn eines Registrierungsprozesses erfassen, der – aus welchen Gründen auch immer – bis zu 7 Tagen dauern kann, und event2 soll den Abschluss der Registrierung erfassen.  s.prop2 erfasst die zum Abschluss des Registrierungsprozesses benötigte Zeit

## Versionsverlauf

### 3.1 (30. September 2019)

* Es wurde eine Logik hinzugefügt, die im ersten Argument entweder den Wert „start“ oder „stop“ erfordert.  Alle anderen übergebenen Werte verhindern die Ausführung des Plug-ins.
* `inList 2.0`-Plug-in auf `inList 2.1` aktualisiert.

### 3.0 (23. August 2018)

* `formatTime v1.0`-Plug-in auf `formatTime v1.1` aktualisiert.

### 3.0 (17. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe).
* Geringfügige Fehlerbehebungen.

### 2.0 (21. Juni 2016)

* Die Abhängigkeit vom `p_fo`-Plug-in wurde beseitigt.
* Kompatibilität mit H-Code und AppMeasurement hinzugefügt.
* Konsolenprotokollierung hinzugefügt.
