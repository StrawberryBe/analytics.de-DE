---
description: Im Kalender können Sie Daten und Datumsbereiche festlegen oder eine Voreinstellung auswählen.
title: Übersicht über Kalender und Datumsbereiche
feature: Calendar
role: User, Admin
exl-id: fbf4bc18-65ba-4e39-96c1-4c41a8e3baa9
source-git-commit: feb6942a54f61850ce11e08008b5694c53436e6d
workflow-type: ht
source-wordcount: '862'
ht-degree: 100%

---

# Übersicht über Kalender und Datumsbereiche

Im Kalender können Sie Daten und Datumsbereiche festlegen oder eine Voreinstellung auswählen.

Im Folgenden finden Sie ein Video zur Verwendung von Datumsbereichen und Kalendern in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/23973/?quality=12)

Wenn Sie im Kalender etwas auswählen, bezieht sich diese Auswahl auf das jeweilige Panel. Sie haben jedoch die Möglichkeit, die Auswahl auf sämtliche Panels anzuwenden. Wenn Sie in Workspace auf einen Datumsbereich klicken, zeigt die Benutzeroberfläche den aktuellen Kalendermonat und den vorherigen Kalendermonat an. Sie können diese beiden Kalender anpassen, indem Sie auf die Rechts- und Linkspfeile in den jeweiligen oberen Ecken klicken.

![Kalender](assets/aw_calendar2.png){width="60%"}

## Auswählen und Anwenden von Datumsbereichen {#select-apply}

Beim ersten Klick auf einen Kalender wird die Auswahl eines Datumsbereichs begonnen. Mit dem zweiten Klick wird die Auswahl des Datumsbereichs beendet und hervorgehoben. Wenn die `Shift` Taste gedrückt gehalten wird (oder ein Rechtsklick verwendet wird), wird der entsprechende Bereich an den derzeit ausgewählten Bereich angehängt.

Sie können Datums- (und Zeitdimensionen) mittels Drag-and-Drop in einem Workspace-Projekt ablegen. Sie können spezifische Tage, Wochen, Monate, Jahre oder ein rollierendes Datum auswählen.

[Verwendung von Datumsbereichen und Kalender in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/using-dates-in-analysis-workspace.html?lang=de) (4:07)

| Einstellung | Beschreibung |
|--- |--- |
| Ausgewählte Tage | Ausgewählte Tage/Wochen/Monate/Jahre |
| Erstellen von Datumsbereichskomponenten relativ zum Bedienfeld-Kalender | Die auf dem Datumsbereich des Bedienfelds basierenden Datumsangaben bleiben gleich. |
| Rollierende Daten verwenden | Mithilfe rollierender Daten können Sie einen dynamischen Bericht generieren, der zum Zeitpunkt seiner Ausführung einen bestimmten Zeitraum voraus oder zurück umfasst. Wenn Sie zum Beispiel einen Bericht zu allen Bestellungen haben möchten, die im letzten Monat aufgegeben wurden (wobei sich „Letzter Monat“ auf das Feld „Erstellungsdatum“ bezieht), und diesen Bericht dann im Dezember ausführen, würden Ihnen alle Bestellungen angezeigt, die im November aufgegeben wurden. Führen Sie den gleichen Bericht im Januar aus, werden Ihnen die Bestellungen aus dem Dezember angezeigt.<ul><li>**[!UICONTROL Datumsvorschau]**: Gibt an, welchen Zeitraum der rollierende Kalender umfasst.</li><li>**[!UICONTROL Start]**: Sie können zwischen den folgenden Optionen wählen: „Aktueller Tag“, „Aktuelle Woche“, „Aktueller Monat“, „Aktuelles Quartal“ und „Aktuelles Jahr“.</li><li>**[!UICONTROL Ende]**: Sie können zwischen den folgenden Optionen wählen: „Aktueller Tag“, „Aktuelle Woche“, „Aktueller Monat“, „Aktuelles Quartal“ und „Aktuelles Jahr“.</li></ul>Ein Beispiel finden Sie unter [Benutzerdefinierte Datumsbereiche](/help/analyze/analysis-workspace/components/calendar-date-ranges/custom-date-ranges.md). <br>Standardmäßig ausgewählt. |
| Datumsbereich | Hier können Sie einen voreingestellten Datumsbereich auswählen. Der Standardwert lautet „Letzte 30 Tage“. **[!UICONTROL Diese Woche/Monat/Quartal/Jahr (außer heute)]** ermöglicht Ihnen, aus Datumsbereichen auszuwählen, die keine Daten von heute enthalten. |
| In alle Bedienfelder übernehmen | Hiermit können Sie den ausgewählten Datumsbereich nicht nur für das aktuelle Bedienfeld, sondern für alle Bedienfelder des Projekts ändern. |
| Übernehmen | Hiermit wird der Datumsbereich nur in diesem Bedienfeld übernommen. |

## Über relative Datumsbereiche des Bedienfelds {#relative-panel-dates}

Wenn Sie in Workspace arbeiten, können Sie die Komponenten der Datumsbereiche relativ zum Bedienfeldkalender festlegen.
Drei gängige Anwendungsfälle, in denen relative Datumsangaben im Bedienfeld verwendet werden, sind Combo-Diagramme, Zusammenfassungen der Schlüsselmetriken und Datumsbereiche in Freiformtabellen.

So verwenden Sie relative Datumsbereiche im Bedienfeld

1. Wählen Sie die Registerkarte **Arbeitsbereich** aus.
1. Wählen Sie **Leeres Projekt** aus.
1. Fügen Sie Dimensionen, Metriken und Segmente über die linke Leiste hinzu.
1. Klicken Sie auf das Feld für den Datumsbereich des Bedienfelds, um in die Einstellung für den relativen Datumsbereich des Bedienfelds umzuschalten.
1. Wählen Sie **Erstellen von Datumsbereichskomponenten relativ zum Bedienfeldkalender** aus.
   * Wählen Sie die Option aus, damit sich die Komponenten für den Datumsbereich relativ zum Bedienfeldkalender verhalten.
Wenn relative Datumswerte ausgewählt sind, basieren rollierende Datumswerte auf dem Startdatum des Bedienfeldkalenders und nicht auf dem heutigen Datum.
   * Ist diese Option nicht ausgewählt, basieren rollierende Datumswerte auf dem heutigen Datum.

   ![relative Bedienfeld-Datumsangaben](assets/relative-date-selected.png){width="60%"}

1. Klicken Sie auf **Anwenden**.
Die relativen Daten werden oben rechts angezeigt.

   ![relative Daten in Freiform ](assets/relative-date-range1.png)

## Richtlinien für relative Bedienfelddatumsbereiche {#guidelines}

Beachten Sie bei der Verwendung relativer Bedienfelddatumsbereiche die folgenden Richtlinien.

### Formeln und relative Datumsbereiche {#formula-relative-dates}

Wenn Sie relative Datumsangaben ausgewählt haben, verwenden alle Datumsformeln das Startdatum des Bedienfelds als Ausgangspunkt.

### Benutzerdefinierte Kalender und relative Datumsbereiche {#custom-calendar-formulas}

Wenn Sie einen wöchentlichen benutzerspezifischen Kalender verwenden und Monate oder Jahre hinzufügen, berechnet die Formel den Versatz des Tages im angegebenen Zeitraum. Das tatsächliche Datum kann sich aufgrund des Versatzes unterscheiden. Durch die Formel wird der Tag ausgewählt, der an derselben Stelle im benutzerdefinierten Kalender liegt, beispielsweise der dritte Freitag der dritten Woche in einem benutzerdefinierten Kalender.

### Über Segmente, die rollierende Datumsangaben und relative Bedienfeld-Datumsbereiche verwenden {#segments-relative-dates}

Wenn Sie ein Segment erstellen oder ein Segment mit einem rollierenden Datum verwenden, z. B. die letzten 7 Tage oder die letzten 2 Wochen, und Sie auf die Segmentvorschau klicken, beginnt das rollierende Datum ab *Heute* anstelle des Startdatums des Bedienfelds. Daher stimmt die Vorschau für das Segment nicht, wenn Sie das Segment in der Tabelle verwenden. Die Vorschau ist zwar falsch, nicht aber das Segment selbst.

## Richtlinien für Panel-Datumsbereiche und Vorschauen {#guidelines-panel-dates}

* Ab der Februarversion basieren die Komponenten- und Datenvorschauen auf dem Datumsbereich des Bedienfelds und nicht auf den letzten 90 Tagen.
* Alle in der linken Leiste aufgelisteten Komponenten sind basierend auf dem Datumsbereich des Bedienfelds verfügbar.
* Alle Datumsvorschauen im Segment und Generatoren für berechnete Metriken basieren auf dem Datumsbereich des Bedienfelds (sofern nicht von den Komponenten-Managern darauf zugegriffen wird, die über kein verknüpftes Bedienfeld verfügen, basieren sie weiterhin auf den letzten 90 Tagen).
* Bei jeder Datenvorschau werden Daten oder Komponenten basierend auf dem Datumsbereich des Bedienfelds angezeigt.