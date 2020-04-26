---
title: Zuordnen von Datenschichtobjekten zu Datenelementen
description: Konfigurieren Sie Launch, um aus Ihrer Datenschicht zu lesen.
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# Zuordnen von Datenschichtobjekten zu Datenelementen

Nachdem Ihr Unternehmen eine Datenschicht auf Ihrer Site eingerichtet und implementiert hat, können Sie Datenschichtobjekte innerhalb von Launch Datenelementen zuordnen.

## Voraussetzungen

[Erstellen Sie eine Datenschicht](../prepare/data-layer.md): Stellen Sie sicher, dass auf Ihrer Site eine Datenschicht vorhanden ist. Obwohl Sie technisch alle JavaScript-Objekte oder CSS-Elemente direkt auf der Seite zuordnen können, empfiehlt Adobe diese Vorgehensweise als letztes Mittel. Wenn sich Ihr Site-Layout ändert, funktionieren die in Launch verwendeten CSS-Selektoren nicht mehr, was zu Datenverlusten führt.

## Verwenden Sie Adobe Experience Platform Launch, um Datenelemente zu erstellen

[Datenelemente](https://docs.adobe.com/content/help/de-DE/launch/using/reference/manage-resources/data-elements.html#create-a-data-element) sind Komponenten in Launch, die Sie über das Tool hinweg verwenden können. Sie können Variablenwerte in der Adobe Analytics-Erweiterung mithilfe von Datenelementen zuweisen.

1. Wechseln Sie zu [Adobe Experience Platform Launch](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die gewünschte Eigenschaft Start.
1. Click the [!UICONTROL Data Elements] tab, then click [!UICONTROL Add Data Element].

   ![Datenelement erstellen](assets/createelement.png)

1. Geben Sie einen Namen für Ihr Datenelement ein. Es kann sich um eine einfache Beschriftung handeln, die einer JavaScript-Variablen in Ihrer Datenschicht entspricht, die Sie verfolgen möchten.
1. Wählen Sie im Dropdownmenü [!UICONTROL Erweiterung] die Option [!UICONTROL Core].
1. Under the [!UICONTROL Data Element Type] dropdown, select [!UICONTROL JavaScript Variable]. Rechts wird ein Textfeld angezeigt, in dem Sie die JavaScript-Variable eingeben können, die diesem Datenelement zugeordnet werden soll.
1. Geben Sie die gewünschte JavaScript-Variable ein, normalerweise in Ihrer Datenschicht. Wenn beispielsweise die Datenschicht Ihres Unternehmens der empfohlenen Vorgehensweise von Adobe sehr ähnlich ist, könnte ein Wert `digitalData.page.pageInfo.pageName`verwendet werden. Sie können die JavaScript-Variablensyntax und -werte in der Browser-Konsole überprüfen.
1. Klicken Sie auf [!UICONTROL Speichern].

## Nächste Schritte

[Zuordnen von Datenelementen zu Analytics-Variablen](elements-to-variable.md): Weisen Sie den Analytics-Variablen Datenelemente zu, damit Sie sie als Dimensionen in Analyse Workspace verwenden können.
