---
description: Der Generator für berechnete Metriken bietet eine Arbeitsfläche, mit der Sie Dimensionen, Segmente und Funktionen per Drag-and-Drop verschieben können, um benutzerdefinierte Metriken basierend auf Containerhierarchielogik, Regeln und Operatoren zu erstellen. Mit diesem integrierten Entwicklungstool können Sie einfache berechnete Metriken oder komplexe, erweiterte berechnete Metriken erstellen und speichern.
title: Metriken erstellen
uuid: 3f51e911-cafa-4af4-90dd-5a4cb42bf0a7
translation-type: ht
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: ht
source-wordcount: '968'
ht-degree: 100%

---


# Metriken erstellen

Der Generator für berechnete Metriken bietet eine Arbeitsfläche, mit der Sie Dimensionen, Segmente und Funktionen per Drag-and-Drop verschieben können, um benutzerdefinierte Metriken basierend auf Containerhierarchielogik, Regeln und Operatoren zu erstellen. Mit diesem integrierten Entwicklungstool können Sie einfache berechnete Metriken oder komplexe, erweiterte berechnete Metriken erstellen und speichern.

Sie erreichen den Generator für berechnete Metriken auf verschiedene Arten:

* Öffnen Sie ein Projekt in Analysis Workspace und klicken Sie auf **[!UICONTROL + Neu]** > **[!UICONTROL Metrik erstellen]** .
* Gehen Sie in [!DNL Analytics] zu **[!UICONTROL Komponenten]** > **[!UICONTROL Berechnete Metriken]**.

* Klicken Sie oben im [Manager für berechnete Metriken](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md) auf **[!UICONTROL + Hinzufügen]** oder

* gehen Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Berichte]**, öffnen Sie einen beliebigen Bericht und klicken Sie auf das Metrikensymbol ![](assets/metrics_icon.png), um die Metrikenleiste aufzurufen. Klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

![](assets/cm_builder_ui.png)

## Komponenten der Benutzeroberfläche {#section_9382AEEBA4244DD6A9F6C1DD3F6D076B}

<table id="table_60A82936321047D1A335331BF83B0972"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Feld </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Anrede/Titel </span> </td> 
   <td colname="col3"> <p>Ein Name für die Metrik ist obligatorisch. Sie können nur benannte Metriken speichern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Beschreibung </span> </td> 
   <td colname="col3"> <p>Geben Sie der Metrik eine benutzerfreundliche Beschreibung, um ihren Zweck anzugeben und sie von ähnlichen Metriken zu unterscheiden. </p> <p>Die Beschreibung wird auch in Berichten angezeigt. Sie sollten die Formel NICHT in die Beschreibung aufnehmen. Erläutern Sie stattdessen, wofür diese Metrik verwendet werden sollte und wofür nicht. (Die Formel wird unter der Überschrift „Zusammenfassung“ generiert, während Sie die Metrik erstellen. Daher müssen Sie die Formel nicht noch der Beschreibung hinzufügen.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Format </span> </td> 
   <td colname="col3"> <p>Hier können Sie zwischen „Dezimal“, „Zeit“, „Prozent“ und „Währung“ wählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Dezimalstellen </span> </td> 
   <td colname="col3"> <p>Zeigt an, wie viele Dezimalstellen im Bericht angezeigt werden. Sie können maximal 10 Dezimalstellen angeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol">Aufwärts-Trend anzeigen als... </span> </td> 
   <td colname="col3"> <p>Diese Einstellung für die Metrikpolarität legt fest, ob Analytics einen Aufwärtstrend in der Metrik als positiv (grün) oder negativ (rot) betrachten soll. Dementsprechend wird ein steigendes Diagramm des Berichts grün oder rot angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Tags </span> </td> 
   <td colname="col3"> <p>Anhand von Tagging können Metriken praktisch organisiert werden. Alle Benutzer können Tags erstellen und eines oder mehrere Tags auf eine Metrik anwenden. Sie sehen Tags jedoch nur für die Segmente, deren Inhaber Sie sind oder die für Sie freigegeben wurden. Welche Arten von Tags sollten Sie erstellen? Hier finden Sie einige Vorschläge für nützliche Tags: 
     <ul id="ul_9A6CE5F179424687A39F2D5C1A953258"> 
      <li id="li_A8815F2D8D284874AD701A7B103D82A3">Auf <b>Teamnamen</b> basierende Tags wie Social Marketing, Mobile Marketing. </li> 
      <li id="li_A51A4515A541488E9D90296A955E9F4F"><b>Projekt</b>-Tags (Analyse-Tags) wie Entrypage-Analyse. </li> 
      <li id="li_B4605470A7094026AC168420B64BBCC3"><b>Kategorie</b>-Tags: Männer, Region. </li> 
      <li id="li_B6EAB0F2A96C41209C4EC97B9E64390B"><b>Workflow</b>-Tags: Genehmigung ausstehend, kuratiert für (einen bestimmten Geschäftsbereich). </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Zusammenfassung </span> </td> 
   <td colname="col3"> <p>Die Formel unter <span class="uicontrol">Zusammenfassung</span> wird jedes Mal, wenn Sie die Metrikdefinition ändern, aktualisiert. Diese Formel wird außerdem in der Metrikleiste links angezeigt, wenn Sie mit der Maus auf eine Metrik zeigen und auf das Symbol <img placement="inline"  src="assets/i_icon.png" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> klicken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Definition </span> </td> 
   <td colname="col3"> <p>Hierhin ziehen Sie die Metriken/berechneten Metriken, Segmente und/oder Funktionen, um die berechnete Metrik zu erstellen. </p> <p> 
     <ul id="ul_B13401A266354DC594C6176025DB61CB"> 
      <li id="li_01776C32C7C5440AA1F847096CBED92B">Wenn Sie eine berechnete Metrik hierhin ziehen, wird die zugehörige Metrikdefinition automatisch eingeblendet. </li> 
      <li id="li_A483D352522E4572AB43042473053359">Sie können Definitionen mit Containern verschachteln. Im Gegensatz zu Segmentcontainern funktionieren diese Container allerdings wie ein mathematischer Ausdruck und bestimmen die Reihenfolge der Vorgänge. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Operator </span> </td> 
   <td colname="col3"> <p>Geteilt durch ( <img placement="inline"  src="assets/divided_icon.png" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" /> ) ist der Standardoperator. Darüber hinaus gibt es die Operatoren +, - und x. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Vorschau </span> </td> 
   <td colname="col3"> <p>Ermöglicht einen schnellen Einblick in potenzielle Fehler. Die Vorschau deckt die letzten 90 Tage ab. So können Sie schnell einschätzen, ob Sie die richtigen Komponenten für die Metrik ausgewählt haben. Bei einem unerwarteten Ergebnis müssten Sie die Metrikdefinition noch einmal genauer prüfen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Produktkompatibilität </span> </td> 
   <td colname="col3"> <p>Über die Produktkompatibilität können Sie sehen, ob die Metrik mit <a href="https://docs.adobe.com/content/help/de-DE/analytics/analyze/reports-analytics/current-data.html"  >aktuellen Daten</a>, mit vollständig verarbeiteten Daten oder nur mit Marketingkanalberichten (Erstkontaktzuordnung) kompatibel ist. <p>Hinweis: Bei aktuellen Daten werden nicht alle Metriken unterstützt. Metriken mit Segmenten oder Funktionen sind nicht mit aktuellen Daten kompatibel. <a href="/help/components/c-calcmetrics/cm-compatibility.md"  > Mehr... </a> </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> Fügen Sie </span> </td> 
   <td colname="col3"> <p>Sie können Container und statische Nummern zu den Definitionen aller Arten berechneter Metriken hinzufügen. Für erweiterte berechnete Metriken können Sie auch Segmente und Funktionen hinzufügen. </p> <p> 
     <ul id="ul_607C1B303F334062BC620317667DE490"> 
      <li id="li_53462789B8AF4F1AA9B45565D37CF22B">Container funktionieren wie mathematische Ausdrücke und bestimmen die Reihenfolge der Vorgänge. Jedes Element in einem Container wird also vor dem nächsten Vorgang verarbeitet. </li> 
      <li id="li_401A9E0D8B3B468990289DBF66A06F63">Wenn Sie ein Segment in einen Container ziehen, werden alle Elemente in diesem Container segmentiert. (Nur erweiterte berechnete Metriken) </li> 
      <li id="li_F191B200D7A944F9ADC0573A9A82A6DA">Sie können mehrere Segmente in einem Container stapeln. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> Zahnradsymbol (<span class="uicontrol">Metriktyp</span>, <span class="uicontrol"> Attribution </span>) </td> 
   <td colname="col3"> <p>Wenn Sie das Zahnradsymbol neben einer Metrik auswählen, können Sie den <a href="/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/m-metric-type-alloc.md"  >Metriktyp und die Attributionsmodelle</a> angeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <span class="uicontrol"> + Neu </span> </td> 
   <td colname="col3"> <p>Ermöglicht Ihnen die Erstellung einer neuen Komponente, z. B. eines neuen Segments (Sie werden zum <a href="/help/components/segmentation/segmentation-workflow/seg-build.md"  >Segmentaufbau</a> geleitet). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Suchkomponenten </p> </td> 
   <td colname="col3"> <p>Mit dieser Suchleiste können Sie nach Dimensionen, Metriken, Segmenten (nur erweiterte berechnete Metriken) und Funktionen (nur erweiterte berechnete Metriken) suchen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Liste von Dimensionen </p> </td> 
   <td colname="col3"> <p>Zum Erstellen eines einfachen Segments (im Segmentaufbau) müssen Sie den Generator für berechnete Metriken nicht verlassen (z. B. „Seite = Homepage“). Sie können das Element „Seite“ hereinziehen und „Homepage“ direkt im Generator für berechnete Metriken auswählen. </p> <p>So profitieren Sie von einem deutlich optimierten Arbeitsablauf bei der Erstellung segmentierter berechneter Metriken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Liste von Metriken </p> </td> 
   <td colname="col3"> <p>Metriken sind in drei Kategorien eingeteilt: </p> 
    <ul id="ul_7BF50F4964EF45858FBA1634FBFA45CF"> 
     <li id="li_90F2312927A6499CA1CE04F8FFC912CF">Standardmetriken ( <img placement="inline"  src="assets/met_icon.png" id="image_65A80F54D73443E78542FE0B31CC3F20" />) </li> 
     <li id="li_A3F59083E79B4AC780D6F8CEDFFD20C9">Berechnete Metriken ( <img placement="inline"  src="assets/calc_met_icon.png" id="image_C5674AB9B9EB4DA9A56782D15822C319" />) </li> 
     <li id="li_8735E76637ED4C3F983731A66E04C93E">Metrikvorlagen (<img placement="inline"  src="assets/cm_template_icon.png" width="25px" id="image_D236601511CC4DD3828F223431E27E88" />) – unten in der Liste. </li> 
    </ul> <p>Wenn Sie mit dem Mauszeiger auf eine Metrik zeigen, wird das Infosymbol rechts neben der Metrik angezeigt: <img placement="inline"  src="assets/info.png" width="150px" id="image_5A65E772A68A4B94ACAD6552CCF21F5F" />. Durch Klicken auf dieses Symbol erhalten Sie die folgenden Informationen: </p> 
    <ul id="ul_DF35DDB9FBFA40C8A93FA0F2286A0BBE"> 
     <li id="li_4215AA9BF93F4C8B941002A7A4D2F50B">Die Formel für die Berechnung der Metrik. </li> 
     <li id="li_6A8E39EB6DCE4377B0B594B6D4FC0294">Ein Vorschautrend der Metrik. </li> 
     <li id="li_44C1595E4BE64ED69D1DB3BB6655ED55">Ein Bearbeitungssymbol (Bleistift) oben rechts, über das Sie zum Generator für berechnete Metriken gelangen, wo Sie diese berechnete Metrik bearbeiten können. </li> 
    </ul> <p><img placement="break" align="center"  src="assets/info2.png" width="200px" id="image_7D5B2F026A034118BE4DA81B9215A883" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Liste von Segmenten </p> </td> 
   <td colname="col3"> <p>(Nur erweiterte berechnete Metriken) Wenn Sie Administrator sind, enthält diese Liste alle in Ihrem Anmeldeunternehmen erstellten Segmente. Wenn Sie kein Administrator sind, enthält diese Liste Segmente, deren Eigentümer Sie sind, sowie Segmente, die für Sie freigegeben wurden. <a href="https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segment-reference/seg-rights.html"  > Mehr... </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Liste von Funktionen </p> </td> 
   <td colname="col3"> <p>(Nur erweiterte berechnete Metriken) Funktionen werden in zwei Listen aufgeteilt:  <a href="/help/components/c-calcmetrics/cm-reference/cm-functions.md"  >Einfach</a> (am häufigsten verwendet) und <a href="/help/components/c-calcmetrics/cm-reference/cm-adv-functions.md"  >Erweitert</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Report Suite-Auswahl </p> </td> 
   <td colname="col3"> <p>Damit können Sie zu einer anderen Report Suite wechseln. </p> </td> 
  </tr> 
 </tbody> 
</table>

