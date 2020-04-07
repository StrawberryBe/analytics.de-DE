---
description: 'null'
title: Fallout-Visualisierung konfigurieren
uuid: fc117745-baf3-46fb-873d-9307092cc337
translation-type: tm+mt
source-git-commit: 2cd9872ed5052b9569d03a07d5171221b9e0af29

---


# Fallout-Visualisierung konfigurieren

Sie können die Touchpoints angeben, um eine mehrdimensionale Fallout-Sequenz zu erstellen. Normalerweise ist ein Touchpoint eine Seite auf Ihrer Site. Touchpoints sind jedoch nicht auf Seiten beschränkt. Sie können beispielsweise Ereignis wie Einheiten sowie individuelle Besucher und rückkehrende Besuche hinzufügen. Sie können auch Dimensionen hinzufügen, z. B. eine Kategorie, einen Browsertyp oder einen internen Suchbegriff.

Sie können sogar Segmente innerhalb eines Touchpoints hinzufügen. Sie können beispielsweise Segmente wie iOS- und Android-Benutzer vergleichen. Ziehen Sie die gewünschten Segmente an den Anfang des Fallout-Berichts, und Informationen zu diesen Segmenten werden dem Fallout-Bericht hinzugefügt. Wenn Sie nur diese Segmente anzeigen möchten, können Sie die Grundlinie &quot;Alle Besuche&quot;entfernen.

Die Anzahl der Schritte, die Sie hinzufügen können, und die Anzahl der verwendeten Dimensionen sind unbegrenzt.

Sie können Pathing an eVars vornehmen, inklusive Merchandising-eVars und [listVars](https://marketing.adobe.com/resources/help/de_DE/sc/implement/listN.html) (Variablen, die mehrere Werte pro Hit haben können, wie Produkte, listVars, Merchandising-eVars und Listen-Props). Beispiel: Angenommen, jemand sucht auf der einen Seite nach „Schuhe,Shirt“ und auf der nächsten Seite nach „Schuhe,Socken“. Der nächste Produktflussbericht von Schuhen ist Hemd und Socken, NICHT Hemd.

1. Drag a [!UICONTROL Fallout] visualization from the Visualizations drop-down into a [!UICONTROL Freeform Table].

1. Drag the Page dimension into the Freeform Table and from there, drag a page (in this case, Home - JJEsquire) into the **[!UICONTROL Add TouchPoint]** field as the first touchpoint.

   ![](assets/fallout1.png)

   Wenn Sie den Mauszeiger über einen Touchpoint halten, werden der Fallout und andere Informationen zu dieser Ebene (wie der Name des Touchpoints, die Anzahl der Besucher an diesem Punkt) sowie die Erfolgsrate für diesen Touchpoint angezeigt (und Sie können die Erfolgsrate mit anderen Touchpoints vergleichen).

   Die kreisförmigen Zahlen im grauen Teil des Balkens zeigen den Fallout zwischen Touchpoints (nicht den Gesamtabgang bis zu diesem Punkt). Der Touchpoint % zeigt den erfolgreichen Fallthrough vom vorherigen Schritt zum aktuellen Schritt im Fallout-Bericht an.

   Sie können dem Fallout-Bericht auch eine einzelne Seite anstatt der gesamten Dimension hinzufügen. Klicken Sie auf den Pfeil nach rechts &quot;>&quot;in der Seitendimension, um die spezifische Seite auszuwählen, die dem Trichteranalysebericht hinzugefügt werden soll.

1. Fügen Sie weitere Touchpoints hinzu, bis Ihre Sequenz abgeschlossen ist.

   Sie können mehrere Touchpoints **kombinieren, indem Sie einen oder mehrere weitere Touchpoints** auf einen Touchpoint ziehen.

   >[!NOTE]
   >
   >Hinweis: Mehrere Segmente werden mit UND verbunden, mehrere Elemente wie Dimensionselemente und Metriken hingegen mit ODER.

   ![](assets/multiple_obj_touchpoint.png)

1. Einzelne Touchpoints können nun auch **auf den nächsten Hit** (statt am Ende) im Pfad eingegrenzt werden. Jedem Touchpoint unterliegen die Auswahlmöglichkeiten „Pfad am Ende“ und „Nächster Hit“:

   ![](assets/next-hit-eventually.png)

<table id="table_A91D99D9364B41929CC5A5BC907E8985"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Endlicher Pfad </p> <p>(Standard) </p> </td> 
   <td colname="col2"> <p>Die Besucher, die „am Ende“ auf der nächsten Seite im Pfad, aber nicht notwendigerweise beim nächsten Hit landen, werden gezählt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nächster Hit </p> </td> 
   <td colname="col2"> <p>Die Besucher, die auf der nächsten Seite im Pfad, genau beim nächsten Hit landen, werden gezählt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Fallout-Einstellungen {#section_0C7C89D72F0B4D6EB467F278AC979093}

| Einstellung | Beschreibung |
|--- |--- |
| Trichteranalyse-Container <ul><li>Besuch</li><li>Besucher.</li></ul> | Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Die Standardeinstellung lautet „Besucher“.  Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. |
| „Alle Besucher“ als ersten Touchpoint anzeigen. | Diese Option können Sie deaktivieren, wenn Sie nicht möchten, dass „Alle Besucher“ der erste Touchpoint ist. |

Wenn Sie **mit der rechten Maustaste auf einen Touchpoint klicken**, werden die folgenden Optionen angezeigt:

| Option | Beschreibung |
|--- |--- |
| Trend-Touchpoint | Siehe Trenddaten für einen Touchpoint in einem Liniendiagramm mit einigen vordefinierten Anomalieerkennungsdaten. |
| Trend-Touchpoint (%) | Trendansicht des gesamten Trichteranalyseprozentsatzes. |
| Trend für alle Touchpoints (%) | Trendt alle Touchpoint-Prozentsätze im Fallout (außer &quot;Alle Besuche&quot;, sofern vorhanden) im gleichen Diagramm. |
| Trichteranalyse an diesem Touchpoint | Ansicht, was Besucher zwischen zwei Touchpoints (diesem Touchpoint und dem nächsten Touchpoint) getan haben, wenn sie bis zum nächsten Touchpoint fortfuhren. Diese Option erstellt eine Freiformtabelle, die Ihre Dimensionen enthält. Sie können Dimensionen und andere Elemente der Tabelle ersetzen. |
| Trichteranalyse an diesem Touchpoint aufschlüsseln | Ansicht, was Personen, die den Trichter nicht durchlaufen haben, unmittelbar nach dem ausgewählten Schritt getan haben. |
| Segment aus Touchpoint erstellen | Erstellen Sie ein neues Segment aus dem ausgewählten Touchpoint. |
