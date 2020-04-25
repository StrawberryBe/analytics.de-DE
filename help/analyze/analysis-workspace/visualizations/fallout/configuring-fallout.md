---
description: 'null'
title: Fallout-Visualisierung konfigurieren
uuid: fc117745-baf3-46fb-873d-9307092cc337
translation-type: tm+mt
source-git-commit: 2cd9872ed5052b9569d03a07d5171221b9e0af29

---


# Fallout-Visualisierung konfigurieren

Sie können die Touchpoints angeben, um eine mehrdimensionale Fallout-Sequenz zu erstellen. Ein Touchpoint ist im Allgemeinen eine Seite auf Ihrer Website. Touchpoints sind jedoch nicht auf Webseiten eingeschränkt. So können Sie zum Beispiel Ereignisse (z. B. Einheiten) sowie Unique Visitors und erneute Besuche hinzufügen. Auch Dimensionen können Sie hinzufügen (wie Kategorie, Browsertyp oder interner Suchbegriff).

Sogar Segmente können Sie innerhalb eines Touchpoints hinzufügen. Vielleicht möchten Sie zum Beispiel Segmente vergleichen (wie iOS- und Android-Benutzer). Wenn Sie die gewünschten Segmente an die Oberseite des Trichters ziehen, werden Informationen über diese Segmente zum Fallout-Bericht hinzugefügt. Wenn Sie möchten, dass nur diese Segmente angezeigt werden, können Sie die Grundlinie „Alle Besuche“ entfernen.

Bezüglich der Anzahl der Schritte, die hinzugefügt, oder der Dimensionen, die verwendet werden können, gibt es keine Einschränkungen.

Sie können Pathing an eVars vornehmen, inklusive Merchandising-eVars und [listVars](https://marketing.adobe.com/resources/help/de_DE/sc/implement/listN.html) (Variablen, die mehrere Werte pro Hit haben können, wie Produkte, listVars, Merchandising-eVars und Listen-Props). Beispiel: Angenommen, jemand sucht auf der einen Seite nach „Schuhe,Shirt“ und auf der nächsten Seite nach „Schuhe,Socken“. Der nächste Produktflussbericht von Schuhe wird „Shirt und Socken“ lauten, NICHT „Shirt“.

1. Drag a [!UICONTROL Fallout] visualization from the Visualizations drop-down into a [!UICONTROL Freeform Table].

1. Drag the Page dimension into the Freeform Table and from there, drag a page (in this case, Home - JJEsquire) into the **[!UICONTROL Add TouchPoint]** field as the first touchpoint.

   ![](assets/fallout1.png)

   Wenn Sie den Mauszeiger über einen Touchpoint halten, werden der Fallout und andere Informationen zu dieser Ebene (wie der Name des Touchpoints, die Anzahl der Besucher an diesem Punkt) sowie die Erfolgsrate für diesen Touchpoint angezeigt (und Sie können die Erfolgsrate mit anderen Touchpoints vergleichen).

   Die umkreisten Zahlen im grauen Abschnitt der Leiste zeigen den Fallout zwischen Touchpoints an (nicht den gesamten Fallout bis zu diesem Punkt). Der Touchpoint-Prozentsatz zeigt den erfolgreichen Fall-through vom vorherigen Schritt zum aktuellen Schritt im Fallout-Bericht an.

   Sie können auch eine einzelne Seite anstatt der gesamten Dimension zum Fallout-Bericht hinzufügen. Klicken Sie auf den rechten Pfeil „>“ auf der Seitendimension, um die Seite auszuwählen, die Sie zum Fallout-Bericht hinzufügen möchten.

1. Fügen Sie weitere Touchpoints hinzu, bis Ihre Sequenz vollständig ist.

   Sie können **mehrere Touchpoints kombinieren**, indem Sie mindestens einen weiteren Touchpoint auf einen Touchpoint ziehen.

   >[!NOTE]
   >
   >Hinweis: Mehrere Segmente werden mit UND verbunden, mehrere Elemente wie Dimensionselemente und Metriken hingegen mit ODER.

   ![](assets/multiple_obj_touchpoint.png)

1. Einzelne Touchpoints können nun auch **auf den nächsten Hit** (statt am Ende) im Pfad eingegrenzt werden. Jedem Touchpoint unterliegen die Auswahlmöglichkeiten „Pfad am Ende“ und „Nächster Hit“:

   ![](assets/next-hit-eventually.png)

<table id="table_A91D99D9364B41929CC5A5BC907E8985"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Pfad am Ende </p> <p>(Standardeinstellung) </p> </td> 
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
| Fallout-Container <ul><li>Besuch</li><li>Besucher.</li></ul> | Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Die Standardeinstellung lautet „Besucher“.  Mithilfe dieser Einstellungen können Sie Einblicke in Besucheraktivitäten auf der Besucherebene (besuchsübergreifend) erhalten oder die Analyse auf einen einzelnen Besuch einschränken. |
| „Alle Besucher“ als ersten Touchpoint anzeigen. | Diese Option können Sie deaktivieren, wenn Sie nicht möchten, dass „Alle Besucher“ der erste Touchpoint ist. |

Wenn Sie **mit der rechten Maustaste auf einen Touchpoint klicken**, werden die folgenden Optionen angezeigt:

| Option | Beschreibung |
|--- |--- |
| Trend-Touchpoint | Zeigt Trenddaten für einen Touchpoint in einem Liniendiagramm mit einigen vorab definierten Anomalieerkennungsdaten an. |
| Trend-Touchpoint (%) | Trends für den gesamten Fallout-Prozentsatz |
| Trenderstellung aller Touchpoints (%) | Trends für alle Touchpoint-Prozentsätze im Fallout (außer „Alle Besuche“, falls vorhanden) im selben Diagramm. |
| Trichteranalyse an diesem Touchpoint | Ansicht, was Besucher zwischen zwei Touchpoints (diesem Touchpoint und dem nächsten Touchpoint) getan haben, wenn sie bis zum nächsten Touchpoint fortfuhren. Diese Option erstellt eine Freiformtabelle, die Ihre Dimensionen enthält. Dimensionen und andere Elemente der Tabelle können Sie austauschen. |
| Trichteranalyse an diesem Touchpoint aufschlüsseln | Zeigt an, was Besucher, die nicht im Trichter verblieben sind, unmittelbar nach dem ausgewählten Schritt getan haben. |
| Segment aus Touchpoint erstellen | Erstellen Sie ein Segment aus dem ausgewählten Touchpoint. |
