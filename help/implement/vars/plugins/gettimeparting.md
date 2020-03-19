---
title: getTimeParting
description: Messen Sie die Zeit, zu der eine bestimmte Aktion stattfindet.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: getTimeParting

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `getTimeParting` Plug-in können Sie die Details zu dem Zeitpunkt erfassen, zu dem eine beliebige messbare Aktivität auf Ihrer Site stattfindet. Dieses Plug-in ist nützlich, wenn Sie Metriken nach wiederholbarer Zeitteilung über einen bestimmten Datumsbereich aufschlüsseln möchten. Sie können beispielsweise die Konversionsraten zwischen zwei verschiedenen Wochentagen vergleichen, z. B. sonntags und donnerstags. Sie können auch Tageszeiträume vergleichen, z. B. jeden Morgen im Vergleich zu allen Abenden.

Analyse Workspace bietet ähnliche vordefinierte Dimensionen, die etwas anders formatiert sind als dieses Plug-in. Weitere Informationen finden Sie unter Dimensionen der [Zeitaufteilung](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md) im Benutzerhandbuch für Analysieren. Einige Unternehmen finden, dass die vordefinierten Dimensionen von Analyse Workspace ausreichend sind.

> [WICHTIGE] Version 4.0+ dieses Plug-ins unterscheidet sich deutlich von früheren Versionen. Adobe empfiehlt dringend, dieses Plug-in &quot;von Grund auf&quot;zu implementieren. Code, der auf das Plug-In vor Version 4.0 verweist, ist nicht mit der aktuellen Version dieses Plug-Ins kompatibel.

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
   * Aktionstyp: getTimeParting initialisieren
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
/* Adobe Consulting Plugin: getTimeParting v6.2 */
var getTimeParting=function(a){a=document.documentMode?void 0:a||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:a, minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `getTimeParting` Methode verwendet das folgende Argument:

**`t`** (Optional, aber empfohlen, Zeichenfolge): Der Name der Zeitzone, in die die Ortszeit des Besuchers konvertiert werden soll.  Die Standardeinstellung ist UTC/GMT-Zeit. Eine vollständige Liste der gültigen Werte finden Sie in der [Liste der Zeitzonen](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) der TZ-Datenbank auf Wikipedia.

Zu den allgemeinen gültigen Werten gehören:

* `"America/New_York"` für Eastern Time
* `"America/Chicago"` für Central Time
* `"America/Denver"` für Mountain Time
* `"America/Los_Angeles"` für Pacific Time

Beim Aufrufen dieser Methode wird eine Zeichenfolge zurückgegeben, die die folgenden durch ein Pipe getrennten Zeichen enthält (`|`):

* Das aktuelle Jahr
* Der aktuelle Monat
* Der Tag des Monats
* Wochentag
* Die aktuelle Zeit (AM/PM)

## Beispielaufrufe

### Beispiele für bestimmte Zeitzonen

Verwenden Sie den folgenden Beispielcode, wenn sich der Client in Paris, Frankreich befindet:

```js
s.eVarX = getTimeParting("Europe/Paris");
```

Befindet sich der Kunde in San Jose, Kalifornien:

```js
s.eVarX = getTimeParting("America/Los_Angeles");
```

Befindet sich der Kunde im afrikanischen Land Ghana:

```js
s.eVarX = getTimeParting();
```

Ghana liegt innerhalb der UTC/GMT-Zeitzone.  Dieses Beispiel zeigt, dass unter solchen Umständen kein Plug-in-Argument erforderlich ist.

### Buchhaltung für Internet Explorer-Browser

Verwenden Sie das folgende Beispiel, wenn Sie Zeitaufteilungsdaten aus Internet Explorer-Besuchern ausschließen möchten (da der von IE-Browsern zurückgegebene Wert nur in der Ortszeit des Besuchers liegen kann)

```js
if(!document.documentMode) s.eVarX = getTimeParting("America/New_York");
else s.eVarX = "Internet Explorer Visitors";
```

### Ergebnisse von Aufrufen

Wenn ein Besucher aus Denver am 31. August 2020 um 9:15 Uhr eine Site besucht,

Ausführen des folgenden Codes...

```js
s.eVar10 = getTimeParting("Europe/Athens");
```

...würde s.eVar10 gleich &quot;year=2020&quot;einstellen| month=August| date=31| day=Friday| time=6:15 PM&quot;

Während der folgende Code...

```js
s.eVar10 = getTimeParting("America/Nome");
```

...würde s.eVar10 gleich &quot;year=2020&quot;einstellen| month=August| date=31| day=Friday| time=6:15 AM&quot;

Der folgende Code...

```js
s.eVar10 = getTimeParting("Asia/Calcutta");
```

...würde s.eVar10 gleich &quot;year=2020&quot;einstellen| month=August| date=31| day=Friday| time=8:45 PM&quot;

Und der folgende Code...

```js
s.eVar10 = getTimeParting("Australia/Sydney");
```

...würde s.eVar10 gleich &quot;year=2020&quot;einstellen| month=September| date=1| day=Saturday| time=1:15 AM&quot;

## Versionsverlauf

### 6.2 (5. November 2019)

* Kleine Fehlerbehebungen
* Reduzierte Codegröße

### 6.1 (26. November 2018)

* Fehlerbehebung für Internet Explorer-Browser. Sie können die Zeit zurückgeben, jedoch nur in der Ortszeit des Besuchers.

### 6.0 (14. August 2018)

* Umschreiben nach internationalen Standards Konvertiert nun die Sommerzeit und alle Zeitzonen entsprechend.

### 5.0 (17. April 2018)

* Point Release (neu kompiliert, kleinere Codegröße)
* Die Notwendigkeit für den `tpDST` Parameter wurde entfernt, da jetzt automatisch Sommerzeit-/Beginn-Daten erkannt werden

### 4.0 (22. August 2016)

* Bietet eine brandneue Lösung und enthält nun Informationen zu Jahr, Monat und Datum.
