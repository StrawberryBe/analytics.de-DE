---
title: Sprache
description: Die bevorzugte Spracheinstellung im Browser.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 80%

---


# Sprache

Die Dimension „Sprache“ zeigt die häufigsten Sprachen an, in denen die Besucher den Inhalt am liebsten sehen möchten. Diese Dimension ist nützlich, wenn Sie die am häufigsten bevorzugten Sprachen der Besucher verstehen möchten, um die Lokalisierungsbemühungen zu unterstützen.

>[!NOTE]
>
>Diese Dimension erfasst nicht die Sprache Ihrer Site. Wenn Sie die Sprache Ihrer Site in einer Dimension erfassen möchten, empfiehlt Adobe die Verwendung einer benutzerdefinierten Variable, z. B. einer [eVar](evar.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `Accept-Language` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert.

## Dimensionen

Dimensionen enthalten benutzerfreundliche Namen der bevorzugten Sprachen der Besucher. Beispiele sind `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"` und `"Spanish (Spain)"`. If an image request does not contain a valid language in the HTTP header, the dimension item is `"None"`.
