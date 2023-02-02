---
title: Festlegen von Benutzer- und Firmenvoreinstellungen in Analysis Workspace
description: Sie können allgemeine Voreinstellungen und Projekteinstellungen für Benutzer sowie eine Voreinstellung für dunkles Design festlegen.
feature: Workspace Basics
role: User, Admin
exl-id: f32e3061-f396-4730-96e1-d251b00e32f0
source-git-commit: 58abc4a8410441a3c76c6737ace8e2c5ab5c1374
workflow-type: tm+mt
source-wordcount: '2556'
ht-degree: 48%

---

# Voreinstellungen

Sie können Einstellungen für Analysis Workspace und die zugehörigen Komponenten für alle neuen Projekte oder Bereiche verwalten, die Sie erstellen. Vorhandene Projekte und Bedienfelder sind davon nicht betroffen.

In diesem Video erhalten Sie einen kurzen Überblick über die Voreinstellungen:

>[!VIDEO](https://video.tv.adobe.com/v/332600/?quality=12)

## Aktualisieren von Voreinstellungen

1. Navigieren Sie in Adobe Analytics zum [!UICONTROL **Projekt**] Landingpage und wählen Sie [!UICONTROL **Voreinstellungen**].

   ![Benutzerpräferenzen](assets/user-preferences.png)

1. Informationen zu den verfügbaren Voreinstellungen auf den einzelnen Registerkarten finden Sie in einem der folgenden Abschnitte in diesem Artikel:

   * [Allgemeine Voreinstellungen](#general-preferences)

   * [Projekteinstellungen](#project-preferences)

   * [Freiformtabellenvoreinstellungen](#freeform-table-preferences)

   * [Visualisierungseinstellungen](#visualizations-preferences)

## Allgemeine Voreinstellungen

Sie können allgemeine Voreinstellungen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

| Einstellung | Optionen |
| --- | --- |
| Landingpage | Wählen Sie aus, welche Seite beim Zugriff auf Adobe Analytics als Standardseite angezeigt wird: <ul><li>Projektliste (Standard)</li><li>Leeres Projekt</li><li>Spezifisches Projekt   ausgewählt aus einer Liste</li></ul> |
| Tipps anzeigen | Zeigt Tipps in einem blauen Feld im rechten unteren Bereich von Analysis Workspace an. <p>Standardmäßig ist diese Option aktiviert.</p> |
| Komponenten, die in Gruppen auf der linken Leiste angezeigt werden | Wählen Sie in der linken Leiste aus, wie viele Komponenten im Menü Komponenten angezeigt werden sollen. <p>Wenn Sie &quot;0&quot;auswählen, ist die Komponente nicht mehr über die linke Leiste Ihrer Arbeitsbereiche zugänglich.</p><p>Standardmäßig werden für jede der folgenden Komponenten fünf Komponenten angezeigt:</p> <ul><li>Dimensionen</li><li>Metriken</li><li>Filter</li><li>Datumsbereiche</li></ul> <p>Weitere Informationen zu Komponenten in Analysis Workspace finden Sie unter [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).</p> |

## Projekteinstellungen

Sie können die Projektvoreinstellungen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für einzelne Projekte angepasst werden, wie unter [Projektübersicht](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md).

Klicken Sie auf die verknüpften Präferenztitel, um weitere Informationen und den Kontext zu den einzelnen Präferenzen zu erhalten.

| Abschnitt | Einstellung | Optionen |
| --- | --- | --- |
| **Anzeigen** |  |  |
|  | [Dichte anzeigen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html?lang=de) | Wählen Sie aus, wie viel Inhalt auf dem Bildschirm angezeigt werden soll, indem Sie den vertikalen Abstand der linken Schiene, Freiformtabellen und Kohortentabellen reduzieren. <ul><li>Kompakt</li><li>Komfortabel</li><li>Erweitert (Standard)</li></ul> |
|  | [Farbpalette](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html?lang=de) | Wählen Sie die in Analysis Workspace verwendete Visualisierungsfarbpalette aus. <ul><li>Adobe-Paletten (Standard)</li><li>Bedingte Formatierungspalette </li><li>Nach-oben-/Nach-unten-Palette (divergierend)<li>Benutzerdefinierte Paletten</li></ul> |
| **Daten** |  |  |
|  | [Report Suite](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de#report-suite) | Wählen Sie aus, von wo aus Tabellen und Visualisierungen ihre Daten ableiten. <ul><li>Zuletzt verwendet (Standard)</li><li>Spezifische Report Suite, die aus einer Liste ausgewählt wurde</li></ul> |
|  | [Kalender](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de#calendar) | Wählen Sie aus einer Liste, die Folgendes enthält: <ul><li>Von Adobe bereitgestellte Bereiche (Standard ist „Diesen Monat“)</li><li>Benutzerdefinierte Bereiche</li></ul> |
|  | [Typ des Bedienfelds](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de) | <ul><li>Freiform (Standard)</li><li>Leer</li><li>Quick Insights</li></ul> |
|  | Wiederholte Instanzen zählen | Diese Einstellung legt fest, ob wiederholte Instanzen in Berichten gezählt werden sollen. Beispielsweise behandelt diese Einstellung (wenn aktiviert) mehrere aufeinander folgende Seitenansichten auf derselben Seite als mehrere Seitenansichten. Ohne zählen sie als Einzelseitenansicht. <p>**Hinweis:** Diese Einstellung betrifft nur bestimmte Metriken (z. B. Einzelseitenbesuche) und gilt nicht für Fluss- oder Fallout-Visualisierungen.</p> |
|  | Zahlenformat | <ul><li>1.000,00 (Standard)</li><li>1.000,00</li><li>1 000,00</li></ul> |
|  | CSV-Trennzeichen   Zeichen | <ul><li>Komma (Standard)</li><li>Semikolon</li><li>Doppelpunkt</li><li>Verkettungszeichen</li><li>Zeitraum</li><li>Leerzeichen</li><li>Tab</li></ul> |
|  | Anmerkungen anzeigen | Wählen Sie aus, ob Anmerkungen in Ihren Projekten sichtbar sind. Weitere Informationen zu Anmerkungen finden Sie unter [Anmerkungen - Übersicht](/help/analyze/analysis-workspace/components/annotations/overview.md). |

## Freiformtabellenvoreinstellungen

Sie können die Freiformtabelleneinstellungen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für einzelne Tabellen angepasst werden.

Klicken Sie auf die entsprechenden Abschnittstitel, um weitere Informationen und den Kontext zu den verfügbaren Voreinstellungen anzuzeigen.

| Abschnitt | Einstellung | Optionen |
| --- | --- | --- |
| **Tabelle** |  |  |
|  | Tabellentyp | <ul><li>Freiform</li><li>Tabellen-Builder</li></ul> |
|  | Standard-Tabellenmetrik | <ul><li>Vorfälle</li><li>Unique Visitors</li><li>Besuche</li></ul> |
|  | Standardabmessung der Tabelle | Wählen Sie zwischen Minute, Stunde, Tag, Woche, Monat, Quartal oder Jahr. |
|  | Datum ausrichten | Wählen Sie diese Option, um die Daten in jeder Spalte so auszurichten, dass sie alle in derselben Zeile beginnen. |
| **[Spalte](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** |  |  |
|  | Umbruch Kopfzeilentext | Hiermit können Sie den Kopfzeilentext in Freiformtabellen umbrechen, damit Kopfzeilen besser lesbar und Tabellen einfacher freizugeben sind. Diese Funktion ist beim .pdf-Rendering und für Metriken mit langen Namen nützlich. Standardmäßig aktiviert. |
|  | Summen anzeigen | Dieser Gesamtwert entspricht in der Regel der [!UICONTROL Gesamtsumme] oder einer Untergruppe davon. Er spiegelt alle Tabellenfilter wider, die innerhalb der Freiformtabelle angewendet werden, einschließlich der Option [!UICONTROL Keine einschließen]. |
|  | Gesamtsummen anzeigen | Dieser Gesamtwert stellt alle erfassten Hits dar, die manchmal als „Report Suite-Gesamtsumme“ bezeichnet werden. Wenn ein Segment entweder auf Bedienfeldebene oder in der Freiformtabelle angewendet wird, passt sich diese Summe an, um alle Treffer wiederzugeben, die den Segmentkriterien entsprechen. Gesamtsumme wird für Tabellen oder Aufschlüsselungen mit [statischen Zeilen](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md) nicht unterstützt. |
|  | Sparkline anzeigen | Liniendiagramme am unteren Rand des Diagramms anzeigen oder ausblenden. Wenn die Legende ausgeblendet wird, wird sie nicht mehr visuell auf die Zeilen verweisen. |
|  | Nummer | Definition, ob in einer Zelle der numerische Wert der Metrik angezeigt wird oder nicht. Ist die Metrik beispielsweise „Seitenansichten“, ist der numerische Wert die Anzahl an Seitenansichten für dieses Zeilenelement. |
|  | Prozent | Definition, ob in einer Zelle der Prozentwert der Metrik angezeigt wird oder nicht. Ist die Metrik beispielsweise „Seitenansichten“, ist der Prozentwert die Anzahl an Seitenansichten für dieses Zeilenelement geteilt durch die Gesamtanzahl der Seitenansichten für diese Spalte.  Hinweis: Für eine höhere Genauigkeit können Prozentsätze über 100 % angezeigt werden. Außerdem wird die obere Grenze auf 1.000 % verschoben, damit Spalten auch verbreitert werden können. |
|  | Anomalien anzeigen <!-- This setting was moved from the "Project" tab. this is already in the tool/docs under "Freeform table, But the doc doesn't give a definition. --> | Definition, ob die Anomalieerkennung für die Werte dieser Spalte ausgeführt wird |
|  | Null nicht als Wert interpretieren | Definition, ob in Zellen mit 0-Wert eine 0 oder nichts angezeigt wird. Diese Option ist praktisch, wenn Sie die Daten für einzelne Tage eines Monats anzeigen und einige Tage noch in der Zukunft liegen.  Statt für in der Zukunft liegende Daten eine 0 anzuzeigen, kann die entsprechende Zelle auch leer angezeigt werden. In Diagrammen wird diese Einstellung ebenfalls berücksichtigt (ist diese Einstellung aktiviert, wird in Diagrammen also keine Linie bzw. kein Balken mit 0-Werten angezeigt). |
|  | Hintergrund | Bestimmt, ob in einer Zelle die gesamte Zellformatierung, einschließlich Balkendiagramm und bedingter Formatierung, ein-/ausgeblendet wird <ul><li>Balkendiagramm</li> Zeigt ein horizontales Balkendiagramm mit dem Zellenwert in Relation zum Gesamtwert der Spalte an. <li>Bedingte Formatierung</li>Weitere Informationen zur bedingten Formatierung finden Sie unter &quot;Bedingte Formatierung&quot;in [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)</ul> |
|  | Zellenvorschau | Vorschau der jeweiligen Zelle mit allen ausgewählten Formatierungsoptionen |
| **[Zeile ](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** |  |  |
|  | Aufschlüsselung nach Position | Wählen Sie diese Option aus, wenn die Aufschlüsselung bei der Position des Elements und nicht beim Element selbst bleiben soll. Weitere Informationen zu Aufschlüsselungen finden Sie unter [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md). |
|  | Prozentuale Berechnung | <ul><li>Spalte</li><li>Zeile </li></ul> |

## Visualisierungseinstellungen

Sie können die Visualisierungseinstellungen für alle neuen Projekte aktualisieren, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für individuelle Visualisierungen angepasst werden.

Klicken Sie auf die entsprechenden Abschnittstitel, um weitere Informationen und den Kontext zu den verfügbaren Voreinstellungen anzuzeigen.

| Abschnitt | Einstellung | Optionen |
| --- | --- | --- |
| **Allgemeine Standardeinstellungen** |  |  |
|  | Prozentsatz | Zeigt Werte in Prozentsätzen für alle Visualisierungen an. |
|  | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für alle Visualisierungen. |
|  | Grenzwert für max. Anzahl von Elementen | Reduziert die Anzahl der Elemente auf der X-Achse für alle Visualisierungen. Dies kann bei großen Datensätzen nützlich sein. |
|  | Doppelachsenanzeige (falls anwendbar) | Gilt nur, wenn Sie zwei Metriken haben – möglich sind eine Y-Achse links (für die eine Metrik) und eine rechts (für die andere). Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
|  | Normalisierung (falls anwendbar) | Erzwingt Metriken für gleiche Anteile. Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
|  | Y-Achse bei null verankern | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |
|  | Skalierung der Y-Achse durch Anomalien zulassen | Wenn ein Diagramm mehrere Metriken enthält, müssen Sie den Mauszeiger über jede Anomalie bewegen, um das Konfidenzband für diese Metrik anzuzeigen. Um die Visualisierung lesbarer zu machen, skaliert das Konfidenzintervall der Anomalieerkennung nicht automatisch die Y-Achse. Mit dieser Option kann das Konfidenzintervall die Visualisierung skalieren. <p>Weitere Informationen finden Sie unter [Anzeigen von Anomalien in Analysis Workspace](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/view-anomalies.md).</p> |
| **[Linie](/help/analyze/analysis-workspace/visualizations/line.md)** |  |  |
|  | Prozentsatz | Zeigt Werte in Prozentwerten für die Linienvisualisierungen an. |
|  | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Linienvisualisierung. |
|  | Grenzwert für max. Anzahl von Elementen | Verkleinert die Anzahl der Elemente auf der X-Achse in der Linienvisualisierung. Dies kann bei großen Datensätzen nützlich sein. |
|  | Doppelachsenanzeige (falls anwendbar) | Gilt nur, wenn Sie zwei Metriken haben – möglich sind eine Y-Achse links (für die eine Metrik) und eine rechts (für die andere). Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
|  | Normalisierung (falls anwendbar) | Erzwingt Metriken für gleiche Anteile. Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
|  | X-Achse anzeigen | Zeigt die X-Achse im Liniendiagramm an. |
|  | y-Achse anzeigen | Zeigt die Y-Achse im Liniendiagramm an. |
|  | Y-Achse verankern | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |
|  | Min. anzeigen | Überlagern Sie eine Beschriftung für den Mindestwert, um die Täler schnell in einer Metrik hervorzuheben. Hinweis: Die Mindestwerte werden aus den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht aus dem vollständigen Satz von Werten innerhalb einer Dimension. |
|  | Maximal anzeigen | überlagern Sie eine Beschriftung für den Höchstwert, um die Spitzen in einer Metrik schnell hervorzuheben. Hinweis: Die max -Werte werden aus den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht aus dem vollständigen Satz von Werten innerhalb einer Dimension. |
|  | Trendlinie anzeigen | Zeigen Sie eine Regression oder eine sich bewegende durchschnittliche Trendlinie zu Ihrer Linienserie an. Trendlinien helfen, ein Muster in den Daten besser darzustellen. |
| **[Kohorte](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md)** |  |  |
|  | Granularität | Für Trend-Visualisierungen können Sie die Zeitgranularität ändern (Tag, Woche, Monat, Quartal oder Jahr). Diese Änderung gilt auch für die Datenquellentabelle. |
|  | Nur Prozentwert anzeigen | Entfernt den Zahlenwert und zeigt nur den Prozentsatz an. |
|  | Prozentwert auf nächste Ganzzahl runden | Kürzt den Prozentwert auf den nächsten ganzzahligen Wert, anstatt den Dezimalwert anzuzeigen. |
|  | Zeile mit durchschnittlichem Prozentsatz anzeigen | Fügt oben in der Tabelle eine neue Zeile ein und fügt dann den Durchschnitt der Werte in den einzelnen Spalten hinzu. |
|  | Kohortenvorschau | Eine Vorschau der Darstellung der Farbpalette in der Kohortenvisualisierung. |
|  | Kohortenpalette | Die in der Kohortenvisualisierung verwendete Farbpalette. |
| **[Kombinationsdiagramme](/help/analyze/analysis-workspace/visualizations/combo-charts.md)** |  |  |
|  | X-Achse zeigen | Zeigt die X-Achse im Kombinationsdiagramm an. |
|  | Y-Achse zeigen | Zeigt die Y-Achse im Kombinationsdiagramm an. |
|  | Balken auf Linien anzeigen | In Combo-Diagrammen Grillen auf Linien anzeigen. |
| **[Zusammenfassung einer Schlüsselmetrik](/help/analyze/analysis-workspace/visualizations/key-metric.md)** |  |  |
|  | Zusammenfassung des Anzeigetyps | <ul><li>Prozentuale Veränderung betonen</li><li>Zahlenwert hervorheben</li></ul> |
|  | Sparklines anzeigen | wie oder blendet Liniendiagramme am unteren Rand des Diagramms aus. Wenn die Legende ausgeblendet wird, wird sie nicht mehr visuell auf die Zeilen verweisen. |
|  | Max. und Min. auf Sparklines anzeigen | Mindest- und Höchstwerte in Primär- und Vergleichsliniendiagrammen anzeigen. |
|  | Vergleich anzeigen | Anzeigen von Vergleichsdaten. Wenn diese Option ausgeblendet ist, werden sowohl das Vergleichszeilendiagramm als auch die Zusammenfassungsänderung der Objekte ausgeblendet. |
|  | Zahlenwert-Optionen | Im [!UICONTROL **Zusammenfassung der Schlüsselmetriken**] Abschnitt <ul><li>Prozentänderung anzeigen</li><li>Rohdifferenz anzeigen</li>Rohdifferenz zwischen dem Gesamtwert der Metrik im primären Datumsbereich und dem sekundären Datumsbereich</ul> |
| **[Fallout](/help/analyze/analysis-workspace/visualizations/fallout/configuring-fallout.md)** |  |  |
|  | Container | Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Die Standardeinstellung lautet „Besucher“.  Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. <p>Die folgenden Optionen sind verfügbar:</p> <ul><li>Besuch</li><li>Besucher.</li></ul> |
| **[Fluss](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md)** |  |  |
|  | Container | Im [!UICONTROL **Fluss**] Abschnitt <ul><li>Besuch</li><li>Besucher.</li></ul> |
|  | Beschriftungen umbrechen | Die Bezeichnungen der Flusselemente werden üblicherweise aus Platzgründen auf dem Bildschirm abgeschnitten. Aktivieren Sie dieses Kontrollkästchen, um die gesamte Bezeichnung anzuzeigen. Standard = deaktiviert. |
|  | Wiederholungsinstanzen einschließen | Flussvisualisierungen basieren auf Instanzen einer Dimension. Diese Einstellung gibt Ihnen die Möglichkeit, wiederholte Instanzen ein- oder auszuschließen, z. B. Seitenneuladungen. Wiederholungen können jedoch nicht aus Flussvisualisierungen entfernt werden, die Dimensionen mit mehreren Werten enthalten, wie listVars, listProps, s.product, Merchandising-eVars usw. Standard = deaktiviert. |
|  | Tooltips anzeigen | Bestimmt, ob QuickInfos mit Knotendaten angezeigt werden, wenn der Mauszeiger über einzelne Knoten in einer Flussvisualisierung bewegt wird. |
|  | Anzahl der Spalten | Gibt an, wie viele Spalten Sie in Ihrem Flussdiagramm anzeigen möchten. |
|  | Erweiterte Elemente pro Spalte | Wie viele Elemente Sie in jeder Spalte anzeigen möchten. |
| **Stapeldiagramme** |  |  |
|  | 100 % gestapelt | Mit dieser Einstellung für die Visualisierungen „Bereich gestapelt“, „Balken gestapelt“ und „Horizontalbalken gestapelt“ wandeln Sie Diagramme in „zu 100 % gestapelte“ Visualisierungen um. <p>Weitere Informationen finden Sie unter [Balken und Balken gestapelt](/help/analyze/analysis-workspace/visualizations/bar.md).</p> |
| **[Histogramm](/help/analyze/analysis-workspace/visualizations/histogram.md)** |  |  |
|  | Anzahl der Behälter | Wählen Sie die Anzahl der Datenbereiche (Behälter) in der Visualisierung aus. Maximal 50 Behälter sind möglich. <p>Weitere Informationen finden Sie unter [Histogramm](/help/analyze/analysis-workspace/visualizations/histogram.md).</p> |
|  | Zählmethode | Wählen Sie aus den folgenden Optionen: <ul><li>Treffer</li><li>Besuch</li><li>Besucher.</li></ul> <p>Wenn Sie beispielsweise in Verbindung mit Seitenansichten verwenden, können Sie Seitenansichten pro Besucher, Seitenansichten für Besuche oder Seitenansichten pro Treffer auswählen. Für Hits wird „Vorkommen“ in der Freiformtabelle als Metrik der Y-Achse verwendet.</p> |
| **[Zuordnung](/help/analyze/analysis-workspace/visualizations/map-visualization.md)** |  |  |
|  | Plotting-Dimension | <ul><li>Mobiler Breitengrad/Längengrad</li><li>Geografische Dimension</li></ul> |
|  | Zuordnungstyp | <ul><li>Blasen</li><li>Heatmap</li></ul> |
|  | Farbschema | Wählen Sie Coral, Reds, Greens, Blues, Heatmap und Positive/Negative. |
|  | Zuordnungsstil | Wählen Sie aus Basic, Streets, Hell, Hell, Dunkel und Satellit. |
| **[Zusammenfassende Änderung](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** |  |  |
|  | Wert | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>Prozentuale Änderung</li><li>Rohdifferenz</li></ul> |
|  | Prozentsatz | Zeigt Werte in Prozentwerten für die Visualisierungen der Zusammenfassungsänderung an. |
|  | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung der Zusammenfassungsänderung. |
| **[Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** |  |  |
|  | Prozentsatz | Zeigt Werte in Prozentwerten für die Visualisierungen der Zusammenfassungsnummer an. |
|  | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung der Zusammenfassungsnummer. |
|  | Zusammenfassungswert nach | Wählen Sie aus &quot;Max&quot;, &quot;Min&quot;, &quot;Mittel&quot;, &quot;Median&quot;und &quot;Summe&quot;. |
|  | Wert abkürzen | Im [!UICONTROL **Zusammenfassungsnummer**] Abschnitt |
| **[Treemap](/help/analyze/analysis-workspace/visualizations/treemap.md)** |  |  |
|  | Prozentsatz | Zeigt Werte in Prozentsätzen für die Treemap-Visualisierungen an. |
|  | Grenzwert für max. Anzahl von Elementen | Reduziert die Anzahl der Elemente auf der X-Achse in der Treemap-Visualisierung. Dies kann bei großen Datensätzen nützlich sein. |
| **[Venn](/help/analyze/analysis-workspace/visualizations/venn.md)** |  |  |
|  | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Venn-Visualisierung. |
| **[Streuung](/help/analyze/analysis-workspace/visualizations/scatterplot.md)** |  |  |
|  | Prozentsatz | Zeigt Werte in Prozentwerten für die Streuvisualisierungen an. |
|  | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Streuungsvisualisierung. |
|  | Grenzwert für max. Anzahl von Elementen | Reduziert die Anzahl der Elemente auf der X-Achse in der Streuungsvisualisierung. Dies kann bei großen Datensätzen nützlich sein. |
|  | Y-Achse bei null verankern | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |

## Unternehmenseinstellungen

Sie können Unternehmenspräferenzen aktualisieren, die für alle Benutzer und Projekte in Ihrer Organisation gelten. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

| Abschnitt | Einstellung | Optionen |
| --- | --- | --- |
| **Registerkarte „Berichte“** |  |  |
|  | Registerkarte &quot;Berichte ausblenden&quot; | Blendet die Registerkarte Berichte für alle Benutzer in Ihrer Organisation aus. |

{style=&quot;table-layout:auto&quot;}

## Standardeinstellungen wiederherstellen

Sie können alle Ihre Benutzereinstellungen auf die Systemstandardwerte zurücksetzen. Dies wirkt sich nicht auf die Administratoreinstellungen auf der Registerkarte Unternehmen aus.

Diese Aktion kann nicht rückgängig gemacht werden.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] **>** [!UICONTROL **Voreinstellungen**].

   ![Benutzerpräferenzen](assets/user-preferences.png)

1. Wählen Sie oben rechts **[!UICONTROL Standardangaben wiederherstellen]**.

1. Wenn Sie dazu aufgefordert werden, wählen Sie **[!UICONTROL Standardangaben wiederherstellen]**.

## [!UICONTROL Dunkles Design]

Wenn Sie einen dunklen Hintergrund für Ihre Adobe Analytics-Benutzeroberfläche bevorzugen, können Sie zu [!UICONTROL Dunkles Design] wechseln.

1. Klicken Sie oben rechts auf das Experience Cloud-Benutzersymbol.

   ![dark-theme](assets/dark-theme.png)

1. Schieben Sie den Umschalter **[!UICONTROL Dunkles Thema]** nach rechts.

