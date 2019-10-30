---
description: Sie können in Analysis Workspace Segmente aus einem Touchpoint erstellen, Segmente als Touchpoints hinzufügen und wichtige Workflows über verschiedene Segmente hinweg vergleichen.
keywords: Trichteranalyse und Segmentierung;Segmente in der Fallout-Analyse;Segmente im Fallout vergleichen
seo-description: Sie können in Analysis Workspace Segmente aus einem Touchpoint erstellen, Segmente als Touchpoints hinzufügen und wichtige Workflows über verschiedene Segmente hinweg vergleichen.
seo-title: Segmente in der Fallout-Analyse anwenden
title: Segmente in der Fallout-Analyse anwenden
uuid: e87a33df-160e-4943-8d02-4d6609ae3bb1
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Segmente in der Fallout-Analyse anwenden

Sie können in Analysis Workspace Segmente aus einem Touchpoint erstellen, Segmente als Touchpoints hinzufügen und wichtige Workflows über verschiedene Segmente hinweg vergleichen.

> [!IMPORTANT] Segmente, die als Checkpoints in Trichteranalyse verwendet werden, müssen einen Behälter verwenden, der auf einer niedrigeren Ebene als der Gesamtkontext der Fallout-Visualisierung liegt. Bei einem Besucherkontext-Trichteranalyse müssen Segmente, die als Checkpoints verwendet werden, besuchsbasierte oder trefferbasierte Segmente sein. Bei einer besuchskontextbezogenen Trichteranalyse müssen Segmente, die als Checkpoint verwendet werden, trefferbasierte Segmente sein. Wenn Sie eine ungültige Kombination verwenden, beträgt der Fallout 100 %. Wir haben eine Warnung zur Fallout-Visualisierung hinzugefügt, die angezeigt wird, wenn Sie ein inkompatibles Segment als Touchpoint hinzufügen. Bestimmte ungültige Segmentbehälterkombinationen führen zu ungültigen Trichteranalysediagrammen, z. B.:

* Verwenden eines besucherbasierten Segments als Touchpoint innerhalb einer Fallout-Visualisierung des Besuchers
* Verwenden eines besucherbasierten Segments als Touchpoint innerhalb einer Fallout-Visualisierung eines Besuches
* Verwenden eines besuchbasierten Segments als Touchpoint innerhalb einer Fallout-Visualisierung eines Besuches

## Create a segment from a touchpoint {#section_915E8FBF35CD4F34828F860C1CCC2272}

1. Erstellen Sie ein Segment aus einem bestimmten Touchpoint, an dem Sie besonders interessiert sind und das sich möglicherweise für andere Berichte eignet. Klicken Sie dazu mit der rechten Maustaste auf den Touchpoint, und wählen Sie dann **[!UICONTROL Segment aus Touchpoint erstellen aus]**.

   ![](assets/segment-from-touchpoint.png)

   Der Segment Builder wird geöffnet und enthält das vorab erstellte sequenzielle Segment, das zu dem von Ihnen ausgewählten Touchpoint passt:

   ![](assets/segment-builder.png)

1. Geben Sie einen Titel und eine Beschreibung für das Segment ein, und speichern Sie es.

   Nun können Sie dieses Segment in jedem gewünschten Bericht verwenden.

## Add a segment as a touchpoint {#section_17611C1A07444BE891DC21EE8FC03EFC}

Wenn Sie zum Beispiel wissen möchten, wie der Trend bei Ihren Benutzern aus den USA aussieht und wie sich dies in der Fallout-Analyse auswirkt, ziehen Sie einfach das Segment „USA-Benutzer“ in den Trichter:

![](assets/segment-touchpoint.png)

Oder Sie erstellen einen AND-Touchpoint, indem Sie das Segment „USA-Benutzer“ auf einen anderen Checkpoint ziehen.

## Compare segments in fallout {#section_E0B761A69B1545908B52E05379277B56}

In der Fallout-Visualisierung können Sie eine unbegrenzte Anzahl von Segmenten miteinander vergleichen.

1. Wählen Sie die zu vergleichenden Segmente links in der Leiste [!UICONTROL Segmente] aus. Im vorliegenden Beispiel haben wir 2 Segmente ausgewählt: „USA-Benutzer“ und „Benutzer außerhalb der USA“.
1. Ziehen Sie sie nach oben in die Ablegezone „Segmente“.

   ![](assets/segment-drop.png)

1. Optional: Sie können „Alle Besuche“ als Standardcontainer belassen oder löschen.

   ![](assets/seg-compare.png)

1. Sie können nun den Fallout über zwei Segmente hinweg vergleichen (z. B. an welcher Stelle ein Segment eine bessere Leistung als das andere hat) oder sonstige Einblicke erhalten.
