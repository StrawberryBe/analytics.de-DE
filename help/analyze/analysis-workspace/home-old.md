---
description: So sehen Ihre ersten Schritte mit Adobe Analytics aus.
keywords: Analysis Workspace
title: Handbuch „Erste Schritte“
translation-type: tm+mt
source-git-commit: 7fbeac0488fbe9b3d10d7c1242f31250f1c7dc16

---


# Analysis Workspace

Analysis Workspace ist eines der wichtigsten Werkzeuge von Adobe, mit dem Sie umsetzbare datenbasierte Entscheidungen für Ihr Unternehmen treffen können. Mit der am häufigsten verwendeten Visualisierung, der Freiformtabelle, können Sie ganz einfach benutzerspezifische Berichte mit Dimensionen, Metriken, Segmenten und Datumsbereichen erstellen.

## Voraussetzungen

[Senden von Daten an Adobe Analytics mithilfe von Adobe Experience Platform Launch](/help/implement/launch/validate-publish-prod.md): Für die Verwendung von Analysis Workspace ist eine funktionierende Implementierung erforderlich. Vergewissern Sie sich, dass Ihr Unternehmen Daten an Adobe sendet, bevor Sie das Tool verwenden. Andere Implementierungen, wie DTM oder ältere manuelle Implementierungen, können ebenfalls funktionieren.

## Abrufen eines einfachen Rangberichts in Workspace

Rufen Sie einen einfachen Rangbericht mithilfe von Analysis Workspace ab. Ein Rangbericht zeigt eine aggregierte Gesamtansicht jedes Dimensionswerts an, wobei die größten Werte zuerst angezeigt werden. Diese Berichtstypen sind nützlich, um zu sehen, welche Komponenten Ihrer Site am effektivsten sind, z. B. welche Seiten den meisten Traffic erhalten oder welche Produkte am häufigsten verkauft werden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
3. Klicken Sie in der oberen Navigationsleiste auf „Workspace“.
4. Klicken Sie auf die Schaltfläche „Neues Projekt erstellen“.
5. Stellen Sie im modalen Popup sicher, dass „Leeres Projekt“ ausgewählt ist, und klicken Sie dann auf „Erstellen“.
6. Links sehen Sie eine Liste mit Dimensionen, Metriken, Segmenten und Datumsbereichen. Suchen Sie die Dimension „Seiten“ (orange) und ziehen Sie sie auf die Arbeitsfläche mit der Angabe „Dimension hier ablegen“.
7. Beachten Sie, dass ein Bericht mit den wichtigsten Seiten für diesen Monat angezeigt werden kann, wenn die Report Suite über Daten verfügt. Analysis Workspace füllt den Bericht automatisch mit der Metrik [Vorfälle](/help/components/c-variables/c-metrics/metrics-occurrences.md).
8. Suchen Sie die Metrik „Besuche“ (grün) und ziehen Sie sie entweder **über** oder **neben** die Kopfzeile der Metrik „Vorfälle“ (vermeiden Sie, sie über der Metrik zu platzieren). Wenn Sie die Metrik „Besuche“ über Vorfälle ziehen, wird die Metrik in den Berichten ersetzt. Wenn Sie die Metrik „Besuche“ neben „Vorfälle“ ziehen, werden beide Metriken nebeneinander angezeigt.
9. If you&#39;d like to save your project, click *[!UICONTROL Project]>[!UICONTROL Save]*in the upper left menu.

## Abrufen eines einfachen Trend-Berichts in Workspace

Rufen Sie einen einfachen Trend-Bericht mit Analysis Workspace ab. Ein Trend-Bericht zeigt eine Zeitverlaufsansicht der Metriken unter Verwendung des ausgewählten Datumsbereichs an. Diese Berichtstypen sind nützlich, um Trends im Zeitverlauf zu identifizieren, und können zur Messung des Erfolgs oder Misserfolgs von Geschäftsentscheidungen verwendet werden. Sie könnten sich beispielsweise einen Trend-Bericht zu Seitenansichten im Lauf der Zeit ansehen, um festzustellen, ob eine Site-Umgestaltung dazu beigetragen hat, den Traffic zu erhöhen oder zu verringern.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
3. Klicken Sie in der oberen Navigationsleiste auf „Workspace“.
4. Klicken Sie auf die Schaltfläche „Neues Projekt erstellen“.
5. Stellen Sie im modalen Popup sicher, dass „Leeres Projekt“ ausgewählt ist, und klicken Sie dann auf „Erstellen“.
6. Links sehen Sie eine Liste mit Dimensionen, Metriken, Segmenten und Datumsbereichen. Suchen Sie die Dimension „Seitenansichten“ und ziehen Sie sie in den kleinen Bereich der Arbeitsfläche mit der Bezeichnung „Metrik hier ablegen“. Vermeiden Sie es (zumindest für diese Übung), ihn in dem für Dimensionen reservierten Bereich abzulegen.
7. Beachten Sie, dass bei einer Report Suite mit Daten ein einfacher Trend-Bericht für die Seitenansichten im laufenden Monat angezeigt werden sollte. Analysis Workspace hat automatisch den Datumsbereich „Tag“ eingefügt, damit Sie den Trend der Seitenansichten für den aktuellen Monat sehen können.
8. Suchen Sie links in der Liste der Datumsbereichskomponenten den Datumsbereich „Woche“ (violett). Klicken Sie auf den Titel des Datumsbereichs, um alle Komponenten des Datumsbereichs zu erweitern und anzuzeigen, oder verwenden Sie die Suchleiste.
9. Ziehen Sie den Datumsbereich „Woche“ auf die Kopfzeile des Datumsbereichs „Tag“ auf der Arbeitsfläche, um ihn zu ersetzen.
10. Beachten Sie, dass Ihr Trend-Bericht jetzt nach Woche statt nach Tag aggregiert wird.
11. If you&#39;d like to save your project, click *[!UICONTROL Project]>[!UICONTROL Save]*in the upper left menu.

## Mit dem Werkzeug experimentieren

Da Analysis Workspace ein Berichtswerkzeug ist, hat dies keine Auswirkungen auf die Datenerfassung. Komponenten wahllos in ein Projekt zu ziehen, um zu sehen, was funktioniert, hat keine weiteren Folgen. Ziehen Sie verschiedene Kombinationen von Dimensionen und Metriken in Ihr Workspace-Projekt, um zu sehen, welche Möglichkeiten Sie haben.

Wenn Sie versehentlich eine ungültige Komponente in Ihr Workspace-Projekt ziehen oder einen Schritt zurückgehen möchten, drücken Sie Strg+Z (Windows) oder Befehl+Z (Mac), um die letzte durchgeführte Aktion rückgängig zu machen. You can also start with a clean slate by clicking *[!UICONTROL Project]>[!UICONTROL New]*in the upper left menu.

## Fehlerbehebung

**Wenn ich eine Metrik ziehe, wird die Meldung „Ungültige Daten“ angezeigt.**

„Ungültige Daten“ bedeuten, dass Adobe keine Daten mit der Kombination von Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei Metriken, die übereinander gestapelt sind, nicht als Daten zurückgegeben werden, da es nicht möglich ist, zwei Metriken in dieser Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander.

**Wenn ich eine Metrik ziehe, sehe ich keine tatsächlichen Daten - nur Nullen.**

Wenn Sie erfolgreich einen Workspace-Bericht erstellen, aber keine Daten vorhanden sind, können Sie einige Punkte prüfen:

* Überprüfen Sie die Report Suite und stellen Sie sicher, dass sie mit Daten gefüllt ist.
* Wenn Sie ein Segment in Ihrem Bericht verwenden, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.
* Überprüfen Sie den Datumsbereich oben rechts und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.
* Navigieren Sie zu Ihrer Website und überprüfen Sie mit dem Debugger, ob Daten erfasst werden.

## Zusätzliche Ressourcen

* [Versionshinweise zu Analysis Workspace](/help/analyze/analysis-workspace/new-features-in-analysis-workspace.md): Lesen Sie die neuesten Funktionen, die in das Tool eingeführt wurden.
* [Analysis Workspace auf YouTube](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS): In dieser umfangreichen Playlist erfahren Sie, wie Sie die meisten Funktionen in Analysis Workspace verwenden.
* Produktinterne Tipps: Tipps zum aktuellen Tag sowie kurze Videos werden gelegentlich in der unteren rechten Ecke von Analysis Workspace angezeigt. If these tips are dismissed, they can be reached through *[!UICONTROL Help]>[!UICONTROL Tips]*at any time.
* [Analysis Workspace-Community](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/analysis-workspace): Diskutieren Sie mit anderen Benutzern über Analysis Workspace und wählen Sie die Funktionen, die Sie im Tool sehen möchten.
* Blog-Beiträge:
   * [Empowering Organizations with Smarter Analysis](https://blogs.adobe.com/digitalmarketing/analytics/adobe-analytics-fall-2016-release-empowering-organizations-smarter-analysis/) (Englisch)
   * [New Adobe Analytics Capabilities Make Powerful Insights More Accessible](https://blogs.adobe.com/digitalmarketing/analytics/new-adobe-analytics-capabilities-make-powerful-insights-accessible/) (Englisch)
   * [5 Tips to Maximize Your Productivity with Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/5-tips-maximize-productivity-analysis-workspace/) (Englisch)
   * [Faster Insights with Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/faster-insights-with-the-analysis-workspace/) (Englisch)
   * [Why You Should Be Using Analysis Workspace](https://blogs.adobe.com/digitalmarketing/analytics/why-you-should-be-using-analysis-workspace-in-adobe-analytics/) (Englisch)

## Nächste Schritte

Es gibt viele Ressourcen, mit deren Hilfe Sie Analysis Workspace besser verstehen können. Im Folgenden finden Sie einige Grundlagen, die Adobe empfiehlt:

### Für Endbenutzer, die Kenntnisse zur Verwendung von Analysis Workspace erweitern möchten

* [Details zur Workspace-Benutzeroberfläche](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md): Nachdem Sie jetzt einen grundlegenden Bericht erstellt haben, sollten Sie sich mit dem Rest der Oberfläche vertraut machen.
* [Visualisierungen in Workspace](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md): Freiformtabellen sind nur eine Art der Visualisierung in Analysis Workspace. Erfahren Sie, wie Sie andere Visualisierungen wie Liniendiagramme, Balkendiagramme und geografische Karten verwenden.
* [Dimensionen in Workspace](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md): Erfahren Sie mehr über Dimensionen und ihre Verwendung in mehr als nur Rangberichten.
* [Metriken in Workspace](/help/analyze/analysis-workspace/components/apply-create-metrics.md): Erfahren Sie mehr darüber, was Metriken sind und wie sie in anderen Teilen von Freiformtabellen verwendet werden.
* [Einführung in die Segmentierung](/help/analyze/analysis-workspace/components/t-freeform-project-segment.md): Erfahren Sie, was Segmente sind, und erstellen Sie einen einfachen Bericht mit einem Segment.
* [Datumsbereiche in Workspace](/help/analyze/analysis-workspace/components/calendar-date-ranges/calendar.md): Erfahren Sie mehr über relative und rollierende Daten und verwenden Sie sie in Workspace-Projekten.
* Freigeben von Projekten in Workspace: Zeigen Sie Ihrem Kollegen das fantastische Workspace-Projekt, das Sie erstellt haben.
* [(Erweitert) Bedienfelder in Workspace](/help/analyze/analysis-workspace/c-panels/panels.md): Verwenden Sie erweiterte Funktionen in Workspace, wie Attribution und Segmentvergleich.

### Analysten und Administratoren, die die Qualität von Workspace in ihrem Unternehmen verbessern möchten

* [Berechtigungen in Analysis Workspace](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/admin-getting-started.html): Weisen Sie über Adobe Admin Console Benutzerberechtigungen für Workspace zu.
* [Vorlagen in Workspace](/help/analyze/analysis-workspace/build-workspace-project/starter-projects.md): Erstellen Sie Vorlagen, damit Ihre Kollegen mit einem auf ihre Bedürfnisse zugeschnittenen Projektraum beginnen können.
* [Workspace-Kuratierung](/help/analyze/analysis-workspace/curate-share/curate.md): Erstellen Sie ein Projekt, das die verfügbaren Komponenten einschränkt, damit Workspace für diejenigen, die mit dem Tool weniger vertraut sind, leichter zugänglich ist.
