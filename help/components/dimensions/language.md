---
title: Sprache
description: Die bevorzugte Spracheinstellung im Browser.
translation-type: tm+mt
source-git-commit: 2c262e5345c39a71a6a54062c607273528294b24
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# Sprache

Die Dimension &quot;Sprache&quot;zeigt die wichtigsten Sprachen an, in denen die Besucher den Inhalt lieber sehen. Diese Dimension ist nützlich, wenn Sie die am häufigsten bevorzugten Sprachen der Besucher verstehen möchten, die bei den Bemühungen um die lokale Anpassung unterstützt werden.

> [!NOTE] Diese Dimension erfasst nicht die Sprache Ihrer Site. Wenn Sie die Sprache Ihrer Site in einer Dimension erfassen möchten, empfiehlt Adobe die Verwendung einer benutzerspezifischen Variablen, z. B. einer [eVar](evar.md).

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf eine interne Nachschlagetabelle von Adobe. Der Nachschlagewert basiert auf dem `Accept-Language` HTTP-Header in Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig.

## Dimensionswerte

Dimensionswerte enthalten Anzeigenamen der bevorzugten Sprachen der Besucher. Examples include `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"`, and `"Spanish (Spain)"`. Wenn eine Bildanforderung keine gültige Sprache im HTTP-Header enthält, lautet der Dimensionswert `"None"`.
