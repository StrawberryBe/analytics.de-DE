---
description: 'null'
seo-description: 'null'
seo-title: Segmente
title: Segmente
uuid: 677 f 6030-5 b 3 e -4 dfa-bb 79-9 f 27 f 3382 fb 1
translation-type: tm+mt
source-git-commit: 07b18333144f992031dca5a5d8838206fa735cb5

---


# Segmente {#topic_DC2917A2E8FD4B62816572F3F6EDA58A}

## Segment rail {#section_3B07D458C43E42FDAF242BB3ACAF3E90}

Die Segmenteleiste im Menü „Komponenten“ zeigt Segmente sowie Segmentvorlagen, die anhand dieser Symbole erkannt werden können:

![](assets/segment_icons.png)

[Verwenden von Segmenten in Analysis Workspace auf youtube](https://www.youtube.com/watch?v=QlUCdQDnni4)(6:46)

## Segmente erstellen {#section_693CFADA668B4542B982446C2B4CF0F5}

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

| Aktion | Beschreibung |
|--- |--- |
| Segment aus Auswahl erstellen | Erstellt ein Inline-Segment. Wählen Sie Zeilen aus, klicken Sie mit der rechten Maustaste auf die Auswahl und erstellen Sie ein Inline-Segment. Dieses Segment wird nur auf das geöffnete Projekt angewendet und nicht als Analytics-Segment gespeichert. 1. Wählen Sie Zeilen aus. 2. Klicken Sie mit der rechten Maustaste auf die Auswahl. 3. Click *Create segment from selection*. |
| Komponenten &gt; Neues Segment | Zeigt den Segment-Builder an See [Segment Builder](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html) for more information about segmentation. |
| Freigeben &gt; Projekt freigeben oder Freigeben &gt; Projekt kuratieren | In [Curate and Share](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html#concept_4A9726927E7C44AFA260E2BB2721AFC6), learn how segments that you apply to the project are available in shared analysis for the recipient. |
| Segmente als Dimensionen verwenden | Video: [Verwenden von Segmenten als Dimensionen in Analysis Workspace](https://www.youtube.com/watch?v=WmSdReKTWto&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS&index=39) |
