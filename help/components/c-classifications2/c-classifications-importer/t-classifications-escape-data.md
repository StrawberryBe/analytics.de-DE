---
description: Schritte, die beschreiben, wie Sie Classification-Daten in der Classification-Datei maskieren.
seo-description: Schritte, die beschreiben, wie Sie Classification-Daten in der Classification-Datei maskieren.
seo-title: Classification-Daten maskieren
solution: Analytics
subtopic: Classifications
title: Classification-Daten maskieren
topic: Admin Tools
uuid: 724 edcc 5-4990-4 f 24-afbb -9 aef 301791 a 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Classification-Daten maskieren

Schritte, die beschreiben, wie Sie Classification-Daten in der Classification-Datei maskieren.

<!--Meike, please check this page against orginal. It might be missing information. -->

1. Stellen Sie sicher, dass das Classification-Dateiformat v2.1 ist.

   Wenn v2.1 aktiviert ist, wird eine Zeile wie die folgende angezeigt:

   >[!NOTE]
   >
   >To specify a format of v2.1, enable **[!UICONTROL Quoted Output]** when exporting the file on the [!UICONTROL Classification Importer] page ( [!UICONTROL Browser Export] or [!UICONTROL FTP Export]).

1. Setzen Sie das Feld mit Sonderzeichen in doppelte Anführungszeichen (`"`).

Ein doppeltes Anführungszeichen kann in einer maskierten Zelle enthalten sein, wenn Sie es durch zwei doppelte Anführungszeichen ersetzen (`" "`). Beispiel:

```
My String "of data"
```

Die Maskierung wäre:

```
"My String ""of data"""
```
