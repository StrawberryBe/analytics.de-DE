---
description: 'null'
seo-description: 'null'
seo-title: Optimieren Sie die Leistung des Analysis Workspace.
title: Optimieren Sie die Leistung des Analysis Workspace.
uuid: de 51 d 03 d-d 555-4 f 0 e-b 19 c -4 a 8 f 140770 fc
translation-type: tm+mt
source-git-commit: ffb855a53d19449c4132dda59d728d3855955d9e

---


# Optimieren Sie die Leistung des Analysis Workspace.

Bestimmte Faktoren können die Leistung eines Projekts in Analysis Workspace beeinflussen. Damit Sie Ihr Projekt optimal planen und erstellen können, sollten Sie vor Beginn diese Faktoren kennen. In dieser Liste sind Faktoren aufgeführt, die die Leistung beeinflussen, sowie Best Practices zur Optimierung Ihrer Projekte. Die Leistung von Analysis Workspace stellt für Adobe eine der höchsten Prioritäten dar und wir arbeiten täglich daran, sie zu verbessern.

## Komplexität der Segmentlogik

Komplizierte Segmente können einen erheblichen Einfluss auf die Projektleistung haben. Zu den Faktoren, die einem Segment Komplexität hinzufügen (in absteigender Reihenfolge der Auswirkung), gehören:

* Operatoren von „enthält“, „enthält eines von“, „entspricht“, „beginnt mit“ oder „endet mit“
* Sequentielle Segmentierung, insbesondere wenn Dimensionseinschränkungen (innerhalb/nachher) verwendet werden
* Anzahl der eindeutigen Dimensionselemente innerhalb der Dimensionen, die im Segment verwendet werden (z. B.: Seite = „A“, wenn Seite 10 eindeutige Elemente hat, ist schneller als Seite = „A“, wenn Seite 100000 eindeutige Elemente hat)
* Anzahl der verschiedenen verwendeten Dimensionen (z. B.: Seite = „Startseite“ und Seite = „Suchergebnisse“ sind schneller als eVar 1 = „rot“ und eVar 2 = „blau“))
* Viele OR-Operatoren (anstelle von AND)
* Verschachtelte Behälter, die unterschiedlich sind (z. B. "Treffer" innerhalb von" Besuch" innerhalb von "Besucher" )

**Best Practices für Logikkomplexität**

Während einige der Komplexitätsfaktoren nicht verhindert werden können, sollten Sie über Möglichkeiten nachdenken, die Komplexität Ihrer Segmente zu verringern. Generell gilt: Je genauer Sie mit Ihren Segmentkriterien umgehen können, desto besser. Beispiel:

* Bei Containern ist die Verwendung eines einzelnen Containers am oberen Rand des Segments schneller als die Verwendung einer Reihe verschachtelter Container.
* Bei Operatoren ist "gleich" schneller als" enthält" , und "gleich" ist schneller als" enthält beliebige" .
* Mit vielen Kriterien sind AND-Operatoren schneller als eine Reihe von OR-Operatoren. Suchen Sie außerdem nach Gelegenheiten, um viele ODER-Aussagen zu reduzieren, die in einer einzigen Anweisung vorhanden sind.

Außerdem können [Klassifizierungen](/help/components/c-classifications2/c-classifications.md) dazu beitragen, viele Werte in präzisen Gruppen zu bündeln, aus denen Sie dann Segmente erstellen. Segmentierungen und Classification-Gruppen bieten leistungsbezogene Vorteile gegenüber Segmenten mit vielen „ODER“-Anweisungen oder „enthält“-Kriterien.

## Angeforderte Datenmenge

Die Menge der während eines Projekts angeforderten Daten beeinflusst die Performance von Analysis Workspace.

**Bewährte Verfahren für den Datumsbereich**

Rufen Sie möglichst nicht mehr Daten ab, als Sie benötigen.

Beachten Sie, dass Datumsbereiche (violette Komponenten) den Datumsbereich des Feldes überschreiben. Wenn Sie also verschiedene Datumsbereiche als Spalten verwenden (z. B. letzter Monat, letzte Woche und gestern), muss der Datumsbereich für das Feld nicht alle Datumsbereiche der Spalten umfassen. Sie können ihn einfach auf „gestern“ festlegen, da die Datumsbereiche in der Freiform-Tabelle den des Feldes überschreiben. Weitere Informationen zu Datumsbereichen in Analysis Workspace erhalten Sie in [diesem Video](https://www.youtube.com/watch?v=ybmv6EBmhn0) .

Use [date comparison options](../../analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md#concept_93BCAD81B7A54ABBBA5CD9E419F6F764) to pull in the specific time periods of data you want to compare. Wenn Sie z. B. die Daten des letzten Monats mit dem entsprechenden Vorjahresmonat vergleichen möchten, können Sie mit der Option „Zeiträume vergleichen“ den Jahresvergleich anzeigen, anstatt das Feld auf die Daten der letzten 13 Monate festzulegen.

## Anzahl der Visualisierungen

Die Anzahl der Diagrammvisualisierungen beeinflusst die Reaktionsschnelligkeit von Analysis Workspace.

**Best Practice für Visualisierungen**

Verwenden Sie weniger Visualisierungen in Ihrem Projekt. Analysis Workspace führt für jede hinzugefügte Visualisierung viele Berechnungen durch. Priorisieren Sie also die Visualisierungen, die für den Nutzer des Berichts am wichtigsten sind, und erstellen Sie bei Bedarf für begleitende Visualisierungen ein separates, detaillierteres Projekt.

## Komplexität der Visualisierungen (Segmente, Metriken, Filter)

Die Art der Visualisierung (z. B. Fallout oder Freiform-Tabelle), die zu einem Projekt hinzugefügt wird, beeinflusst die Leistung selbst nur geringfügig. Die Verarbeitungszeit wird durch die Komplexität der Visualisierung gesteigert. U. a. machen folgende Faktoren eine Visualisierung komplexer:

* Angeforderter Datumsbereich, wie oben erwähnt
* Anzahl der angewandten Segmente, z. B. als Zeilen verwendete Segmente in einer Freiform-Tabelle
* Verwendung von komplizierten Segmenten
* Statische Elementzeilen oder Spalten in Freiform-Tabellen
* Auf Zeilen angewandte Filter in Freiform-Tabellen
* Anzahl verwendeter Metriken, insbesondere berechneter Metriken, die Segmente verwenden

**Best Practice für Visualisierungskomplexität**

Wenn Sie bemerken, dass Ihre Projekte langsamer als gewünscht geladen werden, sollten Sie nach Möglichkeit einige Segmente durch eVars und Filter ersetzen.

Wenn Sie ständig Segmente und berechnete Metriken für Datenpunkte verwenden, die für Ihr Unternehmen wichtig sind, sollten Sie versuchen, Ihre Implementierung zu verbessern, um diese Datenpunkte direkter zu erfassen. Die Verwendung eines Tag-Managers wie Adobe Experience Platform Launch und die Verarbeitungsregeln von Adobe können die Implementierung schnell und einfach implementieren. Um besser zu verstehen, wie man komplizierte Segmente vereinfacht, sehen Sie oben „Komplexität der Segmentlogik“.

## Anzahl der Felder

Ein Bedienfeld kann viele Visualisierungen enthalten. Daher kann die Anzahl der Bedienfelder auch die Gesamtreaktionsgeschwindigkeit des Analysis Workspace beeinflussen.

**Best Practice für die Anzahl der Bedienfelder**

Versuchen Sie nicht, alles in ein Projekt zu packen. Erstellen Sie stattdessen spezifische Projekte, die für einen bestimmten Zweck oder eine Gruppe von Entscheidungsträgern zugeschnitten sind. Organisieren Sie Projekte mithilfe von Tags nach Schlüsselthemen und teilen Sie relevante Projekte mit Gruppen von Entscheidungsträgern.

Wenn Sie Ihre Projekte noch genauer organisieren möchten, denken Sie daran, dass Sie [direkte Links](https://www.youtube.com/watch?v=6IOEewflG2U) auf Ihre Projekte setzen können. Erstellen Sie einen internen Index Ihrer Projekte, sodass Entscheidungsträger einfacher die gewünschten Informationen finden können.

Wenn Sie in einem Projekt viele Felder benötigen, reduzieren Sie sie, bevor Sie das Projekt speichern und freigeben. Wenn ein Projekt geladen wird, lädt Analysis Workspace nur den Inhalt der erweiterten Felder. Reduzierte Felder werden erst geladen, wenn der Nutzer sie erweitert. Dies hilft auf zwei Arten:

* Reduzierte Felder verringern die gesamte Ladezeit eines Projekts
* Mit reduzierten Feldern können Sie Ihre Projekte für den Nutzer des Berichts logisch organisieren

## Größe der Report Suite

Die Größe der Report Suite kann wie ein wichtiger Faktor erscheinen, doch tatsächlich spielt sie aufgrund des von Adobe genutzten Verfahrens zur Datenverarbeitung nur eine geringe Rolle bei der Projektleistung.

## Anzahl der Benutzer gleichzeitig auf den Analysis Workspace

Die Anzahl der Benutzer, die gleichzeitig auf Analysis Workspace oder bestimmte Projekte zugreifen, hat keine wesentlichen Auswirkungen auf die Leistung des Analysis Workspace, wenn Benutzer auf verschiedene Report Suites zugreifen. Wenn gleichzeitig Benutzer auf dieselbe Report Suite zugreifen, wird die Leistung beeinträchtigt.

## Häufige Fehlermeldungen im Analysis Workspace

Bei der Interaktion mit Analysis Workspace treten möglicherweise Fehler auf. Fehler können aus verschiedenen Gründen auftreten und die folgenden sind am häufigsten aufgeführt.

| Fehlermeldung | Warum tritt dies auf? |
|---|---|
| `The report suite is experiencing unusually heavy reporting. Please try again later.` | Ihr Unternehmen versucht, zu viele gleichzeitige Anforderungen gegen eine bestimmte Report Suite auszuführen. Bei diesem Fehler handelt es sich um API-Anforderungen, geplante Projekte, geplante Berichte, geplante Warnungen und gleichzeitige Benutzer, die Berichterstellungsanforderungen erstellen. Es wird empfohlen, dass Ihre Anforderungen und Pläne für die Report Suite im gesamten Tag gleichmäßiger verteilt werden. |
| `A system error has occurred. Please log a Customer Care request under Help > Submit Support Ticket and include your error code.` | Adobe gibt ein Problem, das behoben werden muss. Es wird empfohlen, den Fehlercode über eine Kundenunterstützung zu senden. |
| `The request is too complex.` | Ihre Berichterstellungsanforderung ist zu groß und kann nicht ausgeführt werden. Bei diesem Fehler handelt es sich um Timeouts aufgrund der Größe der Anforderung, zu viele übereinstimmende Elemente in einem Segment oder der Suchfilter, zu viele Metriken, inkompatible Dimensionen und Metrikkombinationen usw. Wir empfehlen, Ihre Anforderung zu vereinfachen. |
