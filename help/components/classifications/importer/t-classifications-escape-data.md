---
description: Schritte, die beschreiben, wie Sie Classification-Daten in der Classification-Datei maskieren.
title: Classification-Daten maskieren
feature: Classifications
exl-id: 0d3a0e91-5537-43ee-bd28-9907ee6eb331
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
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
