---
description: Erfahren Sie, wie Sie Kanälen Kosten- und Budgetbeträge zuweisen.
seo-description: Erfahren Sie, wie Sie Kanälen Kosten- und Budgetbeträge zuweisen.
seo-title: Kosten und Budgets
solution: Analytics
subtopic: Marketingkanäle
title: Kosten und Budgets
topic: Reports and Analytics
uuid: 7 ba 0 e 968-e 565-4 d 4 c -8 fc 0-39 bf 25 d 3 e 5 b 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kosten und Budgets

Erfahren Sie, wie Sie Kanälen Kosten- und Budgetbeträge zuweisen.

## Costs and budgets {#topic_7CCFD3B54440433FBA0E4EE127F58B0C}

Erfahren Sie, wie Sie Kanälen Kosten- und Budgetbeträge zuweisen.

Kosten umfassen Ihre Ausgaben für den Kanal. Budget stellt alle verfügbaren Gelder dar.

Die ROI lässt sich sinnvoll anzeigen, indem Sie eine errechnete Metrik erstellen, die den Umsatz abzüglich der Kosten darstellt. Alternativ können Sie auch eine errechnete Metrik erstellen, die die Gesamtkosten mit einer Unterteilung der Kosten pro neuer Interaktion aufzeigt. Beispiel: Sie können einen [!UICONTROL First Touch-Kanal]bericht ausführen, der neue Interaktionen auflistet, und dann eine Metrik des Typs „First Touch-Kosten“ hinzufügen, die die Kosten pro neuer Interaktion darstellt.

Siehe [Berechnete Metriken verwenden Marketingkanalberichte](../../components/c-marketing-channels/c-channel-calc-metrics.md#topic_4521D324A79E43EF99E69FCDE1E92F74).

Kosten und Budgets können nur Kanälen zugewiesen werden. In der Berichterstellung erhalten alle Kosten einen Gültigkeitszeitraum. Wenn die Kosten in direktem Bezug zum Kanal stehen, wird eine Zuordnungsmetrik gewählt, die die Kostenaufteilung unter den Kampagnen eines Kanals anzeigt.

Nach Hinzufügen der Kosten- und Budgeteinträge können Sie die Tabellendaten in eine CSV-Datei exportieren. Die CSV-Datei können Sie auch in die Seite „Marketingkanal-Kosten“ importieren.

## Hinzufügen von Kosten- und Budgeteinträgen {#task_9238A033994440748960DE21593E6388}

Fügen Sie Marketingkanälen Kosten- und Budgeteinträge hinzu.

1. Click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.
1. Wählen Sie im [!UICONTROL „Report Suite Manager“] die Report Suite aus.
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Marketing Channels]** &gt; **[!UICONTROL Marketing Channel Costs]**.
1. Klicken Sie auf der Seite der [!UICONTROL Marketingkanal-Kosten]**auf[!UICONTROL Kosteneintrag hinzufügen]** oder **[!UICONTROL Budgeteintrag hinzufügen]**.
1. Klicken Sie auf **[!UICONTROL Speichern.]**

   Klicken Sie auf **[!UICONTROL Speichern und eine weitere hinzufügen, wenn Sie weitere Kosteneinträge vornehmen möchten]**.

1. (Optional) To export or import CSV files, access the [!UICONTROL Marketing Channel Costs] page, click **[!UICONTROL Export File]** or **[!UICONTROL Import File]**, then follow the prompts.

## Marketing Channel costs - definitions {#reference_0B193210E10A4B6B84A385A781FD9515}

Felddefinitionen für Marketingkanal-Kosten oder -Budgets.



| Feld | Definition |
|--- |--- |
| Name | Der Name des Kosten- oder Budgeteintrags. (Dieser Wert ist der Schlüsselwert, wenn Sie SAINT verwenden.) |
| Kanal | Der Kanal, mit dem dieser Betrag verbunden sein soll. Geben Sie an, ob die Kosten oder das Budget für einen First Touch- oder Last Touch-Kanal gelten. Ein First Touch-Kostenbetrag entspricht einer einmaligen neuen Interaktion. Ein Last Touch-Kostenbetrag gilt für Clickthroughs. |
| Datumsbereich | Der Zeitraum, der für diesen Betrag gelten soll. |
| Typ | Der Kosten- oder Budgettyp, entweder Rate oder Einmalige Kosten. Die Rate bezeichnet laufende Kosten, wie z. B. ein Betrag pro Klick. Unter Einmalige Kosten können Sie einen Verteilen nach Betrag angeben. Wenn Sie die Kosten pro Klick beispielsweise verteilen, werden dem Geschäftspartner mit 60% aller Klicks 60% der Kosten berechnet. Der Wert Verteilen nach ist die Metrik, die bei der Unterteilung nummerischer Classifications verwendet wird. |
| Datei exportieren | Ermöglicht den Export der Tabellendaten in eine CSV-Datei. |
| Datei importieren | Die CSV-Datei können Sie auch in die Seite Marketingkanal-Kosten importieren. |
