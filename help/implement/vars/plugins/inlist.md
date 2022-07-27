---
title: inList
description: Überprüfen Sie, ob ein Wert in einem anderen, durch Zeichen getrennten Wert enthalten ist.
feature: Variables
exl-id: 7eedfd01-2b9a-4fae-a35b-433ca6900f27
source-git-commit: 7c7a7d8add9edb1538df12b440bc0a15f09efe5e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe-Plug-in: inList

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `inList`-Plug-in können Sie überprüfen, ob ein Wert bereits in einer getrennten Zeichenfolge oder einem JavaScript-Array-Objekt vorhanden ist. Die Funktion einiger anderer Plug-ins hängen vom `inList`-Plug-in ab. Dieses Plug-in bietet einen klaren Vorteil gegenüber der JavaScript-Methode, `indexOf()`, bei der partielle Zeichenfolgen nicht übereinstimmen. Wenn Sie dieses Plug-in z. B. zur Prüfung auf `"event2"` verwendet haben, wird es nicht mit einer Zeichenkette übereinstimmen, die `"event25"` enthält. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht nach Werten in getrennten Zeichenfolgen oder Arrays suchen müssen oder wenn Sie Ihre eigene `indexOf()`-Logik verwenden möchten.

<!--## Install the plug-in using the Web SDK or the Adobe Analytics extension

Adobe offers an extension that allows you to use most commonly-used plug-ins.

1. Log in to [Adobe Experience Platform Data Collection](https://experience.adobe.com/data-collection) using your AdobeID credentials.
1. Click the desired tag property.
1. Go to the [!UICONTROL Extensions] tab, then click on the [!UICONTROL Catalog] button
1. Install and publish the [!UICONTROL Common Analytics Plugins] extension
1. If you haven't already, create a rule labeled "Initialize Plug-ins" with the following configuration:
    * Condition: None
    * Event: Core – Library Loaded (Page Top)
1. Add an action to the above rule with the following configuration:
    * Extension: Common Analytics Plugins
    * Action Type: Initialize inList
1. Save and publish the changes to the rule.-->

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
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
