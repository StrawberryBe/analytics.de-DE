---
description: 'null '
seo-description: 'null '
seo-title: Segmente
title: Segmente
uuid: 677 f 6030-5 b 3 e -4 dfa-bb 79-9 f 27 f 3382 fb 1
translation-type: tm+mt
source-git-commit: f5f5b294f503911108e1693b7c6cd128bee659c6

---


# Segmente {#topic_DC2917A2E8FD4B62816572F3F6EDA58A}

## Segment rail {#section_3B07D458C43E42FDAF242BB3ACAF3E90}

Die Segmenteleiste im Menü „Komponenten“ zeigt Segmente sowie Segmentvorlagen, die anhand dieser Symbole erkannt werden können:

![](assets/segment_icons.png)

[Verwenden von Segmenten in Analysis Workspace auf youtube](https://www.youtube.com/watch?v=QlUCdQDnni4)(6:46)

## Create segments {#section_693CFADA668B4542B982446C2B4CF0F5}

Sie können sofort Segmente erstellen, indem Sie einen beliebigen Komponententyp (Dimension, Dimensionselement, Ereignis, Metrik, Segment, Segmentvorlage, Datenreichweite) in die Ablagefläche für Segmente oben in einem Bereich ablegen.

Komponententypen werden automatisch in Segmente umgewandelt. Alternativ können Sie auf das „+“-Symbol im Ablagefeld „Segment hinzufügen“ klicken.

Bedenken Sie Folgendes:

* Folgende Komponenten können Sie **nicht** im Segmentbereich ablegen: berechnete Metriken und Dimensionen/Metriken, aus denen Sie keine Segmente erstellen können.
* Bei vollständigen Dimensionen und Ereignissen erstellt Analysis Workspace Treffersegmente mit „vorhanden“. Beispiele: „Treffer, wenn eVar1 vorhanden ist“ oder „Treffer, wenn event1 vorhanden ist“.
* Wenn in der Segment-Dropzone "unspecified" oder" none" abgelegt wird, wird sie automatisch in ein "nicht vorhanden" -Segment umgewandelt, sodass es in der Segmentierung korrekt behandelt wird.

![](assets/segment-dropzone.png)

>[!NOTE]
>
>Auf diese Weise erstellte Segmente sind intern zum Projekt.

Sie können diese Segmente wie folgt öffentlich (global) machen:

1. Bewegen Sie den Mauszeiger auf das Segment in der Dropzone und klicken Sie auf das Symbol „i“.
1. Klicken Sie dann im angezeigten Informationsfeld auf **[!UICONTROL Als öffentlich einstellen]**.

   ![](assets/segment-info.png)

## Other methods for applying segments {#section_10FF2E309BA84618990EA5B473015894}

Es gibt verschiedene weitere Methoden für das Anwenden von Segmenten auf ein Freiformprojekt.

<table id="table_45B3839D70674430AF3AC5AA3134F825"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Aktion </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Segment aus Auswahl erstellen </p> </td> 
   <td colname="col2"> <p>Erstellt ein Inline-Segment. Wählen Sie Zeilen aus, klicken Sie mit der rechten Maustaste auf die Auswahl und erstellen Sie ein Inline-Segment. Dieses Segment wird nur auf das geöffnete Projekt angewendet und nicht als Analytics-Segment gespeichert. </p> <p> 
     <ol id="ol_1D1E661387354EBF992CC150915F642E"> 
      <li id="li_B96666FD426F4AEE8EAB61B2C00A07FB">Zeilen auswählen </li> 
      <li id="li_C2245B3EA81F4FAC88A33647922535AF">Rechtsklick auf der Auswahl </li> 
      <li id="li_AB4F8988B9A84920ABA06A91094625F6">Klick auf <span class="uicontrol">Segment aus Auswahl erstellen</span> </li> 
     </ol> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> Komponenten</span> &gt; <span class="uicontrol">Neues Segment</span> </td> 
   <td colname="col2"> <p>Zeigt den <span class="wintitle">Segment-Builder</span> an Weitere Informationen zur Segmentierung finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html" format="https" scope="external">Segmente erstellen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="ignoretag"><span class="uicontrol"> Freigabe</span> &gt; <span class="uicontrol">Projekt freigeben</span></span> oder </p> <p> <span class="ignoretag"><span class="uicontrol">Freigabe</span> &gt; <span class="uicontrol">Projekt kuratieren</span></span> </p> </td> 
   <td colname="col2"> <p>In <a href="../../../analyze/analysis-workspace/curate-share/curate.md#concept_4A9726927E7C44AFA260E2BB2721AFC6" format="dita" scope="local"> Curate &amp; Share</a>, segments that you apply to the project are available in shared analysis for the recipient. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Segmente als Dimensionen verwenden </p> </td> 
   <td colname="col2"> <p>Video: <a href="https://www.youtube.com/watch?v=WmSdReKTWto&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS&amp;index=39" format="https" scope="external">Verwenden von Segmenten als Dimensionen in Analysis Workspace</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

