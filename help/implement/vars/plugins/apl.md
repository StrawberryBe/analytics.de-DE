---
title: apl (appendToList)
description: Fügen Sie Werte an Variablen an, die mehrere Werte unterstützen.
feature: Variables
exl-id: 08ca43f4-f2cc-43fb-a8eb-7c9dd237dfba
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: ht
source-wordcount: '695'
ht-degree: 100%

---

# Adobe-Plug-in: apl (appendToList)

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `apl`-Plug-in können Sie sicher neue Werte zu durch Listen getrennten Variablen hinzufügen, wie z. B. [`events`](../page-vars/events/events-overview.md), [`linkTrackVars`](../config-vars/linktrackvars.md), [`list`](../page-vars/list.md) und andere.

* Wenn der Wert, den Sie hinzufügen möchten, nicht in der Variablen vorhanden ist, fügt der Code den Wert am Ende der Zeichenfolge hinzu.
* Wenn der Wert, den Sie hinzufügen möchten, bereits in der Variablen vorhanden ist, ändert dieses Plug-in den Wert nicht. Diese Funktionen ermöglichen es Ihrer Implementierung, doppelte Werte zu vermeiden.
* Wenn die Variable, der Sie hinzufügen möchten, leer ist, setzt das Plug-in die Variable auf den neuen Wert.

Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie vorhandenen Variablen, die eine Zeichenfolge aus durch Trennzeichen getrennten Werten enthalten, neue Werte hinzufügen möchten. Dieses Plug-in ist nicht erforderlich, wenn Sie Zeichenfolgen für Variablen mit getrennten Werten verknüpfen möchten.

## Installieren des Plug-ins mithilfe von Tags in Adobe Experience Platform

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: APL („Append To List“ (An Liste anhängen)) initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: apl (appendToList) v4.0 */
function apl(lv,va,d1,d2,cc){var b=lv,d=va,e=d1,c=d2,g=cc;if("-v"===b)return{plugin:"apl",version:"4.0"};var h=function(){if("undefined"!==typeof window.s_c_il)for(var k=0,b;k<window.s_c_il.length;k++)if(b=window.s_c_il[k],b._c&&"s_c"===b._c)return b}();"undefined"!==typeof h&&(h.contextData.apl="4.0");window.inList=window.inList||function(b,d,c,e){if("string"!==typeof d)return!1;if("string"===typeof b)b=b.split(c||",");else if("object"!==typeof b)return!1;c=0;for(a=b.length;c<a;c++)if(1==e&&d===b[c]||d.toLowerCase()===b[c].toLowerCase())return!0;return!1};if(!b||"string"===typeof b){if("string"!==typeof d||""===d)return b;e=e||",";c=c||e;1==c&&(c=e,g||(g=1));2==c&&1!=g&&(c=e);d=d.split(",");h=d.length;for(var f=0;f<h;f++)window.inList(b,d[f],e,g)||(b=b?b+c+d[f]:d[f])}return b};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `apl`-Funktion verwendet die folgenden Argumente:

* **`lv`** (erforderlich, Zeichenfolge): Die Variable, die eine durch Trennzeichen getrennte Liste von Elementen enthält, der ein neuer Wert hinzugefügt werden soll
* **`vta`** (erforderlich, Zeichenfolge): Eine durch Komma getrennte Liste der neuen Werte, die dem `lv`-Argumentwert hinzugefügt werden sollen.
* **`d1`** (optional, Zeichenfolge): Das Trennzeichen, mit dem die einzelnen Werte getrennt werden, die bereits im `lv`-Argument enthalten sind.  Die Standardeinstellung ist ein Komma (`,`), wenn nicht festgelegt.
* **`d2`** (optional, Zeichenfolge): Das Ausgabetrennzeichen. Der Standardwert ist derselbe Wert wie `d1`, wenn nicht festgelegt.
* **`cc`** (optional, boolesch): Eine Markierung, die anzeigt, ob bei einer Prüfung die Groß-/Kleinschreibung beachtet wird. Wenn die Markierung `true` ist, wird bei der Duplizierungsprüfung die Groß- und Kleinschreibung beachtet. Wenn die Markierung `false` oder nicht gesetzt ist, wird bei der Duplizierungsprüfung nicht zwischen Groß- und Kleinschreibung unterschieden. Die Standardeinstellung ist `false`.

Die `apl`-Funktion gibt den Wert des `lv`-Arguments sowie alle nicht duplizierten Werte im `vta`-Argument zurück.

## Beispiele

```js
// Set the events variable to "event22,event24,event23".
s.events = "event22,event24";
s.events = apl(s.events,"event23");

// The events variable remains unchanged because the apl function does not add duplicate values
s.events = "event22,event23";
s.events = apl(s.events,"event23");

// Set the events variable to "event23" if the events variable is blank
s.events = "";
s.events = apl(s.events,"event23");

// Append a value to eVar5. The value of prop4 remains unchanged.
// The value of eVar5 is "hello|people|today".
s.prop4 = "hello|people";
s.eVar5 = apl(s.prop4, "today", "|");

// Sets prop4 to "hello|people,today". Be mindful of correct delimiters!
s.prop4 = "hello|people";
s.prop4 = apl(s.prop4, "today");

// Sets the events variable to "event22,event23,EVentT23". Be mindful of capitalization when using the cc argument!
s.events = "event22,event23";
s.events = apl(s.events,"EVenT23", ",", ",", true);

// Sets the events variable to "event22,event23,event24,event25".
s.events = "event22,event23";
s.events = apl(s.events, "event23,event24,event25");

// Sets linkTrackVars to "events,eVar1,campaign".
// The last three arguments at the end of this apl call are not necessary because they match the default argument values.
s.linkTrackVars = "events,eVar1";
s.linkTrackVars = apl(s.linkTrackVars, "campaign", ",", ",", false);

// This apl call does not do anything because the code does not assign the returned value to a variable.
s.events = "event22,event24";
apl(s.events, "event23");

// Sets the list2 variable to "apple-APPLE-Apple".
// Since the two delimiter arguments are different, the value passed in is delimited by "|", then joined together by "-".
s.list2 = "apple|APPLE";
s.list2 = apl(s.list2, "Apple", "|", "-", true);

// Sets the list3 variable to "value1,value1,value1" (unchanged).
// Only new values are deduplicated. Existing duplicate values remain.
s.list3 = "value1,value1,value1";
s.list3 = apl(s.list3,"value1");
```

## Versionsverlauf

### 4.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 3.2 (25. September 2019)

* Kompatibilitätsprobleme mit `apl`-Aufrufen behoben, bei denen ältere Versionen des Plug-ins verwendet wurden
* Konsolenwarnungen zur Reduzierung der Größe entfernt
* Hinzufügung von `inList 2.1`

### 3.1 (22. April 2018)

* Das Argument `d2` wird jetzt standardmäßig auf den Wert des Arguments `d1` gesetzt, wenn nicht festgelegt

### 3.0 (16. April 2018)

* Vollständige Neuanalyse/Umformulierung des Plug-ins
* Erweiterte Fehlerprüfung hinzugefügt
* Das `vta`-Argument akzeptiert jetzt mehrere Werte auf einmal
* Das `d2`-Argument zum Formatieren des Rückgabewerts wurde hinzugefügt
* Das `cc`-Argument wurde in einen boolesches Argument geändert

### 2.5 (18. Februar 2016)

* Verwendet jetzt die `inList`-Funktion für die Vergleichsverarbeitung

### 2.0 (26. Januar 2016)

* Das Argument `d` (Trennzeichen) ist jetzt optional (standardmäßig ein Komma)
* Das Argument `u` (Markierung für Groß-/Kleinschreibung) ist jetzt optional (standardmäßig wird nicht zwischen Groß- und Kleinschreibung unterschieden)
* Unabhängig vom Argument `u` (Markierung für Groß-/Kleinschreibung), hängt das Plug-in keinen Wert mehr an eine Liste an, wenn der Wert bereits in der Liste vorhanden ist
