---
title: Verhaltensberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Verhaltensberichte in Adobe Analytics erstellen
translation-type: tm+mt
source-git-commit: e1cbdf87140b915dccbb8f64694797bb903d8ab8

---


# Verhaltensberichte

Verhaltensberichte zeigen Informationen zur Interaktion der Benutzer mit Ihrer Site an.

Auf dieser Seite wird davon ausgegangen, dass der Benutzer über grundlegende Kenntnisse in der Verwendung des Analysis Workspace verfügt. Siehe [Erstellen eines einfachen Berichts im Analysis Workspace für Google Analytics-Benutzer](create-report.md) , wenn Sie mit dem Tool in Adobe Analytics noch nicht vertraut sind.

## Verhaltensfluss

Der Verhaltensflussbericht kann mithilfe der Flussvisualisierung neu erstellt werden.

1. Klicken Sie auf das Symbol Visualisierungen links und ziehen Sie eine Flussvisualisierung auf den Arbeitsbereich über der Freiformtabelle
2. Suchen Sie die Dimension &quot; **Seite** &quot;und klicken Sie dann auf das Pfeilsymbol, um die Seitenwerte anzuzeigen. Dimensionswerte sind gelb.
3. Suchen Sie den gewünschten Seitenwert, mit dem Sie beginnen möchten, und ziehen Sie ihn in den Bereich mit der Bezeichnung &quot;Dimension oder Element&quot;in der Mitte
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

![Flussbericht](/help/technotes/ga-to-aa/assets/flow.png)

## Site-Inhalt - Alle Seiten

Der Seitenbericht zeigt die Leistung einzelner Seiten auf Ihrer Site an.

1. Suchen Sie im Menü &quot;Komponenten&quot;die Dimension &quot; **Seiten** &quot;und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Als Alternative bietet Adobe mehrere vordefinierte Arbeitsbereiche, die als Vorlagen bezeichnet werden. Die Vorlage &quot;Inhaltskonsum (Web)&quot;bietet einen ähnlichen Wert wie der Bericht &quot;Alle Seiten&quot;.

1. Klicken Sie auf *[!UICONTROL Projekt]>[!UICONTROL Neu]*, um ein modales Fenster mit Projektoptionen zu öffnen.
2. Klicken Sie auf die Vorlage Inhaltskonsum (Web) und dann auf Erstellen.

## Site-Content - Content-Drilldown

Mit dem Bericht zur Inhaltsauswertung können Sie sich den Seitenverkehr nach URL-Struktur ansehen. Für die Verwendung im Analysis Workspace ist eine zusätzliche Implementierung erforderlich. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt erfasst werden.

## Site-Inhalt - Einstiegsseiten

Der Einstiegsseitenbericht zeigt die obersten Einstiegsseiten Ihrer Site an. Einstiegsseiten sind im Arbeitsbereich für Analysen als **Einstiegsseiten** verfügbar.

1. Suchen Sie im Menü &quot;Komponenten&quot;die Dimension &quot; **Entrypage** &quot;und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Adobe empfiehlt die Verwendung der Metrik **Besuche** für diese Dimension.

## Site-Inhalt - Ausstiegsseiten

Der Bericht zu Ausstiegsseiten zeigt die obersten Seiten an, die die letzte Seite eines individuellen Besuchs wurden. Es ist in Analysis Workspace unter demselben Namen verfügbar.

1. Suchen Sie im Menü &quot;Komponenten&quot;die Dimension &quot; **Ausstiegsseite** &quot;und ziehen Sie sie in den großen Freiform-Tabellenbereich mit der Bezeichnung &quot;Dimension hier ablegen&quot;.
2. Ziehen Sie die gewünschten Metriken neben der automatisch erstellten Metrik &quot; **Vorfälle** &quot;in den Arbeitsbereich. Einzelheiten zum Abrufen der jeweiligen Metrik finden Sie im Handbuch[ zur ](common-metrics.md)Metrikübersetzung.

Adobe empfiehlt die Verwendung der Metrik **Besuche** für diese Dimension.

## Site-Geschwindigkeitsberichte

Site-Geschwindigkeitsberichte zeigen, wie schnell Seiten geladen werden. Sie zeigen Möglichkeiten, die Seitenladezeit zu erhöhen.

Diese Funktion erfordert eine zusätzliche Implementierung auf beiden Plattformen. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt für den Analysis Workspace konfiguriert sind. Das [getPageLoadTime-Plug-In](/help/implement/vars/plugins/getpageloadtime.md) wird normalerweise einer eVar zugewiesen, um Leistungsdaten in Adobe Analytics abzurufen.

## Site-Suchberichte

Site-Suchberichte bieten einen Einblick, wie Besucher die internen Suchfunktionen Ihrer Site nutzen.

Diese Funktion erfordert eine zusätzliche Implementierung auf beiden Plattformen. Adobe empfiehlt, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass diese Daten korrekt für den Analysis Workspace konfiguriert sind. In der Regel wird ein interner Suchbegriff aus einem Abfragezeichenfolgenparameter gezogen und zur Berichterstellung in eine eVar eingefügt.

## Ereignisberichte

Ereignisse weisen einige große strukturelle Unterschiede zwischen Google und Adobe Analytics auf. Beide erfordern zusätzliche Implementierungsänderungen, damit sie auf der jeweiligen Plattform ordnungsgemäß funktionieren.

* In Google Analytics werden Ereignisse in Ihrer Implementierung als Text definiert. Ereignisse haben Kategorien, Aktionen und Bezeichnungen.
* In Adobe Analytics werden Ereignisse zuerst in der Admin-Konsole eingerichtet, der eine ID zugewiesen wurde. Diese Kennung wird im Implementierungscode verwendet. Beispiel:
   1. Sie können event1 in der Admin-Konsole als &quot;Registrierungen&quot;festlegen.
   2. In Ihrer Implementierung würden Sie event1 in die Ereignisvariable auf der Registrierungsbestätigungsseite aufnehmen. Jedes Mal, wenn die Registrierungsbestätigungsseite angezeigt wird, steigt event1.
   3. Im Arbeitsbereich für Analysen erscheint &quot;Registrierungen&quot;als Metrik zur Verwendung in einem beliebigen Bericht.

Da für diese Funktion Implementierungsänderungen erforderlich sind, empfiehlt Adobe, mit einem Implementierungsberater zusammenzuarbeiten, um sicherzustellen, dass die Daten für den Analysis Workspace korrekt konfiguriert sind.

## Publisher-Berichte

Ähnlich wie Google eine Verbindung mit Google Ad Manager erfordert, bietet Adobe ein spezielles Produkt zur Bereitstellung von Insight, die Adobe Advertising Cloud. Wenn Ihr Unternehmen an der Verwendung dieses Produkts interessiert ist, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens.
