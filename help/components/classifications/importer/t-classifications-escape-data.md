---
description: Schritte, die beschreiben, wie Sie Classification-Daten in der Classification-Datei maskieren.
subtopic: Classifications
title: Classification-Daten maskieren
feature: Admin Tools
uuid: 724edcc5-4990-4f24-afbb-9aef301791a7
exl-id: 0d3a0e91-5537-43ee-bd28-9907ee6eb331
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '106'
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
