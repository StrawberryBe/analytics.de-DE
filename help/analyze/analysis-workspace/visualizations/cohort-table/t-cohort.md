---
description: Erstellen Sie eine Kohorte und führen Sie einen Kohortenanalysebericht in Analysis Workspace aus.
keywords: Analysis Workspace
seo-description: Erstellen Sie eine Kohorte und führen Sie einen Kohortenanalysebericht in Analysis Workspace aus.
seo-title: Ausführen eines Kohortenanalyseberichts
solution: Analytics
title: Ausführen eines Kohortenanalyseberichts
topic: Reports and Analytics
uuid: 5574230f-8f35-43ea-88d6-cb4960ff0bf4
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Konfigurieren eines Kohortenanalyseberichts

Erstellen Sie eine Kohorte und führen Sie einen Kohortenanalysebericht in Analysis Workspace aus.

1. In Analysis Workspace, click the **[!UICONTROL Visualizations]** icon in the left rail and drag a **[!UICONTROL Cohort Table]** to the canvas.

   ![](assets/cohort-table.png)

1. Define the **[!UICONTROL Inclusion Criteria]**, **[!UICONTROL Return Criteria]**, **[!UICONTROL Cohort Type]**, and **[!UICONTROL Settings]** as defined in the table below.

| Element | Beschreibung |
|--- |--- |
| **[!UICONTROL Aufnahmekriterien]** | Sie können bis zu 10 Aufnahmesegmente und bis zu 3 Aufnahmekennzahlen anwenden. Die Metrik gibt an, was einen Benutzer in einer Kohorte platziert. Wenn die Aufnahmekennzahl z. B. die Bestellungen sind, werden nur Benutzer, die innerhalb des Zeitraums der Kohortenanalyse bestellt haben, in den anfänglichen Kohorten platziert.<br>Der Standardoperator zwischen den Kennzahlen ist AND, kann aber in OR geändert werden. Außerdem können Sie diesen Metriken numerische Filter hinzufügen. Beispielsweise: „Besuche &gt;= 1“.</br> |
| **[!UICONTROL Rückkehrkriterien]** | Sie können bis zu 10 Rückkehrsegmente und bis zu 3 Rückkehrkennzahlen anwenden. Die Kennzahl gibt an, ob ein Benutzer gewonnen wurde (Bindung) oder nicht (Abwanderung). Wenn die Rückkehrmetrik z. B. die Videoansichten sind, werden nur Benutzer, die in nachfolgenden Zeiträumen (nach dem Zeitraum, in dem sie zu einer Kohorte hinzugefügt wurden) Videos angesehen haben, als zurückgekehrt dargestellt. Eine weitere Metrik, die die Treue quantifiziert, sind die Besuche. |
| **[!UICONTROL Granularität]** | Die Zeitgranularität: Tag, Woche, Monat, Quartal oder Jahr. |
| **[!UICONTROL Typ]** | **** Bindung (Standard): Durch die Bindungskohorte wird gemessen, wie die Besucherkohorte im Laufe der Zeit zu Ihnen zurückkehrt. Dabei handelt es sich um die Standardkohorte, die schon immer vorhanden war. Sie zeigt die Rückkehr und wiederkehrendes Benutzerverhalten an. In der Tabelle wird die Bindungskohorte grün angezeigt.<br>**[!UICONTROL Churn]**: Eine Kehrkohorte (auch als "Abgang"oder "Trichteranalyse"bezeichnet) misst, wie Ihre Besucherkohorten im Laufe der Zeit aus Ihrer Eigenschaft fallen. Abwanderung = 1 - Bindung. Die Abwanderung ist ein guter Messwert für die Treue und Opportunity, da Ihnen gezeigt wird, wie häufig Kunden nicht zurückkehren. Sie können den Kurn verwenden, um Schwerpunktbereiche zu analysieren und zu identifizieren: welche Kohortensegmente eine gewisse Aufmerksamkeit nutzen könnten. A Churn Cohort is indicated by the color red in the table (similar to fallout in our **[!UICONTROL Flow]** visualization).</br> |
| **[!UICONTROL Einstellungen]** | **[!UICONTROL Rollierende Berechnung]**: Ermöglicht es Ihnen, die Bindung oder die Abwanderung auf Grundlage der vorherigen Spalte und nicht der Aufnahmespalte zu berechnen (Standard). Durch die rollierende Berechnung wird die Berechnungsmethode für Ihre „Rückkehr“-Zeiten verändert. Die Normalberechnung findet eigenständig Benutzer, die die „Rückkehr“-Kriterien erfüllen und Teil des Aufnahmezeitraums waren, unabhängig davon, ob sie in der Kohorte des vorherigen Zeitraums waren oder nicht. Im Gegensatz dazu findet die rollierende Berechnung Benutzer, die die „Rückkehr“-Kriterien erfüllen und Teil des vorherigen Zeitraums waren. Daher filtert die rollierende Berechnung Benutzer, die die „Rückkehr“-Kriterien kontinuierlich von Zeitraum zu Zeitraum erfüllen, und trichtert sie. Rückgabekriterien werden auf jeden Zeitraum angewendet, was zu dem ausgewählten Zeitraum führt. </br><br>**[!UICONTROL Latenztabelle]**: Misst die Zeit, die vor und nach dem Aufnahmeereignis verstrichen ist. Die Latenz eignet sich ideal vor/nach der Analyse. Wenn beispielsweise ein Produkt- oder Kampagnen-Lauch bevorsteht und Sie das Verhalten vorher verfolgen und sehen möchten, wie es danach ist, zeigt die Latenztabelle das Verhalten vorher und danach nebeneinander an, um die direkten Auswirkungen darzustellen. Die Zellen in der Latenztabelle vor der Aufnahme werden von Benutzern berechnet, die die „Aufnahme“-Kriterien für den Aufnahmezeitraum und anschließend die „Rückkehr“-Kriterien in den Zeiträumen vor dem Aufnahmezeitraum erfüllen. Latenztabellen und angepasste Dimensionskohorte können nicht zusammen verwendet werden.</br><br>**[!UICONTROL Angepasste Dimensionskohorte]**: Erstellen Sie Kohorten auf Grundlage der ausgewählten Dimension und nicht auf Grundlage zeitbasierter Kohorten (Standard). Viele Kunden möchten ihre Kohorten nach etwas anderem als der Zeit analysieren und die neue Funktion der angepassten Dimensionskohorte bietet Ihnen die Flexibilität, Kohorten basierend auf Dimensionen ihrer Wahl zu erstellen. Verwenden Sie Dimensionen wie Marketing-Kanal, Kampagne, Produkt, Seite, Region oder jede andere Dimension in Adobe Analytics, um anzuzeigen, wie die Bindung sich basierend auf verschiedenen Werten dieser Dimensionen verändert. Die Segmentdefinition Benutzerspezifische Kohortendimension wendet das Dimensionselement nur als Teil des Aufnahmezeitraums an, nicht als Teil der Rückgabedefinition.</br><br>Nach Auswahl der Option Angepasste Dimensionskohorte können Sie jede beliebige Dimension in die Dropzone ziehen. Auf diese Weise können Sie ähnliche Dimensionselemente über den gleichen Zeitraum hinweg miteinander vergleichen. Sie können beispielsweise die Leistung von Städten, Produkten, Kampagnen usw. nebeneinander vergleichen. Dabei werden Ihre 14 wichtigsten Dimensionselemente ausgegeben. Sie können jedoch einen Filter verwenden (auf den Sie zugreifen können, indem Sie mit der Maus über den Bereich rechts von der gezogenen Dimension fahren), um nur die gewünschten Dimensionselemente anzuzeigen. Eine angepasste Dimensionskohorte kann nicht mit der Funktion der Latenztabelle verwendet werden.</br> |

1. Passen Sie die **[!UICONTROL Kohortentabelleneinstellungen]** an, indem Sie auf das Zahnradsymbol klicken.

| Einstellung| Beschreibung|| Nur Prozentsatz anzeigen| Entfernt den Zahlenwert und zeigt nur den Prozentsatz an. || Runde Prozent bis zum nächsten Ganzem| Richtet den Prozentwert auf den nächsten ganzzahligen Wert, anstatt den Dezimalwert anzuzeigen. || Durchschnittliche Prozentzeile anzeigen| Fügt oben in der Tabelle eine neue Zeile ein und fügt dann den Durchschnitt der Werte in jeder Spalte hinzu. |

## Erstellen des Kohortenanalyseberichts

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   ![Schritt Ergebnis](assets/cohort-report.png)

   Der Bericht zeigt Besucher an, die eine Bestellung aufgegeben haben ( *`Included`* Spalte) und die bei nachfolgenden Besuchen zu Ihrer Site zurückkehrten. Über den Rückgang der Besuche im Laufe der Zeit können Sie Probleme erkennen und Maßnahmen ergreifen.
1. (Optional) Erstellen Sie ein Segment aus einer Auswahl.

   Wählen Sie Zellen aus (fortlaufende oder nicht fortlaufende) und klicken Sie mit der rechten Maustaste auf &gt; **[!UICONTROL Segment aus Auswahl erstellen]**.

1. In the [Segment Builder](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html), further edit the segment, then click **[!UICONTROL Save]**.

   Das gespeicherte Segment ist in Analysis Workspace im Bereich [!UICONTROL Segment] für die Verwendung verfügbar.
1. Geben Sie Ihrem Kohortenprojekt einen Namen und speichern Sie es.
1. (Optional) [Curate and share](../../../../analyze/analysis-workspace/curate-share/curate.md#concept_4A9726927E7C44AFA260E2BB2721AFC6) the project components.

   >[!NOTE]
   >
   >Sie müssen Ihr Projekt speichern, bevor die Kuratierung verfügbar ist.

