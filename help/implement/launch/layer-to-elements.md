---
title: Zuordnen von Datenschichtobjekten zu Datenelementen
description: Konfigurieren Sie Launch, um aus Ihrer Datenschicht zu lesen.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 100%

---


# Zuordnen von Datenschichtobjekten zu Datenelementen

Nachdem Ihr Unternehmen eine Datenschicht auf Ihrer Site eingerichtet und implementiert hat, können Sie innerhalb von Launch Datenschichtobjekte Datenelementen zuordnen.

## Voraussetzungen

[Erstellen Sie eine Datenschicht](../prepare/data-layer.md): Stellen Sie sicher, dass auf Ihrer Site eine Datenschicht vorhanden ist. Obwohl Sie technisch alle JavaScript-Objekte oder CSS-Elemente direkt auf der Seite zuordnen bzw. von dort scrapen können, empfiehlt Adobe diese Vorgehensweise nur als letztes Mittel. Wenn sich Ihr Sitelayout ändert, funktionieren die in Launch verwendeten CSS-Selektoren nicht mehr, was zu Datenverlusten führt.

## Verwenden von Adobe Experience Platform Launch zum Erstellen von Datenelementen

[Datenelemente](https://docs.adobe.com/content/help/de-DE/launch/using/reference/manage-resources/data-elements.html#create-a-data-element) sind Komponenten in Launch, die Sie im gesamten Tool verwenden können. Sie können mithilfe von Datenelementen Variablenwerte in der Adobe Analytics-Erweiterung zuweisen.

1. Wechseln Sie zu [Adobe Experience Platform Launch](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die gewünschte Launch-Eigenschaft.
1. Klicken Sie auf die Registerkarte **[!UICONTROL Datenelemente]** und dann auf **[!UICONTROL Datenelement hinzufügen]**.

   ![Datenelement erstellen](assets/createelement.png)

1. Geben Sie einen Namen für Ihr Datenelement ein. Dies kann eine einfache Bezeichnung sein, die einer JavaScript-Variablen in Ihrer Datenschicht entspricht, die Sie tracken möchten.
1. Wählen Sie im Dropdown-Menü **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Core]**.
1. Wählen Sie im Dropdown-Menü **[!UICONTROL Datenelementtyp]** die Option **[!UICONTROL JavaScript-Variable]** aus. Rechts wird ein Textfeld angezeigt, in dem Sie die JavaScript-Variable eingeben können, die diesem Datenelement zugeordnet werden soll.
1. Geben Sie die gewünschte JavaScript-Variable ein, normalerweise innerhalb Ihrer Datenschicht. Wenn beispielsweise die Datenschicht Ihres Unternehmens der empfohlenen Vorgehensweise von Adobe sehr ähnlich ist, könnte als Wert `digitalData.page.pageInfo.pageName` verwendet werden. Sie können die Syntax und Werte Ihrer JavaScript-Variablen in der Browser-Konsole überprüfen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Nächste Schritte

[Zuordnen von Datenelementen zu Analytics-Variablen](elements-to-variable.md): Weisen Sie den Analytics-Variablen Datenelemente zu, damit Sie sie als Dimensionen in Analysis Workspace verwenden können.
