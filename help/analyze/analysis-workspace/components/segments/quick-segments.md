---
description: Verwenden Sie Schnellsegmente in Analysis Workspace.
title: Schnellsegmente
feature: Workspace Basics
role: User, Admin
source-git-commit: f3185f1ee341348fb7bdbaab8b68d421e7c79076
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---


# Schnellsegmente

Sie können innerhalb eines Projekts schnelle Segmente erstellen, um die Komplexität des vollständigen [Segment Builders](/help/components/segmentation/segmentation-workflow/seg-build.md) zu umgehen. Einen Vergleich dessen, was Schnellsegmente im Vergleich zu vollständigen Komponentensegmenten tun können, finden Sie unter [hier](/help/analyze/analysis-workspace/components/segments/t-freeform-project-segment.md).

>[!IMPORTANT]
> Schnellsegmente werden derzeit nur eingeschränkt getestet und sind noch nicht allgemein verfügbar.

## Schnellsegmente erstellen

1. Klicken Sie in einer Freiformtabelle auf das Symbol filter+ in der Bedienfeldüberschrift:

   ![](assets/quick-seg1.png)

   Beachten Sie, dass:

   - Es gibt nur einen Segmentbehälter, mit dem Sie eine Dimension/Metrik/einen Datumsbereich in das Segment einbeziehen (oder daraus ausschließen) können.
   - Sie können den Behälter auf Treffer-, Besuchs- oder Besucherebene festlegen. Der Standardwert ist &quot;Treffer&quot;.

1. Fügen Sie eine Dimension/Metrik/einen Datumsbereich auf 3 Arten hinzu:

   - Beginnen Sie mit der Eingabe und der [!UICONTROL Quick Segment Builder] findet automatisch die entsprechende Komponente.
   - Verwenden Sie die Dropdownliste, um die Komponente zu finden.
   - Ziehen Sie Komponenten per Drag-and-Drop aus der linken Leiste.

1. Geben Sie die erste Regel an, z. B. `Page equals workspace`. Sie können bis zu drei Regeln in einer Segmentdefinition haben. Klicken Sie einfach auf das &quot;+&quot;-Zeichen, um eine weitere Regel hinzuzufügen. Sie können den Regeln &quot;AND&quot;- oder &quot;OR&quot;-Kennungen hinzufügen, aber Sie können &quot;AND&quot;und &quot;OR&quot;nicht in einer Segmentdefinition kombinieren.

   Hier ist ein Beispiel für ein Segment, das Dimensionen und Metriken kombiniert:

   ![](assets/quick-seg2.png)

1. Klicken Sie auf **[!UICONTROL Anwenden]** , um dieses Segment auf das Bedienfeld anzuwenden.
Das Segment wird oben angezeigt. Beachten Sie die graue Seitenleiste im Gegensatz zur blauen Seitenleiste für Segmente auf Komponentenebene in der Segmentbibliothek auf der linken Seite.

   ![](assets/quick-seg3.png)

## Schnellsegmente bearbeiten

1. Bewegen Sie den Mauszeiger über das Schnellsegment und wählen Sie das Stiftsymbol aus.
1. Bearbeiten Sie die Segmentdefinition oder den Segmentnamen.

## Schnellsegmente speichern

Sie können schnelle Segmente speichern, indem Sie die folgenden Schritte ausführen.

>[!IMPORTANT]
>Nachdem Sie das Segment gespeichert oder angewendet haben, können Sie es nicht mehr im Quick Segment Builder bearbeiten, sondern nur noch im regulären Segment Builder.

1. Bewegen Sie den Mauszeiger über das Schnellsegment und wählen Sie das Infosymbol (&quot;i&quot;) aus.
1. Wählen Sie **[!UICONTROL Segment speichern]**

   ![](assets/save-quick-seg.png)

1. Belassen Sie den Namen unverändert oder benennen Sie das Segment um.

   Gehen Sie zurück zu Workspace und sehen Sie, wie das Segment jetzt über eine blaue Seitenleiste verfügt. Dies weist darauf hin, dass es nicht mehr im Schnellsegmentaufbau bearbeitet/geöffnet werden kann. Und durch Speichern wird sie Teil der Komponentenliste.

   ![](assets/quick-seg4.png)

Nachdem Sie das Segment angewendet haben, können Sie es Ihrer Segmentkomponentenliste hinzufügen und für alle Ihre Projekte verfügbar machen.

1. Bewegen Sie den Mauszeiger über das gespeicherte Segment und wählen Sie das Stiftsymbol aus.

1. Beachten Sie dieses Dialogfeld oben im Segment Builder:

   ![](assets/project-only.png)

1. Aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Stellen Sie dieses Segment für alle Projekte zur Verfügung und fügen Sie es zur Komponentenliste hinzu.]**
1. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Das Segment wird jetzt in Ihrer Segmentkomponentenliste für alle Ihre Projekte angezeigt.
1. Sie können auch [das Segment](/help/components/segmentation/segmentation-workflow/t-seg-share.md) für andere Personen in Ihrer Organisation freigeben.

## Was sind reine Projektsegmente?

Nur-Projekt-Segmente sind entweder Schnellsegmente oder Ad-hoc-Workspace-Projektsegmente. Wenn Sie sie im Segment Builder bearbeiten/öffnen, wird das Feld &quot;Nur Projekt&quot;angezeigt. Wenn sie ein kurzes Segment im Builder anwenden, aber nicht das Kontrollkästchen &quot;Verfügbar machen&quot;aktivieren, ist es weiterhin ein reines Projekt-Segment, kann jedoch nicht mehr im QS-Builder geöffnet werden. Wenn sie das Kontrollkästchen aktivieren und SPEICHERN, ist es jetzt ein Komponentensegment.