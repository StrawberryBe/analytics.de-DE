---
description: Der Segmentaufbau bietet eine Arbeitsfläche zum Ziehen und Ablegen von metrischen Dimensionen, Segmenten und Ereignissen für das Segmentieren von Besuchern auf der Grundlage von Behälterhierarchielogik, Regeln und Operatoren. Mit diesem integrierten Entwicklungstool können Sie einfache oder komplexe Segmente erstellen und speichern, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden.
title: Segmente erstellen
topic: Segments
uuid: c01393df-ccdd-431c-83a6-3c2700bd4999
translation-type: tm+mt
source-git-commit: f50f33b456656200b4492e6fec2a441d4c29dfa3
workflow-type: tm+mt
source-wordcount: '2436'
ht-degree: 99%

---


# Segmentaufbau

Der [!UICONTROL Segmentaufbau] bietet eine Arbeitsfläche zum Ziehen und Ablegen von Metriken, Dimensionen, Segmenten und Ereignissen für das Segmentieren von Besuchern auf der Grundlage von Behälterhierarchielogik, Regeln und Operatoren. Mit diesem integrierten Entwicklungstool können Sie einfache oder komplexe Segmente erstellen und speichern, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden.

>[!IMPORTANT]
>
>In der Version vom Juni 2019 haben wir Dimensionsattributionsmodelle eingeführt. Siehe #6 unter „Funktionen der Web-Benutzeroberfläche“ unten.

Es gibt mehrere Möglichkeiten für den Zugriff auf den Segmentaufbau:

* **Obere Navigation von Analytics**: Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Segmente]**.
* **[!UICONTROL Analysis Workspace]**: Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Workspace]**, öffnen Sie ein Projekt und klicken Sie auf **[!UICONTROL + Neu]** > **[!UICONTROL Segment erstellen]**.
* **[!UICONTROL Reports &amp; Analytics]**: Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Berichte]**, öffnen Sie einen vorhandenen Bericht, klicken Sie auf das Segmentsymbol ![](assets/segment_icon.png) im linken Navigationsmenü und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.
* **[!UICONTROL Ad Hoc Analysis]**: [Erstellen von Segmenten in Ad Hoc Analysis](/help/components/c-segmentation/c-segmentation-workflow/seg-build.md#build-segments).
* **[!UICONTROL Report Builder]**: [Hinzufügen oder Bearbeiten von Segmenten in Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/data-requests/segmentation.html).

## Benutzeroberfläche von Segment Builder {#concept_643F2DF74C544796B58F4656ABC5F726}

Mit dem [!UICONTROL Segmentaufbau] können Sie einfache oder komplexe Segmente erstellen, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden. Er bietet eine Arbeitsfläche zum Ziehen und Ablegen von metrischen Dimensionen, Ereignissen und anderen Segmenten, um Besucher mithilfe von Hierarchielogik, Regeln und Operatoren zu segmentieren.

## Funktionen der Web-Benutzeroberfläche  {#section_F61C4268A5974C788629399ADE1E6E7C}

Mit [!UICONTROL Segment Builder] können Sie Segmente über die Web-Benutzeroberfläche (oder eine [Java-Benutzeroberfläche in Ad Hoc Analysis](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md)) erstellen und bearbeiten. Sie können Regeldefinitionen und Behälter hinzufügen, um Ihre Segmente zu verfeinern, zu stapeln und zu verschachteln. Sie können auch prüfen, wie viele Seitenansichten, Besuche und Unique Visitors aus der aktuellen Segmentdefinition resultieren. Speichern Sie dann das Segment für den künftigen Bedarf.

Sie können wie folgt auf den Segmentaufbau zugreifen:

* öffnen Sie einen vorhandenen Bericht und klicken Sie auf das Segmentsymbol ![](assets/segment_icon.png) im linken Navigationsmenü. Klicken Sie in der angezeigten Segmentleiste auf **[!UICONTROL Hinzufügen]**.

* Klicken Sie im Segment-Manager auf **[!UICONTROL + Hinzufügen]**.
* Klicken Sie im Segment-Manager auf einen Segmenttitel, um das Segment im Segmentaufbau zu bearbeiten.

![](assets/segment_builder_ui.png)

1. **[!UICONTROL Titel]**: Hiermit können Sie das Segment benennen oder umbenennen.
1. **[!UICONTROL Beschreibung]**: Geben Sie eine Beschreibung für das Segment ein. Wenn Sie das Segment freigeben möchten, ist die Eingabe einer Beschreibung erforderlich.
1. **[!UICONTROL Tags]**: [Kennzeichnen Sie das Segment](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md), das Sie erstellen, mit einem Tag, indem Sie ein vorhandenes es aus der Liste auswählen oder ein neues erstellen.
1. **[!UICONTROL Definitionen]**: Dies ist der Bereich, in dem Sie [Segmente erstellen und konfigurieren](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md), Regeln hinzufügen und Container verschachteln und sequenzieren. Hier können Sie eine Beschreibung für das neue Segment angeben, indem Sie den Behälter auswählen und Dimensionen, Segmente oder Metriken in die Definition ziehen und dort ablegen.
1. **[!UICONTROL Anzeigen]**: (Auswahl des obersten Containers.) Hiermit können Sie die Ebene des [Containers](/help/components/c-segmentation/seg-overview.md) der obersten Ebene auswählen ([!UICONTROL Besucher], [!UICONTROL Besuch], [!UICONTROL Treffer]). Standardmäßig ist der Trefferbehälter der Behälter der obersten Ebene.
1. **[!UICONTROL Optionen]**: (Zahnrad)-Symbol

   * **[!UICONTROL Behälter hinzufügen]**: Hiermit fügen Sie (unter dem obersten Behälter) einen neuen Behälter zur Segmentdefinition hinzu.
   * **[!UICONTROL Behälter aus Auswahl hinzufügen]**: Hiermit erstellen Sie einen neuen Behälter aus den im Feld „Definitionen“ ausgewählten Elementen.
   * **[!UICONTROL Ausschließen]**: Hiermit definieren Sie das Segment, indem Sie eine oder mehrere Dimensionen, Segmente oder Metriken ausschließen.

1. **[!UICONTROL Attributionsmodelle]**: Für die Dimensionssegmentierung. Dimensionsmodelle sind besonders bei der sequenziellen Segmentierung nützlich, z. B. bei denen, die Flussvisualisierungen unterstützen:

   * **[!UICONTROL Wiederholen]** ((Standardeinstellung)): Umfasst Instanzen und beibehaltene Werte für die Dimension.
   * **[!UICONTROL Instanz]**: Umfasst Instanzen für die Dimension.
   * **[!UICONTROL Nicht wiederholende Instanz]**: Umfasst eindeutige Instanzen (nicht wiederholend) für die Dimension.
   ![](assets/attribution-models.jpg)

1. **[!UICONTROL Vergleich]**: Sie können Werte mithilfe ausgewählter Operatoren vergleichen und beschränken.
1. **[!UICONTROL Dimensionen]**: Dimensionen werden aus der Liste der Dimensionen (orangefarbene Seitenleiste) gezogen und abgelegt.
1. **[!UICONTROL Wert]**: Der Wert, den Sie für die Dimension, das Segment oder die Metrik eingegeben oder ausgewählt haben.
1. **[!UICONTROL Und/Oder/Dann]**: Weist die [!UICONTROL UND/ODER/DANN]-Operatoren zwischen Containern oder Regeln zu. Mit dem Operator „DANN“ können Sie [sequenzielle Segmente definieren](/help/components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md).
1. **[!UICONTROL Metrik]** (Grüne Seitenleiste): Metrik, die aus der Liste „Metriken“ gezogen und abgelegt wurde.
1. Operator **[!UICONTROL Vergleich]**: Sie können Werte mithilfe ausgewählter Operatoren vergleichen und beschränken.
1. **[!UICONTROL Wert]**: Der Wert, den Sie für die Dimension, das Segment oder die Metrik eingegeben oder ausgewählt haben.
1. **[!UICONTROL X]** (Löschen): Hiermit können Sie diesen Teil der Segmentdefinition löschen.
1. **[!UICONTROL Speichern]** oder **[!UICONTROL Abbrechen]**: Speichert oder bricht das Segment ab. Nachdem Sie auf **[!UICONTROL Speichern]** geklickt haben, gelangen Sie zum Segment-Manager, in dem Sie das Segment verwalten können.
1. **[!UICONTROL Suche]**: Durchsucht die Liste der Dimensionen, Segmente oder Metriken.
1. **[!UICONTROL Dimensionen]** (Liste): Klicken Sie auf die Kopfzeile zum Erweitern.
1. **[!UICONTROL Metriken]**: Klicken Sie auf die Kopfzeile zum Erweitern.
1. **[!UICONTROL Segmente]**: Klicken Sie auf die Kopfzeile zum Erweitern.
1. **[!UICONTROL Report Suite-Auswahl]**: Erlaubt die Auswahl der Report Suite, unter der dieses Segment gespeichert wird. Sie können das Segment weiterhin in allen Report Suites verwenden.
1. **[!UICONTROL Segmentvorschau]**: Liefert eine Vorschau der Schlüsselmetriken, die anzeigen, ob es sich um ein gültiges Segment handelt und wie breit das Segment ist. Stellt eine Aufschlüsselung des Datensatzes dar, den Sie erwarten können, wenn Sie dieses Segment anwenden. Zeigt 3 konzentrische Kreise und eine Liste mit der Anzahl und dem Prozentsatz der Übereinstimmungen für [!UICONTROL Treffer], [!UICONTROL Besuche] und [!UICONTROL Besucher] für einen mit diesem Segment ausgeführten Datensatz. Dieses Diagramm wird beim Erstellen oder Ändern der Segmentdefinition sofort aktualisiert.
1. **[!UICONTROL Produktkompatibilität]**: Liefert eine Liste der Produkte von Adobe Analytics (Analysis Workspace, [!UICONTROL Reports &amp; Analytics], Ad Hoc Analysis, Data Warehouse), mit denen das von Ihnen erstellte Segment kompatibel ist. Die meisten Segmente sind mit allen Produkten kompatibel. Es sind jedoch nicht alle Operatoren und Dimensionen mit allen Analytics-Produkten kompatibel. Dies betrifft insbesondere  [Data Warehouse](/help/components/c-segmentation/seg-reference/seg-compatibility.md). Dieses Diagramm wird bei Änderungen der Segmentdefinition sofort aktualisiert.

Die Funktionsweise von Segmenten mit eingebetteten Datumsbereichen ist in Analysis Workspace und [!UICONTROL Reports &amp; Analytics] weiterhin unterschiedlich: In Workspace wird der Datumsbereich des Bedienfelds mit dem eingebetteten Datumsbereich des Segments überschrieben. Im Gegensatz dazu erhalten Sie in [!UICONTROL Reports &amp; Analytics] die Schnittmenge des Datumsbereichs des Berichts und des eingebetteten Datumsbereichs des Segments.

**[!UICONTROL In Experience Cloud veröffentlichen (für`<report suite name>`)]** (Nicht auf dem Bildschirm angezeigt): Diese Option wird nur angezeigt, wenn die Report Suite, in der Sie dieses Segment speichern, [für die Experience Cloud aktiviert](/help/components/c-segmentation/c-segmentation-workflow/seg-workflow.md) ist. Durch die Veröffentlichung eines Segments in der Experience Cloud können Sie das Segment für Marketingaktivitäten in der [!UICONTROL Zielgruppenbibliothek], [!DNL Target] und [!DNL Audience Manager] verwenden. Ein Segmenttitel und eine Beschreibung sind erforderlich.

>[!NOTE] In Analytics können Sie ein veröffentlichtes Segment bearbeiten oder löschen. Wird das Segment aktuell verwendet, wird ein Warnhinweis eingeblendet, wenn Sie das Segment bearbeiten. Ein veröffentlichtes Segment, das aktuell in Adobe [!DNL Target] verwendet wird, kann nicht gelöscht werden.

![](assets/segment_publish_to_mac_copy.png)

>[!IMPORTANT]
>
>Begrenzen Sie die Anzahl der von Analytics freigegebenen Zielgruppen auf 20, um zusätzliche Verarbeitungsverzögerungen zu vermeiden. Zielgruppen, die von der Experience Cloud und Analytics gemeinsam verwendet werden, dürfen nicht mehr als 20 Millionen eindeutige Mitglieder umfassen. Aufgrund der Caching-Funktion wird zudem die Löschung von Report Suites in Analytics erst nach 12 Stunden durch Experience Cloud übernommen.

>[!IMPORTANT]
>
>Wenn ein Besucher in die in Analytics freigegebene Zielgruppe aufgenommen wird, ist diese Information erst mit einer Verzögerung von 24 bis 48 Stunden in [!DNL Target], [!DNL Advertising Cloud] und [!DNL Campaign] verfügbar.

## Segmente erstellen {#build-segments}

1. Ziehen Sie einfach eine Dimension, ein Segment oder ein metrisches Ereignis aus dem linken Fenster in das Feld [!UICONTROL Definitionen].

   ![](assets/drag_n_drop_dimension.png)

   Nach dem Ziehen eines Elements in das Feld [!UICONTROL Definitionen] wird der standardmäßige [!UICONTROL Trefferbehälter] der obersten Ebene angezeigt. Über das Dropdown-Menü **[!UICONTROL Anzeigen]** können Sie den Behältertyp in „Besuch“ oder „Besucher“ ändern.

1. Legen Sie den [Operator](/help/components/c-segmentation/seg-reference/seg-operators.md) im Dropdown-Menü fest.
1. Geben Sie für das ausgewählte Element einen Wert ein oder wählen Sie einen aus.
1. Fügen Sie, sofern erforderlich, mithilfe von **[!UICONTROL Und]**-, **[!UICONTROL Oder]**- oder **[!UICONTROL Dann]**-Regeln weitere Behälter hinzu.
1. Sehen Sie sich nach dem Platzieren der Behälter und dem Festlegen der Regeln rechts oben im Validierungsdiagramm die Ergebnisse des Segments an. Der Validator zeigt den Prozentsatz und die absolute Anzahl der Seitenansichten, Besuche und Unique Visitors an, die mit dem erstellten Segment übereinstimmen.
1. Taggen Sie unter **[!UICONTROL Tags]** [](/help/components/c-segmentation/c-segmentation-workflow/seg-tag.md) den Behälter, indem Sie ein vorhandenes Tag auswählen oder ein neues erstellen.
1. Klicken Sie zum **[!UICONTROL Speichern]** des Segments auf Speichern.

Sie gelangen jetzt zum [Segment-Manager](/help/components/c-segmentation/c-segmentation-workflow/seg-manage.md). Dort können Sie Ihr Segment auf verschiedene Arten taggen, freigeben und verwalten.

## Erstellen und Verschachteln von Containern {#section_1C38F15703B44474B0718CEF06639EFD}

Sie können [einen Rahmen aus Containern](/help/components/c-segmentation/seg-overview.md) erstellen und dann Logikregeln und Operatoren dazwischen platzieren.

1. Klicken Sie auf **[!UICONTROL Optionen > Behälter hinzufügen]**.

   ![](assets/add_container.png)

   Daraufhin wird ein neuer [!UICONTROL Trefferbehälter] ohne identifizierten [!UICONTROL Treffer] (Seitenansicht) geöffnet.

   ![](assets/new_container.png)

1. Ändern Sie gegebenenfalls den Behältertyp.
1. Ziehen Sie eine Dimension, ein Segment oder ein Ereignis aus dem linken Fenster in den Behälter.
1. Fügen Sie oben in der Definition weitere neue Behälter über die Schaltfläche **[!UICONTROL Optionen]** > **[!UICONTROL Behälter hinzufügen]** der obersten Ebene hinzu oder fügen Sie Behälter aus einem Behälter hinzu, um die Logik zu verschachteln.

   **ODER**

   Wählen Sie eine oder mehrere Regeln aus und klicken Sie anschließend auf **[!UICONTROL Optionen]** > **[!UICONTROL Behälter aus Auswahl hinzufügen]**. Dadurch wird Ihre Auswahl zu einem separaten Behälter.

## Verwenden von Datumsbereichen in Segmenten {#concept_252A83D43B6F4A4EBAB55F08AB2A1ACE}

Sie können Segmente erstellen, die rollierende Datumsbereiche enthalten, um Fragen zu laufenden Kampagnen oder Ereignissen zu beantworten.

Sie können beispielsweise ganz einfach ein Segment erstellen, das „alle, die etwas in den vergangenen 60 Tagen gekauft haben“ beinhaltet.

Erstellen Sie einen Behälter „Besuch“ und fügen Sie den Zeitraum [!UICONTROL Letzte 60 Tage] und die Metrik [!UICONTROL Menge größer als oder gleich 1] mit einem AND-Operator hinzu:

![](assets/date-ranges.png)

## Stapeln von Segmenten {#task_58140F17FFD64FF1BC30DC7B0A1B0E6D}

Für die Stapelung von Segmenten werden die Kriterien der einzelnen Segmente mit einem „Und“-Operator kombiniert und dann gemeinsam angewendet.

Wenn Sie z. B. ein Segment „Mobiltelefonbenutzer“ und ein Segment „US-Geographie“ stapeln, werden ausschließlich Daten für Mobiltelefonbenutzer in den USA geliefert.

Stellen Sie sich diese Segmente als Bausteine oder Module vor, die Sie in eine Segmentbibliothek aufnehmen können, damit Benutzer diese verwenden können, wenn sie passend erscheinen. Auf diese Art können Sie die Anzahl der benötigten Segmente drastisch reduzieren. Angenommen, Sie haben 40 Segmente:

* 20 für Mobiltelefonbenutzer in verschiedenen Ländern (USA_mobil, Deutschland_mobil, Frankreich_mobil, Brasilien_mobil usw.)
* 20 für Tabletbenutzer in verschiedenen Ländern (USA_tablet, Deutschland_tablet, Frankreich_tablet, Brasilien_tablet usw.)

Indem Sie die Segmentstapelung nutzen, können Sie Ihre Segmente auf 22 verringern und diese bei Bedarf stapeln. Sie müssten folgende Segmente erstellen:

* ein Segment für Mobilbenutzer
* ein Segment für Tabletbenutzer
* 20 Segmente für die verschiedenen Regionen

>[!NOTE] Wenn Sie zwei Segmente stapeln, werden diese standardmäßig durch eine UND-Anweisung verbunden. Dies kann nicht in eine ODER-Anweisung geändert werden.

1. Wechseln Sie zum Segmentaufbau.
1. Geben Sie einen Titel und eine Beschreibung für das Segment ein.

   Schritt Ergebnis 1. Klicken Sie auf **[!UICONTROL Segmente anzeigen]**, um in der linken Navigation eine Liste der Segment anzuzeigen.

   Schritt Ergebnis 1. Ziehen Sie die Segmente, die Sie stapeln möchten, in die Arbeitsfläche der Segmentdefinition. Hier sehen Sie ein Beispiel eines Segments, das die vorhandenen Segmente „Besuche von Tablets“ und „US-Geo“ stapelt:

   ![](assets/seg_stack2.png)

1. Speichern Sie das Segment.

   Schritt Ergebnis

## Verwenden von Segmentvorlagen {#concept_5098446CC78D441E93B8E4D1D1EA6558}

Vorlagen stellen die alten vorkonfigurierten und nützlichen Segmente dar.

Klicken Sie im Segment-Manager auf **[!UICONTROL Hinzufügen]**. Dadurch gelangen Sie zum Segment Builder. Klicken Sie dann auf das Segmentsymbol ![](assets/segment_icon.png),

um die Segmentleiste aufzurufen. Die Segmentvorlagen werden am Ende der Segmentliste angezeigt. Sie sind durch ein Ordnersymbol links neben dem Vorlagennamen gekennzeichnet:

![](assets/seg_template.png)

Sie können diese Vorlagen in die Arbeitsfläche für die Definitionen ziehen und sie dort so verwenden, wie sie definiert wurden, oder vorher anpassen.

<table id="table_98B87D807E9344C9BEBF072C65D87B1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vorlagenname </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Warenkorb vorzeitig verlassen </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die Elemente zum Warenkorb hinzugefügt, aber nichts bestellt haben. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel für dieses sequenzielle Segment ist <p> Zusätze zum Warenkorb ist nicht null </p> <p>Dann </p> <p>Bestellungen gleich 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Erstbesuche </td> 
   <td colname="col2">Daten zu Besuchern mit maximal einem [1] Besuch anzeigen. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Besuchsnummer gleich 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nichtkäufer </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die nicht zu einem Bestellereignis beitrugen. In der Segmentdefinition ist der Behälter „Besucher“. Dieses Segment verwendet die Ausschließen-Logik. Die Regel ist <p>Bestellungen ist nicht null. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nicht-Einzelseitenbesuche (Keine Absprünge) </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die mehr als einen Besuch ausgeführt haben. In der Segmentdefinition ist der Behälter „Besucher“. Dieses Segment verwendet die Ausschließen-Logik. Die Regel ist <p>Einzelzugriff ist nicht null. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Paid Search </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die von einer gebührenpflichtigen Suche stammen. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Gebührenpflichtige Sucherkennung gleich 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Käufern </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die zu einem Bestellereignis beitrugen. In der Segmentdefinition ist der Behälter „Besucher“. Die Regel ist <p>Bestellungen ist nicht null. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rückkehrende Besucher </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die mindestens einen Besuch durchgeführt haben. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Besuchsnummer ist größer als 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Einzelseitenbesuche </td> 
   <td colname="col2"> Daten zu Besuchen anzeigen, bei denen ein Einzelseitenwert vorliegt, auch wenn während des Besuchs mehrere Seitenansichten übermittelt werden. Einzelseitenbesuche mit Exitlink-Ereignissen werden in das Segment einbezogen. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Einzelseitenbesuche gleich 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Angesehenes Produkt wurde nicht dem Warenkorb hinzugefügt </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die Produkte angesehen, aber keine zum Warenkorb hinzugefügt haben. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel für dieses sequenzielle Segment ist <p>Produktansichten ist nicht null </p> <p>Dann </p> <p> Warenkorbzusätze gleich 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche von Kampagnen </td> 
   <td colname="col2">Daten zu Besuchern aus Kampagnen anzeigen. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Trackingcode ist nicht null. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche von Mobilgeräten </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die Mobilgeräte verwenden. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Mobiles Gerät ist ungleich null. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche über eine kostenlose Suche </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die nicht von einer gebührenpflichtigen Suche stammen. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Gebührenpflichtige Sucherkennung gleich 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche von Nicht-Mobilgerät </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die kein Mobilgerät verwenden. In der Segmentdefinition ist der Behälter „Besuche“. Dieses Segment verwendet die Ausschließen-Logik. Die Regel ist <p>Mobilgerätetyp gleich Mobiltelefon </p> <p>Oder </p> <p>Mobilgerätetyp gleich Tablet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche von Smartphones </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die Smartphones verwenden. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Gerätetyp gleich Mobiltelefon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche über Suchmaschinen </td> 
   <td colname="col2">Daten zu Besuchern aus Suchmaschinen anzeigen. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Referrer-Typ gleich Suchmaschinen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche von sozialen Netzwerken aus </td> 
   <td colname="col2">Daten zu Besuchern aus sozialen Netzwerken anzeigen. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Referrer-Typ gleich soziale Netzwerke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche von Tablets </td> 
   <td colname="col2">Daten zu Besuchern anzeigen, die Tablets verwenden. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Gerätetyp gleich Tablet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuche mit Besucher-ID-Cookie </td> 
   <td colname="col2">Daten zu Besuchern Ihrer Site anzeigen, für die ein persistentes Cookie erforderlich ist. In der Segmentdefinition ist der Behälter „Besuche“. Die Regel ist <p>Beständiges Cookie gleich 1. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel: Kampagnenbesuchersegment {#concept_61AC6115097B4EB3AEFE8CE98F38315D}

Präsentiert ein Beispiel für dieses häufig verwendete Segment.

Viele Kunden möchten Metriken von Besuchern sehen, die auf bestimmte Kampagnen reagiert haben. Das Erstellen eines Kampagnenbesuchersegments bietet eine einfache Möglichkeit, diese Daten zu erhalten.

Wenn Sie dieses Segment im Segmentaufbau erstellen, ziehen Sie eine Kampagnendimension – in diesem Fall „Kampagnenname“ – in einen Besuchebehälter der obersten Ebene:

![](assets/seg_campaign_visitor.png)

(Optional) Sie können auch ein Kampagnen-Tag auf dieses Segment anwenden, wenn Sie Ihre gesamten kampagnenbezogenen Segmente auf einfache Art filtern möchten.
