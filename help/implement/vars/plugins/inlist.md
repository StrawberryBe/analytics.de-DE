---
title: inList
description: Überprüfen Sie, ob ein Wert in einem anderen, durch Zeichen getrennten Wert enthalten ist.
feature: Variables
exl-id: 7eedfd01-2b9a-4fae-a35b-433ca6900f27
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 87%

---

# Adobe-Plug-in: inList

{{plug-in}}

Mit dem `inList`-Plug-in können Sie überprüfen, ob ein Wert bereits in einer getrennten Zeichenfolge oder einem JavaScript-Array-Objekt vorhanden ist. Die Funktion einiger anderer Plug-ins hängen vom `inList`-Plug-in ab. Dieses Plug-in bietet einen klaren Vorteil gegenüber der JavaScript-Methode, `indexOf()`, bei der partielle Zeichenfolgen nicht übereinstimmen. Wenn Sie dieses Plug-in z. B. zur Prüfung auf `"event2"` verwendet haben, wird es nicht mit einer Zeichenkette übereinstimmen, die `"event25"` enthält. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht nach Werten in getrennten Zeichenfolgen oder Arrays suchen müssen oder wenn Sie Ihre eigene `indexOf()`-Logik verwenden möchten.

## Installieren des Plug-ins mit der Web SDK- oder Web SDK-Erweiterung

Dieses Plug-in wird noch nicht für die Verwendung im Web SDK unterstützt.

## Installieren des Plug-ins mit der Adobe Analytics-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins mit Adobe Analytics verwenden können.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: inList initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung &quot;Common Analytics Plugins&quot;nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
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

Die Funktion `inList` gibt je nach Eingaben einen booleschen Wert zurück. Sie verwendet die folgenden Argumente:

* **`lv`** (erforderlich, Zeichenfolge oder Array): Eine durch Trennzeichen getrennte Liste von Werten oder ein JavaScript-Array-Objekt, die durchsucht werden soll
* **`vtc`** (erforderlich, Zeichenfolge): Der zu suchende Wert
* **`d`** (optional, Zeichenfolge): Das Trennzeichen, mit dem die einzelnen Werte im `lv`-Argument getrennt werden. Die Standardeinstellung ist ein Komma (`,`), wenn nicht festgelegt.
* **`cc`** (optional, boolesch): Wenn auf `true` oder `1` gesetzt, wird die Groß-/Kleinschreibung geprüft. Wenn auf `false` gesetzt oder nicht festgelegt, wird die Groß-/Kleinschreibung nicht überprüft. Die Standardeinstellung ist `false`.

Der Aufruf dieser Funktion gibt `true` zurück, wenn sie eine Übereinstimmung findet, und `false`, wenn sie keine Übereinstimmung findet.

## Beispiele

```js
// Returns true
s.events = "event22,event24";
if(inList(s.events,"event22")) {
    // Code will execute
}

// Returns false because event2 is not an exact match in the string
s.events = "event22,event24";
if(inList(s.events,"event2")) {
    // Code will not execute
}

// Returns true because of the NOT operator
s.events = "event22,event24";
if(!inList(s.events,"event23")) {
    // Code will execute
}

// Returns false because of the case-sensitive check
s.events = "event22,event23";
if(inList(s.events,"EVenT23","",true)) {
    // Code will not execute
}

// Returns false because of a mismatched delimiter, treating "events,eVar1" as a single value
s.linkTrackVars = "events,eVar1";
if(inList(s.linkTrackVars,"eVar1","|")) {
    // Code will not execute
}
```

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
