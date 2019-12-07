---
description: Die Variable „s.products“ ist bei der Erfassung von Daten wahrscheinlich die Variable, die die komplizierteste Syntax hat.
keywords: Analytics Implementation
subtopic: Troubleshooting
title: Häufige Fehler bei der Produktvariablen
topic: Developer and implementation
uuid: 94075c56-37c3-44de-bf37-1dfd228c6665
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Häufige Fehler bei der Produktvariablen

Die Variable „s.products“ ist bei der Erfassung von Daten wahrscheinlich die Variable, die die komplizierteste Syntax hat.

Kommas, Semikolons, Pipeline-Symbole und Gleichheitszeichen spielen bei dieser Variablen jeweils eigene Rollen. Bei der Gesamtlänge gibt es keine Einschränkungen, jedoch darf jeder einzelne Produkteintrag nicht länger als 100 Byte sein (inklusive Multi-Byte-Zeichen). Fehler bei der Implementierung dieser Variablen sind verständlich. Zum Leidwesen der Entwickler ist [!UICONTROL s.products] häufig die wichtigste Variable einer Site, da es mit ihr möglich ist, Erlöse, Einheiten, Produktnamen u.v.m. zu verfolgen.

Nachfolgend sind einige der gängigsten Fehler aufgeführt, die Entwicklern besonders leicht unterlaufen können, und die dann bei jeder Implementation zu Problemen führen.

Achten Sie darauf, dass Ihre Summen bei [!UICONTROL Kategorie], [!UICONTROL Produktname] und [!UICONTROL Umsatz] keine Kommas und Semikolons enthalten. Mit Kommas werden die einzelnen Einträge in der [!UICONTROL s.products]-Zeichenfolge getrennt. Dies geschieht, wenn in einer Transaktion zwei Produkte vorhanden sind. Mit dem Semikolon wiederum werden Felder innerhalb eines Eintrags abgegrenzt. Wenn Sie Kommas oder Semikolons anderweitig einsetzen, geht die Datenerfassung davon aus, dass hiermit Produkteinträge getrennt werden sollen. Siehe folgendes Beispiel:

```js
s.products="widgets;large widget, 40′x40′;1;19.99,wugs;tiny wug;2;1,999.98";
```

In dieser Implementation hat der Entwickler wahrscheinlich beabsichtigt, dass die Datenerfassung wie folgt aussieht:

Kategorie 1: Widgets

Produkt 1: großes Widget, 40′x40′

Einheiten 1: 1

Umsatz 1: 19.99

Kategorie 2: Wugs

Produkt 2: kleines Wug

Einheiten 2: 2

Umsatz 2: 1,999.98

Achten Sie auf die Kommas in den Einträgen von Produkt 1 und Umsatz 2. Diese würden einen neuen Produkteintrag angeben. Die Datenerfassung würde dies dann wie folgt interpretieren:

Kategorie 1: Widgets

Produkt 1: großes Widget

Kategorie 2: 40'x40'

Produkt 2: 1

Einheiten 2: 19.99

Kategorie 3: Wugs

Produkt 3: kleines Wug

Einheiten 3: 2

Umsatz 3: 1

Kategorie 4: 999.98

Ein Fehler wie dieser führt oft zu unerwarteten numerischen Werten im Bericht [!UICONTROL Produkte], da das Einheitenfeld als Produktname verstanden wird. Wenn in Ihrem [!UICONTROL Produkte]-Bericht unzulässige Produktnamen aufgeführt sind, überprüfen Sie, ob Sie in Ihrer Implementation der [!UICONTROL s.products]-Variablen versehentlich reservierte Zeichen (wie Kommas) verwendet haben.

Produkt- und Kategorienamen dürfen keine Zeichen enthalten, die nicht unterstützt werden. Dies kann besonders in der [!UICONTROL s.products]-Zeichenfolge problematisch sein, da Produktnamen häufig Zeichen wie ™, © und ® enthalten. Diese Zeichen müssen in Produkt- und Kategoriewerten entfernt werden, bevor die Werte in [!UICONTROL s.products] eingefügt werden. Außerdem müssen Sie auch darauf achten, dass Umsatzwerte keine Währungssymbole enthalten. Unterstützt werden die ASCII-Zeichen von 1 bis 127.

Wenn Sie in der Produktzeichenfolge keine Produktkategorie übergeben, müssen Sie an der Stelle, an der normalerweise die Produktkategorie angezeigt wird, ein Semikolon einfügen:

```js
s.products=";product name"
```

In diesem Fall stellt das Semikolon einen Platzhalter für die Produktkategorie dar. Wenn das Semikolon in der Produktzeichenfolge weggelassen wird, würden der Produktname als Kategorie, die Anzahl der Einheiten als Produktname, der Umsatz als Einheiten usw. gezählt werden.
