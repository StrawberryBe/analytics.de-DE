---
description: Erstellen Sie in Analysis Workspace eine Kohorte und führen Sie einen Kohortenanalysebericht aus.
keywords: Analysis Workspace
title: Ausführen eines Kohortenanalyseberichts
topic: Reports and analytics
uuid: 5574230f-8f35-43ea-88d6-cb4960ff0bf4
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Konfigurieren eines Kohortenanalyseberichts

Erstellen Sie in Analysis Workspace eine Kohorte und führen Sie einen Kohortenanalysebericht aus.

1. In Analysis Workspace, click the **[!UICONTROL Visualizations]** icon in the left rail and drag a **[!UICONTROL Cohort Table]** to the canvas.

   ![](assets/cohort-table.png)

1. Definieren Sie die **[!UICONTROL Inclusion Criteria]**, **[!UICONTROL Return Criteria]**, **[!UICONTROL Cohort Type]** und **[!UICONTROL Settings]** wie in der unten stehenden Tabelle definiert.

| Element | Beschreibung |
|--- |--- |
| **[!UICONTROL Inclusion Criteria]** | Sie können bis zu 10 Aufnahmesegmente und bis zu 3 Aufnahmekennzahlen anwenden. Die Kennzahl bestimmt, durch welche Kennzahl ein Benutzer in einer Kohorte platziert wird. Wenn die Aufnahmekennzahl z. B. die Bestellungen sind, werden nur Benutzer, die innerhalb des Zeitraums der Kohortenanalyse bestellt haben, in den anfänglichen Kohorten platziert.<br>Der Standardoperator zwischen den Kennzahlen ist UND, kann aber in ODER geändert werden. Außerdem können Sie diesen Metriken numerische Filter hinzufügen. Beispielsweise: „Besuche >= 1“.</br> |
| **[!UICONTROL Return Criteria]** | Sie können bis zu 10 Rückkehrsegmente und bis zu 3 Rückkehrkennzahlen anwenden. Die Kennzahl gibt an, ob ein Benutzer gewonnen wurde (Bindung) oder nicht (Abwanderung). Wenn die Rückkehrmetrik z. B. die Videoansichten sind, werden nur Benutzer, die in nachfolgenden Zeiträumen (nach dem Zeitraum, in dem sie zu einer Kohorte hinzugefügt wurden) Videos angesehen haben, als zurückgekehrt dargestellt. Eine weitere Metrik, die die Treue quantifiziert, sind die Besuche. |
| **[!UICONTROL Granularity]** | Die Zeitgranularität: Tag, Woche, Monat, Quartal oder Jahr. |
| **[!UICONTROL Type]** | **[!UICONTROL Retention]**(Standard): Eine Retentionskohorte misst, wie gut Ihre Besucher-Kohorten im Laufe der Zeit zu Ihrer Eigenschaft zurückkehren. Dabei handelt es sich um die Standardkohorte, die schon immer vorhanden war. Sie zeigt die Rückkehr und wiederkehrendes Benutzerverhalten an. In der Tabelle wird die Bindungskohorte grün angezeigt.<br>**[!UICONTROL Churn]**: Eine Churn-Kohorte (auch als &quot;Abbruch&quot;oder &quot;Trichteranalyse&quot;bezeichnet) misst, wie Ihre Besucher-Kohorten im Laufe der Zeit aus Ihrer Eigenschaft fallen. Abwanderung = 1 - Bindung. Die Abwanderung ist ein guter Messwert für die Treue und Chancen, da Ihnen gezeigt wird, wie häufig Kunden nicht zurückkehren. Sie können die Abwanderung nutzen, um Fokusbereiche zu analysieren und zu identifizieren, um herauszufinden, welche Kohortensegmente etwas Aufmerksamkeit erfordern. A Churn Cohort is indicated by the color red in the table (similar to fallout in our **[!UICONTROL Flow]** visualization).</br> |
| **[!UICONTROL Settings]** | **[!UICONTROL Rolling Calculation]**: Berechnen Sie die Treue oder die Abwanderung auf der Basis der vorherigen Spalte anstatt der einbezogenen Spalte (Standardeinstellung). Durch die rollierende Berechnung wird die Berechnungsmethode für Ihre „Rückkehr“-Zeiten verändert. Die Normalberechnung findet eigenständig Benutzer, die die „Rückkehr“-Kriterien erfüllen und Teil des Aufnahmezeitraums waren, unabhängig davon, ob sie in der Kohorte des vorherigen Zeitraums waren oder nicht. Im Gegensatz dazu findet die rollierende Berechnung Benutzer, die die „Rückkehr“-Kriterien erfüllen und Teil des vorherigen Zeitraums waren. Daher filtert die rollierende Berechnung Benutzer, die die „Rückkehr“-Kriterien kontinuierlich in jedem Zeitraum erfüllen, und trichtert sie. Rückgabekriterien werden auf jeden Zeitraum bis zum ausgewählten Zeitraum angewendet. </br><br>**[!UICONTROL Latency Table]**: Eine Latenztabelle misst die verstrichene Zeit vor und nach dem Aufnahmeereignis. Die Latenz eignet sich ideal vor/nach der Analyse. Wenn beispielsweise ein Produkt- oder Kampagnen-Lauch bevorsteht und Sie das Verhalten vorher verfolgen und sehen möchten, wie es danach ist, zeigt die Latenztabelle das Verhalten vorher und danach nebeneinander an, um die direkten Auswirkungen darzustellen. Die Zellen in der Latenztabelle vor der Aufnahme werden von Benutzern berechnet, die die „Aufnahme“-Kriterien für den Aufnahmezeitraum und anschließend die „Rückkehr“-Kriterien in den Zeiträumen vor dem Aufnahmezeitraum erfüllen. Latenztabellen und angepasste Dimensionskohorte können nicht zusammen verwendet werden.</br><br>**[!UICONTROL Custom Dimension Cohort]**: Erstellen Sie Kohorten auf der Basis der ausgewählten Dimension anstatt der zeitbasierten Kohorten (Standardeinstellung). Viele Kunden möchten ihre Kohorten nach etwas anderem als der Zeit analysieren und die neue Funktion der angepassten Dimensionskohorte bietet Ihnen die Flexibilität, Kohorten basierend auf Dimensionen ihrer Wahl zu erstellen. Verwenden Sie Dimensionen wie Marketing-Kanal, Kampagne, Produkt, Seite, Region oder jede andere Dimension in Adobe Analytics, um anzuzeigen, wie die Bindung sich basierend auf verschiedenen Werten dieser Dimensionen verändert. Die Segmentdefinition Benutzerspezifische Kohortendimension wendet das Dimensionselement nur als Teil des Aufnahmezeitraums an, nicht als Teil der Rückgabedefinition.</br><br>Nach Auswahl der Option „Angepasste Dimensionskohorte“ können Sie jede beliebige Dimension in die Dropzone ziehen. Auf diese Weise können Sie ähnliche Dimensionselemente über den gleichen Zeitraum hinweg miteinander vergleichen. Sie können beispielsweise die Leistung von Städten, Produkten, Kampagnen usw. nebeneinander vergleichen. Dabei werden Ihre 14 wichtigsten Dimensionselemente ausgegeben. Sie können jedoch einen Filter verwenden (auf den Sie zugreifen können, indem Sie mit der Maus über den Bereich rechts von der gezogenen Dimension fahren), um nur die gewünschten Dimensionselemente anzuzeigen. Eine angepasste Dimensionskohorte kann nicht mit der Funktion der Latenztabelle verwendet werden.</br> |

1. Passen Sie die Einstellung an, **[!UICONTROL Cohort Table Settings]** indem Sie auf das Zahnradsymbol klicken.

| Einstellung | Beschreibung |
| Nur Prozentwert anzeigen | Entfernt den Zahlenwert und zeigt nur den Prozentsatz an. |
| Prozentwert auf nächste Ganzzahl runden | Rundet den Prozentwert auf den nächsten ganzzahligen Wert, anstatt den Dezimalwert anzuzeigen. |
| Zeile mit durchschnittlichem Porzentwert anzeigen | Fügt oben in der Tabelle eine neue Zeile ein und fügt dann den Durchschnitt der Werte in jeder Spalte hinzu. |

## Erstellen des Kohortenanalyseberichts

1. Klicken Sie auf **[!UICONTROL Build]**.

   ![Schritt Ergebnis](assets/cohort-report.png)

   Der Bericht zeigt Besucher an, die eine Bestellung aufgegeben haben (Spalte *`Included`*) und die bei nachfolgenden Besuchen zu Ihrer Website zurückkehrten. Über den Rückgang der Besuche im Laufe der Zeit können Sie Probleme erkennen und Maßnahmen ergreifen.
1. (Optional) Erstellen Sie ein Segment aus einer Auswahl.

   Wählen Sie Zellen (zusammenhängend oder nicht zusammenhängend) und klicken Sie dann mit der rechten Maustaste auf > **[!UICONTROL Create Segment From Selection]**.

1. In the [Segment Builder](https://marketing.adobe.com/resources/help/de_DE/analytics/segment/seg_build.html), further edit the segment, then click **[!UICONTROL Save]**.

   Das gespeicherte ist in Analysis Workspace im Bereich [!UICONTROL Segment]Segment für die Verwendung verfügbar.
1. Geben Sie Ihrem Kohortenprojekt einen Namen und speichern Sie es.
1. (Optional) [Kuratieren Sie die Projektkomponenten und geben Sie sie frei](/help/analyze/analysis-workspace/curate-share/curate.md).

   >[!NOTE]
   >
   >Sie müssen Ihr Projekt speichern, damit das Kuratieren verfügbar wird.

