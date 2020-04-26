---
title: Zuordnen von Datenelementen zu Analytics-Variablen
description: Weisen Sie den Analytics-Variablen Datenelemente zu, damit Sie sie als Dimensionen in Analyse Workspace verwenden können.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Zuordnen von Datenelementen zu Analytics-Variablen

Sobald Sie über ein Repository mit Datenelementen in Adobe Experience Platform Launch verfügen, können Sie sie Analytics-Dimensionen zuweisen.

## Voraussetzungen

[Ordnen Sie Datenschichtobjekte Datenelementen](layer-to-elements.md)zu: Vergewissern Sie sich, dass Sie die Datenelemente in Launch verstehen und dass Sie mit mehreren Elementen arbeiten müssen.

[Erstellen Sie ein Lösungsdesigndesign-Dokument](../prepare/solution-design.md): Ein Lösungsdesign-Dokument ist unverzichtbar, um organisiert zu bleiben. Durch das Befolgen Ihres Lösungsdesignprojekts wird die Zuweisung von Datenelementen zu Analytics-Variablen vereinfacht.

## Zuweisen von Datenelementen zu Analytics-Variablen

Wenn Sie eine Bibliothek in Launch veröffentlichen, nachdem Sie diese Schritte ausgeführt haben, können Sie benutzerdefinierte Dimensionen in Analyse Workspace verwenden. Sie können Analytics-Variablen global oder in einzelnen Regeln festlegen.

### Globale Variablen festlegen

Globale Variablen eignen sich ideal, wenn Sie Variablenwerte auf allen Seiten festlegen möchten, auf denen Ihr Datenelement vorhanden ist.

1. Wechseln Sie zu [Adobe Experience Platform Launch](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die gewünschte Eigenschaft Start.
1. Click the [!UICONTROL Extensions tab], then click [!UICONTROL Configure] under the Adobe Analytics extension.
1. Klicken Sie auf das Akkordeon [!UICONTROL Globale Variablen] , das die Oberfläche zum Zuweisen globaler Variablen anzeigt.

### Variablen in Regeln festlegen

Die in Regeln festgelegten Variablen eignen sich ideal, wenn Sie nicht möchten, dass Variablen auf jeder Seite festgelegt werden. Sie definieren die Kriterien in der Regel. See [Rules](https://docs.adobe.com/content/help/de-DE/launch/using/reference/manage-resources/rules.html) in the Adobe Experience Platform Launch user guide.

1. Wechseln Sie zu [Adobe Experience Platform Launch](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
1. Klicken Sie auf die gewünschte Eigenschaft Start.
1. Klicken Sie auf die Registerkarte [!UICONTROL Regeln] und dann auf die gewünschte Regel (oder erstellen Sie eine).
1. Klicken Sie auf die [!UICONTROL Hinzufügen] -Schaltfläche unter [!UICONTROL Aktionen].
1. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf Variablen festlegen.
1. Klicken Sie auf das Symbol ![Datenelement](assets/data-element.png) rechts neben der gewünschten Analytics-Variable. Das [Lösungsdesign-Dokument](../prepare/solution-design.md) Ihres Unternehmens bestimmt, welche Analytics-Variable verwendet werden soll.
1. Wählen Sie im modalen Fenster das gewünschte Datenelement aus. Klicken Sie auf [!UICONTROL Auswählen].
1. Der Name des Datenelements wird dem Textfeld, das von `%` Zeichen umgeben ist, hinzugefügt. Wenn Sie Ihr Datenelement beispielsweise &quot;Seitenname&quot;nennen, wird die Zeichenfolge angezeigt, `%Page name%` wenn Sie einer Variablen ein Datenelement zuweisen.

>[!TIP] Sie können Datenelemente in derselben Variablen verketten. Wenn Sie beispielsweise ein Datenelement &quot;Hostname&quot;und ein Datenelement &quot;Pathname&quot;haben, können Sie beide mit `%Hostname%%Pathname%`einer Variablen kombinieren.

## Nächste Schritte

[Seitenvariablen](../vars/page-vars/page-variables.md): Erfahren Sie, welche Variablen auf Seitenebene Sie in Ihrer Implementierung verwenden können, um mehr aus den Dimensionen in Analyse Workspace herauszuholen.

[Konfigurationsvariablen](../vars/config-vars/configuration-variables.md): Erfahren Sie, welche Konfigurationsvariablen Sie in Ihrer Implementierung verwenden können, um weitere Funktionen in Adobe Analytics zu entsperren.
