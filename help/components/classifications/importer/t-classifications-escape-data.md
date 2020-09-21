---
description: Schritte, die beschreiben, wie Sie Classification-Daten in der Classification-Datei maskieren.
subtopic: Classifications
title: Classification-Daten maskieren
topic: Admin tools
uuid: 724edcc5-4990-4f24-afbb-9aef301791a7
translation-type: ht
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: ht
source-wordcount: '104'
ht-degree: 100%

---


# Classification-Daten maskieren

Schritte, die beschreiben, wie Sie Classification-Daten in der Classification-Datei maskieren.

<!--Meike, please check this page against orginal. It might be missing information. -->

1. Stellen Sie sicher, dass das Classification-Dateiformat v2.1 ist.

   Wenn v2.1 aktiviert ist, wird eine Zeile wie die folgende angezeigt:

   >[!NOTE]
   >
   >Um das Format v2.1 anzugeben, aktivieren Sie **[!UICONTROL Anführungszeichenausgabe]**, wenn Sie die Datei auf der Seite [!UICONTROL Classification Importer] ([!UICONTROL Browser-Export] oder [!UICONTROL FTP-Export]) exportieren.

1. Setzen Sie das Feld mit Sonderzeichen in doppelte Anführungszeichen (`"`).

Ein doppeltes Anführungszeichen kann in einer maskierten Zelle enthalten sein, wenn Sie es durch zwei doppelte Anführungszeichen ersetzen (`" "`). Beispiel:

```
My String "of data"
```

Die Maskierung wäre:

```
"My String ""of data"""
```
