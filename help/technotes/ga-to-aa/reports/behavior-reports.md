---
title: Verhaltensberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Verhaltensberichte in Adobe Analytics erstellen.
translation-type: tm+mt
source-git-commit: 71899840dd5b401c6892b6ad5088d4a32fd07042

---


# Verhaltensberichte

Verhaltensberichte zeigen Informationen darüber an, wie Benutzer mit Ihrer Site interagieren.

Diese Seite geht davon aus, dass der Benutzer über grundlegende Kenntnisse zur Verwendung des Analysis Workspace verfügt. See [Create a basic report in Analysis Workspace for Google Analytics users](create-report.md) if you are not yet familiar with the tool in Adobe Analytics.

## Verhaltensfluss

Der Flussflussbericht kann mithilfe der Flussvisualisierung neu erstellt werden.

1. Klicken Sie links auf das Visualisierungssymbol und ziehen Sie eine Flussvisualisierung auf den Arbeitsbereich oberhalb der Freiformtabelle.
2. Locate the **Page** dimension, then click the Arrow icon to reveal page values. Dimensionswerte sind gelb farbig.
3. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den Bereich mit der Bezeichnung &quot;Dimension oder Element&quot; in der Mitte.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um die Flüsse auf die nachfolgenden oder vorherigen Seiten zu erweitern. Verwenden Sie das Rechtsklick-Menü, um Spalten zu erweitern oder zu minimieren. Innerhalb desselben Flussberichts können auch unterschiedliche Dimensionen verwendet werden.

![Flussbericht](../assets/flow.png)

## Site-Inhalt - Alle Seiten

Der Seitenbericht zeigt die Leistung einzelner Seiten auf Ihrer Site.

1. In the Components menu, locate the **Pages** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Alternativ stellt Adobe verschiedene vorgefertigte Arbeitsbereiche bereit, die Vorlagen genannt werden. Die Inhaltskonsum-Vorlage (Web) bietet einen ähnlichen Wert wie den gesamten Seitenbericht.

1. Click *[!UICONTROL Project] &gt; [!UICONTROL New]*, which opens a modal window with project options.
2. Klicken Sie auf die Inhaltskonsum-Vorlage (Web) und anschließend auf Erstellen.

## Site-Inhalt - Inhaltsdrilldown

Mit dem Drilldown-Bericht können Sie einen Blick auf den Seitenverkehr nach URL-Struktur werfen. Zusätzliche Implementierungen sind für die Verwendung in Analysis Workspace erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten genau erfasst werden.

## Site-Inhalt - Einstiegsseiten

Der Einstiegsseitenbericht zeigt die Top-Landingpages auf Ihrer Site an. Landing pages are available in Analysis Workspace as the **Entry Page** dimension.

1. In the Components menu, locate the **Entry Page** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Adobe recommends using the **Visits** metric for this dimension.

## Site-Inhalt - Ausstiegsseiten

Der Ausstiegsseitenbericht zeigt die Top-Seiten an, die zur letzten Seite eines individuellen Besuchs geworden sind. Sie ist im Analysis Workspace unter demselben Namen verfügbar.

1. In the Components menu, locate the **Exit Page** dimension and drag it onto the large freeform table area labeled &#39;Drop a Dimension here&#39;.
2. Drag the desired metrics onto the workspace alongside the automatically created **Occurrences** metric. See the [Metric translation guide](common-metrics.md) for details on how to obtain each respective metric.

Adobe recommends using the **Visits** metric for this dimension.

## Site-Geschwindigkeitsberichte

Site-Geschwindigkeitsberichte zeigen, wie schnell Seiten geladen werden, und zeigt Gelegenheiten zur Steigerung Ihrer Seitenladezeiten.

Diese Funktion erfordert zusätzliche Implementierungen auf beiden Plattformen; Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten für den Analysis Workspace richtig konfiguriert wurden. The [Performance Timing plugin](../../../implement/js-implementation/plugins/performancetiming.md) is typically assigned to an eVar to obtain performance data in Adobe Analytics.

## Site-Suchberichte

Site-Suchberichte bieten einen Einblick, wie Besucher die internen Suchfunktionen Ihrer Site nutzen.

Diese Funktion erfordert zusätzliche Implementierungen auf beiden Plattformen; Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten für den Analysis Workspace richtig konfiguriert wurden. Normalerweise wird ein interner Suchbegriff aus einem Abfragezeichenfolgenparameter gezogen und in eine evar für die Berichterstellung eingefügt.

## Ereignisberichte

Ereignisse haben wesentliche strukturelle Unterschiede zwischen Google und Adobe Analytics. Beide erfordern zusätzliche Implementierungsänderungen, damit sie auf ihrer jeweiligen Plattform ordnungsgemäß funktionieren.

* In Google Analytics werden Ereignisse in Ihrer Implementierung als Text definiert. Ereignisse verfügen über Kategorien, Aktionen und Beschriftungen.
* In Adobe Analytics werden Ereignisse zuerst in der Admin-Konsole eingerichtet, wo ihnen ein Bezeichner zugewiesen wird. Diese Kennung wird im Implementierungscode verwendet. Beispiel:
   1. Sie können event 1 in der Admin-Konsole als &quot;Registrierungen&quot; festlegen.
   2. In Ihrer Implementierung würden Sie event 1 in die Variable &quot;events&quot; auf der Registrierungsbestätigungsseite einbeziehen. Jedes Mal, wenn die Registrierungsbestätigungsseite angezeigt wird, erhöht sich event 1.
   3. In Analysis Workspace wird &quot;Registrierungen&quot; als Metrik für die Verwendung in einem beliebigen Bericht angezeigt.

Da diese Funktion Implementierungsänderungen erfordert, empfiehlt Adobe die Zusammenarbeit mit einem Implementierungsberater, um sicherzustellen, dass die Daten für den Analysis Workspace richtig konfiguriert wurden.

## Publisher-Berichte

Ähnlich wie Google für eine Verbindung mit Google Ad Manager bietet Adobe ein dediziertes Produkt, das Einblicke in die Adobe Advertising Cloud bietet. Wenn Ihr Unternehmen an der Nutzung dieses Produkts interessiert ist, wenden Sie sich an den Kundenbetreuer Ihrer Organisation.
