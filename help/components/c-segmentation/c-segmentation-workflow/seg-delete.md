---
description: Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.
seo-description: Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.
seo-title: Segmente löschen
solution: Analytics
title: Segmente löschen
topic: Segmente
uuid: cb 6 db 6 ad-f 400-4633-900 a -8 a 02 dcfccf 2 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Segmente löschen

Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.

Wenn Sie ein Segment löschen, hat dies folgende Auswirkungen:

* Terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, funktionieren weiter normal, d. h., das Segment bzw. das Dashboard verwendet weiterhin das gelöschte Segment.
* Terminierte Berichte werden nicht aktualisiert, wenn Sie ein Segment mit demselben Namen aktualisieren. Ein Beispiel: Angenommen, Sie haben 2 Segmente mit demselben Namen in unterschiedlichen Report Suites:

   ![](assets/duplicate_seg_names.png)

   Sie haben ein Lesezeichen, das das Segment für die Report Suite „mainprod“ referenziert. Dann löschen Sie das Segment, weil es sich um ein Duplikat handelt. Das Lesezeichen funktioniert weiterhin und referenziert die Definition des gelöschten Segments. Wenn Sie die Segmentdefinition des verbleibenden Segments ändern und „Catalina Island“ und „Tijuana Mexiko“ einfügen, wird das auf das Lesezeichen angewendete Segment nicht geändert. Es verwendet weiterhin die alte Definition. Um dies zu beheben, müssen Sie das Lesezeichen aktualisieren, damit es die neue Definition referenziert. Wenn Sie nicht sicher sind, ob ein Lesezeichen, ein Dashboard oder ein terminierter Bericht ein gelöschtes Segment verwenden, können Sie den Namen des Segments ändern, damit deutlich wird, ob das Lesezeichen das Segment verwendet.

## Edit Embedded Deleted Segments in Ad Hoc Analysis {#section_976D601DBD2244E38B0A0222E31D2610}

Mit Ad-hoc-Analysen können Sie jetzt eingebettete gelöschte Segmente im [Generator für berechnete Metriken](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/) bearbeiten und eine „Speichern als“-Handlung an diesem Segment vornehmen.

Alle anderen gelöschten Segmente, die auf das gelöschte Segment verweisen, bleiben jedoch unverändert.
