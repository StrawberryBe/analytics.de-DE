---
description: Erste Schritte mit Adobe Analytics.
keywords: Analysis Workspace
seo-description: Erste Schritte mit Adobe Analytics.
seo-title: Handbuch "Erste Schritte «
solution: Analytics
title: Handbuch "Erste Schritte «
topic: Reports and Analytics
uuid: 851 feadb -5 e 30-45 ab -9 f 66-02 bdf 844 fa 54
translation-type: tm+mt
source-git-commit: a0158b98089c044091f61796d782604865aa4eba

---


# Analysis Workspace

Der Analysis Workspace ist eine der Adobe-Leistungswerkzeuge, mit deren Hilfe Sie praktische datenbasierte Entscheidungen für Ihr Unternehmen treffen können. Die gängigste Visualisierung, die Freiform-Tabelle, ermöglicht Ihnen, benutzerspezifische Berichte mithilfe von Dimensionen, Metriken, Segmenten und Datumsbereichen zu erstellen.

## Voraussetzungen

[Daten mit Adobe Experience Platform Launch an Adobe Analytics senden](../../implement/implement-with-launch/validate-publish-prod.md): Für den Analysis Workspace ist eine funktionierende Implementierung erforderlich. Stellen Sie sicher, dass Ihr Unternehmen Daten an Adobe sendet, bevor Sie das Tool verwenden. Andere Implementierungen wie DTM oder ältere manuelle Implementierungen können ebenfalls funktionieren.

## Einen einfachen Rangbericht in Workspace abrufen

Ziehen Sie einen einfachen Rangbericht mit Analysis Workspace. Ein Rangbericht zeigt eine aggregierte Gesamtansicht der einzelnen Dimensionswerte an, die zuerst die größten Werte anzeigt. Diese Berichtstypen sind nützlich, um zu sehen, welche Komponenten Ihrer Site am effektivsten sind, z. B. welche Seiten den meisten Traffic erhalten oder welche Produkte am meisten verkauft werden.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
2. Klicken Sie oben rechts auf das 9-quadratische Symbol und dann auf das farbige Analytics-Logo.
3. Klicken Sie in der oberen Navigationsleiste auf Arbeitsbereich.
4. Klicken Sie auf die Schaltfläche "Neues Projekt erstellen" .
5. Stellen Sie im modalen Popup sicher, dass "Leeres Projekt" ausgewählt ist, und klicken Sie dann auf Erstellen.
6. Auf der linken Seite sollte eine Liste von Dimensionen, Metriken, Segmenten und Datumsbereichen angezeigt werden. Suchen Sie die Dimension "Seiten" (orange) und ziehen Sie sie auf die Arbeitsfläche, in der sie" Dimension hier ablegen" lautet.
7. Beachten Sie, dass, wenn die Report Suite Daten enthält, ein Bericht angezeigt wird, der die Top-Seiten für diesen Monat anzeigt. Analysis Workspace automatically populated the report with the [Occurrences](../../components/c-variables/c-metrics/metrics-occurrences.md) metric.
8. Locate the Visits metric (colored green), and drag it either **over** or **next to** the Occurrences metric header (avoid placing it above the metric). Wenn Sie die Besuchsmetrik auf Vorfälle ziehen, wird die Metrik in den Berichten ersetzt. Wenn Sie die Metrik "Besuche" neben" Vorfälle" ziehen, werden beide Metriken nebeneinander angezeigt.
9. If you'd like to save your project, click *[!UICONTROL Project]&gt;[!UICONTROL Save]* in the upper left menu.

## Einen grundlegenden Trendbericht in Workspace abrufen

Ziehen Sie einen grundlegenden Trendbericht mit Analysis Workspace. Ein Trendbericht zeigt eine Zeitverlaufsansicht von Metriken mit dem ausgewählten Datumsbereich an. Diese Berichtstypen sind hilfreich, um Trends im Laufe der Zeit zu identifizieren, und können verwendet werden, um Erfolg oder Fehlschlagen von Geschäftsentscheidungen zu messen. Sie könnten sich beispielsweise einen Trendbericht für Seitenansichten im Verlauf der Zeit ansehen, um zu sehen, ob ein Site-Design den Traffic steigern oder verringern konnte.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
2. Klicken Sie oben rechts auf das 9-quadratische Symbol und dann auf das farbige Analytics-Logo.
3. Klicken Sie in der oberen Navigationsleiste auf Arbeitsbereich.
4. Klicken Sie auf die Schaltfläche "Neues Projekt erstellen" .
5. Stellen Sie im modalen Popup sicher, dass "Leeres Projekt" ausgewählt ist, und klicken Sie dann auf Erstellen.
6. Auf der linken Seite sollte eine Liste von Dimensionen, Metriken, Segmenten und Datumsbereichen angezeigt werden. Suchen Sie die Dimension "Seitenansichten" und ziehen Sie sie in den kleinen Bereich auf der Arbeitsfläche mit der Bezeichnung" Metrik hier ablegen" . Vermeiden Sie es, es in den für Dimensionen reservierten Platz zu setzen (zumindest für diese Übung).
7. Hinweis: Wenn die Report Suite Daten enthält, sollte ein Trendbericht für Seitenansichten im aktuellen Monat verfolgt werden. Der Analysis Workspace wird automatisch im Datumsbereich des Tages geladen, sodass Sie den Trend der Seitenansichten für den aktuellen Monat sehen können.
8. Suchen Sie den Datumsbereich der Woche (farbig farbig) in der Liste der Datumsbereichskomponenten auf der linken Seite. Klicken Sie auf den Titel des Datumsbereichs, um alle Komponenten des Datumsbereiches zu erweitern und anzuzeigen, oder verwenden Sie die Suchleiste.
9. Ziehen Sie den Datumsbereich "Woche" auf die Kopfzeile des Tages-Datumsbereichs auf der Arbeitsfläche, um ihn zu ersetzen.
10. Beachten Sie, dass Ihr Trendbericht nun nach Wochentag aggregiert wird.
11. If you'd like to save your project, click *[!UICONTROL Project]&gt;[!UICONTROL Save]* in the upper left menu.

## Experimentieren Sie mit dem Tool

Da Analysis Workspace ein Berichterstellungswerkzeug ist, hat es keine Auswirkung auf die Datenerfassung. Es gibt keine Auswirkungen auf die inkrementelle Ziehen von Komponenten in ein Projekt, um zu sehen, was funktioniert. Ziehen Sie verschiedene Kombinationen von Dimensionen und Metriken in Ihr Arbeitsflächenprojekt, um zu sehen, was für Sie zur Verfügung steht.

Wenn Sie versehentlich eine ungültige Komponente in Ihr Arbeitsflächenprojekt ziehen oder einen Schritt zurückgehen möchten, drücken Sie Strg + Z (Windows) oder Cmd + Z (Mac), um die letzte durchgeführte Aktion rückgängig zu machen. You can also start with a clean slate by clicking *[!UICONTROL Project]&gt;[!UICONTROL New]* in the upper left menu.

## Fehlerbehebung 

**Wenn ich eine Metrik ziehe, lautet sie "Ungültige Daten" .**

Ungültige Daten bedeutet, dass Adobe keine Daten mit der Kombination aus Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei übereinander übereinander gestapelte Metriken nicht als Daten zurückgegeben werden, da es keine Möglichkeit gibt, zwei Metriken auf diese Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander.

**Wenn ich eine Metrik ziehe, sehe ich keine tatsächlichen Daten, sondern nur Nullen.**

Wenn Sie einen Arbeitsbereichsbericht erfolgreich erstellen, aber keine Daten vorhanden sind, können Sie Folgendes prüfen:

* Überprüfen Sie die Report Suite und stellen Sie sicher, dass sie mit Daten gefüllt ist.
* Wenn Sie ein Segment in Ihrem Bericht verwenden, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.
* Überprüfen Sie den Datumsbereich oben rechts und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.
* Navigieren Sie zu Ihrer Website und verwenden Sie den Debugger, um zu überprüfen, ob die Daten erfasst werden.

## Zusätzliche Ressourcen

* [Versionshinweise zu Analysis Workspace](../../analyze/analysis-workspace/new-features-in-analysis-workspace.md): Lesen Sie die neuen Funktionen des Tools.
* [Analysis Workspace auf youtube](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS): Hier erfahren Sie, wie Sie mit dieser umfangreichen Wiedergabeliste die meisten Funktionen in Analysis Workspace verwenden.
* In-Produkt-Tipps: Tipps des Tages sowie kurze Videos werden gelegentlich in der rechten unteren Ecke des Analysis Workspace angezeigt. If these tips are dismissed, they can be reached through *[!UICONTROL Help]&gt;[!UICONTROL Tips]* at any time.
* [Analysis Workspace-Community](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace): Besprechen Sie den Analysis Workspace mit Kollegen und stimmen Sie über Funktionen zu, die Sie im Tool sehen möchten.
* Blog-Posts:
   * [Organisationen mit Smarter Analysis fördern](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [Neue Adobe Analytics Capabilities Make Powerful Insights More Accessible](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/)
   * [5 Tipps zur Maximierung Ihrer Produktivität mit Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/)
   * [Schnellere Einblicke mit dem Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/)
   * [Deshalb sollten Sie den Analysis Workspace verwenden](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)

## Nächste Schritte

Es gibt viele Anweisungen, um Ihr Verständnis des Analysis Workspace zu vertiefen. Hier sind einige Grundlagen von Adobe:

### Endbenutzer möchten wissen, wie Sie den Analysis Workspace verwenden

* [Details zur Workspace-Benutzeroberfläche](../../analyze/analysis-workspace/build-workspace-project/t-freeform-project.md): Nachdem Sie einen grundlegenden Bericht erstellt haben, sollten Sie sich mit dem Rest der Oberfläche vertraut machen.
* [Visualisierungen in Workspace](visualizations/freeform-analysis-visualizations.md): Freiformtabellen sind nur eine Art Visualisierung im Analysis Workspace. Hier erfahren Sie, wie Sie andere Visualisierungen wie Liniendiagramme, Balkendiagramme und Geo-Maps verwenden.
* [Dimensionen in Workspace](../../analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md): Erfahren Sie mehr über die Dimensionen und deren Verwendung in mehr als nur Rangberichten.
* [Metriken in Workspace](../../analyze/analysis-workspace/components/apply-create-metrics.md): Erfahren Sie mehr darüber, welche Metriken und wie sie in anderen Freiformtabellen verwendet werden sollen.
* [Einführung in die Segmentierung](../../analyze/analysis-workspace/components/t-freeform-project-segment.md): Erfahren Sie mehr über die Segmente und ziehen Sie einen einfachen Bericht mit einem Segment.
* [Datumsbereiche in Workspace](../../analyze/analysis-workspace/components/calendar-date-ranges/calendar.md): Lernen Sie die relativen und rollierenden Daten kennen und verwenden Sie sie in Workspace-Projekten.
* Freigeben von Projekten in Workspace: Zeigen Sie Ihren Kollegen das beeindruckende Workspace-Projekt an, das Sie erstellt haben.
* [(Erweitert) Bedienfelder in Workspace](c-panels/panels.md): Verwenden Sie erweiterte Funktionen in Workspace, z. B. Zuordnung und Segmentvergleich.

### Analysten und Administratoren möchten die Qualität von Arbeitsbereichen in ihrem Unternehmen verbessern

* [Berechtigungen für Analysis Workspace](https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html): Weisen Sie Benutzern über die Adobe Admin-Konsole Berechtigungen zu.
* [Erstellen Sie ein Dokument für das Lösungsdesign](../../implement/prepare/solution-design.md): Beginnen Sie mit der Planung, wie Ihre Organisation zusätzliche Dimensionen oder Metriken sammelt, die für Ihre Site spezifisch sind.
* [Vorlagen in Workspace](../../analyze/analysis-workspace/build-workspace-project/starter-projects.md): Erstellen Sie Vorlagen, damit Ihre Kollegen mit einem Projektbereich beginnen können, der auf ihren Bedarf zugeschnitten ist.
* [Workspace-Kuration](curate-share/curate.md): Erstellen Sie ein Projekt, das die verfügbaren Komponenten begrenzt, sodass die Arbeitsfläche für weniger bekannte Benutzer besser zugänglich ist.