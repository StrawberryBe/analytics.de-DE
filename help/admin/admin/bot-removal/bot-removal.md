---
title: Bot-Entfernung in Adobe Analytics
seo-title: Bot-Entfernung in Adobe Analytics
description: 3 Möglichkeiten zum Entfernen von Bots in Adobe Analytics
seo-description: 3 Möglichkeiten zum Entfernen von Bots in Adobe Analytics
translation-type: tm+mt
source-git-commit: 07b18333144f992031dca5a5d8838206fa735cb5

---


# Bot-Entfernung in Adobe Analytics

In Adobe Analytics haben Sie mehrere Optionen zum Entfernen von Bot-Traffic aus der Berichterstellung:

## Bot-Regeln verwenden

Die standardmäßige Bot-Filtermethode in Adobe Analytics [besteht darin, Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) zu erstellen, die auf der IAB-Bot-Liste basieren. Diese Liste wird monatlich aktualisiert und die Liste aus vielen Quellen, einschließlich cdns und Hauptinterneteigenschaften, kompiliert. Es enthält Tausende bekannter Bots, einschließlich all Ihrer Favoriten: Google, Bing, Mozilla usw. Diese Liste enthält die überwältigende Mehrheit der Anwendungsfälle und Anforderungen rund um Bot-Filter.

## Verwenden des `hitGovernor` Implementierungs-Plug-ins

Verwenden Sie das [s. hitcampaign-Implementierungs-Plug-in](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/plugins/hitgovernor.html), das Besucher, die sich wie Bots verhalten, durch Dutzende oder Hunderte von Treffern pro Minute entfernen.

## Verwenden einer Kombination aus Adobe Tools

Da Bots schnell vorankommen, bietet Adobe einige weitere leistungsstarke Funktionen, die, wenn sie richtig und regelmäßig kombiniert werden, zum Entfernen dieser Feind der Datenqualität beitragen können. Diese Funktionen sind: Experience Cloud ID-Dienst, Segmentierung, Data Warehouse, Kundenattribute und Virtual Report Suites. Hier finden Sie eine Übersicht darüber, wie Sie diese Tools nutzen können.

### Schritt 1: Übermitteln der Experience Cloud ID Ihrer Besucher an eine neue deklarierte ID

Um zu beginnen, möchten Sie eine neue deklarierte ID im Hauptdienst [Zielgruppen erstellen](https://docs.adobe.com/content/help/en/core-services/interface/audiences/audience-library.html). Sie müssen die Experience Cloud ID Ihres Besuchers an diese neue deklarierte ID übergeben, die mit dem [Adobe Experience Platform Launch schnell und einfach ausgeführt werden kann](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html). Verwenden wir den Namen "ECID" für die deklarierte ID.

Screenshot hier

So kann diese ID über Datenelement erfasst werden. Stellen Sie sicher, dass Sie Ihre Adobe ecorg-ID korrekt in das Datenelement einbetten.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

Nachdem dieses Datenelement eingerichtet wurde, befolgen [Sie diese Anweisungen,](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) um die deklarierten Ids im ECID-Tool im Start zu übergeben.

### Schritt 2: Verwenden der Segmentierung zur Identifizierung von Bots

Nachdem Sie die ECID Ihres Besuchers an eine deklarierte ID weitergegeben haben, können Sie [die Segmentierung im Analysis Workspace](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/components/t-freeform-project-segment.html) verwenden, um Besucher zu identifizieren, die wie Bots fungieren. Bots werden häufig durch ihr Verhalten definiert: Einzelzugriff, ungewöhnliche Benutzeragenten, unbekannte Geräte-/Browserinformationen, keine verweisenden Stellen, neue Besucher, ungewöhnliche Einstiegsseiten usw. Verwenden Sie die Funktionen von Workspace-Drilldowns und -segmentierungen, um die Bots herauszufinden, die eine EVAB-Filterung und Ihre Report Suite-Bot-Regeln haben. Beispiel: Hier ein Screenshot eines Segments, das Sie verwenden könnten:

![](assets/bot-filter-seg1.png)

### Schritt 3: Alle ecids aus dem Segment über Data Warehouse exportieren

Nachdem Sie die Bots mithilfe von Segmenten identifiziert haben, dient der nächste Schritt zur Nutzung von Data Warehouse, um alle mit diesem Segment verknüpften Experience Cloud-IDs zu extrahieren. So sollten Sie Ihre [Data Warehouse](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) -Anforderung einrichten:

![](assets/bot-dwh-3.png)

Denken Sie daran, die Experience Cloud Besucher-ID als Dimension zu verwenden und das Bots-Segment anzuwenden.

### Schritt 4: Übergeben Sie diese Liste zurück an Adobe als Kundenattribut

Sobald der Data Warehouse-Bericht eingehen, erhalten Sie eine Liste mit ecids, die aus historischen Daten gefiltert werden müssen. Kopieren Sie diese ecids in eine leere. CSV-Datei mit nur zwei Spalten, ECID und Bot Flag:

![](assets/bot-csv-4.png)

Stellen Sie sicher, dass die erste Spaltenüberschrift mit dem Namen übereinstimmt, den Sie der neuen deklarierten ID oben gegeben haben. Verwenden Sie diese. CSV-Datei als Importdatei für Kundenattribute und abonnieren Sie Ihre Report Suite (s) dem Kundenattribut, wie in diesem [Blog-Beitrag beschrieben](https://theblog.adobe.com/link-digital-behavior-customers).

### Schritt 5: Erstellen Sie ein Segment, das das neue Kundenattribut nutzt.

Nachdem Ihr Datensatz verarbeitet und in den Analysis Workspace integriert wurde, erstellen Sie ein weiteres Segment, das Ihre neue Kundenattributdimension "Bot-Marke" nutzt:

![](assets/bot-filter-seg2.png)

### Schritt 6: Verwenden Sie dieses Segment als Filter für Virtual Report Suite

Schließlich sollten Sie eine [Virtual Report Suite](/help/components/vrs/vrs-about.md) erstellen, die dieses Segment nutzt, um die identifizierten Bots zu filtern:

![](assets/bot-vrs.png)

Diese neu segmentierte Virtual Report Suite führt jetzt zu einem deutlich saubereren Datensatz, wobei die identifizierten Bots vollständig entfernt werden.

### Schritt 7: Wiederholen Sie die Schritte 2, 3 und 4 regelmäßig.

Legen Sie mindestens eine monatliche Erinnerung zur Identifizierung und Filterung neuer Bots, möglicherweise vor der regelmäßigen geplanten Analyse, fest.

