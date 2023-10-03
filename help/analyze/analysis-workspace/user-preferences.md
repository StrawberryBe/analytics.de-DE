---
title: So legen Sie Benutzer- und Firmenvoreinstellungen in Analysis Workspace fest
description: Sie können allgemeine Voreinstellungen und Projekteinstellungen für Benutzende sowie eine Voreinstellung für dunkles Design festlegen.
feature: Workspace Basics
role: User, Admin
exl-id: f32e3061-f396-4730-96e1-d251b00e32f0
source-git-commit: cca740f66783de4323b91dd722e3a108dde6b023
workflow-type: tm+mt
source-wordcount: '3156'
ht-degree: 95%

---

# Voreinstellungen

Sie können für alle neu erstellten Projekte oder Bedienfelder die auf Analysis Workspace und die zugehörigen Komponenten anzuwendenden Einstellungen verwalten. Bestehende Projekte und Bedienfelder sind davon nicht betroffen.

In diesem Video erhalten Sie einen kurzen Überblick über Voreinstellungen:

>[!VIDEO](https://video.tv.adobe.com/v/332600/?quality=12)

## Aktualisieren von Voreinstellungen

1. Navigieren Sie in Customer Journey Analytics zur Landingpage [!UICONTROL **Projekt**] und wählen Sie [!UICONTROL **Voreinstellungen**] aus.

   ![Benutzervoreinstellungen](assets/user-preferences.png)

1. Informationen zu den verfügbaren Voreinstellungen auf den einzelnen Registerkarten finden Sie in jedem der folgenden Abschnitte in diesem Artikel:

   * [Allgemeine Voreinstellungen](#general-preferences)

   * [Firma](#company-preferences)

   * [Projektvoreinstellungen](#project-preferences)

   * [Voreinstellungen für Freiformtabellen](#freeform-table-preferences)

   * [Voreinstellungen für Visualisierungen](#visualizations-preferences)

## Allgemeine Voreinstellungen

Sie können die allgemeinen Voreinstellungen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

| Voreinstellung | Optionen |
| --- | --- |
| Landingpage | Wählen Sie aus, welche Seite beim Zugriff auf Adobe Analytics als Standardseite angezeigt werden soll: <ul><li>Projektliste (Standard)</li><li>Leeres Projekt</li><li>Spezifisches Projekt  ausgewählt aus einer Liste</li></ul> |
| Tipps anzeigen | Zeigt Tipps in einem blauen Feld im rechten unteren Bereich von Analysis Workspace an. <p>Standardmäßig ist diese Option aktiviert.</p> |
| Komponenten, die in Gruppen auf der linken Leiste angezeigt werden | Wählen Sie aus, wie viele Komponenten im Komponentenmenü in der linken Leiste angezeigt werden sollen. <p>Wenn Sie „0“ auswählen, kann die Komponente nicht mehr über die linke Leiste Ihrer Arbeitsbereiche aufgerufen werden.</p><p>Standardmäßig werden für jede der folgenden Objekte fünf Komponenten angezeigt:</p> <ul><li>Dimensionen</li><li>Metriken</li><li>Filter</li><li>Datumsbereiche</li></ul> <p>Weitere Informationen zu Komponenten in Analysis Workspace finden Sie unter [Komponentenübersicht](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).</p> |

## Unternehmensvoreinstellungen

Sie können Unternehmensvoreinstellungen aktualisieren, die für alle Benutzerinnen und Benutzer sowie Projekte in Ihrer Organisation gelten. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Registerkarte „Berichte“** | | |
|  | Registerkarte „Berichte“ ausblenden | Blendet die Registerkarte „Berichte“ für alle Benutzerinnen und Benutzer in Ihrer Organisation aus. |
| **Projektfreigabe** | | |
| | Freigabe nur für Workspace-Benutzende zulassen | <p>Wenn diese Option aktiviert ist, können Benutzerinnen und Benutzer in Ihrer Organisation im Menü „Freigeben“ die Option „Für alle freigeben“ nicht sehen. Das bedeutet, dass Benutzerinnen und Benutzer keine Projekte für Personen freigeben können, die kein Analysis Workspace-Konto in Ihrer Organisation haben, wie unter [Projekt für andere freigeben (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md) beschrieben wird.</p><p>Beachten Sie beim Aktivieren oder Deaktivieren dieser Option Folgendes:</p> <ul><li><p>Wenn Sie diese Option aktivieren, können Personen, die zuvor über die Freigabeoption „Für alle freigeben“ Zugriff auf ein Projekt erhalten haben, nicht mehr auf das Projekt zugreifen.</p></li><li><p>Wenn diese Option aktiviert ist (um die Freigabe nur für Workspace-Benutzende zuzulassen) und später deaktiviert wird (um die Freigabe für andere zuzulassen), erhalten Personen, die zuvor über die Freigabeoption „Für alle freigeben“ Zugriff auf ein Projekt erhalten hatten, nicht automatisch wieder Zugriff auf das Projekt. In diesem Fall muss die Person, die das Projekt freigegeben hat, die Option [!UICONTROL **Link ist aktiv**] aktivieren, die beim Freigeben eines Projekts für alle verfügbar ist ([!UICONTROL **Freigeben**] > [!UICONTROL **Für alle freigeben**]), wie unter [Projekt für alle freigeben (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md).</p></li> |
| | Experience Cloud-Authentifizierung verlangen | <p>Wenn diese Option aktiviert ist, müssen sich Personen, die über die Option „Für alle freigeben“ in Analysis Workspace Zugriff auf ein Projekt erhalten haben, sich mit ihren Anmeldeinformationen von Experience Cloud authentifizieren.</p> <p>Wenn diese Option aktiviert ist, wird jedes Mal, wenn eine Person ein Projekt mithilfe der Freigabeoption „Für alle freigeben“ teilt, die Option „Authentifizierung für dieses Projekt erforderlich“ im Freigabe-Dialogfeld aktiviert und kann von der Person, die das Projekt freigegeben hat, nicht deaktiviert werden. (Informationen dazu, wie Benutzerinnen und Benutzer Projekte für alle freigeben können, finden Sie unter [Projekt für alle freigeben (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md).)</p> <p>Beachten Sie beim Aktivieren dieser Option Folgendes:</p><ul><li><p>Wenn Sie diese Option aktivieren, werden alle Projekte, die zuvor mit der Freigabeoption „Für alle freigeben“ freigegeben wurden und für die die Option „Experience Cloud-Authentifizierung erfordern“ nicht aktiviert ist, deaktiviert.</p></li> <li><p>Wenn diese Option aktiviert ist (d. h. eine Experience Cloud-Authentifizierung erforderlich ist) und später deaktiviert wird (damit alle Benutzerinnen und Benutzer mit dem Link auf das Projekt zugreifen können), erhalten Personen, die zuvor über die Freigabeoption „Für alle freigeben“ Zugriff auf ein Projekt erhalten haben, nicht automatisch wieder Zugriff auf das Projekt. In diesem Fall muss die Person, die das Projekt freigegeben hat, die Option „Link ist aktiv“ aktivieren, die verfügbar ist, wenn ein Projekt für alle freigegeben wird ([!UICONTROL **Freigeben**] > [!UICONTROL **Für alle freigeben**] > [!UICONTROL **Link ist aktiv**]), wie unter [Projekt für alle freigeben (keine Anmeldung erforderlich)](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Freigeben von Projekten](/help/analyze/analysis-workspace/curate-share/share-projects.md) beschrieben wird.</p></li> <li><p>Diese Option ist nur verfügbar, wenn SSO in Ihrem Unternehmen implementiert ist. Informationen dazu, wie System-Admins SSO für Ihre Organisation aktivieren können, finden Sie unter [Einrichten von Identität und Single Sign-On](https://helpx.adobe.com/de/enterprise/using/set-up-identity.html){target=_blank}.</p><p>Wenn SSO für Ihre Organisation konfiguriert ist, überprüfen Sie, ob in der Konsole eine automatische Kontoerstellung implementiert ist. Normalerweise richten System-Admins dies ein, wie unter [Aktivieren der automatischen Kontoerstellung](https://helpx.adobe.com/de/enterprise/using/automatic-account-creation.html){target=_blank} beschrieben wird.</p></li><li><p>Wenn Ihr Unternehmen in einer Branche tätig ist, die HIPAA-Compliance erfordert, wird diese Option automatisch aktiviert und kann nicht deaktiviert werden.</p></li></ul> |

{style="table-layout:auto"}

## Voreinstellungen für Projekte und Analysen

Sie können die Projektvoreinstellungen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für einzelne Projekte angepasst werden, wie unter [Projektübersicht](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) beschrieben.

Klicken Sie auf die verlinkten Voreinstellungstitel, um weitere Informationen und Kontext zu den einzelnen Voreinstellungen zu erhalten.

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Anzeigen** | | |
|  | [Dichte anzeigen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html?lang=de) | Wählen Sie aus, wie viel Inhalt auf dem Bildschirm angezeigt werden soll, indem Sie den vertikalen Abstand der linken Schiene, der Freiformtabellen und der Kohortentabellen verkleinern. <ul><li>Kompakt</li><li>Komfortabel</li><li>Erweitert (Standard)</li></ul> |
| | [Farbpalette](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html?lang=de) | Wählen Sie die in Analysis Workspace verwendeten Farbpaletten für die Visualisierung aus.<ul><li>**Kategorische Palette**: Wird auf viele Visualisierungen in Analysis Workspace angewendet. Jede Farbe stellt einen eindeutigen Kategorenwert dar. Wählen Sie aus den von Adobe bereitgestellten Optionen oder geben Sie eine benutzerdefinierte Palette ein, die durch kommagetrennte Hexadezimalwerte definiert wird.</li><li>**Divergent, Palette**: Wird auf die Kohortentabelle in Analysis Workspace angewendet. Diese Palette enthält eine numerische Bedeutung mit zwei Extremen und eine Grundlinie in der Mitte.</li><li>**Sequenzielle Palette**: Angewandt auf die geleitete Analyse der Häufigkeitstrends (gestapelte Leiste). Diese Palette hat eine numerische Bedeutung von hell bis dunkel.</li></ul> |
| **Daten** | | |
|  | [Report Suite](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de#report-suite) | Wählen Sie aus, von wo Tabellen und Visualisierungen ihre Daten beziehen sollen. <ul><li>Zuletzt verwendet (Standard)</li><li>Spezifische Report Suite, die aus einer Liste ausgewählt wurde</li></ul> |
|  | [Kalender](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de#calendar) | Wählen Sie aus einer Liste, die Folgendes enthält: <ul><li>Von Adobe bereitgestellte Bereiche (Standard ist „Diesen Monat“)</li><li>Benutzerdefinierte Bereiche</li></ul> |
|  | [Typ des Bedienfelds](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?lang=de) | <ul><li>Freiform (Standard)</li><li>Leer</li><li>Quick Insights</li></ul> |
|  | Wiederholte Instanzen zählen | Diese Einstellung legt fest, ob wiederholte Instanzen in Berichten gezählt werden sollen. Beispielsweise werden mit dieser Einstellung (wenn aktiviert) mehrere aufeinanderfolgende Aufrufe derselben Seite wie mehrere Seitenaufrufe gezählt. Ist diese Einstellung deaktiviert, werden sie als nur ein einziger Seitenaufruf gezählt. <p>**Hinweis:** Diese Einstellung wirkt sich nur auf bestimmte Metriken aus (z. B. Einzelseitenbesuche) und nicht auf Fluss- oder Fallout-Visualisierungen.</p> |
|  | Zahlenformat | <ul><li>1.000,00 (Standard)</li><li>1.000,00</li><li>1 000,00</li></ul> |
|  | CSV-Trennzeichen    Zeichen | <ul><li>Komma (Standard)</li><li>Semikolon</li><li>Doppelpunkt</li><li>Verkettungszeichen</li><li>Zeitraum</li><li>Leerzeichen</li><li>Tab</li></ul> |
|  | Anmerkungen anzeigen | Wählen Sie aus, ob Anmerkungen in Ihren Projekten sichtbar sein sollen. Weitere Informationen zu Anmerkungen finden Sie unter [Anmerkungen – Überblick](/help/analyze/analysis-workspace/components/annotations/overview.md). |

## Voreinstellungen für Freiformtabellen

Sie können die Voreinstellungen für Freiformtabellen für alle neuen Projekte anpassen, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für einzelne Tabellen angepasst werden.

Klicken Sie auf die verlinkten Abschnittstitel, um weitere Informationen und den Kontext zu den verfügbaren Voreinstellungen anzuzeigen.

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Tabelle** | | |
| | Tabellentyp | <ul><li>Freiform</li><li>Tabellen-Builder</li></ul> |
| | Standard-Tabellenmetrik | <ul><li>Vorkommen</li><li>Unique Visitors</li><li>Besuche</li></ul> |
| | Standarddimension der Tabelle | Wählen Sie zwischen Minute, Stunde, Tag, Woche, Monat, Quartal oder Jahr. |
| | Datum ausrichten | Wählen Sie diese Option, um die Daten in allen Spalten so auszurichten, dass sie alle in derselben Zeile beginnen. |
| **[Spalte](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** | | |
| | Kopfzeilentext umbrechen | Hiermit können Sie den Kopfzeilentext in Freiformtabellen umbrechen, damit Kopfzeilen besser lesbar und Tabellen einfacher freizugeben sind. Diese Funktion ist beim .pdf-Rendering und für Metriken mit langen Namen nützlich. Standardmäßig aktiviert. |
| | Summen anzeigen | Dieser Gesamtwert entspricht in der Regel der [!UICONTROL Gesamtsumme] oder einer Untergruppe davon. Er spiegelt alle Tabellenfilter wider, die innerhalb der Freiformtabelle angewendet werden, einschließlich der Option [!UICONTROL Keine einschließen]. |
| | Gesamtsummen anzeigen | Dieser Gesamtwert stellt alle erfassten Hits dar, die manchmal als „Report Suite-Gesamtsumme“ bezeichnet werden. Wenn ein Segment entweder auf Bedienfeldebene oder in der Freiformtabelle angewendet wird, passt sich diese Summe an, um alle Treffer wiederzugeben, die den Segmentkriterien entsprechen. Gesamtsumme wird für Tabellen oder Aufschlüsselungen mit [statischen Zeilen](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md) nicht unterstützt. |
| | Sparkline anzeigen | Liniendiagramme am unteren Rand des Diagramms anzeigen oder ausblenden. Wenn sie ausgeblendet sind, wird die Legende so geändert, dass sie keinen visuellen Bezug mehr zu den Linien hat. |
| | Nummer | Definition, ob in einer Zelle der numerische Wert der Metrik angezeigt wird oder nicht. Ist die Metrik beispielsweise „Seitenansichten“, ist der numerische Wert die Anzahl an Seitenansichten für dieses Zeilenelement. |
| | Prozent | Definition, ob in einer Zelle der Prozentwert der Metrik angezeigt wird oder nicht. Ist die Metrik beispielsweise „Seitenansichten“, ist der Prozentwert die Anzahl an Seitenansichten für dieses Zeilenelement geteilt durch die Gesamtanzahl der Seitenansichten für diese Spalte.  Hinweis: Für eine höhere Genauigkeit können Prozentsätze über 100 % angezeigt werden. Außerdem wird die obere Grenze auf 1.000 % verschoben, damit Spalten auch verbreitert werden können. |
| | Anomalien anzeigen <!-- This setting was moved from the "Project" tab. this is already in the tool/docs under "Freeform table, But the doc doesn't give a definition. --> | Gibt an, ob die Anomalieerkennung für die Werte dieser Spalte ausgeführt wird |
| | Null nicht als Wert interpretieren | Definition, ob in Zellen mit 0-Wert eine 0 oder nichts angezeigt wird. Diese Option ist praktisch, wenn Sie die Daten für einzelne Tage eines Monats anzeigen und einige Tage noch in der Zukunft liegen.  Statt für in der Zukunft liegende Daten eine 0 anzuzeigen, kann die entsprechende Zelle auch leer angezeigt werden. In Diagrammen wird diese Einstellung ebenfalls berücksichtigt (ist diese Einstellung aktiviert, wird in Diagrammen also keine Linie bzw. kein Balken mit 0-Werten angezeigt). |
| | Hintergrund | Gibt an, ob in einer Zelle alle Zellformatierungen ein-/ausgeblendet werden, einschließlich Balkendiagramm und bedingter Formatierung <ul><li>Balkendiagramm</li> Zeigt ein horizontales Balkendiagramm mit dem Zellenwert in Relation zum Gesamtwert der Spalte an. <li>Bedingte Formatierung</li>Weitere Informationen zur bedingten Formatierung finden Sie unter „Bedingte Formatierung“ in den [Spalteneinstellungen](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md).</ul> |
| | Zellenvorschau | Vorschau der jeweiligen Zelle mit allen ausgewählten Formatierungsoptionen |
| **[Zeile ](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** | | |
| | Aufschlüsselung nach Position | Wählen Sie diese Option aus, wenn die Aufschlüsselung bei der Position des Elements und nicht beim Element selbst bleiben soll. Weitere Informationen zur Aufschlüsselungen finden Sie unter [Dimensionen aufschlüsseln](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md). |
| | Prozentuale Berechnung | <ul><li>Spalte</li><li>Zeile</li></ul> |
| | Spaltensummen (nur statische Zeilen) | <ul><li>Summe der Zeilen anzeigen: Zeigt die Summe der einzelnen Zeileneinträge an </li><li>Gesamtsumme anzeigen: Zeigt die deduplizierte Summe der Zeilen an.</li></ul> |

## Voreinstellungen für Visualisierungen

Sie können die Visualisierungseinstellungen für alle neuen Projekte aktualisieren, die Sie in Analysis Workspace erstellen. Informationen zum Zugriff auf diese Voreinstellungen finden Sie unter [Aktualisieren von Voreinstellungen](#update-preferences).

Einige dieser Voreinstellungen können auch für individuelle Visualisierungen angepasst werden.

Klicken Sie auf die verlinkten Abschnittstitel, um weitere Informationen und den Kontext zu den verfügbaren Voreinstellungen anzuzeigen.

| Abschnitt | Voreinstellung | Optionen |
| --- | --- | --- |
| **Allgemeine Standardeinstellungen** | | |
| | Prozentsatz | Zeigt für alle Visualisierungen Werte in Prozentsätzen an. |
| | Legende sichtbar | Ermöglicht für alle Visualisierungen das Ausblenden des detaillierten Legendentextes. |
| | Grenzwert für max. Anzahl von Elementen | Reduziert für alle Visualisierungen die Anzahl der Elemente auf der X-Achse. Dies kann bei großen Datensätzen nützlich sein. |
| | Zwei Achsen anzeigen (falls anwendbar) | Gilt nur, wenn Sie zwei Metriken haben – möglich sind eine Y-Achse links (für die eine Metrik) und eine rechts (für die andere). Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | Normalisierung (falls anwendbar) | Erzwingt Metriken für gleiche Anteile. Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | Y-Achse bei null verankern | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |
| | Skalierung der Y-Achse durch Anomalien zulassen | Wenn ein Diagramm mehrere Metriken enthält, bewegen Sie den Mauszeiger über die einzelnen Anomalien, damit das Konfidenzband für diese Metrik eingeblendet wird. Damit die Visualisierung besser lesbar ist, wird die Y-Achse nicht automatisch durch das Konfidenzintervall der Anomalieerkennung skaliert. Mit dieser Option kann die Visualisierung durch das Konfidenzintervall skaliert werden. <p>Weitere Informationen finden Sie unter [Anzeige von Anomalien in Analysis Workspace](/help/analyze/analysis-workspace/virtual-analyst/c-anomaly-detection/view-anomalies.md).</p> |
| **[Linie](/help/analyze/analysis-workspace/visualizations/line.md)** | | |
| | Prozentsatz | Zeigt in Linienvisualisierungen Werte in Prozentsätzen an. |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Linienvisualisierung. |
| | Grenzwert für max. Anzahl von Elementen | Verringert die Anzahl der Elemente auf der X-Achse in der Linienvisualisierung. Dies kann bei großen Datensätzen nützlich sein. |
| | Zwei Achsen anzeigen (falls anwendbar) | Gilt nur, wenn Sie zwei Metriken haben – möglich sind eine Y-Achse links (für die eine Metrik) und eine rechts (für die andere). Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | Normalisierung (falls anwendbar) | Erzwingt Metriken für gleiche Anteile. Dies ist hilfreich, wenn grafisch dargestellte Metriken sehr unterschiedliche Größenordnungen aufweisen. |
| | X-Achse anzeigen | Zeigt die X-Achse im Liniendiagramm an. |
| | Y-Achse anzeigen | Zeigt die Y-Achse im Liniendiagramm an. |
| | Y-Achse verankern | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |
| | Min. anzeigen | Blenden Sie eine Kennzeichnung für den Mindestwert ein, um die Täler einer Metrik schnell hervorzuheben. Hinweis: Die Minimalwerte werden von den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht von dem vollständigen Satz von Werten innerhalb einer Dimension. |
| | Max. anzeigen | Blenden Sie eine Kennzeichnung für den Maximalwert ein, um die Spitzen einer Metrik schnell hervorzuheben. Hinweis: Die Maximalwerte werden von den sichtbaren Datenpunkten in der Visualisierung abgeleitet, nicht von dem vollständigen Satz von Werten innerhalb einer Dimension. |
| | Trendlinie anzeigen | Zeigen Sie zu Ihrer Linienserie eine Regressions-Trendlinie oder eine Trendlinie mit angepasstem Durchschnittswert an. Trendlinien helfen, ein Muster in den Daten besser darzustellen. |
| **[Kohorte](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md)** | | |
| | Granularität | Für Trend-Visualisierungen können Sie die Zeitgranularität ändern (Tag, Woche, Monat, Quartal oder Jahr). Diese Änderung gilt auch für die Datenquellentabelle. |
| | Nur Prozentwert anzeigen | Entfernt den Zahlenwert und zeigt nur den Prozentsatz an. |
| | Prozentwert auf nächste Ganzzahl runden | Rundet den Prozentwert auf den nächsten ganzzahligen Wert, anstatt den Dezimalwert anzuzeigen. |
| | Zeile mit durchschnittlichem Prozentwert anzeigen | Fügt oben in der Tabelle eine neue Zeile ein und fügt dann den Spaltendurchschnitt der Werte hinzu. |
| | Kohortenvorschau | Eine Vorschau davon, wie die Farbpalette in der Kohortenvisualisierung aussieht. |
| | Kohortenpalette | Die in der Kohortenvisualisierung verwendete Farbpalette. |
| **[Kombinationsdiagramme](/help/analyze/analysis-workspace/visualizations/combo-charts.md)** | | |
| | X-Achse anzeigen | Zeigt die X-Achse im Kombinationsdiagramm an. |
| | Y-Achse anzeigen | Zeigt die Y-Achse im Kombinationsdiagramm an. |
| | Hanteln auf Linien anzeigen | Zeigt Hanteln auf Linien im Kombinationsdiagramm. |
| **[Zusammenfassung einer Schlüsselmetrik](/help/analyze/analysis-workspace/visualizations/key-metric.md)** | | |
| | Zusammenfassung des Anzeigetyps | <ul><li>Prozentuale Veränderung hervorheben</li><li>Zahlenwert hervorheben</li></ul> |
| | Sparklines anzeigen | Liniendiagramme am unteren Rand des Diagramms anzeigen oder ausblenden. Wenn sie ausgeblendet sind, wird die Legende so geändert, dass sie keinen visuellen Bezug mehr zu den Linien hat. |
| | Max. und Min. auf Sparklines anzeigen | Einblenden von Minimal- und Maximalwerten in Primär- und Vergleichsliniendiagrammen. |
| | Vergleich anzeigen | Anzeigen von Vergleichsdaten. Wenn diese Option ausgeblendet ist, werden sowohl das Vergleichszeilendiagramm als auch die Objekte der Zusammenfassungsänderung ausgeblendet. |
| | Zahlenwert-Optionen | Im Abschnitt [!UICONTROL **Zusammenfassung der Schlüsselmetriken**] <ul><li>Prozentuale Veränderung anzeigen</li><li>Rohdifferenz anzeigen</li>Rohdifferenz zwischen dem Gesamtwert der Metrik im primären Datumsbereich und im sekundären Datumsbereich</ul> |
| **[Fallout](/help/analyze/analysis-workspace/visualizations/fallout/configuring-fallout.md)** | | |
| | Container | Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Die Standardeinstellung lautet „Besucher“. Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. <p>Die folgenden Optionen sind verfügbar:</p> <ul><li>Besuch</li><li>Besucher</li></ul> |
| **[Fluss](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md)** | | |
| | Container | Im Abschnitt [!UICONTROL **Fluss**] <ul><li>Besuch</li><li>Besucher</li></ul> |
| | Beschriftungen umbrechen | Die Beschriftungen der Flusselemente werden üblicherweise aus Platzgründen auf dem Bildschirm abgeschnitten. Aktivieren Sie dieses Kontrollkästchen, um die gesamte Beschriftung anzuzeigen. Standard = deaktiviert. |
| | Wiederholungsinstanzen einschließen | Flussvisualisierungen basieren auf Instanzen einer Dimension. Diese Einstellung gibt Ihnen die Möglichkeit, wiederholte Instanzen ein- oder auszuschließen, z. B. Seitenneuladungen. Wiederholungen können jedoch nicht aus Flussvisualisierungen entfernt werden, die Dimensionen mit mehreren Werten enthalten, wie listVars, listProps, s.product, Merchandising-eVars usw. Standard = deaktiviert. |
| | Tooltips anzeigen | Bestimmt, ob Tooltips mit Knotendaten angezeigt werden, wenn der Mauszeiger über einzelne Knoten in einer Flussvisualisierung bewegt wird. |
| | Anzahl der Spalten | Gibt an, wie viele Spalten Sie in Ihrem Flussdiagramm anzeigen möchten. |
| | Erweiterte Elemente pro Spalte | Wie viele Elemente Sie in jeder Spalte anzeigen möchten. |
| **Stapeldiagramme** | | |
| | 100 % gestapelt | Mit dieser Einstellung für die Visualisierungen „Bereich gestapelt“, „Balken gestapelt“ und „Horizontalbalken gestapelt“ wandeln Sie Diagramme in „zu 100 % gestapelte“ Visualisierungen um. <p>Weitere Informationen finden Sie unter [Balken und Balken gestapelt](/help/analyze/analysis-workspace/visualizations/bar.md).</p> |
| **[Histogramm](/help/analyze/analysis-workspace/visualizations/histogram.md)** | | |
| | Anzahl der Buckets | Wählen Sie die Anzahl der Datenbereiche (Buckets) in der Visualisierung aus. Maximal 50 Buckets sind möglich. <p>Weitere Informationen finden Sie unter [Histogramm](/help/analyze/analysis-workspace/visualizations/histogram.md).</p> |
| | Zählmethode | Wählen Sie aus den folgenden Optionen: <ul><li>Treffer</li><li>Besuch</li><li>Besucher</li></ul> <p>Sie können beispielsweise in Verbindung mit Seitenansichten „Seitenansichten pro Besucher“, „Seitenansichten für Besuche“ oder „Seitenansichten pro Treffer“ auswählen. Für Treffer wird in einer Freiformtabelle „Vorkommen“ als Metrik der Y-Achse verwendet.</p> |
| **[Zuordnung](/help/analyze/analysis-workspace/visualizations/map-visualization.md)** | | |
| | Plotting-Dimension | <ul><li>Breitengrad/Längengrad für Mobile</li><li>Geografische Dimension</li></ul> |
| | Zuordnungstyp | <ul><li>Blasen</li><li>Heatmap</li></ul> |
| | Farbschema | Wählen Sie aus Korallentönen, Rottönen, Grüntönen, Blautönen, Heatmap und Positiv/Negativ aus. |
| | Zuordnungsstil | Wählen Sie aus Einfach, Straßen, Hell, Licht, Dunkel und Satellit aus. |
| **[Änderung der Zusammenfassung](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Wert | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>Prozentuale Veränderung</li><li>Rohdifferenz</li></ul> |
| | Prozentsatz | Zeigt Werte in Prozent für die Visualisierungen der Zusammenfassungsänderung an. |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung der Zusammenfassungsänderung. |
| **[Zusammenfassungszahl](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Prozentsatz | Zeigt Werte in Prozent für die Visualisierungen der Zusammenfassungszahl an. |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Visualisierung der Zusammenfassungszahl. |
| | Zusammenfassungswert nach | Wählen Sie aus „Max“, „Min“, „Mittel“, „Median“ und „Summe“ aus. |
| | Wert abkürzen | Im Abschnitt [!UICONTROL **Zusammenfassungszahl**] |
| **[Treemap](/help/analyze/analysis-workspace/visualizations/treemap.md)** | | |
| | Prozentsatz | Zeigt für die Treemap-Visualisierungen Werte in Prozentsätzen an. |
| | Grenzwert für max. Anzahl von Elementen | Verringert die Anzahl der Elemente auf der X-Achse in der Treemap-Visualisierung. Dies kann bei großen Datensätzen nützlich sein. |
| **[Venn](/help/analyze/analysis-workspace/visualizations/venn.md)** | | |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Venn-Visualisierung. |
| **[Streuung](/help/analyze/analysis-workspace/visualizations/scatterplot.md)** | | |
| | Prozentsatz | Zeigt Werte in Prozent für die Streuvisualisierungen an. |
| | Legende sichtbar | Ermöglicht das Ausblenden des detaillierten Legendentextes für die Streuvisualisierung. |
| | Grenzwert für max. Anzahl von Elementen | Verringert die Anzahl der Elemente auf der X-Achse in der Streuvisualisierung. Dies kann bei großen Datensätzen nützlich sein. |
| | Y-Achse bei null verankern | Wenn alle im Diagramm dargestellten Werte deutlich größer als null sind, wird der untere Teil der Y-Achse standardmäßig zu NICHT-NULL gemacht. Wenn Sie dieses Kontrollkästchen aktivieren, wird die Y-Achse zwangsweise auf null gesetzt (und das Diagramm neu gezeichnet). |

## Standardeinstellungen wiederherstellen

Sie können alle Ihre Benutzervoreinstellungen auf die Systemstandardwerte zurücksetzen. Dies wirkt sich nicht auf die Administratoreinstellungen auf der Registerkarte „Unternehmen“ aus.

Diese Aktion kann nicht rückgängig gemacht werden.

1. Wählen Sie in Adobe Analytics [!UICONTROL **Komponenten**] **>** [!UICONTROL **Voreinstellungen**] aus.

   ![Benutzervoreinstellungen](assets/user-preferences.png)

1. Wählen Sie oben rechts **[!UICONTROL Standardeinstellungen wiederherstellen]** aus.

1. Wenn Sie dazu aufgefordert werden, wählen Sie **[!UICONTROL Standardeinstellungen wiederherstellen]** aus.

## [!UICONTROL Dunkles Design]

Wenn Sie einen dunklen Hintergrund für Ihre Adobe Analytics-Benutzeroberfläche bevorzugen, können Sie zu [!UICONTROL Dunkles Design] wechseln.

1. Klicken Sie oben rechts auf das Experience Cloud-Benutzersymbol.

   ![dark-theme](assets/dark-theme.png)

1. Schieben Sie den Umschalter **[!UICONTROL Dunkles Thema]** nach rechts.

