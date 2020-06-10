---
description: Mithilfe der Kuratierung können Sie Komponenten einschränken, bevor Sie ein Projekt freigeben.
keywords: Analysis Workspace curation
title: Projekte im Arbeitsbereich kuratieren
translation-type: tm+mt
source-git-commit: f7c2a366b409995c1fe790db97de5c708882ab3d
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 39%

---


# Projekte im Arbeitsbereich kuratieren

Mit der Kuratierung können Sie die Komponenten (Dimensionen, Metriken, Segmente, Datumsbereiche) vor der Freigabe eines Projekts einschränken. Wenn ein Empfänger das Projekt öffnet, wird ihm eine begrenzte Anzahl von Komponenten angezeigt, die Sie für sie kuratiert haben. Die Kuratierung ist ein optionaler, aber empfehlenswerter Schritt, bevor Sie ein Projekt freigeben.

>[!NOTE]
> Produktprofile bestimmen als Hauptmechanismen, welche Komponenten ein Anwender sehen kann. Sie werden über die Admin Console verwaltet. Kuratierung ist ein Sekundärfilter.

## Projektkuratierung anwenden

1. Click **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]**.
Die im Projekt verwendeten Komponenten werden automatisch hinzugefügt.
   **Hinweis**: Wenn ein Projekt mehrere Report Suites hat, wird ein kuratiertes Feld für jede Report Suite im Projekt angezeigt.
1. (Optional) Um weitere Komponenten hinzuzufügen, ziehen Sie die freizugebenden Komponenten aus der linken Leiste in das Feld [!UICONTROL Kuratieren der Komponenten] .
1. Klicken Sie auf **[!UICONTROL Fertig]**.

![](assets/curation-field.png)

Wenn ein Empfänger ein kuratiertes Projekt öffnet, wird ihm nur der ausgewählte Satz der von Ihnen definierten Komponenten angezeigt:

![](assets/curate-project.png)

Kuratieren können Sie auch über das Menü &quot; [!UICONTROL Freigeben] &quot;anwenden, indem Sie auf **[!UICONTROL Kuratieren und Freigeben]** klicken. Diese Option kuratiert das Projekt automatisch auf die im Projekt verwendeten Komponenten. Sie können weitere Komponenten hinzufügen, wie oben beschrieben.

## Projektkuratierung entfernen

So entfernen Sie die Projektkuratierung und stellen Sie den vollständigen Satz der Komponenten in der linken Leiste wieder her:
1. Click **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]**.
1. Klicken Sie auf Kuration **[!UICONTROL entfernen]**.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Kuratierung der Virtual Report Suite (VRS)

Um die Kuration auf Report Suite-Ebene anzuwenden, sodass sie für viele Projekte gleichzeitig gilt, können Sie Komponenten in einer Virtual Report Suite (VRS) [](https://docs.adobe.com/content/help/de-DE/analytics/components/virtual-report-suites/vrs-components.html)kuratieren.

>[!NOTE]
> Die VRS-Kuratierung wird immer vor der Projektkuratierung ausgeführt. Das bedeutet, dass selbst wenn Ihr kuratiertes Projekt bestimmte Komponenten enthält, werden diese herausgefiltert, wenn die kuratierte VRS diese nicht enthält.

### Alle Komponenten anzeigen

In einem kuratierten Projekt oder einer VRS wird dem Empfänger die Option zum **[!UICONTROL Anzeigen aller]** Komponenten in der linken Leiste angezeigt. [!UICONTROL &quot;Alle] anzeigen&quot;zeigt verschiedene Komponentensätze an, je nach:

* die Berechtigungsebene des Benutzers (Admin oder Nicht-Admin)
* Rolle des Projekts (Eigentümer/Editor oder nicht)
* Art der angewendeten Kuration

| Kuratierungstyp | Admins | Projektinhaber ohne Administratorrechte | Ohne Administratorrechte |
|---|---|---|---|
| Kuratierte VRS | Alle nicht kuratierten VRS-Komponenten | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden | Nicht kuratierte VRS-Komponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte | Alle nicht kuratierten Projektkomponenten | Alle nicht kuratierten Projektkomponenten | Nicht kuratierte Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratierte Projekte in kuratierte VRS | Alle nicht kuratierten Komponenten, aufgeführt unter  **[!UICONTROL Nicht kuratierte Projektkomponenten]** und **[!UICONTROL Nicht kuratierte VRS-Komponenten]** | Alle nicht kuratierten Projektkomponenten UND nicht kuratierten VRS-Komponenten, die dieser Rolle gehören oder für sie freigegeben wurden | Nicht kuratierte VRS- und Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
