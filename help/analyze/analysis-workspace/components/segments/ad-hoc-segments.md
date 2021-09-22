---
description: Verwenden Sie Ad-hoc-Segmente in Analysis Workspace.
title: Ad-hoc-Segmente
feature: Workspace Basics
role: User, Admin
source-git-commit: f3185f1ee341348fb7bdbaab8b68d421e7c79076
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 25%

---


# Ad-hoc-Projektsegmente

Hier finden Sie ein Video zum Erstellen von Ad-hoc-Projektsegmenten:

>[!VIDEO](https://video.tv.adobe.com/v/23978/?quality=12)

Sie können Ad-hoc-Projektsegmente erstellen, wenn Sie schnell untersuchen möchten, wie sich ein Segment auf Ihr Projekt auswirken könnte, ohne den Segment Builder aufzurufen. Stellen Sie sich diese Segmente als temporäre Segmente auf Projektebene vor. Sie sind normalerweise nicht Teil Ihrer Segmentbibliothek wie Komponentensegmente in der linken Leiste. Sie können sie jedoch speichern, wie unten dargestellt.

Einen Vergleich dessen, was Ad-hoc-Projektsegmente im Vergleich zu vollständigen Komponentensegmenten tun können, finden Sie unter [hier](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md).

1. Ziehen Sie einen beliebigen Komponententyp (Dimension, Dimensionselement, Ereignis, Metrik, Segment, Segmentvorlage, Datumsbereich) in die Segment-Dropzone am oberen Rand eines Bedienfelds. Komponententypen werden automatisch in Segmente umgewandelt.
Hier ist ein Beispiel für das Erstellen eines Segments für die Twitter-Referrer-Domäne:

   ![](assets/ad-hoc1.png)

   In Ihrem Bedienfeld wird dieses Segment automatisch angewendet und Sie können die Ergebnisse sofort sehen.

1. Sie können einem Bedienfeld eine unbegrenzte Anzahl von Komponenten hinzufügen.
1. Wenn Sie dieses Segment speichern möchten, lesen Sie den folgenden Abschnitt.

Bitte beachten Sie:

* Folgende Komponenten können Sie **nicht** im Segmentbereich ablegen: berechnete Metriken und Dimensionen/Metriken, aus denen Sie keine Segmente erstellen können.
* Bei vollständigen Dimensionen und Ereignissen erstellt Analysis Workspace Hit-Segmente mit „vorhanden“. Beispiele: `Hit where eVar1 exists` oder `Hit where event1 exists`.
* Wenn „nicht angegeben“ oder „keine“ im Segmentablagebereich abgelegt werden, werden sie automatisch in ein Segment mit „nicht vorhanden“ umgewandelt, damit sie bei der Segmentierung korrekt behandelt werden.

>[!NOTE]
>
>Auf diese Weise erstellte Segmente sind interne Segmente des Projekts.

## Speichern von Ad-hoc-Projektsegmenten {#ad-hoc-save}

Sie können diese Segmente speichern, indem Sie die folgenden Schritte ausführen:

1. Bewegen Sie den Mauszeiger auf das Segment in der Dropzone und klicken Sie auf das Symbol „i“.
1. Klicken Sie im angezeigten Informationsfeld auf **[!UICONTROL Speichern]**.

   ![](assets/segment-info.png)

## Was sind reine Projektsegmente?

Nur-Projekt-Segmente sind entweder Schnellsegmente oder Ad-hoc-Workspace-Projektsegmente. Wenn Sie sie im Segment Builder bearbeiten/öffnen, wird das Feld &quot;Nur Projekt&quot;angezeigt. Wenn sie ein kurzes Segment im Builder anwenden, aber nicht das Kontrollkästchen &quot;Verfügbar machen&quot;aktivieren, ist es weiterhin ein reines Projekt-Segment, kann jedoch nicht mehr im QS-Builder geöffnet werden. Wenn sie das Kontrollkästchen aktivieren und SPEICHERN, ist es jetzt ein Komponentensegment.