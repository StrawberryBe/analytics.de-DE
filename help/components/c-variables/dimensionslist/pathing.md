---
description: Eine Gruppe von auf Pfadanalysen basierenden Berichten. Technisch gesehen, sind Pfade die Navigation von einem Seitennamen zu einem anderen (von einem Wert zum nächsten).
title: Pathing
topic: Reports
uuid: c4ff9fa8-e567-4039-9c86-322800a942da
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Pathing

Eine Gruppe von auf Pfadanalysen basierenden Berichten. Technisch gesehen, sind Pfade die Navigation von einem Seitennamen zu einem anderen (von einem Wert zum nächsten).

Verwenden Sie die [Flussfunktion in Analysis Workspace](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) für flexiblere Pfadoptionen.

>[!NOTE] Gehen Sie zu , um Pfade zu aktivieren **[!UICONTROL Admin > Report Suites > Edit Settings > Traffic > Traffic Variables]**. Wenden Sie sich zum Aktivieren von Pfaden in den Sitebereichs- und Server-Berichten an die Kundenunterstützung.

Wenn Sie die Reihenfolge benötigen, in der Werte erfasst werden, müssen Sie Pfade für die Variablenerfassung dieser Werte aktivieren. Pfade werden standardmäßig für Seiten aktiviert. Pfade werden nicht standardmäßig für Eigenschaften aktiviert, da dies nur in bestimmten Fällen angebracht ist. Wenden Sie sich an den Kundendienst, um Pfade für eine Eigenschaft zu aktivieren.

>[!NOTE] Wenn Sie in Ad Hoc Analysis Klassifizierungen für Eigenschaften aktivieren, werden Pfadmetriken aller für die aktivierte Eigenschaft eingerichteten Klassifizierungen angezeigt.

**Beispiel: Pfade für Sitebereiche**

Mit dem Aktivieren von Pfaden für  *`s.channel`* die Variable können Sie verfolgen, wie Sitebesucher zwischen Sitebereichen wechseln (da sich der Wert ändert).

![](assets/path_sections.png)

Pathing is then available in various paths reports, such as [!UICONTROL Next Site Section Flow], which displays how visitors move through page groups, or sections of your site.

![](assets/paths_report.png)

**Beispiel: Pfade bei Suchvorgängen**

Dieses Konzept der Navigation von einem Wert zum nächsten gilt auch für andere Traffic-Variablen, wie  *`s.props`*. Wenn Sie beispielsweise Pfade für Ihren internen Suchbegriff *`s.prop`* aktivieren, können Sie sehen, welchen Pfad Besucher durch Suchbegriffe nehmen.

**Beispiel: Pfade pro Anmeldestatus**

Sie möchten vielleicht wissen, wie Besucher basierend auf ihrem Anmeldestatus durch Ihre Site navigieren. Um diese Informationen zu erhalten, würden Sie nicht die Pfadsetzungsberichte zum Anmeldestatus ansehen, da diese zeigen, wie Besucher Werte in diesem Bericht verändert haben oder welche Veränderungen Besucher zwischen An- und Abmelden durchgemacht haben. Sie würden stattdessen den Segmentwert mit der  *`s.pageName`* Variablen verketten und dann den Pfad für die sich ergebende Variable analysieren. Hier ist ein Codebeispiel für eine Seitenpfadanalyse nach Mitgliedsstatus:

```js
s.pageName="Home Page"; 
s.prop18="Gold"; // Member Status 
s.prop19=s.prop18 + ":" + s.pageName;
```

Aktivieren Sie dann die Pfade für  *`s.prop19`*, um zu verfolgen, wie Besucher durch die Seiten navigieren.

>[!NOTE] Wenn Sie Ad-hoc-Analysen durchführen, können Sie Seitenpfade segmentieren, ohne die Segmentwerte verketten zu müssen. Weisen Sie dann alle Segmente den Pfadsetzungsberichten zu.

