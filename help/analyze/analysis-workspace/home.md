---
description: Erste Schritte mit Adobe Analytics
keywords: Analysis Workspace
solution: Analytics
title: Handbuch "Erste Schritte"
topic: Reports and analytics
uuid: 851feadb-5e30-45ab-9f66-02bdf844fa54
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analysis Workspace

Der Arbeitsbereich für Analysen ist eines der wichtigsten Werkzeuge von Adobe, mit denen Sie umsetzbare datenbasierte Entscheidungen für Ihr Unternehmen treffen können. Mit der am häufigsten verwendeten Visualisierung, der Freiformtabelle, können Sie ganz einfach benutzerspezifische Berichte mit Dimensionen, Metriken, Segmenten und Datumsbereichen erstellen.

## Voraussetzungen

[Senden von Daten an Adobe Analytics mithilfe von Adobe Experience Platform Launch](/help/implement/implement-with-launch/validate-publish-prod.md): Für die Verwendung des Analysis Workspace ist eine funktionierende Implementierung erforderlich. Vergewissern Sie sich, dass Ihr Unternehmen Daten an Adobe sendet, bevor Sie das Tool verwenden. Andere Implementierungen, wie DTM oder ältere manuelle Implementierungen, können ebenfalls funktionieren.

## Ziehen eines Berichts mit einer einfachen Rangfolge in Workspace

Ziehen Sie einen Bericht mit einer einfachen Rangfolge mithilfe des Analysis Workspace. Ein Rangbericht zeigt eine aggregierte Gesamtansicht jedes Dimensionswerts an, wobei die größten Werte zuerst angezeigt werden. Diese Berichtstypen sind nützlich, um zu sehen, welche Komponenten Ihrer Site am effektivsten sind, z. B. welche Seiten den meisten Traffic erhalten oder welche Produkte am meisten verkaufen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
3. Klicken Sie in der oberen Navigationsleiste auf Workspace.
4. Klicken Sie auf die Schaltfläche "Neues Projekt erstellen".
5. Stellen Sie im modalen Popup sicher, dass 'Leeres Projekt' ausgewählt ist, und klicken Sie dann auf Erstellen.
6. Links sehen Sie eine Liste mit Dimensionen, Metriken, Segmenten und Datumsbereichen. Suchen Sie die Dimension "Seiten"(farbig orange) und ziehen Sie sie auf die Arbeitsfläche mit der Angabe "Dimension hier ablegen".
7. Beachten Sie, dass ein Bericht mit den wichtigsten Seiten für diesen Monat angezeigt werden kann, wenn die Report Suite über Daten verfügt. Analysis Workspace füllt den Bericht automatisch mit der Metrik [Vorfälle](/help/components/c-variables/c-metrics/metrics-occurrences.md) .
8. Suchen Sie die Metrik "Besuche"(farbig grün) und ziehen Sie sie entweder **über** oder **neben** die Kopfzeile der Metrik "Vorfälle"(vermeiden Sie, sie über der Metrik zu platzieren). Wenn Sie die Metrik "Besuche"über Vorfälle ziehen, wird die Metrik in den Berichten ersetzt. Wenn Sie die Metrik "Besuche"neben "Vorfälle"ziehen, werden beide Metriken nebeneinander angezeigt.
9. Wenn Sie Ihr Projekt speichern möchten, klicken Sie im Menü oben links auf *[!UICONTROL Projekt]&gt;[!UICONTROL Speichern]* .

## Ziehen eines grundlegenden Trendberichts in Workspace

Ziehen Sie einen grundlegenden Trendbericht mit Analysis Workspace. Ein Trendbericht zeigt eine Zeitverlaufsansicht der Metriken unter Verwendung des ausgewählten Datumsbereichs an. Diese Berichtstypen sind nützlich, um Trends im Zeitverlauf zu identifizieren, und können zur Messung des Erfolgs oder Misserfolgs von Geschäftsentscheidungen verwendet werden. Sie könnten sich beispielsweise einen Seitenansichtsbericht mit der Zeit ansehen, um festzustellen, ob eine Site-Umgestaltung dazu beigetragen hat, den Traffic zu erhöhen oder zu verringern.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
3. Klicken Sie in der oberen Navigationsleiste auf Workspace.
4. Klicken Sie auf die Schaltfläche "Neues Projekt erstellen".
5. Stellen Sie im modalen Popup sicher, dass 'Leeres Projekt' ausgewählt ist, und klicken Sie dann auf Erstellen.
6. Links sehen Sie eine Liste mit Dimensionen, Metriken, Segmenten und Datumsbereichen. Suchen Sie die Dimension "Seitenansichten"und ziehen Sie sie in den kleinen Bereich der Arbeitsfläche mit der Bezeichnung "Metrik hier ablegen". Vermeiden Sie es, ihn in dem für Dimensionen reservierten Bereich (zumindest für diese Übung) abzulegen.
7. Beachten Sie, dass bei einer Report Suite mit Daten ein einfacher Seitenansichtsbericht im Verlauf des aktuellen Monats als Trend angezeigt werden sollte. Der Analysis Workspace hat automatisch den Datumsbereich "Tag"eingefügt, damit Sie den Trend der Seitenansichten für den aktuellen Monat sehen können.
8. Suchen Sie links in der Liste der Datumsbereichskomponenten den Datumsbereich "Woche"(farbig violett). Klicken Sie auf den Titel des Datumsbereichs, um alle Komponenten des Datumsbereichs zu erweitern und anzuzeigen, oder verwenden Sie die Suchleiste.
9. Ziehen Sie den Datumsbereich "Woche"auf die Kopfzeile des Datumsbereichs "Tag"auf der Arbeitsfläche, um ihn zu ersetzen.
10. Beachten Sie, dass Ihr Trendbericht jetzt nach Woche statt nach Tag aggregiert wird.
11. Wenn Sie Ihr Projekt speichern möchten, klicken Sie im Menü oben links auf *[!UICONTROL Projekt]&gt;[!UICONTROL Speichern]* .

## Experimentieren Sie mit dem Werkzeug

Da der Arbeitsbereich für Analysen ein Berichtswerkzeug ist, hat dies keine Auswirkungen auf die Datenerfassung. Es gibt keine Auswirkungen darauf, Komponenten wahllos in ein Projekt zu ziehen, um zu sehen, was funktioniert. Ziehen Sie verschiedene Kombinationen von Dimensionen und Metriken in Ihr Arbeitsbereichsprojekt, um zu sehen, was für Sie verfügbar ist.

Wenn Sie versehentlich eine ungültige Komponente in Ihr Workspace-Projekt ziehen oder einen Schritt zurückgehen möchten, drücken Sie Strg+Z (Windows) oder Cmd+Z (Mac), um die letzte durchgeführte Aktion rückgängig zu machen. Sie können auch mit einem sauberen Schiefer beginnen, indem Sie im Menü oben links auf *[!UICONTROL Projekt]&gt;[!UICONTROL Neu]* klicken.

## Fehlerbehebung

**Wenn ich eine Metrik herumziehe, steht "Ungültige Daten".**

Ungültige Daten bedeuten, dass Adobe keine Daten mit der Kombination von Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei Metriken, die übereinander gestapelt sind, nicht als Daten zurückgegeben werden, da es nicht möglich ist, zwei Metriken in dieser Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander.

**Wenn ich eine Metrik herumziehe, sehe ich keine tatsächlichen Daten - nur Nullen.**

Wenn Sie erfolgreich einen Arbeitsbereichbericht erstellen, aber keine Daten vorhanden sind, können Sie einige Punkte prüfen:

* Überprüfen Sie die Report Suite, und stellen Sie sicher, dass sie mit Daten gefüllt ist.
* Wenn Sie ein Segment in Ihrem Bericht verwenden, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.
* Überprüfen Sie den Datumsbereich oben rechts und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.
* Navigieren Sie zu Ihrer Website und überprüfen Sie mit dem Debugger, ob Daten erfasst werden.

## Zusätzliche Ressourcen

* [Versionshinweise](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md)zum Analysis Workspace: Lesen Sie die neuesten Funktionen, die in das Tool eingeführt wurden.
* [Analysis Workspace auf YouTube](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS): In dieser umfangreichen Wiedergabeliste erfahren Sie, wie Sie die meisten Funktionen in Analysis Workspace verwenden.
* Tipps zum In-Produkt: Tipps zum aktuellen Tag sowie kurze Videos werden gelegentlich in der unteren rechten Ecke des Analysis Workspace angezeigt. Wenn diese Tipps nicht mehr angezeigt werden, können sie jederzeit über *[!UICONTROL Hilfe]&gt;[!UICONTROL Tipps]* erreicht werden.
* [Analysis Workspace-Community](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace): Diskutieren Sie mit anderen Benutzern über den Analysis Workspace und wählen Sie die Funktionen, die Sie im Tool sehen möchten.
* Blog-Beiträge:
   * [Organisationen mit Smarter Analysis fördern](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/)
   * [Neue Funktionen von Adobe Analytics machen leistungsstarke Insights leichter zugänglich](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/)
   * [5 Tipps zur Optimierung Ihrer Produktivität mit Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/)
   * [Schnellere Einblicke mit dem Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/)
   * [Deshalb sollten Sie den Analysis Workspace verwenden](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/)

## Nächste Schritte

Es gibt viele Anleitungen, wie Sie den Analysis Workspace besser verstehen können. Im Folgenden finden Sie einige Grundlagen, die Adobe empfiehlt:

### Für Endbenutzer, die Kenntnisse zur Verwendung des Analysis Workspace erweitern möchten

* [Details zur Workspace-Benutzeroberfläche](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md): Nachdem Sie jetzt einen grundlegenden Bericht erstellt haben, sollten Sie sich mit dem Rest der Oberfläche vertraut machen.
* [Visualisierungen in Workspace](visualizations/freeform-analysis-visualizations.md): Freiformtabellen sind nur eine Art der Visualisierung im Analysis Workspace. Erfahren Sie, wie Sie andere Visualisierungen wie Liniendiagramme, Balkendiagramme und Geo-Karten verwenden.
* [Dimensionen in Workspace](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md): Erfahren Sie mehr über Dimensionen und ihre Verwendung in mehr als nur Rangberichten.
* [Metriken in Workspace](/help/analyze/analysis-workspace/components/apply-create-metrics.md): Erfahren Sie mehr darüber, was Metriken sind und wie sie in anderen Teilen von Freiformtabellen verwendet werden.
* [Einführung in die Segmentierung](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md): Erfahren Sie, was Segmente sind, und ziehen Sie einen einfachen Bericht mit einem Segment.
* [Datumsbereiche in Workspace](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md): Erfahren Sie mehr über relative und rollierende Daten und verwenden Sie sie in Workspace-Projekten.
* Freigeben von Projekten in Workspace: Zeigen Sie Ihrem Kollegen das fantastische Workspace-Projekt, das Sie erstellt haben.
* [(Erweitert) Bedienfelder in Workspace](c-panels/panels.md): Verwenden Sie erweiterte Funktionen in Workspace, wie Zuordnung und Segmentvergleich.

### Für Analysten und Administratoren, die die Qualität der Arbeitsfläche in ihrem Unternehmen verbessern möchten

* [Berechtigungen](https://marketing.adobe.com/resources/help/en_US/mcloud/admin_getting_started.html)im Arbeitsbereich für Analysen: Weisen Sie Workspace über die Adobe Admin Console Benutzerberechtigungen zu.
* [Erstellen Sie ein Lösungsdesigndokument](/help/implement/prepare/solution-design.md): Beginnen Sie mit der Planung, wie Ihr Unternehmen zusätzliche Dimensionen oder Metriken zu Ihrer Site sammelt.
* [Vorlagen in Workspace](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md): Erstellen Sie Vorlagen, damit Ihre Kollegen mit einem auf ihre Bedürfnisse zugeschnittenen Projektraum beginnen können.
* [Arbeitsflächenkuratierung](curate-share/curate.md): Erstellen Sie ein Projekt, das die verfügbaren Komponenten einschränkt, damit der Arbeitsbereich für diejenigen, die mit dem Tool weniger vertraut sind, leichter zugänglich ist.
