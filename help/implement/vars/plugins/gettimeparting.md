---
title: getTimeParting
description: Messen Sie die Zeit, zu der eine bestimmte Aktion stattfindet.
translation-type: tm+mt
source-git-commit: c56891495b610ae14b0341e6a8e64edd115ae105
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 82%

---


# Adobe-Plug-in: getTimeParting

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getTimeParting`-Plug-in können Sie die Details zu dem Zeitpunkt erfassen, zu dem eine beliebige messbare Aktivität auf Ihrer Website stattfindet. Dieses Plug-in ist nützlich, wenn Sie Metriken nach wiederholbarer Zeitteilung über einen bestimmten Datumsbereich aufschlüsseln möchten. Sie können beispielsweise die Konversionsraten zwischen zwei verschiedenen Wochentagen vergleichen, z. B. alle Sonntage im Vergleich zu allen Donnerstagen. Sie können auch Tageszeiträume vergleichen, z. B. alle Morgen im Vergleich zu allen Abenden.

Analysis Workspace bietet ähnliche vordefinierte Dimensionen, die etwas anders formatiert sind als dieses Plug-in. Weitere Informationen finden Sie unter [Dimensionen für die Zeitunterteilung](/help/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.md) im Analysebenutzerhandbuch. Für einige Unternehmen sind die vordefinierten Dimensionen von Analysis Workspace ausreichend.

>[!IMPORTANT]
>
>Version 4.0+ dieses Plug-ins unterscheidet sich deutlich von früheren Versionen. Adobe empfiehlt dringend, dieses Plug-in von Grund auf neu zu implementieren. Code, der auf das Plug-in vor Version 4.0 verweist, ist nicht mit der aktuellen Version dieses Plug-ins kompatibel.

>[!IMPORTANT]
>
>Frühere Versionen dieses Plug-Ins konnten in Zukunft nicht alle Jahre verwendet werden. Wenn Sie eine frühere Version dieses Plug-Ins verwenden, empfiehlt Adobe dringend, ein Upgrade auf die neueste Version durchzuführen, um JavaScript-Fehler und Datenverluste zu vermeiden. Wenn eine Aktualisierung dieses Plug-Ins nicht möglich ist, stellen Sie sicher, dass die Variable `s._tpdst` im Plug-in-Code die entsprechenden Jahre in der Zukunft enthält. Diese Variable ist in der neuesten Version des Plug-Ins nicht vorhanden oder erforderlich.

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
   * Aktionstyp: getTimeParting initialisieren
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
/* Adobe Consulting Plugin: getTimeParting v6.2 */
var getTimeParting=function(a){a=document.documentMode?void 0:a||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:a, minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getTimeParting`-Methode verwendet das folgende Argument:

**`t`** (Optional, aber empfohlen, Zeichenfolge): Der Name der Zeitzone, in die die Ortszeit des Besuchers umgerechnet werden soll.  Die Standardeinstellung ist die UTC/GMT-Zeit. Eine vollständige Liste der gültigen Werte finden Sie unter [List of tz database time zones (Liste der Zeitzonen der Zeitzonen-Datenbank)](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) auf Wikipedia.

Zu den üblichen gültigen Werten gehören:

* `"America/New_York"` für Eastern Time (EST)
* `"America/Chicago"` für Central Time (CST)
* `"America/Denver"` für Mountain Time (MST)
* `"America/Los_Angeles"` für Pacific Time (PST)

Beim Aufrufen dieser Methode wird eine Zeichenfolge zurückgegeben, die die folgenden, durch einen senkrechten Strich (`|`) getrennte, Zeichen enthält:

* Das aktuelle Jahr
* Der aktuelle Monat
* Der Tag des Monats
* Der Tag des Woche
* Die aktuelle Zeit

## Beispielaufrufe

### Beispiele für bestimmte Zeitzonen

Verwenden Sie den folgenden Beispielcode, wenn sich der Client in Paris, Frankreich befindet:

```js
s.eVarX = getTimeParting("Europe/Paris");
```

Der Client befindet sich in San Jose, Kalifornien:

```js
s.eVarX = getTimeParting("America/Los_Angeles");
```

Der Client befindet sich in Ghana:

```js
s.eVarX = getTimeParting();
```

Ghana liegt innerhalb der UTC/GMT-Zeitzone. Dieses Beispiel zeigt, dass kein Plug-in-Argument für UTC/GMT erforderlich ist.

### Für Internet Explorer-Browser

Verwenden Sie das folgende Beispiel, wenn Sie Zeitaufteilungsdaten aus Internet Explorer-Besuchern ausschließen möchten. Der von IE-Browsern zurückgegebene Wert ist nur in der Ortszeit des Besuchers angegeben.

```js
if(!document.documentMode) s.eVarX = getTimeParting("America/New_York");
else s.eVarX = "Internet Explorer Visitors";
```

### Ergebnisse von Aufrufen

Man denke an ein Szenario, bei dem ein Besucher von Denver Colorado am 31. August 2020 um 9:15 Uhr eine Site besucht.

```js
s.eVar10 = getTimeParting("Europe/Athens");
// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 PM"

s.eVar11 = getTimeParting("America/Nome");
// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=6:15 AM"

s.eVar12 = getTimeParting("Asia/Calcutta");
// Returns the string value "year=2020 | month=August | date=31 | day=Friday | time=8:45 PM"

s.eVar13 = getTimeParting("Australia/Sydney");
// Returns the string value "year=2020 | month=September | date=1 | day=Saturday | time=1:15 AM"
```

## Versionsverlauf

### 6.2 (5. November 2019)

* Kleine Fehlerbehebungen
* Reduzierte Gesamt-Code-Größe

### 6.1 (26. November 2018)

* Korrektur für Internet Explorer-Browser. Sie können die Zeit zurückgeben, jedoch nur in der Ortszeit des Besuchers.

### 6.0 (14. August 2018)

* Vollständige Neufassung zur Anpassung an internationale Standards. Die Sommerzeit und alle Zeitzonen werden jetzt richtig konvertiert.

### 5.0 (17. April 2018)

* Zwischenversion (neu kompiliert, kleinere Code-Größe)
* Der `tpDST`-Parameter ist nicht mehr erforderlich, da das Start-/Enddatum der Sommerzeit jetzt automatisch erkannt wird.

### 4.0 (22. August 2016)

* Bietet eine brandneue Lösung und enthält jetzt Informationen zu Jahr, Monat und Datum.
