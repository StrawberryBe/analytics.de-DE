---
title: getPageName
description: Erstellen Sie einen leicht lesbaren pageName aus dem aktuellen Website-Pfad.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getPageName

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Das `getPageName` Plug-in erstellt eine leicht lesbare, benutzerfreundliche formatierte Version der aktuellen URL. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie einen [`pageName`](../page-vars/pagename.md) Wert wünschen, der in Berichte leicht festzulegen und verständlich ist. Dieses Plug-in ist nicht erforderlich, wenn Sie bereits über eine Benennungsstruktur für die `pageName` Variable verfügen, z. B. über eine Datenschicht. Es wird am besten verwendet, wenn Sie keine andere Lösung zum Festlegen der `pageName` Variablen haben.

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
   * Aktionstyp: getPageName initialisieren
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
/* Adobe Consulting Plugin: getPageName v4.0 */
var getPageName=function(si,qv,hv,de){var c=location.hostname,f=location.pathname.substring(1).split("/"),h=f.length, g=location.search.substring(1).split("&"),l=g.length,k=location.hash.substring(1).split("&"),m=k.length;de=de?de:": ";si=si?si:c;qv= qv?qv:"";hv=hv?hv:"";if(1===h&&""===f[0])si=si+de+"home";else for(c=0;c<h;c++)si=si+de+decodeURIComponent(f[c]); if(qv&&(1!==l||""!== g[0]))for(f=qv.split(","),h=f.length,c=0;c<h;c++)for(qv=0;qv<l;qv++)if(f[c]===g[qv].split("=")[0]){si=si+de+decodeURIComponent(g[qv]);break}if(hv&&(1!==m||""!==k[0]))for(hv=hv.split(","),g=hv.length,c=0;c<g;c++)for(qv=0;qv<m;qv++)if(hv[c]===k[qv].split("=")[0]){si=si+de+decodeURIComponent(k[qv]);break}return si.substring(si.length-de.length)===de?si.substring(0,si.length-de.length):si};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getPageName` Methode verwendet die folgenden Argumente:

* **`si`** (optional, Zeichenfolge): Eine ID, die am Anfang der Zeichenfolge eingefügt wird, welche die ID der Site darstellt. Dieser Wert kann entweder eine numerische ID oder ein benutzerfreundlicher Name sein. Wenn sie nicht eingestellt ist, wird standardmäßig die aktuelle Domäne verwendet.
* **`qv`** (optional, Zeichenfolge): Eine kommagetrennte Liste von Abfrage-Zeichenfolgenparametern, die, falls sie in der URL enthalten sind, der Zeichenfolge hinzugefügt werden
* **`hv`** (optional, Zeichenfolge): Eine kommagetrennte Liste von Parametern im URL-Hash, die, falls sie in der URL gefunden werden, der Zeichenfolge hinzugefügt werden
* **`de`** (optional, Zeichenfolge): Das Trennzeichen zum Aufteilen einzelner Teile der Zeichenfolge. Der Standardwert ist ein Rohr (`|`).

Die Methode gibt eine Zeichenfolge zurück, die eine benutzerfreundliche Version der URL enthält. Diese Zeichenfolge wird in der Regel der `pageName` Variablen zugewiesen, kann aber auch in anderen Variablen verwendet werden.

## Beispielaufrufe

### Beispiel 1

Wenn die aktuelle URL...

```js
https://mail.google.com/mail/u/0/#inbox
```

...und der folgende Code wird ausgeführt...

```js
s.pageName = getPageName()
```

...Der Endwert von s.pageName lautet:

```js
s.pageName = "mail.google.com|mail|u|0";
```

### Beispiel 2

Wenn die aktuelle URL...

```js
https://mail.google.com/mail/u/0/#inbox
```

...und der folgende Code wird ausgeführt...

```js
s.pageName = getPageName("gmail")
```

...Der Endwert von s.pageName lautet:

```js
s.pageName = "gmail|mail|u|0";
```

### Beispiel 3

Wenn die aktuelle URL...

```js
https://www.google.com/
```

...und der folgende Code wird ausgeführt...

```js
s.pageName = getPageName()
```

...Der Endwert von s.pageName lautet:

```js
s.pageName = "www.google.com|home"
```

**Hinweis**: Wenn der Code auf einer URL ausgeführt wird, die keinen Pfad enthält, wird immer der Wert &quot;home&quot;am Ende des Rückgabewerts hinzugefügt

### Beispiel 4

Wenn die aktuelle URL...

```js
https://www.google.com/
```

...und der folgende Code wird ausgeführt...

```js
s.pageName = getPageName("google","","","|")
```

...Der Endwert von s.pageName lautet:

```js
s.pageName = "google|home"
```

### Beispiel 5

Wenn die aktuelle URL...

```js
https://www.hotelrooms.com/en/booking/room-booking.html?cid=1235#/step2&arrive=2018-05-26&depart=2018-05-27&numGuests=2
```

...und der folgende Code wird ausgeführt...

```js
s.pageName = getPageName()
```

...Der Endwert von s.pageName lautet:

```js
s.pageName = "www.hotelrooms.com|en|booking|room-booking.html"
```

Wenn der folgende Code jedoch stattdessen ausgeführt wird...

```js
s.pageName = getPageName("hotelrooms","cid","arrive,numGuests",": ")
```

...Der Endwert von s.pageName lautet:

```js
s.pageName = "hotelrooms: en: booking: room-booking.html: cid=1235: arrive=2018-05-26: numGuests=2"
```

## Von früheren Versionen aktualisieren

Version 4.0+ des getPageName-Plug-Ins ist nicht von der Existenz des AppMeasurement-Objekts von Adobe Analytics (d. h. des &quot;s&quot;-Objekts), das ausgeführt werden soll, abhängig.  Wenn Sie sich für eine Aktualisierung auf diese Version entscheiden, vergewissern Sie sich, dass Sie den Code ändern, der das Plug-In aufruft, indem Sie alle Instanzen des &quot;s&quot;-Objekts aus dem Aufruf entfernen.
Ändern Sie beispielsweise Folgendes:

```js
s.pageName = s.getPageName();
```

...wie folgt:

```js
s.pageName = getPageName();
```

## Versionsverlauf

### 4.1 (17. September 2019)

* Der Standardwert für das Trennzeichen wurde in ein Senkrechtstrich geändert (aus einem Doppelpunkt + Leerzeichen).

### 4.0 (22. Mai 2018)

* Vollständige Neuanalyse/Umschreiben des Plug-Ins
