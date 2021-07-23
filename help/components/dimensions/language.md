---
title: Sprache
description: Die bevorzugte Spracheinstellung im Browser.
exl-id: 590406a4-d336-42c7-8048-e7cd8e611d43
source-git-commit: e6f3beadfba340cea07f5fd2694105ad31de9751
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 86%

---

# Sprache

Die Dimension „Sprache“ zeigt die häufigsten Sprachen an, in denen die Besucher den Inhalt am liebsten sehen möchten. Diese Dimension ist nützlich, wenn Sie die am häufigsten bevorzugten Sprachen der Besucher verstehen möchten, um die Lokalisierungsbemühungen zu unterstützen.

>[!NOTE]
>
>Diese Dimension erfasst nicht die Sprache Ihrer Site. Wenn Sie die Sprache Ihrer Site in einer Dimension erfassen möchten, empfiehlt Adobe die Verwendung einer benutzerdefinierten Variable, z. B. einer [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `Accept-Language` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über -Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Die Dimensionselemente enthalten die Anzeigenamen der bevorzugten Sprachen der Besucher. Beispiele sind `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"` und `"Spanish (Spain)"`. Wenn eine Bildanforderung keine gültige Sprache in der HTTP-Kopfzeile enthält, lautet das Dimensionselement `"None"`.
