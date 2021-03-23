---
description: Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.
title: Segmente löschen
topic: Segmente
uuid: cb6db6ad-f400-4633-900a-8a02dcfccf2c
translation-type: ht
source-git-commit: d0fe97b9368cbc4c9e79f9e56adf9786b58dce1a
workflow-type: ht
source-wordcount: '204'
ht-degree: 100%

---


# Segmente löschen

Führt einige Überlegungen auf, die Sie vor dem Löschen von Segmenten anstellen sollten.

Wenn Sie ein Segment löschen, hat dies folgende Auswirkungen:

* Terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, funktionieren weiter normal, d. h., das Segment bzw. das Dashboard verwendet weiterhin das gelöschte Segment.
* Terminierte Berichte werden nicht aktualisiert, wenn Sie ein Segment mit demselben Namen aktualisieren. Ein Beispiel: Angenommen, Sie haben 2 Segmente mit demselben Namen in unterschiedlichen Report Suites:

   ![](assets/duplicate_seg_names.png)

   Sie haben ein Lesezeichen, das das Segment für die Report Suite „mainprod“ referenziert. Dann löschen Sie das Segment, weil es sich um ein Duplikat handelt. Das Lesezeichen funktioniert weiterhin und referenziert die Definition des gelöschten Segments. Wenn Sie die Segmentdefinition des verbleibenden Segments ändern und „Catalina Island“ und „Tijuana Mexiko“ einfügen, wird das auf das Lesezeichen angewendete Segment nicht geändert. Es verwendet weiterhin die alte Definition. Um dies zu beheben, müssen Sie das Lesezeichen aktualisieren, damit es die neue Definition referenziert. Wenn Sie nicht sicher sind, ob ein Lesezeichen, ein Dashboard oder ein terminierter Bericht ein gelöschtes Segment verwendet, können Sie den Namen des Segments ändern, damit deutlich wird, ob das Lesezeichen das Segment verwendet.
