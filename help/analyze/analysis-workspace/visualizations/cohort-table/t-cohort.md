---
description: Erstellen Sie in Analysis Workspace eine Kohorte und führen Sie einen Kohortenanalysebericht aus.
keywords: Analysis Workspace
title: Ausführen eines Kohortenanalyseberichts
topic: Reports and analytics
uuid: 5574230f-8f35-43ea-88d6-cb4960ff0bf4
translation-type: tm+mt
source-git-commit: 79849c574909543d74e2935e493008927700585d
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 75%

---


# Configure a [!UICONTROL Cohort Analysis] report

Create a cohort and run a [!UICONTROL Cohort Analysis] report in Analysis Workspace.

1. Klicken Sie in Analysis Workspace in der linken Leiste auf das Symbol **[!UICONTROL Visualisierungen]** und ziehen Sie eine **[!UICONTROL Kohortentabelle]** auf die Arbeitsfläche.

   ![](assets/cohort-table.png)

1. Bestimmen Sie die **[!UICONTROL Aufnahmekriterien]**, die **[!UICONTROL Rückkehrkriterien]**, den **[!UICONTROL Kohortentyp]** und die **[!UICONTROL Einstellungen]** wie in der Tabelle unten definiert.

| Element | Beschreibung |
|--- |--- |
| **[!UICONTROL Aufnahmekriterien]** | Sie können bis zu 10 Aufnahmesegmente und bis zu 3 Aufnahmekennzahlen anwenden. Die Kennzahl bestimmt, durch welche Kennzahl ein Benutzer in einer Kohorte platziert wird. Wenn die Aufnahmekennzahl z. B. die Bestellungen sind, werden nur Benutzer, die innerhalb des Zeitraums der Kohortenanalyse bestellt haben, in den anfänglichen Kohorten platziert.<br>Der Standardoperator zwischen den Kennzahlen ist UND, kann aber in ODER geändert werden. Außerdem können Sie diesen Metriken numerische Filter hinzufügen. Beispielsweise: „Besuche >= 1“.</br> |
| **[!UICONTROL Rückkehrkriterien]** | Sie können bis zu 10 Rückkehrsegmente und bis zu 3 Rückkehrkennzahlen anwenden. Die Kennzahl gibt an, ob ein Benutzer gewonnen wurde (Bindung) oder nicht (Abwanderung). Wenn die Rückkehrmetrik z. B. die Videoansichten sind, werden nur Benutzer, die in nachfolgenden Zeiträumen (nach dem Zeitraum, in dem sie zu einer Kohorte hinzugefügt wurden) Videos angesehen haben, als zurückgekehrt dargestellt. Eine weitere Metrik, die die Treue quantifiziert, sind die Besuche. |
| **[!UICONTROL Granularität]** | Die Zeitgranularität: Tag, Woche, Monat, Quartal oder Jahr. |
| **[!UICONTROL Typ]** | **[!UICONTROL Bindung]** (Standard): Durch die Bindungskohorte wird gemessen, wie die Besucherkohorte im Laufe der Zeit zu Ihnen zurückkehrt. Dabei handelt es sich um die Standardkohorte, die schon immer vorhanden war. Sie zeigt die Rückkehr und wiederkehrendes Benutzerverhalten an. A [!UICONTROL Retention] Cohort is indicated by the color green in the table.<br>**[!UICONTROL Abwanderung ]**: Bei einer Abwanderungskohorte (auch „Abbruch“ oder „Fallout“) wird gemessen, wie Ihre Besucher im Laufe der Zeit abwandern. Abwanderung = 1 - Bindung.[!UICONTROL Die Abwanderung ist ein guter Messwert für die Treue und Chancen, da Ihnen gezeigt wird, wie häufig Kunden nicht zurückkehren.]Sie können die Abwanderung nutzen, um Fokusbereiche zu analysieren und zu identifizieren, um herauszufinden, welche Kohortensegmente etwas Aufmerksamkeit erfordern. A[!UICONTROL Churn]Cohort is indicated by the color red in the table (similar to fallout in our**[!UICONTROL  Flow ]**visualization).</br> |
| **[!UICONTROL Einstellungen]** | **[!UICONTROL Rollierende Berechnung]**: Ermöglicht es Ihnen, die Bindung oder die Abwanderung auf Grundlage der vorherigen Spalte und nicht der Aufnahmespalte zu berechnen (Standard). [!UICONTROL Durch die rollierende Berechnung wird die Berechnungsmethode für Ihre „Rückkehr“-Zeiten verändert. ] Die Normalberechnung findet eigenständig Benutzer, die die „Rückkehr“-Kriterien erfüllen und Teil des Aufnahmezeitraums waren, unabhängig davon, ob sie in der Kohorte des vorherigen Zeitraums waren oder nicht. Instead, [!UICONTROL Rolling Calculation] finds users who meet &quot;return&quot; criteria and were part of the previous period. Therefore, [!UICONTROL Rolling Calculation] filters and funnels the users who continually meet the &quot;return&quot; criteria period over period. [!UICONTROL Rückgabekriterien werden auf jeden Zeitraum bis zum ausgewählten Zeitraum angewendet. ] </br><br>**[!UICONTROL Latenztabelle ]**: Eine[!UICONTROL Latenztabelle]misst den Zeitraum, der vor und nach dem Einschluss-Ereignis verstrichen ist.[!UICONTROL Die Latenz eignet sich ideal vor/nach der Analyse.]For example, if you have an upcoming product or campaign launch and you want to track behavior before as well as see how it performs after, the[!UICONTROL Latency]table will display the pre and post behavior side by side to see the direct impact. The pre-inclusion cells in the[!UICONTROL Latency]Table are calculated by users who meet the[!UICONTROL Inclusion]criteria on the inclusion period and then meet the[!UICONTROL Return]criteria in the periods before the inclusion period. Note that[!UICONTROL Latency]tables and[!UICONTROL Custom Dimension]Cohort cannot be used together.</br><br>**[!UICONTROL Angepasste Dimensionskohorte]**: Erstellen Sie Kohorten auf Grundlage der ausgewählten Dimension und nicht auf Grundlage zeitbasierter Kohorten (Standard). Viele Kunden möchten ihre Kohorten nach etwas anderem als der Zeit analysieren und die neue Funktion der angepassten Dimensionskohorte bietet Ihnen die Flexibilität, Kohorten basierend auf Dimensionen ihrer Wahl zu erstellen. Verwenden Sie Dimensionen wie Marketing-Kanal, Kampagne, Produkt, Seite, Region oder jede andere Dimension in Adobe Analytics, um anzuzeigen, wie die Bindung sich basierend auf verschiedenen Werten dieser Dimensionen verändert. The [!UICONTROL Custom Dimension] Cohort segment definition applies the dimension item only as part of the inclusion period, not as part of the return definition.</br><br>[!UICONTROL Nach Auswahl der Option „Angepasste Dimensionskohorte“ können Sie jede beliebige Dimension in die Dropzone ziehen. ] Auf diese Weise können Sie ähnliche Dimensionselemente über den gleichen Zeitraum hinweg miteinander vergleichen. Sie können beispielsweise die Leistung von Städten, Produkten, Kampagnen usw. nebeneinander vergleichen. Dabei werden Ihre 14 wichtigsten Dimensionselemente ausgegeben. Sie können jedoch einen Filter verwenden (auf den Sie zugreifen können, indem Sie mit der Maus über den Bereich rechts von der gezogenen Dimension fahren), um nur die gewünschten Dimensionselemente anzuzeigen. A [!UICONTROL Custom Dimension] Cohort cannot be used with the [!UICONTROL Latency] Table feature.</br> |

1. Passen Sie die **[!UICONTROL Kohortentabelleneinstellungen]** an, indem Sie auf das Zahnradsymbol klicken.

| Einstellung | Beschreibung |
| Nur Prozentwert anzeigen | Entfernt den Zahlenwert und zeigt nur den Prozentsatz an. |
| Prozentwert auf nächste Ganzzahl runden | Rundet den Prozentwert auf den nächsten ganzzahligen Wert, anstatt den Dezimalwert anzuzeigen. |
| Zeile mit durchschnittlichem Porzentwert anzeigen | Fügt oben in der Tabelle eine neue Zeile ein und fügt dann den Durchschnitt der Werte in jeder Spalte hinzu. |

## Build the [!UICONTROL Cohort Analysis] report

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![Schritt Ergebnis](assets/cohort-report.png)

   Der Bericht zeigt Besucher an, die eine Bestellung aufgegeben haben (Spalte *`Included`*) und die bei nachfolgenden Besuchen zu Ihrer Website zurückkehrten. Über den Rückgang der Besuche im Laufe der Zeit können Sie Probleme erkennen und Maßnahmen ergreifen.
1. (Optional) Erstellen Sie ein Segment aus einer Auswahl.

   Wählen Sie Zellen aus (fortlaufende oder nicht fortlaufende) und klicken Sie mit der rechten Maustaste auf **[!UICONTROL Segment aus Auswahl erstellen]**.

1. Bearbeiten Sie das Segment im [Segment Builder](/help/components/c-segmentation/c-segmentation-workflow/seg-build.md) weiter und klicken Sie anschließend auf **[!UICONTROL Speichern]**.

   Das gespeicherte Segment ist in Analysis Workspace im Bereich [!UICONTROL Segment][!UICONTROL  für die Verwendung verfügbar].
1. Geben Sie Ihrem Kohortenprojekt einen Namen und speichern Sie es.
1. (Optional) [Kuratieren Sie die Projektkomponenten und geben Sie sie frei](/help/analyze/analysis-workspace/curate-share/curate.md).

   >[!NOTE]
   >
   >Sie müssen Ihr Projekt speichern, damit das Kuratieren verfügbar wird.

