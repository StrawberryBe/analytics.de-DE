---
title: Tag-Datenelemente Analytics-Variablen zuordnen
description: Weisen Sie den Analytics-Variablen Datenelemente zu, damit Sie sie als Dimensionen in Analysis Workspace verwenden können.
exl-id: 996c1204-3f8a-453e-8104-5e8e1279517c
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 65%

---

# Tag-Datenelemente Analytics-Variablen zuordnen

Sobald Sie über ein Repository mit Tag-Datenelementen verfügen, können Sie sie Analytics-Dimensionen zuweisen.

>[!NOTE]
>Adobe Experience Platform Launch wurde in Experience Platform als eine Suite von Datenerfassungstechnologien umbenannt. Infolgedessen wurden in der gesamten Produktdokumentation mehrere terminologische Änderungen eingeführt. Eine konsolidierte Übersicht der terminologischen Änderungen finden Sie im folgenden [Dokument](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en).

## Voraussetzungen

[Ordnen Sie Datenschichtobjekte Datenelementen](layer-to-elements.md) zu: Vergewissern Sie sich, dass Sie mit Tag-Datenelementen vertraut sind und mehrere Elemente zur Verfügung haben.

[Erstellen Sie ein Lösungs-Design-Dokument](../prepare/solution-design.md): Ein Lösungs-Design-Dokument ist für eine übersichtliche Organisation unverzichtbar. Wenn Sie Ihrem Lösungs-Design-Projekts folgen, wird die Zuweisung von Datenelementen zu Analytics-Variablen einfacher.

## Zuweisen von Datenelementen zu Analytics-Variablen

Wenn Sie eine Tag-Bibliothek veröffentlichen, nachdem Sie diese Schritte ausgeführt haben, können Sie benutzerdefinierte Dimensionen in Analysis Workspace verwenden. Sie können Analytics-Variablen global oder in einzelnen Regeln festlegen.

### Globale Variablen festlegen

Globale Variablen eignen sich ideal, wenn Sie Variablenwerte auf allen Seiten festlegen möchten, auf denen Ihr Datenelement vorhanden ist.

1. Gehen Sie zu `experience.adobe.com` und melden Sie sich bei entsprechender Aufforderung an.
1. Wählen Sie [!UICONTROL Launch/Data Collection] aus.
1. Klicken Sie auf [!UICONTROL Gehen Sie zu Launch/Data Collection] und wählen Sie [!UICONTROL Tags] aus.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie auf die Registerkarte [!UICONTROL Erweiterungen] und dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].
1. Klicken Sie auf das Akkordeon [!UICONTROL Globale Variablen]. Daraufhin wird die Benutzeroberfläche zum Zuweisen globaler Variablen angezeigt.

### Variablen in Regeln festlegen

Die in Regeln festgelegten Variablen sind optimal, wenn Sie nicht möchten, dass Variablen auf jeder Seite festgelegt werden. Sie definieren die Kriterien in der Regel. Siehe [Rules](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html) in der Dokumentation zur Adobe Experience Platform-Datenerfassung.

1. Gehen Sie zu `experience.adobe.com` und melden Sie sich bei entsprechender Aufforderung an.
1. Wählen Sie [!UICONTROL Launch/Data Collection] aus.
1. Klicken Sie auf [!UICONTROL Gehen Sie zu Launch/Data Collection] und wählen Sie [!UICONTROL Tags] aus.
1. Klicken Sie auf die gewünschte Tag-Eigenschaft.
1. Klicken Sie auf die Registerkarte [!UICONTROL Regeln] und dann auf die gewünschte Regel (oder erstellen Sie eine).
1. Klicken Sie auf die Schaltfläche [!UICONTROL Hinzufügen] unter [!UICONTROL Aktionen].
1. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf „Variablen festlegen“.
1. Klicken Sie auf das Symbol ![Datenelement](assets/data-element.png) rechts neben der gewünschten Analytics-Variable. Das [Lösungs-Design-Dokument](../prepare/solution-design.md) Ihres Unternehmens bestimmt, welche Analytics-Variable verwendet werden soll.
1. Wählen Sie im modalen Fenster das gewünschte Datenelement aus. Klicken Sie auf [!UICONTROL Auswählen].
1. Der Name des Datenelements wird dem Textfeld, das von `%`-Zeichen eingeschlossen ist, hinzugefügt. Wenn Sie Ihr Datenelement beispielsweise „Seitenname“ nennen, wird die Zeichenfolge `%Page name%` angezeigt, wenn Sie einer Variablen ein Datenelement zuweisen.

>[!TIP]
>
>Sie können Datenelemente in derselben Variablen verketten. Wenn Sie beispielsweise das Datenelement „Hostname“ und das Datenelement „Pathname“ haben, können Sie beide durch `%Hostname%%Pathname%` in einer einzigen Variablen kombinieren.

## Nächste Schritte

[Seitenvariablen](../vars/page-vars/page-variables.md): Erfahren Sie, welche Seitenebenenvariablen Sie in Ihrer Implementierung verwenden können, um die Dimensionen in Analysis Workspace optimal zu nutzen.

[Konfigurationsvariablen](../vars/config-vars/configuration-variables.md): Erfahren Sie, welche Konfigurationsvariablen Sie in Ihrer Implementierung verwenden können, um weitere Funktionen in Adobe Analytics zu verwenden.
