---
description: 'null'
title: Optimieren der Analysis Workspace-Leistung
uuid: de51d03d-d555-4f0e-b19c-4a8f140770fc
translation-type: tm+mt
source-git-commit: 8ac408613d9aae1745cc6b876ef2a4c252f0665d
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 94%

---


# Optimieren der Analysis Workspace-Leistung

Bestimmte Faktoren können die Leistung eines Projekts in Analysis Workspace beeinflussen. Damit Sie Ihr Projekt optimal planen und erstellen können, sollten Sie vor Beginn diese Faktoren kennen. In dieser Liste sind Faktoren aufgeführt, die die Leistung beeinflussen, sowie Best Practices zur Optimierung Ihrer Projekte. Die Leistung von Analysis Workspace stellt für Adobe eine der höchsten Prioritäten dar und wir arbeiten täglich daran, sie zu verbessern.

## Komplexität der Segmentlogik

Komplizierte Segmente können einen erheblichen Einfluss auf die Projektleistung haben. Zu den Faktoren, die einem Segment Komplexität verleihen (in grober Reihenfolge der Auswirkungen), gehören:

* Operatoren von „enthält“, „enthält beliebige von“, „stimmt überein mit“, „beginnt mit“ oder „endet mit“
* Sequentielle Segmentierung, insbesondere wenn Dimensionseinschränkungen (innerhalb/nachher) verwendet werden
* Anzahl der eindeutigen Dimensionselemente innerhalb der Dimensionen, die im Segment verwendet werden (z. B.: Seite = „A“, wenn Seite 10 eindeutige Elemente hat, ist schneller als Seite = „A“, wenn Seite 100000 eindeutige Elemente hat)
* Anzahl der verschiedenen verwendeten Dimensionen (z. B.: Seite = „Startseite“ und Seite = „Suchergebnisse“ sind schneller als eVar 1 = „rot“ und eVar 2 = „blau“)
* Viele OR-Operatoren (anstelle von AND)
* Verschachtelte Container mit unterschiedlichem Umfang (z. B. Hit innerhalb des Besuchs innerhalb des Besuchers)

**Best Practices für logische Komplexität**

Während einige der Komplexitätsfaktoren nicht verhindert werden können, sollten Sie über Möglichkeiten nachdenken, die Komplexität Ihrer Segmente zu verringern. Generell gilt: Je genauer Sie mit Ihren Segmentkriterien umgehen können, desto besser. Beispiel:

* Bei Containern ist die Verwendung eines einzelnen Containers am oberen Rand des Segments schneller als die Verwendung einer Reihe verschachtelter Container
* Bei Operatoren ist „stimmt überein mit“ schneller als „enthält“ und „entspricht beliebigen von“ ist schneller als „enthält beliebige von“
* Mit vielen Kriterien sind AND-Operatoren schneller als eine Reihe von OR-Operatoren. Suchen Sie außerdem nach Möglichkeiten, viele OR-Anweisungen in eine einzelne Anweisung „entspricht einem von“ zu reduzieren

Außerdem können [Klassifizierungen](/help/components/classifications/c-classifications.md) dazu beitragen, viele Werte in präzisen Gruppen zu bündeln, aus denen Sie dann Segmente erstellen. Segmentierungen und Classification-Gruppen bieten leistungsbezogene Vorteile gegenüber Segmenten mit vielen OR-Anweisungen oder „enthält“-Kriterien.

## Angeforderter Datenbereich

Der Bereich der während eines Projekts angeforderten Daten beeinflusst die Performance von Analysis Workspace.

**Best Practices für Datumsbereiche**

Rufen Sie möglichst nicht mehr Daten ab, als Sie benötigen. Schränken Sie den Kalender des Bedienfelds auf die relevanten Daten für Ihre Analyse ein oder verwenden Sie Datumsbereichskomponenten (violette Komponenten) in Ihren Freiform-Tabellen. In einer Tabelle verwendete Datumsbereiche überschreiben den Datumsbereich des Bedienfelds. Beispielsweise können Sie den Tabellenspalten „Letzter Monat“, „Letzte Woche“ und „Gestern“ hinzufügen, um diese spezifischen Datenbereiche anzufordern. Weitere Informationen zu Datumsbereichen in Analysis Workspace erhalten Sie in [diesem Video](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/date-ranges-and-calendar-in-analysis-workspace.html).

Minimieren Sie die Anzahl der im Projekt verwendeten Jahresvergleiche. Bei der Berechnung eines Jahresvergleichs werden die gesamten 13 Monate von Daten zwischen den betrachteten Monaten berücksichtigt. Dies hat die gleiche Auswirkung wie die Änderung des Datumsbereichs des Bedienfelds auf 13 Monate.

## Anzahl der Visualisierungen

Die Anzahl der Visualisierungen beeinflusst die Reaktionsschnelligkeit von Analysis Workspace. Dies liegt daran, dass jede Visualisierung, sei es eine Tabelle oder ein Diagramm, eine Datenquelle hat, die angefordert werden muss.

**Best Practices für die Anzahl der Visualisierungen**

Verwenden Sie weniger Visualisierungen in Ihrem Projekt. Analysis Workspace führt für jede hinzugefügte Visualisierung viele Berechnungen durch. Priorisieren Sie also die Visualisierungen, die für den Nutzer des Berichts am wichtigsten sind, und erstellen Sie bei Bedarf für begleitende Visualisierungen ein separates, detaillierteres Projekt.

## Komplexität der Visualisierungen (Segmente, Metriken, Filter)

Die Art der Visualisierung (z. B. Fallout oder Freiformtabelle), die zu einem Projekt hinzugefügt wird, beeinflusst die Leistung selbst nur geringfügig. Die Verarbeitungszeit wird durch die Komplexität der Visualisierung gesteigert. U. a. machen folgende Faktoren eine Visualisierung komplexer:

* Angeforderter Datumsbereich, wie oben erwähnt
* Anzahl der angewandten Segmente, z. B. als Zeilen verwendete Segmente in einer Freiformtabelle
* Verwendung von komplizierten Segmenten
* [Statische Elementzeilen oder Spalten in Freiformtabellen](/help/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.md)
* Auf Zeilen angewandte Filter in Freiformtabellen
* Anzahl verwendeter Metriken, insbesondere berechneter Metriken, die Segmente verwenden

**Best Practice für die Visualisierungskomplexität**

Wenn Sie bemerken, dass Ihre Projekte langsamer als gewünscht geladen werden, sollten Sie nach Möglichkeit einige Segmente durch eVars und Filter ersetzen.

Wenn Sie ständig Segmente und berechnete Metriken für Datenpunkte verwenden, die für Ihr Unternehmen wichtig sind, sollten Sie versuchen, Ihre Implementierung zu verbessern, um diese Datenpunkte direkter zu erfassen. Mit einem Tag-Manager wie Adobe Experience Platform Launch und den Verarbeitungsregeln von Adobe sind Änderungen an der Implementierung schneller und leichter umzusetzen. Informationen zur Vereinfachung komplizierter Segmente finden Sie oben unter „Komplexität der Segmentlogik“.

## Anzahl der Bereiche

Ein Bereich kann viele Visualisierungen enthalten. Deshalb kann die Anzahl der Felder die Reaktionsschnelligkeit von Analysis Workspace beeinflussen.

**Best Practices für die Anzahl der Bereiche**

Versuchen Sie nicht, alles in ein Projekt zu packen. Erstellen Sie stattdessen spezifische Projekte, die für einen bestimmten Zweck oder eine Gruppe von Entscheidungsträgern zugeschnitten sind. Organisieren Sie Projekte mithilfe von Tags nach Schlüsselthemen und teilen Sie relevante Projekte mit Gruppen von Entscheidungsträgern.

Wenn Sie Ihre Projekte noch genauer organisieren möchten, denken Sie daran, dass Sie [direkte Links](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/curate-and-share-projects/direct-link-to-a-project.html) auf Ihre Projekte setzen können. Erstellen Sie einen internen Index Ihrer Projekte, sodass Entscheidungsträger einfacher die gewünschten Informationen finden können.

Wenn Sie in einem Projekt viele Bedienfelder benötigen, reduzieren Sie sie, bevor Sie das Projekt speichern und freigeben. Wenn ein Projekt geladen wird, lädt Analysis Workspace nur den Inhalt der erweiterten Felder. Reduzierte Felder werden erst geladen, wenn der Nutzer sie erweitert. Dies hilft auf zwei Arten:

* Reduzierte Felder verringern die gesamte Ladezeit eines Projekts
* Mit reduzierten Feldern können Sie Ihre Projekte für den Nutzer des Berichts logisch organisieren

## Größe der Report Suite

Die Größe der Report Suite kann wie ein wichtiger Faktor erscheinen, doch tatsächlich spielt sie aufgrund des von Adobe genutzten Verfahrens zur Datenverarbeitung nur eine geringe Rolle bei der Projektleistung.  Es kann Ausnahmen von dieser Regel geben. Wenden Sie sich an Ihr Implementierungs-Team oder einen Adobe-Experten, um festzustellen, ob es Verbesserungen bei der Implementierung gibt, die zur Verbesserung des Gesamterlebnisses mit Adobe Analytics beitragen können.

## Anzahl der Personen, die gleichzeitig auf Analysis Workspace zugreifen

Die Anzahl der Benutzer, die gleichzeitig auf Analysis Workspace oder bestimmte Projekte zugreifen, hat keine wesentlichen Auswirkungen auf die Leistung von Analysis Workspace, wenn Benutzer auf verschiedene Report Suites zugreifen. Wenn Benutzer gleichzeitig auf dieselbe Report Suite zugreifen, wird die Leistung beeinträchtigt.

## Allgemeine Fehlermeldungen in Analysis Workspace

Bei der Interaktion mit Analysis Workspace können Fehler auftreten. Fehler können aus verschiedenen Gründen auftreten. Die häufigsten sind im Folgenden aufgeführt.

| Fehlermeldung | Grund |
| --- | --- |
| [!UICONTROL Die Report Suite verzeichnet derzeit ein ungewöhnlich hohes Aufkommen von Berichtsdaten. Versuchen Sie es später erneut.] | Ihr Unternehmen versucht, zu viele Anforderungen gleichzeitig für eine bestimmte Report Suite auszuführen. Zu diesem Fehler gehören API-Anforderungen, geplante Projekte, terminierte Berichte, terminierte Warnungen und gleichzeitige Benutzer, die Berichterstellungsanforderungen ausführen. Wir empfehlen, dass Ihre Anforderungen und Zeitpläne für die Report Suite gleichmäßig über den Tag verteilt werden. |
| [!UICONTROL Es ist ein Systemfehler aufgetreten. Bitte melden Sie eine Anfrage an den Kundendienst unter Hilfe > Support-Ticket senden an und geben Sie Ihren Fehlercode ein.] | Adobe hat ein Problem, das behoben werden muss. Es wird empfohlen, den Fehlercode über eine Anfrage an den Kundendienst zu senden. |
| [!UICONTROL Die Anfrage ist zu komplex.] | Ihre Berichtsanfrage ist zu groß und kann nicht ausgeführt werden. Gründe für diesen Fehler sind Zeitüberschreitungen aufgrund der Anfragengröße, zu viele übereinstimmende Elemente in einem Segment oder Suchfilter, zu viele eingeschlossene Metriken, inkompatible Dimensions- und Metrikkombinationen usw. Wir haben empfohlen, dass Sie Ihre Anfrage vereinfachen. |
| [!UICONTROL Eines der Segmente oder die Suche in dieser Visualisierung enthält eine Textsuche, die zu viele Ergebnisse zurückgab.] | Es wird empfohlen, die Suchtextkriterien einzuschränken und die Anfrage erneut auszuführen. |
| [!UICONTROL Diese Dimension unterstützt nicht-standardmäßige Zuordnungsmodelle derzeit nicht.] | Wir empfehlen, die Dimension in Ihrer Tabelle durch eine Dimension zu ersetzen, die mit [Attribution IQ](/help/analyze/analysis-workspace/attribution/overview.md) kompatibel ist. |
| [!UICONTROL Ihre Anforderung schlug aufgrund zu vieler Spalten oder vorkonfigurierter Zeilen fehl.] | Es wird empfohlen, einige Spalten oder Zeilen zu entfernen oder sie in separate Visualisierungen aufzuteilen. |
