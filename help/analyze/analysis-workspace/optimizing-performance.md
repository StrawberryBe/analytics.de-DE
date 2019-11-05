---
description: 'null'
seo-description: 'null'
seo-title: Analysis Workspace-Leistung optimieren
title: Analysis Workspace-Leistung optimieren
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# Analysis Workspace-Leistung optimieren

Bestimmte Faktoren können die Leistung eines Projekts in Analysis Workspace beeinflussen. Es ist wichtig zu wissen, was diese Mitarbeiter sind, bevor Sie mit dem Erstellen eines Projekts beginnen, damit Sie das Projekt optimal planen und erstellen können. In dieser Liste sind Faktoren aufgeführt, die die Leistung beeinflussen, sowie Best Practices zur Optimierung Ihrer Projekte. Die Leistung des Arbeitsbereichs für Analysen ist eine der wichtigsten Prioritäten von Adobe und wird täglich weiter verbessert.

## Komplexität der Segmentlogik

Komplizierte Segmente können einen erheblichen Einfluss auf die Projektleistung haben. Zu den Faktoren, die einem Segment (in absteigender Reihenfolge der Auswirkungen) Komplexität hinzufügen, zählen:

* Operatoren von "contains", "contains any of", "match", "starts with"oder "ends with"
* Sequentielle Segmentierung, insbesondere wenn Dimensionseinschränkungen (innerhalb/nachher) verwendet werden
* Anzahl der eindeutigen Dimensionselemente innerhalb der Dimensionen, die im Segment verwendet werden (z. B.: Seite = „A“, wenn Seite 10 eindeutige Elemente hat, ist schneller als Seite = „A“, wenn Seite 100000 eindeutige Elemente hat)
* Anzahl der verschiedenen verwendeten Dimensionen (z. B.: Seite = „Startseite“ und Seite = „Suchergebnisse“ sind schneller als eVar 1 = „rot“ und eVar 2 = „blau“))
* Viele OR-Operatoren (anstelle von AND)
* Verschachtelte Behälter, die sich im Umfang unterscheiden (z. B. "Treffer"innerhalb von "Besuch"innerhalb von "Besucher")

**Bewährte Verfahren zur logischen Komplexität**

Während einige der Komplexitätsfaktoren nicht verhindert werden können, sollten Sie über Möglichkeiten nachdenken, die Komplexität Ihrer Segmente zu verringern. Generell gilt: Je genauer Sie mit Ihren Segmentkriterien umgehen können, desto besser. Beispiel:

* Bei Containern ist die Verwendung eines einzelnen Containers am oberen Rand des Segments schneller als die Verwendung einer Reihe verschachtelter Container.
* Bei Operatoren ist "equals"schneller als "contains", und "equals any of"ist schneller als "contains any of".
* Mit vielen Kriterien sind AND-Operatoren schneller als eine Reihe von OR-Operatoren. Suchen Sie außerdem nach Möglichkeiten, viele ODER-Anweisungen in eine einzelne Anweisung "Gleich einer von"zu reduzieren.

Außerdem können [Klassifizierungen](/help/components/c-classifications2/c-classifications.md) dazu beitragen, viele Werte in präzisen Gruppen zu bündeln, aus denen Sie dann Segmente erstellen. Die Segmentierung von Classification-Gruppen bietet Leistungsvorteile gegenüber Segmenten, die viele ODER-Anweisungen oder "enthält"-Kriterien enthalten.

## Angeforderte Datenmenge

Die Menge der während eines Projekts angeforderten Daten beeinflusst die Performance von Analysis Workspace.

**Bewährte Verfahren für den Datenbereich**

Wenn möglich, sollten Sie nicht mehr Daten einziehen, als Sie benötigen.

Beachten Sie, dass Datumsbereiche (violette Komponenten) den Datumsbereich des Feldes überschreiben. Wenn Sie also verschiedene Datumsbereiche als Spalten verwenden (z. B. letzter Monat, letzte Woche und gestern), muss der Datumsbereich für das Feld nicht alle Datumsbereiche der Spalten umfassen. Sie können ihn einfach auf „gestern“ festlegen, da die Datumsbereiche in der Freiform-Tabelle den des Feldes überschreiben. Weitere Informationen zu Datumsbereichen in Analysis Workspace erhalten Sie in [diesem Video](https://www.youtube.com/watch?v=ybmv6EBmhn0) .

Use [date comparison options](/help/analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md) to pull in the specific time periods of data you want to compare. Wenn Sie z. B. die Daten des letzten Monats mit dem entsprechenden Vorjahresmonat vergleichen möchten, können Sie mit der Option „Zeiträume vergleichen“ den Jahresvergleich anzeigen, anstatt das Feld auf die Daten der letzten 13 Monate festzulegen.

## Anzahl der Visualisierungen

Die Anzahl der Diagrammvisualisierungen beeinflusst die Reaktionsschnelligkeit von Analysis Workspace.

**Bewährte Verfahren für die Anzahl der Visualisierungen**

Verwenden Sie weniger Visualisierungen in Ihrem Projekt. Analysis Workspace führt für jede hinzugefügte Visualisierung viele Berechnungen durch. Priorisieren Sie also die Visualisierungen, die für den Nutzer des Berichts am wichtigsten sind, und erstellen Sie bei Bedarf für begleitende Visualisierungen ein separates, detaillierteres Projekt.

## Komplexität der Visualisierungen (Segmente, Metriken, Filter)

Die Art der Visualisierung (z. B. Fallout im Vergleich zu einer Freiformtabelle), die einem Projekt hinzugefügt wird, hat keinen großen Einfluss auf die Projektleistung. Die Verarbeitungszeit wird durch die Komplexität der Visualisierung gesteigert. U. a. machen folgende Faktoren eine Visualisierung komplexer:

* Angeforderter Datumsbereich, wie oben erwähnt
* Anzahl der angewandten Segmente, z. B. als Zeilen verwendete Segmente in einer Freiform-Tabelle
* Verwendung von komplizierten Segmenten
* Statische Elementzeilen oder Spalten in Freiform-Tabellen
* Auf Zeilen angewandte Filter in Freiform-Tabellen
* Anzahl verwendeter Metriken, insbesondere berechneter Metriken, die Segmente verwenden

**Best Practice für die Visualisierungskomplexität**

Wenn Sie bemerken, dass Ihre Projekte langsamer als gewünscht geladen werden, sollten Sie nach Möglichkeit einige Segmente durch eVars und Filter ersetzen.

Wenn Sie ständig Segmente und berechnete Metriken für Datenpunkte verwenden, die für Ihr Unternehmen wichtig sind, sollten Sie versuchen, Ihre Implementierung zu verbessern, um diese Datenpunkte direkter zu erfassen. Die Verwendung eines Tag-Managers wie Adobe Experience Platform Launch und die Verarbeitungsregeln von Adobe können die Implementierungsänderungen schnell und einfach implementieren. Um besser zu verstehen, wie man komplizierte Segmente vereinfacht, sehen Sie oben „Komplexität der Segmentlogik“.

## Anzahl der Felder

Ein Bedienfeld kann viele Visualisierungen enthalten. Daher kann die Anzahl der Bedienfelder auch die Gesamtreaktion des Analysis Workspace beeinflussen.

**Bewährte Verfahren für die Anzahl der Bereiche**

Versuchen Sie nicht, alles in ein Projekt einzufügen, sondern erstellen Sie unterschiedliche Projekte, die einem bestimmten Zweck oder einer Gruppe von Interessenvertretern dienen. Organisieren Sie Projekte mithilfe von Tags nach Schlüsselthemen und teilen Sie relevante Projekte mit Gruppen von Entscheidungsträgern.

Wenn Sie Ihre Projekte noch genauer organisieren möchten, denken Sie daran, dass Sie [direkte Links](https://www.youtube.com/watch?v=6IOEewflG2U) auf Ihre Projekte setzen können. Erstellen Sie einen internen Index Ihrer Projekte, sodass Entscheidungsträger einfacher die gewünschten Informationen finden können.

Wenn Sie in einem Projekt viele Felder benötigen, reduzieren Sie sie, bevor Sie das Projekt speichern und freigeben. Wenn ein Projekt geladen wird, lädt Analysis Workspace nur den Inhalt der erweiterten Felder. Reduzierte Felder werden erst geladen, wenn der Nutzer sie erweitert. Dies hilft auf zwei Arten:

* Reduzierte Felder verringern die gesamte Ladezeit eines Projekts
* Mit reduzierten Feldern können Sie Ihre Projekte für den Nutzer des Berichts logisch organisieren

## Größe der Report Suite

Die Größe der Report Suite kann wie ein wichtiger Faktor erscheinen, doch tatsächlich spielt sie aufgrund des von Adobe genutzten Verfahrens zur Datenverarbeitung nur eine geringe Rolle bei der Projektleistung.

## Anzahl der Benutzer, die gleichzeitig auf den Analysis Workspace zugreifen

Die Anzahl der Benutzer, die gleichzeitig auf den Analysis Workspace oder bestimmte Projekte zugreifen, hat keine wesentlichen Auswirkungen auf die Leistung des Analysis Workspace, wenn Benutzer auf verschiedene Report Suites zugreifen. Wenn gleichzeitige Benutzer auf dieselbe Report Suite zugreifen, wird die Leistung beeinträchtigt.

## Allgemeine Fehlermeldungen im Analysis Workspace

Bei der Interaktion mit dem Analysis Workspace können Fehler auftreten. Fehler können aus verschiedenen Gründen auftreten. Die folgenden sind am häufigsten aufgeführt.

| Fehlermeldung | Warum geschieht das? |
|---|---|
| `The report suite is experiencing unusually heavy reporting. Please try again later.` | Ihr Unternehmen versucht, zu viele Anforderungen gleichzeitig für eine bestimmte Report Suite auszuführen. Zu diesem Fehler gehören API-Anforderungen, geplante Projekte, terminierte Berichte, terminierte Warnungen und gleichzeitige Benutzer, die Berichterstellungsanforderungen ausführen. Wir empfehlen, dass Ihre Anforderungen und Zeitpläne für die Report Suite gleichmäßig über den Tag verteilt werden. |
| `A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.` | Adobe hat ein Problem, das behoben werden muss. Es wird empfohlen, den Fehlercode über eine Anfrage des Kundendienstes zu senden. |
| `The request is too complex.` | Ihre Berichtsanforderung ist zu groß und kann nicht ausgeführt werden. Bei den Mitwirkenden an diesem Fehler handelt es sich um Timeouts aufgrund der Anforderungsgröße, zu viele übereinstimmende Elemente in einem Segment oder Suchfilter, zu viele eingeschlossene Metriken, inkompatible Dimensions- und Metrikkombinationen usw. Wir haben empfohlen, dass Sie Ihre Anforderung vereinfachen. |
| `One of the segments or the search in this visualization contains a text search that returned too many results.` | Es wird empfohlen, die Suchtextkriterien einzuschränken und die Anforderung erneut auszuführen. |
| `This dimension does not currently support non-default attribution models.` | Wir empfehlen, die Dimension in Ihrer Tabelle durch eine Dimension zu ersetzen, die mit [Attribution IQ](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution.html)kompatibel ist. |
| `Your request failed as a result of too many columns or pre-configured rows.` | Es wird empfohlen, einige Spalten oder Zeilen zu entfernen oder sie in separate Visualisierungen aufzuteilen. |
