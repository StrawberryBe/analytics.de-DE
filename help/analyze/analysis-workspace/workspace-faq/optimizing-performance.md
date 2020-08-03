---
description: 'null'
title: Optimieren der Analysis Workspace-Leistung
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: 3cf68f3ba50c7a27a86d37591477812537b8ae1a
workflow-type: tm+mt
source-wordcount: '1306'
ht-degree: 85%

---


# Optimieren der Analysis Workspace-Leistung

Bestimmte Faktoren können die Leistung eines Projekts in Analysis Workspace beeinflussen. Damit Sie Ihr Projekt optimal planen und erstellen können, sollten Sie vor Beginn diese Faktoren kennen. In dieser Liste sind Faktoren aufgeführt, die die Leistung beeinflussen, sowie Best Practices zur Optimierung Ihrer Projekte. Die Leistung von Analysis Workspace stellt für Adobe eine der höchsten Prioritäten dar und wir arbeiten täglich daran, sie zu verbessern.

## Komplexität der Segmentlogik

Komplizierte Segmente können einen erheblichen Einfluss auf die Projektleistung haben. Zu den Faktoren, die einem Segment Komplexität verleihen (in grober Reihenfolge der Auswirkungen), gehören:

* Operatoren von „enthält“, „enthält beliebige von“, „stimmt überein mit“, „beginnt mit“ oder „endet mit“
* Sequentielle Segmentierung, insbesondere wenn Dimensionseinschränkungen (innerhalb/nachher) verwendet werden
* Anzahl der eindeutigen Dimensionselemente innerhalb der Dimensionen, die im Segment verwendet werden (z. B.: Seite = „A“, wenn Seite 10 eindeutige Elemente hat, ist schneller als Seite = „A“, wenn Seite 100000 eindeutige Elemente hat)
* Anzahl der verschiedenen verwendeten Dimensionen (z. B.: Seite = „Startseite“ und Seite = „Suchergebnisse“ sind schneller als eVar 1 = „rot“ und eVar 2 = „blau“)
* Viele ODER-Operatoren (anstelle von UND)
* Verschachtelte Container mit unterschiedlichem Umfang (z. B. Hit innerhalb des Besuchs innerhalb des Besuchers)

**Best Practices für logische Komplexität**

Während einige der Komplexitätsfaktoren nicht verhindert werden können, sollten Sie über Möglichkeiten nachdenken, die Komplexität Ihrer Segmente zu verringern. Generell gilt: Je genauer Sie mit Ihren Segmentkriterien umgehen können, desto besser. Beispiel:

* Bei Containern ist die Verwendung eines einzelnen Containers am oberen Rand des Segments schneller als die Verwendung einer Reihe verschachtelter Container
* Bei Operatoren ist „stimmt überein mit“ schneller als „enthält“ und „entspricht beliebigen von“ ist schneller als „enthält beliebige von“
* Mit vielen Kriterien sind UND-Operatoren schneller als eine Reihe von ODER-Operatoren. Suchen Sie außerdem nach Möglichkeiten, viele ODER-Anweisungen in eine einzelne Anweisung „entspricht einem von“ zu reduzieren

Außerdem können [Klassifizierungen](/help/components/classifications/c-classifications.md) dazu beitragen, viele Werte in präzisen Gruppen zu bündeln, aus denen Sie dann Segmente erstellen. Segmentierungen und Klassifizierungsgruppen bieten leistungsbezogene Vorteile gegenüber Segmenten mit vielen ODER-Anweisungen oder „enthält“-Kriterien.

## Angeforderter Datenbereich

Der Bereich der während eines Projekts angeforderten Daten beeinflusst die Performance von Analysis Workspace.

**Bewährte Verfahren für Datumsbereiche**

Rufen Sie möglichst nicht mehr Daten ab, als Sie benötigen. Schränken Sie den Bereichskalender auf die relevanten Daten für Ihre Analyse ein oder verwenden Sie Datumsbereichskomponenten (violette Komponenten) in Ihren Freiformtabellen. Datumsbereiche, die in einer Tabelle verwendet werden, setzen den Datumsbereich des Bereichs außer Kraft. Sie können beispielsweise den Tabellenspalten &quot;Letzter Monat&quot;, &quot;Letzte Woche&quot;und &quot;Gestern&quot;hinzufügen, um diese spezifischen Datenbereiche anzufordern. Weitere Informationen zu Datumsbereichen in Analysis Workspace erhalten Sie in [diesem Video](https://www.youtube.com/watch?v=MIkT6FZ5gKk).

Minimieren Sie die Anzahl der im Vergleich zum Vorjahr verwendeten Vergleiche. Bei der Berechnung eines Jahresvergleichs werden alle 13 Monate der Daten zwischen den Zinsmonaten berücksichtigt. Dies hat die gleiche Auswirkung wie die Änderung des Datumsbereichs des Bedienfelds auf 13 Monate.

## Anzahl der Visualisierungen

Die Anzahl der in einem Projekt enthaltenen Visualisierungen wirkt sich auf die Reaktionsgeschwindigkeit des Analysis Workspace insgesamt aus. Das liegt daran, dass jede Visualisierung, ob eine Tabelle oder ein Diagramm, über eine Datenquelle verfügt, die angefordert werden muss.

**Best Practices für die Anzahl der Visualisierungen**

Verwenden Sie weniger Visualisierungen in Ihrem Projekt. Analysis Workspace führt für jede hinzugefügte Visualisierung viele Berechnungen durch. Priorisieren Sie also die Visualisierungen, die für den Nutzer des Berichts am wichtigsten sind, und erstellen Sie bei Bedarf für begleitende Visualisierungen ein separates, detaillierteres Projekt.

## Komplexität der Visualisierungen (Segmente, Metriken, Filter)

Die Art der Visualisierung (z. B. Fallout oder Freiformtabelle), die zu einem Projekt hinzugefügt wird, beeinflusst die Leistung selbst nur geringfügig. Die Verarbeitungszeit wird durch die Komplexität der Visualisierung gesteigert. U. a. machen folgende Faktoren eine Visualisierung komplexer:

* Angeforderter Datumsbereich, wie oben erwähnt
* Anzahl der angewandten Segmente, z. B. als Zeilen verwendete Segmente in einer Freiformtabelle
* Verwendung von komplizierten Segmenten
* [Statische Elementzeilen oder Spalten in Freiformtabellen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html)
* Auf Zeilen angewandte Filter in Freiformtabellen
* Anzahl verwendeter Metriken, insbesondere berechneter Metriken, die Segmente verwenden

**Best Practice für die Visualisierungskomplexität**

Wenn Sie bemerken, dass Ihre Projekte langsamer als gewünscht geladen werden, sollten Sie nach Möglichkeit einige Segmente durch eVars und Filter ersetzen.

Wenn Sie ständig Segmente und berechnete Metriken für Datenpunkte verwenden, die für Ihr Unternehmen wichtig sind, sollten Sie versuchen, Ihre Implementierung zu verbessern, um diese Datenpunkte direkter zu erfassen. Mit einem Tag-Manager wie Adobe Experience Platform Launch und den Verarbeitungsregeln von Adobe sind Änderungen an der Implementierung schneller und leichter umzusetzen. Informationen zur Vereinfachung komplizierter Segmente finden Sie oben unter „Komplexität der Segmentlogik“.

## Anzahl der Bereiche

Ein Bereich kann viele Visualisierungen enthalten. Deshalb kann die Anzahl der Felder die Reaktionsschnelligkeit von Analysis Workspace beeinflussen.

**Best Practices für die Anzahl der Bereiche**

Versuchen Sie nicht, alles in ein Projekt zu packen. Erstellen Sie stattdessen spezifische Projekte, die für einen bestimmten Zweck oder eine Gruppe von Entscheidungsträgern zugeschnitten sind. Organisieren Sie Projekte mithilfe von Tags nach Schlüsselthemen und teilen Sie relevante Projekte mit Gruppen von Entscheidungsträgern.

Wenn Sie Ihre Projekte noch genauer organisieren möchten, denken Sie daran, dass Sie [direkte Links](https://www.youtube.com/watch?v=6IOEewflG2U) auf Ihre Projekte setzen können. Erstellen Sie einen internen Index Ihrer Projekte, sodass Entscheidungsträger einfacher die gewünschten Informationen finden können.

Wenn in einem Projekt viele Bedienfelder benötigt werden, reduzieren Sie die Bedienfelder vor dem Speichern und Freigeben. Wenn ein Projekt geladen wird, lädt Analysis Workspace nur den Inhalt der erweiterten Felder. Reduzierte Felder werden erst geladen, wenn der Nutzer sie erweitert. Dies hilft auf zwei Arten:

* Reduzierte Felder verringern die gesamte Ladezeit eines Projekts
* Mit reduzierten Feldern können Sie Ihre Projekte für den Nutzer des Berichts logisch organisieren

## Größe der Report Suite

Die Größe der Report Suite kann wie ein wichtiger Faktor erscheinen, doch tatsächlich spielt sie aufgrund des von Adobe genutzten Verfahrens zur Datenverarbeitung nur eine geringe Rolle bei der Projektleistung.  Es kann Ausnahmen von dieser Regel geben. Wenden Sie sich an Ihr Implementierungsteam oder einen Experten für Adobe, um festzustellen, ob Implementierungsverbesserungen zur Verbesserung der Gesamterfahrung in Adobe Analytics möglich sind.

## Anzahl der Personen, die gleichzeitig auf Analysis Workspace zugreifen

Die Anzahl der Benutzer, die gleichzeitig auf Analysis Workspace oder bestimmte Projekte zugreifen, hat keine wesentlichen Auswirkungen auf die Leistung von Analysis Workspace, wenn Benutzer auf verschiedene Report Suites zugreifen. Wenn Benutzer gleichzeitig auf dieselbe Report Suite zugreifen, wird die Leistung beeinträchtigt.

## Allgemeine Fehlermeldungen in Analysis Workspace

Bei der Interaktion mit Analysis Workspace können Fehler auftreten. Fehler können aus verschiedenen Gründen auftreten. Die häufigsten sind im Folgenden aufgeführt.

| Fehlermeldung | Grund |
|---|---|
| `The report suite is experiencing unusually heavy reporting. Please try again later.` | Ihr Unternehmen versucht, zu viele Anforderungen gleichzeitig für eine bestimmte Report Suite auszuführen. Zu diesem Fehler gehören API-Anforderungen, geplante Projekte, terminierte Berichte, terminierte Warnungen und gleichzeitige Benutzer, die Berichterstellungsanforderungen ausführen. Wir empfehlen, dass Ihre Anforderungen und Zeitpläne für die Report Suite gleichmäßig über den Tag verteilt werden. |
| `A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.` | Adobe hat ein Problem, das behoben werden muss. Es wird empfohlen, den Fehlercode über eine Anfrage an den Kundendienst zu senden. |
| `The request is too complex.` | Ihre Berichtsanfrage ist zu groß und kann nicht ausgeführt werden. Gründe für diesen Fehler sind Zeitüberschreitungen aufgrund der Anfragengröße, zu viele übereinstimmende Elemente in einem Segment oder Suchfilter, zu viele eingeschlossene Metriken, inkompatible Dimensions- und Metrikkombinationen usw. Wir haben empfohlen, dass Sie Ihre Anfrage vereinfachen. |
| `One of the segments or the search in this visualization contains a text search that returned too many results.` | Es wird empfohlen, die Suchtextkriterien einzuschränken und die Anfrage erneut auszuführen. |
| `This dimension does not currently support non-default attribution models.` | Wir empfehlen, die Dimension in Ihrer Tabelle durch eine Dimension zu ersetzen, die mit [Attribution IQ](../attribution/overview.md) kompatibel ist. |
| `Your request failed as a result of too many columns or pre-configured rows.` | Es wird empfohlen, einige Spalten oder Zeilen zu entfernen oder sie in separate Visualisierungen aufzuteilen. |
