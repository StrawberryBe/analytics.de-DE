---
description: Durch Kuratierung können Sie die Komponenten einschränken, bevor Sie ein Projekt freigeben.
keywords: Analysis Workspace-Kuratierung
title: Kuratieren von Projekten
feature: Curate and Share
role: User, Admin
exl-id: 5e23be83-586a-4543-9be9-65c631b8b0b7
source-git-commit: 266cf18050d60f08f7e170c56453d1e1d805cb7b
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 63%

---

# Kuratieren von Projekten

Mit der Kuratierung können Sie die Komponenten (Dimensionen, Metriken, Segmente, Datumsbereiche) vor der Freigabe eines Projekts einschränken. Wenn ein Empfänger das Projekt öffnet, wird ihm eine begrenzte Anzahl von Komponenten angezeigt, die Sie für ihn kuratiert haben. Die Kuratierung ist ein optionaler, aber empfehlenswerter Schritt, bevor Sie ein Projekt freigeben.

>[!NOTE]
> Produktprofile bestimmen als Hauptmechanismen, welche Komponenten ein Anwender sehen kann. Sie werden über die Adobe Experience Cloud Admin Console verwaltet. Kuratierung ist ein Sekundärfilter.

Im Folgenden finden Sie ein Video zur Projektkuratierung und -freigabe:

>[!VIDEO](https://video.tv.adobe.com/v/24711/?quality=12)

## Anwenden der Projektkuratierung

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projektdaten kuratieren]**.
Die im Projekt verwendeten Komponenten werden automatisch hinzugefügt.
   **Hinweis**: Wenn ein Projekt mehrere Report Suites hat, wird für jede Report Suite im Projekt ein Feld zum Kuratieren angezeigt.
1. (Optional) Um weitere Komponenten hinzuzufügen, ziehen Sie die freizugebenden Komponenten aus der linken Leiste in das Feld [!UICONTROL Komponenten kuratieren].
1. Klicken Sie auf **[!UICONTROL Fertig]**.

Eine Kuratierung kann auch über das Menü [!UICONTROL Freigeben] angewendet werden, indem Sie auf **[!UICONTROL Kuratieren und freigeben]** klicken. Diese Option kuratiert das Projekt automatisch auf die im Projekt verwendeten Komponenten. Sie können weitere Komponenten hinzufügen, wie oben beschrieben.

![](assets/curation-field.png)

## Ansicht des kuratierten Projekts

Wenn ein Empfänger ein kuratiertes Projekt öffnet, wird ihm nur der ausgewählte Satz der von Ihnen definierten Komponenten angezeigt:

![](assets/curate-project.png)

## Entfernen der Projektkuratierung

So entfernen Sie die Projektkuratierung und stellen Sie den vollständigen Satz der Komponenten in der linken Leiste wieder her:

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projektdaten kuratieren]**.
1. Klicken Sie auf **[!UICONTROL Kuratierung entfernen]**.
1. Klicken Sie auf **[!UICONTROL Fertig]**.

## Kuratierung von Virtual Report Suites

Wenn Sie die Kuratierung auf Report Suite-Ebene anwenden möchten, sodass sie für viele Projekte gleichzeitig gilt, können Sie [Kuratieren von Komponenten in einer Virtual Report Suite](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-components.html?lang=de).

>[!NOTE]
> Die Kuratierung der Virtual Report Suite wird immer vor der Projektkuratierung angewendet. Das bedeutet, dass selbst wenn Ihr kuratiertes Projekt bestimmte Komponenten enthält, diese herausgefiltert werden, wenn die kuratierte Virtual Report Suite diese nicht enthält.

## Option „Alle anzeigen“ für Komponenten

In einem kuratierten Projekt oder einer Virtual Report Suite wird dem Empfänger die Option **[!UICONTROL Alle anzeigen]** Komponenten in der linken Leiste. [!UICONTROL Alle anzeigen] zeigt verschiedene Komponentensätze an, je nach:

* Berechtigungsstufe des Benutzers (Administrator oder Nicht-Administrator)
* Projektrolle (Inhaber/Bearbeiter oder nicht)
* Art der angewendeten Kuratierung (Virtual Report SuiteS oder Projekt)
* Komponenten, die dem Benutzer gehören oder für ihn freigegeben wurden. Zu den eigenen/freigegebenen Komponenten gehören Segmente, berechnete Kennzahlen und Datumsbereiche. Sie enthalten keine implementierten Komponenten wie eVars, Props und benutzerdefinierte Ereignisse.

Hinweis: Rollen ohne Administratoransicht haben keinen Zugriff auf die linke Leiste in einem Projekt, daher wurden sie in der unten stehenden Tabelle weggelassen.

| Kuratierungstyp | Admins | Inhaber- oder Bearbeiterrolle, kein Admin | Duplizierte Rolle „Nicht-Administrator“ |
|---|---|---|---|
| Kuratierte Virtual Report Suite | Alle nicht kuratierten Virtual Report Suite-Komponenten | Nicht kuratierte Virtual Report Suite-Komponenten, die dieser Rolle gehören oder für sie freigegeben wurden | Nicht kuratierte Virtual Report Suite-Komponenten, die dieser Rolle gehören oder für sie freigegeben wurden |
| Kuratierte Projekte | Alle nicht kuratierten Projektkomponenten | Alle nicht kuratierten Projektkomponenten | Nicht kuratierte Projektkomponenten, die diese Rolle besitzt oder die für diese Rolle freigegeben wurden |
| Kuratiertes Projekt in einer kuratierten Virtual Report Suite | Alle nicht kuratierten Komponenten, aufgeführt unter **[!UICONTROL Nicht kuratierte Projektkomponenten]** und **[!UICONTROL Nicht kuratierte Virtual Report Suite-Komponenten]** | Alle nicht kuratierten Projektkomponenten UND nicht kuratierten Virtual Report Suite-Komponenten, die dieser Rolle gehören oder für sie freigegeben wurden | Nicht kuratierte Virtual Report Suite und Projektkomponenten, die dieser Rolle gehören oder für sie freigegeben wurden |
