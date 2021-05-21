---
title: Sprache
description: Die bevorzugte Spracheinstellung im Browser.
exl-id: 590406a4-d336-42c7-8048-e7cd8e611d43
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '157'
ht-degree: 100%

---

# Sprache

Die Dimension „Sprache“ zeigt die häufigsten Sprachen an, in denen die Besucher den Inhalt am liebsten sehen möchten. Diese Dimension ist nützlich, wenn Sie die am häufigsten bevorzugten Sprachen der Besucher verstehen möchten, um die Lokalisierungsbemühungen zu unterstützen.

>[!NOTE]
>
>Diese Dimension erfasst nicht die Sprache Ihrer Site. Wenn Sie die Sprache Ihrer Site in einer Dimension erfassen möchten, empfiehlt Adobe die Verwendung einer benutzerdefinierten Variable, z. B. einer [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `Accept-Language` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Die Dimensionselemente enthalten die Anzeigenamen der bevorzugten Sprachen der Besucher. Beispiele sind `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"` und `"Spanish (Spain)"`. Wenn eine Bildanforderung keine gültige Sprache in der HTTP-Kopfzeile enthält, lautet das Dimensionselement `"None"`.
