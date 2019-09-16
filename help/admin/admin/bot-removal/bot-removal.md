---
title: Bot-Entfernung in Adobe Analytics
seo-title: Bot-Entfernung in Adobe Analytics
description: 3 Möglichkeiten zum Entfernen von Bots in Adobe Analytics
seo-description: 3 Möglichkeiten zum Entfernen von Bots in Adobe Analytics
translation-type: tm+mt
source-git-commit: ef17712b4a8a4a5c13dde9be9fdf2281eeb40091

---


# Bot-Entfernung in Adobe Analytics

In Adobe Analytics stehen Ihnen mehrere Optionen zum Entfernen des Bot-Traffics aus der Berichterstellung zur Verfügung:

## Bot-Regeln verwenden

Sowohl Standard- als auch benutzerdefinierte Bot-Filtermethoden werden unter **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL Einstellungen]** bearbeiten &gt; **[!UICONTROL Allgemein]** ****&gt;Bot-Regelnunterstützt:

| Regeltyp | Beschreibung |
|--- |--- |
| Standard-IAB-Bot-Regeln | Wenn Sie IAB-Bot-Filterregeln **** aktivieren auswählen, wird die internationale Spiders &amp; Bots-Liste des [IABs](https://www.iab.com/) (International Advertising Bureau) verwendet, um Bot-Traffic zu entfernen. Die meisten Kunden wählen diese Option mindestens aus. |
| Benutzerspezifische Bot-Regeln | Sie können benutzerspezifische Bot-Regeln basierend auf Benutzeragenten, IP-Adressen oder IP-Bereichen definieren und hinzufügen. |

Weitere Informationen finden Sie unter Übersicht über [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md).

## Verwenden des `hitGovernor` Implementierungs-Plug-ins

Verwenden Sie das [s.hitGovernor-Implementierungs-Plugin](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/plugins/hitgovernor.html), das Besucher entfernt, die sich wie Bots verhalten, d. h., diese Besucher senden Dutzende oder Hunderte von Treffern pro Minute.

## Verwenden Sie eine Kombination aus Adobe Tools

Da Bots sich schnell wandeln, bietet Adobe außerdem einige weitere leistungsstarke Funktionen, die bei korrekter und regelmäßiger Kombination dazu beitragen können, diese Feinde der Datenqualität zu beseitigen. Diese Funktionen sind: Experience Cloud ID-Dienst, Segmentierung, Data Warehouse, Kundenattribute und Virtual Report Suites. Im Folgenden finden Sie eine Übersicht darüber, wie Sie diese Werkzeuge nutzen können.

### Schritt 1: Erhalten der Experience Cloud ID Ihrer Besucher in eine neue deklarierte ID

Zunächst möchten Sie eine neue deklarierte ID im [People Core Service](https://docs.adobe.com/content/help/en/core-services/interface/audiences/audience-library.html)erstellen. Sie müssen die Experience Cloud ID Ihres Besuchers an diese neue deklarierte ID weitergeben, die mit [Adobe Experience Platform Launch](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html)schnell und einfach ausgeführt werden kann. Verwenden wir den Namen "ECID"für die deklarierte ID.

![](assets/bot-cust-attr-setup.png)

Im Folgenden wird beschrieben, wie diese ID über Datenelement erfasst werden kann. Achten Sie darauf, Ihre Experience Cloud-Organisations-ID korrekt in das Datenelement einzutragen.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

Nachdem dieses Datenelement eingerichtet wurde, befolgen Sie [diese Anweisungen](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) , um deklarierte IDs in das ECID-Tool beim Start zu übertragen.

### Schritt 2: Verwenden Sie die Segmentierung, um Bots zu identifizieren.

Nachdem die ECID Ihres Besuchers an eine deklarierte ID weitergegeben wurde, können Sie die [Segmentierung in Analysis Workspace](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html) verwenden, um Besucher zu identifizieren, die sich wie Bots verhalten. Bots werden oft durch ihr Verhalten definiert: Besuche mit Einzelzugriff, ungewöhnliche Benutzeragenten, unbekannte Geräte-/Browserinformationen, keine Referrer, neue Besucher, ungewöhnliche Einstiegsseiten usw. Verwenden Sie die Möglichkeiten von Workspace-Drilldowns und Segmentierung, um die Bots zu identifizieren, die die IAB-Filterung und Ihre Report Suite-Bot-Regeln umgangen haben. Hier sehen Sie beispielsweise einen Screenshot eines Segments, das Sie verwenden könnten:

![](assets/bot-filter-seg1.png)

### Schritt 3: Exportieren Sie alle [!DNL Experience Cloud IDs] Segmente über Data Warehouse

Nachdem Sie nun die Bots mithilfe von Segmenten identifiziert haben, besteht der nächste Schritt darin, Data Warehouse zu nutzen, um alle Experience Cloud-IDs zu extrahieren, die diesem Segment zugeordnet sind. So sollten Sie Ihre [Data Warehouse](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) -Anforderung einrichten:

![](assets/bot-dwh-3.png)

Denken Sie daran, die Experience Cloud-Besucher-ID als Ihre Dimension zu verwenden und das Bots-Segment anzuwenden.

### Schritt 4: Diese Liste als Kundenattribut an Adobe zurückgeben

Sobald der Data Warehouse-Bericht ankommt, verfügen Sie über eine Liste der ECIDs, die aus historischen Daten gefiltert werden müssen. Kopieren Sie diese ECIDs und fügen Sie sie in eine leere .CSV-Datei mit nur zwei Spalten, ECID und Bot Flag, ein.

* **ECID**: Stellen Sie sicher, dass diese Spaltenüberschrift mit dem Namen übereinstimmt, den Sie oben für die neue deklarierte ID angegeben haben.
* **Bot-Flag**: Fügen Sie dies als Dimension des Kundenattributschemas hinzu.

Verwenden Sie diese .CSV-Datei als Importdatei für Kundenattribute und abonnieren Sie dann Ihre Report Suites für das Kundenattribut, wie in diesem [Blog-Beitrag](https://theblog.adobe.com/link-digital-behavior-customers)beschrieben.

![](assets/bot-csv-4.png)

### Schritt 5: Erstellen eines Segments, das das neue Kundenattribut nutzt

Nachdem Ihr Datensatz verarbeitet und in den Analysis Workspace integriert wurde, erstellen Sie ein weiteres Segment, das Ihre neue Kundenattributdimension "Bot-Kennzeichnung"und einen [!UICONTROL Ausschließen] -Container nutzt:

![](assets/bot-filter-seg2.png)

### Schritt 6: Dieses Segment als Virtual Report Suite-Filter verwenden

Schließlich sollten Sie eine [Virtual Report Suite](/help/components/vrs/vrs-about.md) erstellen, die dieses Segment nutzt, um die identifizierten Bots auszufiltern:

![](assets/bot-vrs.png)

Diese neu segmentierte Virtual Report Suite führt nun zu einem deutlich saubereren Datensatz, wobei die identifizierten Bots vollständig entfernt werden.

### Schritt 7: Wiederholen Sie die Schritte 2, 3 und 4 regelmäßig

Legen Sie mindestens eine monatliche Erinnerung fest, um neue Bots zu identifizieren und zu filtern, vielleicht vor der regelmäßigen Analyse.
