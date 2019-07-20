---
description: Der Segmentaufbau bietet eine Arbeitsfläche zum Ziehen und Ablegen von metrischen Dimensionen, Segmenten und Ereignissen für das Segmentieren von Besuchern auf der Grundlage von Behälterhierarchielogik, Regeln und Operatoren. Mit diesem integrierten Entwicklungstool können Sie einfache oder komplexe Segmente erstellen und speichern, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden.
seo-description: Der Segmentaufbau bietet eine Arbeitsfläche zum Ziehen und Ablegen von metrischen Dimensionen, Segmenten und Ereignissen für das Segmentieren von Besuchern auf der Grundlage von Behälterhierarchielogik, Regeln und Operatoren. Mit diesem integrierten Entwicklungstool können Sie einfache oder komplexe Segmente erstellen und speichern, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden.
seo-title: Segmente erstellen
solution: Analytics
title: Segmente erstellen
topic: Segmente
uuid: c 01393 df-ccdd -431 c -83 a 6-3 c 2700 bd 4999
translation-type: tm+mt
source-git-commit: e3b1ac3139f26ca3a97f3d2228276e690ec4cb79

---


# Segmentaufbau

Der Segmentaufbau bietet eine Arbeitsfläche zum Ziehen und Ablegen von metrischen Dimensionen, Segmenten und Ereignissen für das Segmentieren von Besuchern auf der Grundlage von Behälterhierarchielogik, Regeln und Operatoren. Mit diesem integrierten Entwicklungstool können Sie einfache oder komplexe Segmente erstellen und speichern, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden.

Der [!UICONTROL Segmentaufbau] bietet eine Arbeitsfläche zum Ziehen und Ablegen von metrischen Dimensionen, Segmenten und Ereignissen für das Segmentieren von Besuchern auf der Grundlage von Behälterhierarchielogik, Regeln und Operatoren. Mit diesem integrierten Entwicklungstool können Sie einfache oder komplexe Segmente erstellen und speichern, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden.

>[!IMPORTANT]
>
>In der Version Juni 2019 wurden Dimensionszuordnungsmodelle eingeführt. Siehe # 6 unter Funktionen der Web-Benutzeroberfläche.

Es gibt mehrere Möglichkeiten für den Zugriff auf den Segmentaufbau:

* **Navigation in Analytics:** Klicken **[!UICONTROL Sie auf Analysen]** &gt; **[!UICONTROL Komponenten]** &gt; **[!UICONTROL Segmente]**.
* **[!UICONTROL Analysis Workspace]:** Klicken **[!UICONTROL Sie auf Analysen]** &gt; **[!UICONTROL Arbeitsbereich]**, öffnen Sie ein Projekt und klicken **[!UICONTROL Sie auf + Neu]** &gt; **[!UICONTROL Segment erstellen]**.
* **[!UICONTROL Reports &amp; Analysen]:** Klicken Sie auf **[!UICONTROL Analysen]** &gt; **[!UICONTROL Berichte]**, öffnen Sie einen vorhandenen Bericht und klicken Sie in der linken Navigation auf das Segmentsymbol ![](assets/segment_icon.png) und anschließend **[!UICONTROL auf Hinzufügen]**.
* **[!UICONTROL Ad-hoc-Analysen]:**[Segmente in Ad-hoc-Analysen erstellen](../../../components/c-segmentation/c-segmentation-workflow/seg-build.md#section_E440630183D64999BA2369D1B8048AA6).
* **[!UICONTROL Reportbuilder]:**[Segmente in Reportbuilder hinzufügen oder bearbeiten](https://marketing.adobe.com/resources/help/en_US/arb/segmentation.html).

## Segment Builder user interface {#concept_643F2DF74C544796B58F4656ABC5F726}

Mit dem [!UICONTROL Segmentaufbau] können Sie einfache oder komplexe Segmente erstellen, mit deren Hilfe Besucherattribute und Aktionen bei Besuchen und Seitentreffern identifiziert werden. Er bietet eine Arbeitsfläche zum Ziehen und Ablegen von metrischen Dimensionen, Ereignissen und anderen Segmenten, um Besucher mithilfe von Hierarchielogik, Regeln und Operatoren zu segmentieren.

## Funktionen der Web-Benutzeroberfläche {#section_F61C4268A5974C788629399ADE1E6E7C}

Mit [!UICONTROL Segment Builder] können Sie Segmente über die Web-Benutzeroberfläche (oder eine [Java-Benutzeroberfläche in Ad-hoc-Analysen](../../../components/c-segmentation/c-segmentation-workflow/seg-workflow.md#section_E440630183D64999BA2369D1B8048AA6)) erstellen und bearbeiten. Sie können Regeldefinitionen und Behälter hinzufügen, um Ihre Segmente zu verfeinern, zu stapeln und zu verschachteln. Sie können auch prüfen, wie viele Seitenansichten, Besuche und Unique Visitors aus der aktuellen Segmentdefinition resultieren. Speichern Sie dann das Segment für den künftigen Bedarf.

Sie können wie folgt auf den Segmentaufbau zugreifen

* öffnen Sie einen vorhandenen Bericht und klicken Sie auf das Segmentsymbol ![ im linken Navigationsmenü. ](assets/segment_icon.png) Klicken Sie in der angezeigten Segmentleiste auf **[!UICONTROL Hinzufügen]**.

* Klicken Sie im Segment-Manager auf **[!UICONTROL + Hinzufügen]**.
* Klicken Sie im Segment-Manager auf einen Segmenttitel, um das Segment im Segmentaufbau zu bearbeiten.

![](assets/segment_builder_ui.png)

1. **[!UICONTROL Titel:]** Hiermit können Sie das Segment benennen oder umbenennen.
1. **[!UICONTROL Beschreibung:]** Geben Sie eine Beschreibung für das Segment ein. Wenn Sie das Segment freigeben möchten, ist die Eingabe einer Beschreibung erforderlich.
1. **[!UICONTROL Tags:]**[Markieren Sie das Segment, das](../../../components/c-segmentation/c-segmentation-workflow/seg-workflow.md#concept_CD892CEB326C4986A1B67487052DBA50) Sie erstellen, indem Sie es aus einer Liste vorhandener Tags auswählen oder ein neues Tag erstellen.
1. **[!UICONTROL Definitionen:]** Hier [erstellen und konfigurieren Sie Segmente](../../../components/c-segmentation/c-segmentation-workflow/seg-workflow.md#concept_BD4C17B01C5B4E378D0C14C852D055D4), fügen Regeln hinzu und verschachteln Behälter und sequenzieren Behälter. Hier können Sie eine Beschreibung für das neue Segment angeben, indem Sie den Behälter auswählen und Dimensionen, Segmente oder Metriken in die Definition ziehen und dort ablegen.
1. **[!UICONTROL Anzeigen:]** (Top Container Selector.) Lets you select the top-level [container](../../../components/c-segmentation/seg-overview.md#concept_A38E7000056547399E346559D85E2551) ( [!UICONTROL Visitor], [!UICONTROL Visit], [!UICONTROL Hit]). Standardmäßig ist der Trefferbehälter der Behälter der obersten Ebene.
1. **[!UICONTROL Optionen:]** (Zahnradsymbol)

   * **[!UICONTROL + Behälter hinzufügen:]** Ermöglicht das Hinzufügen eines neuen Behälters (unterhalb des Behälters der obersten Ebene) zur Segmentdefinition.
   * **[!UICONTROL + Behälter aus Auswahl hinzufügen:]** Sie können einen neuen Behälter aus dem Element/der s erstellen, das Sie (mehrere) im Feld Definitionen ausgewählt haben.
   * **[!UICONTROL Ausschließen:]** Hiermit können Sie das Segment definieren, indem Sie eine oder mehrere Dimensionen, Segmente oder Metriken ausschließen.
   **[!UICONTROL Zuordnungsmodelle:]** Für die Dimensionssegmentierung. Dimensionsmodelle sind besonders in der sequenziellen Segmentierung nützlich, z. B. in solchen, die Flussvisualisierungen unterstützen:
   * **[!UICONTROL Wiederholen]** ((Standard)): Umfasst Instanzen und beibehaltene Werte für die Dimension.
   * **[!UICONTROL Instanz]**: Umfasst Instanzen für die Dimension.
   * **[!UICONTROL Nicht wiederholende Instanz]**: Enthält eindeutige Instanzen (nicht wiederholend) für die Dimension.
   ![](assets/attribution-models.jpg)

1. **[!UICONTROL Dimensionen:]** Dimension wird aus der Liste Dimensionen (orange Seitenleiste) gezogen und abgelegt.
1. **[!UICONTROL Vergleich:]** Sie können Werte mithilfe ausgewählter Operatoren vergleichen und beschränken.
1. **[!UICONTROL Wert:]** Der Wert, den Sie für die Dimension oder das Segment oder die Metrik eingegeben oder ausgewählt haben.
1. **[!UICONTROL Und/Oder/Dann]**: Weist die [!UICONTROL Operatoren AND/ODER/DANN] zwischen Behältern oder Regeln zu. The THEN operator lets you [define sequential segments](../../../components/c-segmentation/c-segmentation-workflow/seg-sequential-build.md#concept_83AEC78CD25F442EBEE364856A889560).
1. **[!UICONTROL Metrik: (Grüne Seitenleiste) Die Metrik, die aus der Liste "Metriken" gezogen und abgelegt wurde.]**
1. **[!UICONTROL Vergleichsoperator]** : Sie können Werte mithilfe ausgewählter Operatoren vergleichen und beschränken.
1. **[!UICONTROL Wert]**: Der Wert, den Sie für die Dimension oder das Segment oder die Metrik eingegeben oder ausgewählt haben.
1. **[!UICONTROL X]**: (Löschen) Hiermit können Sie diesen Teil der Segmentdefinition löschen.
1. **[!UICONTROL Speichern]** oder **[!UICONTROL Abbrechen]**: Speichert das Segment oder bricht es ab. After clicking **[!UICONTROL Save]**, you are taken to the Segment Manager where you can manage the segment.
1. **[!UICONTROL Suchen:]** Durchsucht die Liste der Dimensionen, Segmente oder Metriken.
1. **[!UICONTROL Dimensionen:]** (Liste) Klicken Sie auf die Kopfzeile, um sie zu erweitern.
1. **[!UICONTROL Metriken:]** Klicken Sie auf die Kopfzeile, um sie zu erweitern.
1. **[!UICONTROL Segmente:]** Klicken Sie auf die Kopfzeile, um sie zu erweitern.
1. **[!UICONTROL Report Suite-Auswahl:]** Sie können die Report Suite auswählen, unter der dieses Segment gespeichert wird. Sie können das Segment weiterhin in allen Report Suites verwenden.
1. **[!UICONTROL Segmentvorschau:]** Sie können eine Vorschau der Schlüsselmetriken anzeigen, um zu sehen, ob Sie über ein gültiges Segment verfügen und wie breit das Segment ist. Stellt eine Aufschlüsselung des Datensatzes dar, den Sie erwarten können, wenn Sie dieses Segment anwenden. Zeigt 3 konzentrische Kreise und eine Liste mit der Anzahl und dem Prozentsatz der Übereinstimmungen für [!UICONTROL Treffer], [!UICONTROL Besuche] und [!UICONTROL Besucher] für einen mit diesem Segment ausgeführten Datensatz. Dieses Diagramm wird beim Erstellen oder Ändern der Segmentdefinition sofort aktualisiert.
1. **[!UICONTROL Produktkompatibilität:]** Liefert eine Liste der Adobe Analytics-Produkte (Analysis Workspace, [!UICONTROL Reports &amp; Analysen], Ad-hoc-Analysen, Data Warehouse), mit denen das erstellte Segment kompatibel ist. Die meisten Segmente sind mit allen Produkten kompatibel. Es sind jedoch nicht alle Operatoren und Dimensionen mit allen Analytics-Produkten kompatibel. Dies betrifft insbesondere [Data Warehouse](../../../components/c-segmentation/seg-reference/seg-compatibility.md#concept_7A2CC00352274A75ACD4949CA3C144D4). Dieses Diagramm wird bei Änderungen der Segmentdefinition sofort aktualisiert.

   Segments with embedded date ranges continue to operate differently in Analysis Workspace versus [!UICONTROL Reports &amp; Analytics]: In Workspace, a segment with an embedded date range overrides the panel date range. By contrast, [!UICONTROL Reports &amp; Analytics] gives you the intersection of the report date range and the segment's embedded date range.

**[!UICONTROL Veröffentlichen in Experience Cloud (for`<report suite name>`)]**: (Wird auf dem Bildschirm nicht angezeigt) Diese Option wird nur angezeigt, wenn die Report Suite, für die Sie dieses Segment speichern, [für die Experience Cloud aktiviert](../../../components/c-segmentation/c-segmentation-workflow/seg-workflow.md#concept_1E9FC92437D748C392546542B6511D01)ist. By publishing a segment to the Experience Cloud, you can use the segment for marketing activity in the [!UICONTROL Audience Library], [!DNL Target], and [!DNL Audience Manager]. Ein Segmenttitel und eine Beschreibung sind erforderlich.

>[!NOTE]
>
>In Analytics können Sie ein veröffentlichtes Segment bearbeiten oder löschen. Wird das Segment aktuell verwendet, wird ein Warnhinweis eingeblendet, wenn Sie das Segment bearbeiten. Ein veröffentlichtes Segment, das aktuell in Adobe [!DNL Target] verwendet wird, kann nicht gelöscht werden.

![](assets/segment_publish_to_mac_copy.png)

>[!IMPORTANT]
>
>Sie müssen die Anzahl der für Analytics freigegebenen Zielgruppen auf 20 beschränken, um zusätzliche Verarbeitungsverzögerungen zu vermeiden. Zielgruppen, die von der Experience Cloud und Analytics gemeinsam verwendet werden, dürfen nicht mehr als 20 Millionen eindeutige Mitglieder umfassen. Aufgrund der Caching-Funktion wird die Löschung von Report Suites in Analytics erst nach 12 Stunden durch die Experience Cloud übernommen.

>[!IMPORTANT]
>
>Once a visitor qualifies for the audience shared from Analytics, there is a 24 - 48 hour delay before that information is actionable in [!DNL Target], [!DNL Advertising Cloud], and [!DNL Campaign].

## Build segments {#section_050E3343533E45C3923242398E0E0213}

1. Ziehen Sie einfach eine Dimension, ein Segment oder ein metrisches Ereignis aus dem linken Fenster in das Feld [!UICONTROL Definitionen].

   ![](assets/drag_n_drop_dimension.png)

   Nach dem Ziehen eines Elements in das Feld [!UICONTROL Definitionen] wird der standardmäßige [!UICONTROL Trefferbehälter] der obersten Ebene angezeigt. Über das Dropdown-Menü **[!UICONTROL Anzeigen]können Sie den Behältertyp in „Besuch“ oder „Besucher“ ändern.**

1. Set the [operator](../../../components/c-segmentation/seg-reference/seg-operators.md) from the drop-down menu.
1. Geben Sie für das ausgewählte Element einen Wert ein oder wählen Sie einen aus.
1. Add additional containers if needed, using **[!UICONTROL And]**, **[!UICONTROL Or]**, or **[!UICONTROL Then]** rules.
1. Sehen Sie sich nach dem Platzieren der Behälter und dem Festlegen der Regeln rechts oben im Validierungsdiagramm die Ergebnisse des Segments an. Der Validator zeigt den Prozentsatz und die absolute Anzahl der Seitenansichten, Besuche und Unique Visitors an, die mit dem erstellten Segment übereinstimmen.
1. Under **[!UICONTROL Tags]**, [tag](../../../components/c-segmentation/c-segmentation-workflow/seg-tag.md#concept_CD892CEB326C4986A1B67487052DBA50) the container by selecting an existing tag or creating a new one.
1. Klicken Sie zum Speichern des Segments auf **[!UICONTROL Speichern.]**

You are now taken to the [Segment Manager](../../../components/c-segmentation/c-segmentation-workflow/seg-manage.md#concept_7A2E019317864065B7C641DC3315928F), where you can tag, share, and manage your segment in multiple ways.

## Build and nest containers {#section_1C38F15703B44474B0718CEF06639EFD}

You can [build a framework of containers](../../../components/c-segmentation/seg-overview.md#concept_82653C7E29FE49F5A4B5E5E93B0A6399) and then place logic rules and operators between.

1. Klicken Sie auf **[!UICONTROL Optionen &gt; Behälter hinzufügen]**.

   ![](assets/add_container.png)

   Daraufhin wird ein neuer [!UICONTROL Trefferbehälter] ohne identifizierten [!UICONTROL Treffer] (Seitenansicht) geöffnet.

   ![](assets/new_container.png)

1. Ändern Sie gegebenenfalls den Behältertyp.
1. Ziehen Sie eine Dimension, ein Segment oder ein Ereignis aus dem linken Fenster in den Behälter.
1. Continue to add new containers from the top-level **[!UICONTROL Options]** &gt; **[!UICONTROL Add container]** button at the top of the definition, or add containers from within a container to nest logic.

   **ODER**

   Select one or more rules and then click **[!UICONTROL Options]** &gt; **[!UICONTROL Add container from selection]**. Dadurch wird Ihre Auswahl zu einem separaten Behälter.

## Use date ranges in segments {#concept_252A83D43B6F4A4EBAB55F08AB2A1ACE}

Sie können Segmente erstellen, die rollierende Datumsbereiche enthalten, um Fragen zu laufenden Kampagnen oder Ereignissen zu beantworten.

Sie können beispielsweise ganz einfach ein Segment erstellen, das „alle, die etwas in den vergangenen 60 Tagen gekauft haben“ beinhaltet.

Erstellen Sie einen Behälter „Besuch“ und fügen Sie den Zeitraum [!UICONTROL Letzte 60 Tage] und die Metrik [!UICONTROL Menge größer als oder gleich 1] mit einem AND-Operator hinzu:

![](assets/date-ranges.png)

## Stack segments {#task_58140F17FFD64FF1BC30DC7B0A1B0E6D}

Für die Stapelung von Segmenten werden die Kriterien der einzelnen Segmente mit einem „Und“-Operator kombiniert und dann gemeinsam angewendet.

Wenn Sie z. B. ein Segment „Mobiltelefonbenutzer“ und ein Segment „US-Geographie“ stapeln, werden ausschließlich Daten für Mobiltelefonbenutzer in den USA geliefert.

Stellen Sie sich diese Segmente als Bausteine oder Module vor, die Sie in eine Segmentbibliothek aufnehmen können, damit Benutzer diese verwenden können, wenn sie passend erscheinen. Auf diese Art können Sie die Anzahl der benötigten Segmente drastisch reduzieren. Angenommen, Sie haben 40 Segmente:

* 20 für Mobiltelefonbenutzer in verschiedenen Ländern (USA_mobil, Deutschland_mobil, Frankreich_mobil, Brasilien_mobil usw.)
* 20 für Tabletbenutzer in verschiedenen Ländern (USA_tablet, Deutschland_tablet, Frankreich_tablet, Brasilien_tablet usw.)

Indem Sie die Segmentstapelung nutzen, können Sie Ihre Segmente auf 22 verringern und diese bei Bedarf stapeln. Sie müssten folgende Segmente erstellen:

* ein Segment für Mobilbenutzer
* ein Segment für Tabletbenutzer
* 20 Segmente für die verschiedenen Regionen

>[!NOTE]
>
>Wenn Sie zwei Segmente stapeln, werden sie standardmäßig durch eine AND-Anweisung verbunden. Dies kann nicht in eine ODER-Anweisung geändert werden.

1. Wechseln Sie zum Segmentaufbau.
1. Geben Sie einen Titel und eine Beschreibung für das Segment ein.

   Schritt 1. Klicken Sie auf **[!UICONTROL Segmente anzeigen], um in der linken Navigation eine Liste der Segment anzuzeigen.**

   Schritt 1. Ziehen Sie die Segmente, die Sie stapeln möchten, in die Arbeitsfläche der Segmentdefinition. Hier sehen Sie ein Beispiel eines Segments, das die vorhandenen Segmente „Besuche von Tablets“ und „US-Geo“ stapelt:

   ![](assets/seg_stack2.png)

1. Speichern Sie das Segment.

   Schritt Ergebnis

## Use segment templates {#concept_5098446CC78D441E93B8E4D1D1EA6558}

Vorlagen stellen die alten vorkonfigurierten und nützlichen Segmente dar.

In the Segment Manager, click **[!UICONTROL Add]**, which takes you to the Segment Builder. Now click the Segments icon  ![](assets/segment_icon.png)

, um die Segmentleiste aufzurufen. Die Segmentvorlagen werden am Ende der Segmentliste angezeigt. Sie sind durch ein Ordnersymbol links neben dem Vorlagennamen gekennzeichnet:

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
   <td colname="col1"> Gebührenpflichtige Suche </td> 
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

## Example: Campaign visitors segment {#concept_61AC6115097B4EB3AEFE8CE98F38315D}

Präsentiert ein Beispiel für dieses häufig verwendete Segment.

Viele Kunden möchten Metriken von Besuchern sehen, die auf bestimmte Kampagnen reagiert haben. Das Erstellen eines Kampagnenbesuchersegments bietet eine einfache Möglichkeit, diese Daten zu erhalten.

Wenn Sie dieses Segment im Segmentaufbau erstellen, ziehen Sie eine Kampagnendimension – in diesem Fall „Kampagnenname“ – in einen Besuchebehälter der obersten Ebene:

![](assets/seg_campaign_visitor.png)

(Optional) Sie können auch ein Kampagnen-Tag auf dieses Segment anwenden, wenn Sie Ihre gesamten kampagnenbezogenen Segmente auf einfache Art filtern möchten.
