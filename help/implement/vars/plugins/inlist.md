---
title: inList
description: Überprüfen Sie, ob ein Wert in einem anderen, durch Zeichen getrennten Wert enthalten ist.
translation-type: ht
source-git-commit: 27d151abe9bdf52c6eabdc3e9c785a99d08f971e
workflow-type: ht
source-wordcount: '743'
ht-degree: 100%

---


# Adobe-Plug-in: inList

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `inList`-Plug-in können Sie überprüfen, ob ein Wert bereits in einer getrennten Zeichenfolge oder einem JavaScript-Array-Objekt vorhanden ist. Die Funktion einiger anderer Plug-ins hängen vom `inList`-Plug-in ab. Dieses Plug-in bietet einen klaren Vorteil gegenüber der JavaScript-Methode, `indexOf()`, bei der partielle Zeichenfolgen nicht übereinstimmen. Wenn Sie dieses Plug-in z. B. zur Prüfung auf `"event2"` verwendet haben, wird es nicht mit einer Zeichenkette übereinstimmen, die `"event25"` enthält. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht nach Werten in getrennten Zeichenfolgen oder Arrays suchen müssen oder wenn Sie Ihre eigene `indexOf()`-Logik verwenden möchten.

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
   * Aktionstyp: inList initialisieren
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
/* Adobe Consulting Plugin: inList v3.0 */
function inList(lv,vtc,d,cc){var b=lv,e=vtc,c=d,f=cc;if("-v"===b)return{plugin:"inList",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var d;a<window.s_c_il.length;a++)if(d=window.s_c_il[a],d._c&&"s_c"===d._c){a=d;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.inList="3.0");if("string"!==typeof e)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==f&&e===b[c]||e.toLowerCase()===b[c].toLowerCase())return!0;return!1};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `inList`-Methode verwendet die folgenden Argumente:

* **`lv`** (erforderlich, Zeichenfolge oder Array): Eine durch Trennzeichen getrennte Liste von Werten oder ein JavaScript-Array-Objekt, die durchsucht werden soll
* **`vtc`** (erforderlich, Zeichenfolge): Der zu suchende Wert
* **`d`** (optional, Zeichenfolge): Das Trennzeichen, mit dem die einzelnen Werte im `lv`-Argument getrennt werden. Die Standardeinstellung ist ein Komma (`,`), wenn nicht festgelegt.
* **`cc`** (optional, boolesch): Wenn auf `true` gesetzt, wird die Groß-/Kleinschreibung überprüft. Wenn auf `false` gesetzt oder nicht festgelegt, wird die Groß-/Kleinschreibung nicht überprüft. Die Standardeinstellung ist `false`.

Der Aufruf dieser Methode gibt `true` zurück, wenn sie eine Übereinstimmung findet, und `false`, wenn sie keine Übereinstimmung findet.

## Beispielaufrufe

### Beispiel 1

Wenn ...

```js
s.events="event22,event24";
```

 ... und der folgende Code ausgeführt wird ...

```js
if(s.inList(s.events,"event22"))
```

... ist die bedingte Wenn-Anweisung „true“

### Beispiel 2

Wenn ...

```js
s.events="event22,event24";
```

 ... und der folgende Code ausgeführt wird ...

```js
if(s.inList(s.events,"event2"))
```

... ist die bedingte Wenn-Anweisung „false“, da der inList-Aufruf keine exakte Übereinstimmung zwischen event2 und einem der durch Trennzeichen getrennten Werte in s.events gefunden hat

### Beispiel 3

Wenn ...

```js
s.events="event22,event24";
```

 ... und der folgende Code ausgeführt wird ...

```js
if(!s.inList(s.events,"event23"))
```

... ist die bedingte WENN-Anweisung „true“, da der inList-Aufruf keine exakte Übereinstimmung zwischen event23 und einem der durch Trennzeichen getrennten Werte in s.events gefunden hat (beachten Sie den NICHT-Operator am Anfang des inList-Variablenaufrufs).

### Beispiel 4

Wenn ...

```js
s.events = "event22,event23";
```

 ... und der folgende Code ausgeführt wird ...

```js
if(s.inList(s.events,"EVenT23","",1))
```

... ist die bedingte WENN-Anweisung „false“.  Obwohl dieses Beispiel nicht praktikabel ist, zeigt es, dass bei Verwendung der Markierung, bei der die Groß- und Kleinschreibung beachtet werden muss, Vorsicht geboten ist.

### Beispiel 5

Wenn ...

```js
s.linkTrackVars = "events,eVar1";
```

 ... und der folgende Code ausgeführt wird ...

```js
if(s.inList(s.linkTrackVars,"eVar1","|"))
```

... ist die bedingte WENN-Anweisung „false“.  Der Wert des d-Arguments, das an den Aufruf übergeben wird (d. h. „|“) geht davon aus, dass die einzelnen Werte in s.linkTrackVars durch einen senkrechten Strich getrennt werden, während die Werte in Wirklichkeit durch ein Komma getrennt werden.  In diesem Fall versucht das Plug-in, eine Übereinstimmung zwischen dem gesamten Wert von s.linkTrackVars (d. h. „events,eVar1“) und dem zu suchenden Wert (d. h. „eVar1“) zu finden.

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### v2.1 (26. September 2019)

* Es wurde die Option hinzugefügt, dass das `cc`-Argument kein boolescher Wert sein darf. Beispiel: `1` ist ein gültiger Wert für die Prüfung der Groß-/Kleinschreibung.

### v2.0 (17. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe).

### v1.01 (27. September 2017)

* Code optimiert, um Größe zu reduzieren

### v1.0 (2009)

* Erste Version.


