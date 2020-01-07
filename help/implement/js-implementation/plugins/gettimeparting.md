---
description: Das getTimeParting-Plug-in füllt benutzerdefinierte Variablen mit Werten für Stunde, Tag der Woche und Wochenende oder Wochentag auf. Analysis Workspace bietet vordefinierte Zeitunterteilungsdimensionen. Das Plug-in sollte verwendet werden, wenn Zeitunterteilungsdimensionen in anderen Analytics-Lösungen außerhalb von Analysis Workspace benötigt werden.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getTimeParting
topic: Developer and implementation
uuid: 74f696a3-7169-4560-89b2-478b3d8385e1
translation-type: tm+mt
source-git-commit: 73d20b23e38bc619c156c418c95096a94d2fdfce

---


# getTimeParting

Das getTimeParting-Plugin bietet eine vollständige Analyselösung, mit der Sie die Details des Zeitpunkts erfassen können, zu dem eine messbare Aktivität auf Ihrer Site stattfindet.

Sie sollten das getTimeParting-Plugin verwenden, wenn Sie Ihre Metriken nach wiederholbarer Zeitteilung über einen bestimmten Datumsbereich unterteilen möchten.  Mit dem Plug-in getTimeParting können Sie beispielsweise Konversionsraten zwischen zwei verschiedenen Wochentagen (z. B. alle Sonntage im Vergleich zu allen Donnerstagen), zwei verschiedenen Tageszeiträumen (z. B. alle Morgens im Vergleich zu allen Abenden) oder sogar zwei darauffolgende Minuten (z. B. alle Instanzen von 10:00 Uhr im Vergleich zu allen Instanzen von 10:01 Uhr am Tag) im Datumsbereich vergleichen im Bericht angeben.

[!DNL Analysis Workspace] bietet ähnliche vordefinierte Dimensionen, die etwas anders formatiert sind als das, was dieses Plugin bietet (siehe [hier](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/dimensions/time-parting-dimensions.html)).  Adobe Consulting empfiehlt, den Rest dieses Hilfeabschnitts durchzulesen, um festzustellen, ob dieses Plugin Daten auf eine für Ihre Anforderungen geeignetere Weise bereitstellt.

Wenn Sie Ihre Metriken nicht durch eine wiederholbare Zeitteilung in einen bestimmten Datumsbereich unterteilen müssen, müssen Sie das Plugin getTimeParting nicht verwenden.  Wenn Sie die [!DNL Analysis Workspace] Zeitaufteilungsdimensionen ausreichend finden, müssen Sie dieses Plugin nicht implementieren.

>[!CAUTION] Die Lösung, die Version 4.0+ des getTimeParting-Plugins bietet, unterscheidet sich deutlich von der, die frühere Versionen des Plugins bieten.  Wenn Sie sich für ein Upgrade von einer Version vor 4.0 entscheiden, sollten Sie die Lösung &quot;von Grund auf&quot;implementieren.  Mit anderen Worten, Sie sollten eine völlig neue eVar - eine eVar - einrichten, um die vom Plugin bereitgestellten Daten zu speichern und diese Dokumentation sorgfältig durchzulesen, bevor Sie die Lösung implementieren.

>[!CAUTION] Außerdem: Diese Version des Plugins ist nicht *vollständig* mit Microsoft Internet Explorer kompatibel, obwohl das Plugin vollständig mit Microsoft Edge-Browsern kompatibel ist.   Besucher, die Internet Explorer verwenden, können die Zeit nur in ihrer *lokalen* Zeitzone angeben und nicht in die von Ihnen angegebene Zeitzone konvertieren.  In den folgenden Beispielen finden Sie eine Lösung, die keine Daten aus Internet Explorer-Browsern enthält, deren Präsenz jedoch weiterhin berücksichtigt wird.

> [!NOTE] Für die folgenden Anweisungen müssen Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

> [!WARNING] Testen Sie stets alle Plug-in-Implementierungen vor der Bereitstellung in der Produktion, um sicherzustellen, dass die Datenerfassung erwartungsgemäß funktioniert.

## Voraussetzungen

Keine

## Umsetzung

* Kopieren Sie den folgenden Code und fügen Sie ihn an eine beliebige Stelle im Abschnitt Plugins des AppMeasurement-Codes ein:

```function getTimeParting(a){a=document.documentMode?void 0:a||"Etc/GMT";a=(new Date).toLocaleDateString("en-US",{timeZone:a, minute:"numeric",hour:"numeric",weekday:"long",day:"numeric",year:"numeric",month:"long"});a=/([a-zA-Z]+).*?([a-zA-Z]+).*?([0-9]+).*?([0-9]+)(.*?)([0-9])(.*)/.exec(a);return"year="+a[4]+" | month="+a[2]+" | date="+a[3]+" | day="+a[1]+" | time="+(a[6]+a[7])}```

> [!NOTE] Sie können auch einen Tag-Manager wie Adobe Launch verwenden, um den Plugin-Code bereitzustellen, ohne ihn an AppMeasurement oder eine andere Analyselösung anhängen zu müssen

* Führen Sie die Funktion getTimeParting wie unten in der Funktion doPlugins oder an einem anderen Ort aus, an dem Sie die Zeitaufteilungsdaten erfassen müssen

**Zu übergebende Argumente**

* t: (**OPTIONAL, aber empfohlen**, Zeichenfolge) Der Name der Zeitzone, in die die Ortszeit des Besuchers konvertiert werden soll.  Die Standardeinstellung lautet &quot;Etc/GMT&quot;, bzw. &quot;UTC/GMT time&quot;, wenn keine Angabe gemacht wird.  Die vollständige Liste der einzugebenden Werte finden Sie unter [https://en.wikipedia.org/wiki/List_of_tz_database_time_zones] .

Zu den gebräuchlichen Werten gehören:

* &quot;America/New_York&quot;für &quot;Eastern Time&quot;
* &quot;Amerika/Chicago&quot;für Central Time
* &quot;America/Denver&quot;für die Bergregion
* &quot;America/Los_Angeles&quot;für Pacific Time

## Rückgabe

Das getTimeParting-Plugin gibt eine Zeichenfolge zurück, die Folgendes enthält:

* Das aktuelle Jahr
* Der aktuelle Monat
* Das aktuelle Datum (d.h. der Tag des Monats)
* Der aktuelle Tag (d.h. der Wochentag)
* Die aktuelle Zeit (nicht-militärische Zeit)

Jedes der oben genannten Elemente wird durch ein Pipe-Zeichen (&quot;|&quot;) getrennt.

## Beispielaufrufe

Verwenden Sie den folgenden Code, wenn Sie sich in Paris, Frankreich befinden und eVar10 (in Adobe Analytics) verwenden möchten, um die Zeitunterteilungsdaten zu erfassen:

```s.eVar10 = getTimeParting("Europe/Paris")```

Verwenden Sie den folgenden Code, wenn Sie sich in San Jose, Kalifornien, befinden:

```s.eVar10 = getTimeParting("America/Los_Angeles")```

Verwenden Sie den folgenden Code, wenn Sie sich im afrikanischen Land Ghana befinden:

```s.eVar10 = getTimeParting();```

Ghana liegt innerhalb der UTC/GMT-Zeitzone.  Dieses Beispiel zeigt also, dass unter solchen Umständen kein Plugin-Argument erforderlich ist.

Verwenden Sie den folgenden Code, wenn Sie sich in New York befinden und keine Daten von Internet Explorer-Besuchern einbeziehen möchten (da die von IE-Browsern zurückgegebenen Werte nur in der Ortszeit des Besuchers bereitgestellt werden können)

```if(!document.documentMode) s.eVar10 = getTimeParting("America/New_York");```
```else s.eVar10 = "Internet Explorer Visitors";```

**Ergebnisse von Aufrufen**

Wenn ein Besucher aus Denver, Colorado besucht eine Site am 31. August 2020 um 9:15 Uhr, der folgende Code...

```s.eVar10 = getTimeParting("Europe/Athens");```

...würde s.eVar10 gleich **year=2020 festlegen| month=August| date=31| day=Monday| time=6:15 PM**

Der folgende Code...

```s.eVar10 = getTimeParting("America/Nome");```

... würde stattdessen s.eVar10 gleich **year=2020 festlegen| month=August| date=31| day=Monday| time=6:15**

Der folgende Code...

```s.eVar10 = getTimeParting("Asia/Calcutta");```

... würde stattdessen s.eVar10 gleich **year=2020 festlegen| month=August| date=31| day=Monday| time=8:45 PM**

Der folgende Code...

```s.eVar10 = getTimeParting("Australia/Sydney");```

... würde stattdessen s.eVar10 gleich **year=2020 festlegen| month=September| date=1| day=Dienstag| time=1:15**

## Adobe Analytics-Einrichtung

Wenn Sie die Zeitaufteilungsdaten in Adobe Analytics erfassen möchten, richten Sie eine neue eVar mit folgenden Eigenschaften ein:

* Name: Zeitaufteilung
* Zuordnung: Zuletzt verwendet (Letzter)
* Läuft ab nach: Besuch
* Alle anderen Attribute verwenden die angegebenen Standardwerte
