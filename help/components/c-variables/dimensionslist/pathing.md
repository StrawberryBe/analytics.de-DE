---
description: Eine Gruppe von Berichten, die auf der Analyse des Pfads basieren. Technisch gesehen bedeutet Pfade, von einem Seitennamen zu einem anderen zu wechseln (von einem Wert zum anderen).
title: Pathing
topic: Reports
uuid: c4ff9fa8-e567-4039-9c86-322800a942da
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Pathing

Eine Gruppe von Berichten, die auf der Analyse des Pfads basieren. Technisch gesehen bedeutet Pfade, von einem Seitennamen zu einem anderen zu wechseln (von einem Wert zum anderen).

Verwenden Sie die [Flussfunktion in Analysis Workspace](https://marketing.adobe.com/resources/help/en_US/analytics/analysis-workspace/flow.html) für flexiblere Pfadoptionen.

>[!NOTE] Gehen Sie zu , um Pfade zu aktivieren **[!UICONTROL Admin > Report Suites > Edit Settings > Traffic > Traffic Variables]**. Wenden Sie sich zum Aktivieren von Pfaden in den Sitebereichs- und Server-Berichten an die Kundenunterstützung.

Wenn Sie wissen müssen, in welcher Reihenfolge Werte erfasst werden, müssen Sie die Pathing-Funktion für die Variable aktivieren, die diese Werte erfasst. Pfade sind für Seiten standardmäßig aktiviert. Pfade sind für Props standardmäßig nicht aktiviert, da sie nur in bestimmten Fällen geeignet sind. Wenden Sie sich an den Kundendienst, um Pfade für eine Eigenschaftsvariable zu aktivieren.

>[!NOTE] Wenn Sie in Ad Hoc Analysis Klassifizierungen für Eigenschaften aktivieren, werden Pfadmetriken aller für die aktivierte Eigenschaft eingerichteten Klassifizierungen angezeigt.

**Beispiel: Pfade für Sitebereiche**

Mit dem Aktivieren von Pfaden für  *`s.channel`* die Variable können Sie verfolgen, wie Sitebesucher zwischen Sitebereichen wechseln (da sich der Wert ändert).

![](assets/path_sections.png)

Pfade stehen dann in verschiedenen Pfadberichten zur Verfügung, z. B. [!UICONTROL Next Site Section Flow]in denen angezeigt wird, wie Besucher durch Seitengruppen oder Bereiche Ihrer Site navigieren.

![](assets/paths_report.png)

**Beispiel: Pfade bei Suchvorgängen**

Dieses Konzept der Navigation von einem Wert zum nächsten gilt auch für andere Traffic-Variablen, wie  *`s.props`*. Wenn Sie beispielsweise Pfade für Ihren internen Suchbegriff *`s.prop`* aktivieren, können Sie sehen, welchen Pfad Besucher durch Suchbegriffe nehmen.

**Beispiel: Pfade pro Anmeldestatus**

Möglicherweise möchten Sie wissen, wie die Besucher anhand des Anmeldestatus eines Besuchers durch Ihre Site navigieren. Um diese Informationen anzuzeigen, würden Sie die Pfadberichte nicht auf den Anmeldestatus prüfen, da sie Ihnen zeigen würden, wie Besucher die Werte in diesem Bericht geändert haben oder wie sich Besucher möglicherweise von angemeldet zu abgemeldet haben. Sie würden stattdessen den Segmentwert mit der  *`s.pageName`* Variablen verketten und dann den Pfad für die sich ergebende Variable analysieren. Hier ist ein Codebeispiel für eine Seitenpfadanalyse nach Mitgliedsstatus:

```js
s.pageName="Home Page"; 
s.prop18="Gold"; // Member Status 
s.prop19=s.prop18 + ":" + s.pageName;
```

Aktivieren Sie dann die Pfade für  *`s.prop19`*, um zu verfolgen, wie Besucher durch die Seiten navigieren.

>[!NOTE] Wenn Sie Ad-hoc-Analysen durchführen, können Sie Seitenpfade segmentieren, ohne die Segmentwerte verketten zu müssen. Weisen Sie dann alle Segmente den Pfadsetzungsberichten zu.

