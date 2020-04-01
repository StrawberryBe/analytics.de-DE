---
description: 'null'
title: Analysis Workspace-Leistung optimieren
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: e6ca7f56dab0928e13ae68d810149ca97b2ae5bd

---


# Analysis Workspace-Leistung optimieren

Bestimmte Faktoren können die Leistung eines Projekts in Analysis Workspace beeinflussen. Damit Sie Ihr Projekt optimal planen und erstellen können, sollten Sie vor Beginn diese Faktoren kennen. In dieser Liste sind Faktoren aufgeführt, die die Leistung beeinflussen, sowie Best Practices zur Optimierung Ihrer Projekte. Die Leistung von Analysis Workspace stellt für Adobe eine der höchsten Prioritäten dar und wir arbeiten täglich daran, sie zu verbessern.

## Komplexität der Segmentlogik

Komplizierte Segmente können einen erheblichen Einfluss auf die Projektleistung haben. Zu den Faktoren, die einem Segment Komplexität verleihen (in grober Reihenfolge der Auswirkungen), gehören:

* Operatoren von „enthält“, „enthält beliebige von“, „stimmt überein mit“, „beginnt mit“ oder „endet mit“
* Sequenzielle Segmentierung, insbesondere wenn Dimensionsbeschränkungen (In/Nach) verwendet werden
* Anzahl der Elemente mit eindeutiger Dimension innerhalb der im Segment verwendeten Dimensionen (z. B. Seite = &#39;A&#39;, wenn Seite 10 eindeutige Elemente enthält, ist schneller als Seite = &#39;A&#39;, wenn Seite 100000 eindeutige Elemente hat)
* Anzahl der verschiedenen verwendeten Dimensionen (z. B.: Seite = „Startseite“ und Seite = „Suchergebnisse“ sind schneller als eVar 1 = „rot“ und eVar 2 = „blau“)
* Viele ODER-Operatoren (anstelle von UND)
* Verschachtelte Container mit unterschiedlichem Umfang (z. B. Hit innerhalb des Besuchs innerhalb des Besuchers)

**Best Practices für logische Komplexität**

Während einige der Komplexitätsfaktoren nicht verhindert werden können, sollten Sie über Möglichkeiten nachdenken, die Komplexität Ihrer Segmente zu verringern. Generell gilt: Je genauer Sie mit Ihren Segmentkriterien umgehen können, desto besser. Beispiel:

* Bei Containern ist die Verwendung eines einzigen Containers am oberen Segmentrand schneller als bei einer Reihe verschachtelter Container.
* Bei Operatoren ist „stimmt überein mit“ schneller als „enthält“ und „entspricht beliebigen von“ ist schneller als „enthält beliebige von“.
* Mit vielen Kriterien sind UND-Operatoren schneller als eine Reihe von ODER-Operatoren. Suchen Sie außerdem nach Möglichkeiten, viele ODER-Anweisungen in eine einzelne Anweisung „entspricht einem von“ zu reduzieren.

Außerdem können [Klassifizierungen](/help/components/c-classifications2/c-classifications.md) dazu beitragen, viele Werte in präzisen Gruppen zu bündeln, aus denen Sie dann Segmente erstellen. Segmentierungen und Klassifizierungsgruppen bieten leistungsbezogene Vorteile gegenüber Segmenten mit vielen ODER-Anweisungen oder „enthält“-Kriterien.

## Angeforderter Datenbereich

Der Bereich der während eines Projekts angeforderten Daten beeinflusst die Performance von Analysis Workspace.

**Best Practices für den Datenbereich**

Rufen Sie möglichst nicht mehr Daten ab, als Sie benötigen.

Denken Sie daran, dass Datumsbereiche (violette Komponenten) den Datumsbereich des Bedienfelds außer Kraft setzen. Wenn Sie daher unterschiedliche Datumsbereiche als Spalten verwenden (z. B. Spalten vom letzten Monat, letzte Woche und gestern), muss der Datumsbereich des Bereichs nicht alle Datumsbereiche der Spalte umfassen. Sie können ihn einfach auf „gestern“ festlegen, da die Datumsbereiche in der Freiformtabelle den des Feldes überschreiben. Weitere Informationen zu Datumsbereichen in Analysis Workspace erhalten Sie in [diesem Video](https://www.youtube.com/watch?v=ybmv6EBmhn0).

Nutzen Sie [Datumsvergleichsoptionen](/help/analyze/analysis-workspace/components/calendar-date-ranges/time-comparison.md), um die Daten für die Zeiträume abzurufen, die Sie vergleichen möchten. Wenn Sie z. B. die Daten des letzten Monats mit dem entsprechenden Vorjahresmonat vergleichen möchten, können Sie mit der Option „Zeiträume vergleichen“ den Jahresvergleich anzeigen, anstatt das Feld auf die Daten der letzten 13 Monate festzulegen.

## Anzahl der Visualisierungen

Die Anzahl der Diagrammvisualisierungen beeinflusst die Reaktionsschnelligkeit von Analysis Workspace.

**Best Practices für die Anzahl der Visualisierungen**

Verringern Sie die Anzahl der Visualisierungen in Ihrem Projekt. Im Arbeitsbereich für Analysen werden hinter den Kulissen viele Visualisierungen für jede hinzugefügte Visualisierung verarbeitet. Priorisieren Sie daher die Visualisierungen, die für den Benutzer des Berichts am wichtigsten sind, und unterteilen Sie ggf. unterstützende Visualisierungen in ein separates, detaillierteres Projekt.

## Komplexität der Visualisierungen (Segmente, Metriken, Filter)

Die Art der Visualisierung (z. B. Fallout oder Freiformtabelle), die zu einem Projekt hinzugefügt wird, beeinflusst die Leistung selbst nur geringfügig. Die Komplexität der Visualisierung erhöht die Verarbeitungszeit. Zu den Faktoren, die eine Visualisierung komplexer machen, zählen:

* Umfang der angeforderten Daten, wie oben erwähnt
* Anzahl der angewandten Segmente, z. B. als Zeilen verwendete Segmente in einer Freiformtabelle
* Verwendung komplexer Segmente
* Statische Elementzeilen oder Spalten in Freiformtabellen
* Auf Zeilen angewandte Filter in Freiformtabellen
* Anzahl der enthaltenen Metriken, insbesondere berechnete Metriken, die Segmente verwenden

**Best Practice für die Visualisierungskomplexität**

Wenn Sie bemerken, dass Ihre Projekte langsamer als gewünscht geladen werden, sollten Sie nach Möglichkeit einige Segmente durch eVars und Filter ersetzen.

Wenn Sie ständig Segmente und berechnete Metriken für Datenpunkte verwenden, die für Ihr Unternehmen wichtig sind, sollten Sie versuchen, Ihre Implementierung zu verbessern, um diese Datenpunkte direkter zu erfassen. Mit einem Tag-Manager wie Adobe Experience Platform Launch und den Verarbeitungsregeln von Adobe sind Änderungen an der Implementierung schneller und leichter umzusetzen. Informationen zur Vereinfachung komplizierter Segmente finden Sie oben unter „Komplexität der Segmentlogik“.

## Anzahl der Bereiche

Ein Bereich kann viele Visualisierungen enthalten. Deshalb kann die Anzahl der Felder die Reaktionsschnelligkeit von Analysis Workspace beeinflussen.

**Best Practices für die Anzahl der Bereiche**

Versuchen Sie nicht, alles in ein Projekt zu packen. Erstellen Sie stattdessen spezifische Projekte, die für einen bestimmten Zweck oder eine Gruppe von Entscheidungsträgern zugeschnitten sind. Verwenden Sie Tags, um Projekte in wichtigen Themen zu organisieren und zugehörige Projekte mit Interessengruppen zu teilen.

Wenn Sie eine größere Organisation von Projekten wünschen, denken Sie daran, dass eine [direkte Verknüpfung](https://www.youtube.com/watch?v=6IOEewflG2U) mit Ihrem Projekt eine Option ist. Erstellen Sie einen internen Index Ihrer Projekte, sodass Entscheidungsträger einfacher die gewünschten Informationen finden können.

Wenn in einem Arbeitsbereich viele Bedienfelder benötigt werden, reduzieren Sie die Bedienfelder vor dem Speichern und Freigeben. Beim Laden eines Projekts lädt der Arbeitsbereich für Analysen nur Inhalte für die erweiterten Bereiche. Reduzierte Bereiche werden erst geladen, wenn der Benutzer sie erweitert. Dieser Ansatz hilft in zweierlei Hinsicht:

* Reduzierte Bedienfelder werden bei der Gesamtladezeit eines Projekts gespeichert
* Reduzierte Bereiche sind eine hervorragende Möglichkeit, Ihre Projekte logisch für den Verbraucher des Berichts zu organisieren.

## Größe der Report Suite

Die Größe der Report Suite kann wie ein wichtiger Faktor erscheinen, doch tatsächlich spielt sie aufgrund des von Adobe genutzten Verfahrens zur Datenverarbeitung nur eine geringe Rolle bei der Projektleistung.

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
| `This dimension does not currently support non-default attribution models.` | Wir empfehlen, die Dimension in Ihrer Tabelle durch eine Dimension zu ersetzen, die mit [Attribution IQ](/help/analyze/analysis-workspace/c-panels/attribution/attribution.md) kompatibel ist. |
| `Your request failed as a result of too many columns or pre-configured rows.` | Es wird empfohlen, einige Spalten oder Zeilen zu entfernen oder sie in separate Visualisierungen aufzuteilen. |
