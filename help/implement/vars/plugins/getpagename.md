---
title: getPageName
description: Erstellen Sie einen leicht verständlichen Seitennamen aus dem aktuellen Website-Pfad.
translation-type: ht
source-git-commit: 063da38c105072944a46ec0ab31930623b7974c8
workflow-type: ht
source-wordcount: '736'
ht-degree: 100%

---


# Adobe-Plug-in: getPageName

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `getPageName`-Plug-in erstellt eine leicht verständliche, benutzerfreundlich formatierte Version der aktuellen URL. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie einen [`pageName`](../page-vars/pagename.md)-Wert wünschen, der sich leicht in der Berichterstellung einstellen und verstehen lässt. Dieses Plug-in ist nicht erforderlich, wenn Sie bereits über eine Namensstruktur für die `pageName`-Variable verfügen, z. B. über eine Datenschicht. Es wird am besten verwendet, wenn Sie keine andere Lösung zum Festlegen der `pageName`-Variablen haben.

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
   * Aktionstyp: getPageName initialisieren
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
/* Adobe Consulting Plugin: getPageName v4.2 */
var getPageName=function(si,qv,hv,de){var a=si,b=qv,f=hv,e=de;if("-v"===a)return{plugin:"getPageName",version:"4.2"};a:{if("undefined"!==typeof window.s_c_il){var d=0;for(var g;d<window.s_c_il.length;d++)if(g=window.s_c_il[d],g._c&&"s_c"===g._c){d=g;break a}}d=void 0}"undefined"!==typeof d&&(d.contextData.getPageName="4.2");var c=location.hostname,h=location.pathname.substring(1).split("/"),l=h.length,k=location.search.substring(1).split("&"),m=k.length;d=location.hash.substring(1).split("&");g=d.length;e=e?e:"|";a=a?a:c;b=b?b:"";f=f?f:"";if(1===l&&""===h[0])a=a+e+"home";else for(c=0;c<l;c++)a=a+e+decodeURIComponent(h[c]);if(b&&(1!==m||""!==k[0]))for(h=b.split(","),l=h.length,c=0;c<l;c++)for(b=0;b<m;b++)if(h[c]===k[b].split("=")[0]){a=a+e+decodeURIComponent(k[b]);break}if(f&&(1!==g||""!==d[0]))for(f=f.split(","),k=f.length,c=0;c<k;c++)for(b=0;b<g;b++)if(f[c]===d[b].split("=")[0]){a=a+e+decodeURIComponent(d[b]);break}return a.substring(a.length-e.length)===e?a.substring(0,a.length-e.length):a};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getPageName`-Methode verwendet die folgenden Argumente:

* **`si`** (optional, Zeichenfolge): Eine ID, die am Anfang der Zeichenfolge eingefügt wird, welche die ID der Website darstellt. Dieser Wert kann entweder eine numerische ID oder ein benutzerfreundlicher Name sein. Wenn sie nicht eingestellt ist, wird standardmäßig die aktuelle Domäne verwendet.
* **`qv`** (optional, Zeichenfolge): Eine durch Komma getrennte Liste von Abfragezeichenfolgenparametern, die, falls sie in der URL enthalten sind, der Zeichenfolge hinzugefügt werden
* **`hv`** (optional, Zeichenfolge): Eine durch Komma getrennte Liste von Parametern im URL-Hash, die, wenn sie in der URL gefunden werden, der Zeichenfolge hinzugefügt werden
* **`de`** (optional, Zeichenfolge): Das Trennzeichen zum Aufteilen einzelner Teile der Zeichenfolge. Der Standardwert ist ein senkrechter Strich (`|`).

Die Methode gibt eine Zeichenfolge zurück, die eine benutzerfreundlich formatierte Version der URL enthält. Diese Zeichenfolge wird normalerweise der `pageName`-Variablen zugewiesen, kann aber auch in anderen Variablen verwendet werden.

## Beispielaufrufe

### Beispiel 1

Wenn die aktuelle URL lautet ...

```js
https://mail.google.com/mail/u/0/#inbox
```

 ... und der folgende Code ausgeführt wird ...

```js
s.pageName = getPageName()
```

... lautet der Endwert von s.pageName:

```js
s.pageName = "mail.google.com|mail|u|0";
```

### Beispiel 2

Wenn die aktuelle URL lautet ...

```js
https://mail.google.com/mail/u/0/#inbox
```

 ... und der folgende Code ausgeführt wird ...

```js
s.pageName = getPageName("gmail")
```

... lautet der Endwert von s.pageName:

```js
s.pageName = "gmail|mail|u|0";
```

### Beispiel 3

Wenn die aktuelle URL lautet ...

```js
https://www.google.com/
```

 ... und der folgende Code ausgeführt wird ...

```js
s.pageName = getPageName()
```

... lautet der Endwert von s.pageName:

```js
s.pageName = "www.google.com|home"
```

**Hinweis**: Wenn der Code auf einer URL ausgeführt wird, die keinen Pfad enthält, wird immer der Wert „home“ am Ende des Rückgabewerts hinzugefügt

### Beispiel 4

Wenn die aktuelle URL lautet ...

```js
https://www.google.com/
```

 ... und der folgende Code ausgeführt wird ...

```js
s.pageName = getPageName("google","","","|")
```

... lautet der Endwert von s.pageName:

```js
s.pageName = "google|home"
```

### Beispiel 5

Wenn die aktuelle URL lautet ...

```js
https://www.hotelrooms.com/en/booking/room-booking.html?cid=1235#/step2&arrive=2018-05-26&depart=2018-05-27&numGuests=2
```

 ... und der folgende Code ausgeführt wird ...

```js
s.pageName = getPageName()
```

... lautet der Endwert von s.pageName:

```js
s.pageName = "www.hotelrooms.com|en|booking|room-booking.html"
```

Wenn stattdessen jedoch der folgende Code ausgeführt wird...

```js
s.pageName = getPageName("hotelrooms","cid","arrive,numGuests",": ")
```

... lautet der Endwert von s.pageName:

```js
s.pageName = "hotelrooms: en: booking: room-booking.html: cid=1235: arrive=2018-05-26: numGuests=2"
```

## Aktualisieren von früheren Versionen

Die Ausführung von Version 4.0+ des getPageName-Plug-ins hängt nicht von der Existenz des AppMeasurement-Objekts von Adobe Analytics (d. h. des „s“ -Objekts) ab.  Wenn Sie sich für eine Aktualisierung auf diese Version entscheiden, müssen Sie den Code ändern, der das Plug-in aufruft, indem Sie alle Instanzen des „s“-Objekts aus dem Aufruf entfernen.
Ändern Sie beispielsweise:

```js
s.pageName = s.getPageName();
```

... wie folgt:

```js
s.pageName = getPageName();
```

## Versionsverlauf

### 4.2 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 4.1 (17. September 2019)

* Der Standardwert für das Trennzeichen wurde in einen senkrechten Strich geändert (von einem Doppelpunkt + Leerzeichen).

### 4.0 (22. Mai 2018)

* Vollständige Neuanalyse/Umformulierung des Plug-ins
