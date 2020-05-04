---
description: Häufig gestellte Fragen zum Arbeitsbereich
title: Häufig gestellte Fragen und Fehlerbehebung in Workspace
translation-type: tm+mt
source-git-commit: 7fbeac0488fbe9b3d10d7c1242f31250f1c7dc16

---


# Häufig gestellte Fragen

| Frage | Antwort |
|--- |--- |
| Was sind die Voraussetzungen für die Verwendung von Analyse Workspace? | [Senden von Daten an Adobe Analytics mithilfe von Adobe Experience Platform Launch](/help/implement/launch/validate-publish-prod.md): Für die Verwendung von Analysis Workspace ist eine funktionierende Implementierung erforderlich. Vergewissern Sie sich, dass Ihr Unternehmen Daten an Adobe sendet, bevor Sie das Tool verwenden. Andere Implementierungen, wie DTM oder ältere manuelle Implementierungen, können ebenfalls funktionieren. |
| Welche Administrations- und Zugriffsanforderungen gibt es für Analysis Workspace? | Siehe [ Administrationsanforderungen](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Wirkt sich die Verwendung von Analyse Workspace auf die Datenerfassung aus? | Da Analysis Workspace ein Berichtswerkzeug ist, hat dies keine Auswirkungen auf die Datenerfassung. Komponenten wahllos in ein Projekt zu ziehen, um zu sehen, was funktioniert, hat keine weiteren Folgen. Ziehen Sie verschiedene Kombinationen von Dimensionen und Metriken in Ihr Workspace-Projekt, um zu sehen, welche Möglichkeiten Sie haben. Wenn Sie versehentlich eine ungültige Komponente in Ihr Workspace-Projekt ziehen oder einen Schritt zurückgehen möchten, drücken Sie Strg+Z (Windows) oder Befehl+Z (Mac), um die letzte durchgeführte Aktion rückgängig zu machen. You can also start with a clean slate by clicking *[!UICONTROL Project]>[!UICONTROL New]*in the upper left menu. |
| Wie viele Report Suites können in einem Projekt des Analysis Workspace angezeigt werden? | You can now create projects in Analysis Workspace with data from more [multiple report suites](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html). |
| Wie wird der Analysis Workspace implementiert? | Es ist keine spezielle Implementierung erforderlich. Der Analysis Workspace steht allen Unternehmen mit Analytics Standard oder Premium zur Verfügung. Es gelten jedoch die Standardberechtigungen für Inhalte (z. B. Report Suites und Projektkomponenten) und für die Kuratierung und Freigabe von Projekten. Weitere Informationen finden Sie unter [Administrations- und Zugriffsanforderungen](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md). |
| Ändert der Analysis Workspace die vorkonfigurierten Berichte in Adobe Analytics? | Nein. Da es sich hier um eine separate Umgebung handelt, ergeben sich keine Änderungen an Ihren vorhandenen oder vorkonfigurierten Berichten in Adobe Analytics. Sie können mit Analysis Workspace weiterhin Standardberichte aus Reports &amp; Analytics sowie vom Report Builder nutzen. |
| Kann ich den Analysis Workspace für Data Warehouse verwenden? | Der Analysis Workspace wird für den Export von Massendaten nicht empfohlen. Es handelt sich um einen VisualisierungsWorkspace für das Erstellen dashboardartiger Analyseprojekte. |
| Wie kann ich die Leistung von Analysis Workspace optimieren? | Siehe [Leistungsoptimierung](/help/analyze/analysis-workspace/workspace-faq/optimizing-performance.md). |
| Wie unterscheiden sich die Funktionen von Analysis Workspace von den Funktionen von Ad Hoc Analysis? | Siehe [Analysis Workspace im Vergleich mit Ad Hoc Analysis](/help/analyze/analysis-workspace/workspace-faq/adhocanalysis-vs-analysisworkspace.md). |

## Fehlerbehebung

**Wenn ich eine Metrik ziehe, wird die Meldung „Ungültige Daten“ angezeigt.**

„Ungültige Daten“ bedeuten, dass Adobe keine Daten mit der Kombination von Dimensionen und Metriken zurückgeben kann, die im Bericht verwendet werden. Beispielsweise können zwei Metriken, die übereinander gestapelt sind, nicht als Daten zurückgegeben werden, da es nicht möglich ist, zwei Metriken in dieser Weise anzuzeigen. Platzieren Sie die Metriken stattdessen nebeneinander.

**Wenn ich eine Metrik ziehe, sehe ich keine tatsächlichen Daten - nur Nullen.**

Wenn Sie erfolgreich einen Arbeitsbereichbericht erstellt haben, aber keine Daten vorhanden sind, können Sie Folgendes überprüfen:

* Dublette überprüft die Report Suite und stellt sicher, dass sie mit Daten gefüllt ist.
* Wenn Sie ein Segment in Ihrem Bericht angewendet haben, stimmen die Segmentkriterien möglicherweise nicht mit den Daten überein. Versuchen Sie, das Segment zu entfernen oder die Segmentdefinition anzupassen.
* Überprüfen Sie den Datumsbereich in der oberen rechten Ecke und stellen Sie sicher, dass er auf einen erwarteten Wert eingestellt ist.
* Navigate to your website and use the [Debugger](https://docs.adobe.com/content/help/de-DE/debugger/using/experience-cloud-debugger.html) to validate that data is being collected.