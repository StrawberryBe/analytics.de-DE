---
title: Bot-Entfernung in Adobe Analytics
seo-title: Bot-Entfernung in Adobe Analytics
description: 3 Möglichkeiten zum Entfernen von Bots in Adobe Analytics
seo-description: 3 Möglichkeiten zum Entfernen von Bots in Adobe Analytics
translation-type: tm+mt
source-git-commit: 97c24ca865e11aa418febc40842d8fe9372d9cc3

---


# Bot-Entfernung in Adobe Analytics

In Adobe Analytics haben Sie drei Hauptoptionen zum Entfernen von Bot-Traffic aus der Berichterstellung:

1. Die standardmäßige Bot-Filtermethode in Adobe Analytics [besteht darin, Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) zu erstellen, die auf der IAB-Bot-Liste basieren. Diese Liste wird monatlich aktualisiert und die Liste aus vielen Quellen, einschließlich cdns und Hauptinterneteigenschaften, kompiliert. Es enthält Tausende bekannter Bots, einschließlich all Ihrer Favoriten: Google, Bing, Mozilla usw. Diese Liste enthält die überwältigende Mehrheit der Anwendungsfälle und Anforderungen rund um Bot-Filter.

1. Verwenden Sie das [s. hitcampaign-Implementierungs-Plug-in](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/plugins/hitgovernor.html), das Besucher, die sich wie Bots verhalten, durch Dutzende oder Hunderte von Treffern pro Minute entfernen.

1. Da Bots schnell vorankommen, bietet Adobe einige weitere leistungsstarke Funktionen, die, wenn sie richtig und regelmäßig kombiniert werden, zum Entfernen dieser Feind der Datenqualität beitragen können. Diese Funktionen sind: Experience Cloud ID-Dienst, Segmentierung, Data Warehouse, Kundenattribute und Virtual Report Suites. Im Folgenden finden Sie einen Überblick darüber, wie Sie diese Werkzeuge nutzen können:

## Schritt 1: Übermitteln der Experience Cloud ID Ihrer Besucher an eine neue deklarierte ID

Um zu beginnen, möchten Sie eine neue deklarierte ID im Hauptdienst [Zielgruppen erstellen](https://docs.adobe.com/content/help/en/core-services/interface/audiences/audience-library.html). Sie müssen die Experience Cloud ID Ihres Besuchers an diese neue deklarierte ID übergeben, die mit dem [Adobe Experience Platform Launch schnell und einfach ausgeführt werden kann](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html). Verwenden wir den Namen "ECID" für die deklarierte ID.

Screenshot hier

Hier ein Screenshot, wie diese ID über Datenelement erfasst werden kann. Stellen Sie sicher, dass die Adobe mcorg-ID korrekt in das Datenelement eingetragen ist.

```return Visitor.getInstance("REPLACE_WITH_YOUR_ECORG_ID@AdobeOrg").getExperienceCloudVisitorID();```

Nachdem dieses Datenelement eingerichtet wurde, befolgen [Sie diese Anweisungen,](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) um die deklarierten Ids im ECID-Tool im Start zu übergeben.

## Schritt 2: Verwenden der Segmentierung zur Identifizierung von Bots

Nachdem Sie die ECID Ihres Besuchers an eine deklarierte ID weitergegeben haben, ist es Zeit, die Segmentierung im Analysis Workspace zu verwenden, um Besucher zu identifizieren, die wie Bots fungieren. Bots werden häufig durch ihr Verhalten definiert: Einzelzugriff, ungewöhnliche Benutzeragenten, unbekannte Geräte-/Browserinformationen, keine verweisenden Stellen, neue Besucher, ungewöhnliche Einstiegsseiten usw. Verwenden Sie die Funktionen von Workspace-Drilldowns und -segmentierungen, um die Bots herauszufinden, die eine EVAB-Filterung und Ihre Report Suite-Bot-Regeln haben. Beispiel: Hier ein Screenshot eines Segments, das Sie verwenden könnten:

![](assets/bot-filter-seg1.png)

## Schritt 3: Alle ecids aus dem Segment über Data Warehouse exportieren

Nachdem Sie die Bots mithilfe von Segmenten identifiziert haben, dient der nächste Schritt zur Nutzung von Data Warehouse, um alle mit diesem Segment verknüpften Experience Cloud-IDs zu extrahieren. So sollten Sie Ihren [Data Warehouse](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html) -Bericht einrichten:

![](assets/bot-dwh-3.png)

Denken Sie daran, die Experience Cloud Besucher-ID als Dimension zu verwenden und das Bots-Segment anzuwenden.

## Schritt 4: Übergeben Sie diese Liste zurück an Adobe als Kundenattribut

Sobald der Data Warehouse-Bericht eingehen, erhalten Sie eine Liste mit ecids, die aus historischen Daten gefiltert werden müssen. Kopieren Sie diese ecids in eine leere CSV-Datei mit nur zwei Spalten, ECID und Bot Flag:



Stellen Sie sicher, dass die erste Spaltenüberschrift mit dem Namen übereinstimmt, den Sie der neuen deklarierten ID oben gegeben haben. Verwenden Sie diese. CSV-Datei als Importdatei für Kundenattribute und abonnieren Sie Ihre Report Suite (s) dem Kundenattribut, wie in diesem [Blog-Beitrag beschrieben](https://theblog.adobe.com/link-digital-behavior-customers).

## Schritt 5: Erstellen Sie ein Segment, das das neue Kundenattribut nutzt.

Nachdem Ihr Datensatz verarbeitet und in den Analysis Workspace integriert wurde, erstellen Sie ein weiteres Segment, das Ihre neue Kundenattributdimension "Bot-Marke" nutzt:
