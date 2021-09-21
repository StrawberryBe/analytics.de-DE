---
description: Verwenden Sie Ad-hoc-Segmente in Analysis Workspace.
title: Ad-hoc-Segmente
feature: Workspace Basics
role: User, Admin
source-git-commit: 9622131ebd4a856cb7756e6844d7d7979029e70e
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 45%

---


# Ad-hoc-Segmente

Hier finden Sie ein Video zum Erstellen von Ad-hoc-Segmenten:

>[!VIDEO](https://video.tv.adobe.com/v/23978/?quality=12)

Sie können Ad-hoc-Segmente erstellen, wenn Sie schnell untersuchen möchten, wie sich ein Segment auf Ihr Projekt auswirken könnte, ohne dazu den Segment Builder aufzurufen. Stellen Sie sich diese Segmente als temporäre Segmente auf Projektebene vor. Sie sind normalerweise nicht Teil Ihrer Segmentbibliothek wie Komponentensegmente in der linken Leiste. Sie können sie jedoch veröffentlichen, wie unten dargestellt.

1. Ziehen Sie einen beliebigen Komponententyp (Dimension, Dimensionselement, Ereignis, Metrik, Segment, Segmentvorlage, Datumsbereich) in die Segment-Dropzone am oberen Rand eines Bedienfelds. Komponententypen werden automatisch in Segmente umgewandelt.
Hier ist ein Beispiel für das Erstellen eines Segments für die Twitter-Referrer-Domäne:

   ![](assets/ad-hoc1.png)

   In Ihrem Bedienfeld wird dieses Segment automatisch angewendet und Sie können die Ergebnisse sofort sehen.

1. Hierzu

Bitte beachten Sie:

* Folgende Komponenten können Sie **nicht** im Segmentbereich ablegen: berechnete Metriken und Dimensionen/Metriken, aus denen Sie keine Segmente erstellen können.
* Bei vollständigen Dimensionen und Ereignissen erstellt Analysis Workspace Hit-Segmente mit „vorhanden“. Beispiele: `Hit where eVar1 exists` oder `Hit where event1 exists`.
* Wenn „nicht angegeben“ oder „keine“ im Segmentablagebereich abgelegt werden, werden sie automatisch in ein Segment mit „nicht vorhanden“ umgewandelt, damit sie bei der Segmentierung korrekt behandelt werden.

>[!NOTE]
>
>Auf diese Weise erstellte Segmente sind interne Segmente des Projekts.

## Ad-hoc-Segmente öffentlich machen {#ad-hoc-public}

Sie können diese Segmente wie folgt öffentlich (global) machen:

1. Bewegen Sie den Mauszeiger auf das Segment in der Dropzone und klicken Sie auf das Symbol „i“.
1. Klicken Sie dann im angezeigten Informationsfeld auf **[!UICONTROL Als öffentlich einstellen]**.

   ![](assets/segment-info.png)