---
description: 'Die Erkennung von Paid Search unterscheidet gebührenpflichtige von kostenlosen Suchvorgängen in Suchmaschinen- und Such-Keyword-Berichten. '
title: 'Erkennung von Paid Search '
feature: Admin Tools
uuid: 41aadf17-7b8b-49ce-84ca-dc3293660205
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
source-git-commit: b88f9d373d715b295dc4982a6ee05bd982f5bae7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 72%

---

# Erkennung von Paid Search 

[!UICONTROL Die Erkennung von Paid Search unterscheidet gebührenpflichtige von kostenlosen Suchvorgängen in Suchmaschinen- und Such-Keyword-Berichten. ] Sie können die Suchmaschinen angeben, in denen Sie kostenpflichtige Werbung verwenden, und eine in der URL von einem Besuch bei einer kostenpflichtigen Werbung gefundene Zeichenfolge eingeben.

## Konfigurationsoptionen {#section_0C2CFA0AF77B47098BE37CB024665D0D}

In der folgenden Tabelle werden die Felder und Optionen beschrieben, die Sie zur [Konfiguration der Erkennung von Paid Search](/help/admin/admin/paid-search-detection/t-paid-search-detection.md) verwenden.

| Option | Beschreibung |
| --- | --- |
| [!UICONTROL Suchmaschine] | Wählen Sie eine Suchmaschine aus der Dropdown-Liste. Sie geben die Suchmaschine an, wenn Sie unterschiedliche Parameter für die Abfragezeichenfolge in unterschiedlichen Suchmaschinen verwenden. Normalerweise ist der Wert `Any` ausreichend. |
| [!UICONTROL Abfragezeichenfolge] | Gibt eine Zeichenfolge für eine Übereinstimmung zwischen Groß- und Kleinschreibung und einem beliebigen Teil des Abfragezeichenfolgenparameters an, der nach dem &quot;?&quot;Teil der URL ist. <br>**Hinweis**:  [!UICONTROL Bei der ] Erkennung gebührenpflichtiger Suchvorgänge wird zwischen Groß- und Kleinschreibung unterschieden. Beispielsweise stimmt eine Regel, die &quot;PID&quot;als Abfragezeichenfolgenparameter angibt, nicht mit &quot;pid&quot;überein. Wenn das Unternehmen Groß- und Kleinschreibung verwendet, geben Sie die exakten Werte als separate Regeln ein, damit alle gewünschten Abfragezeichenfolgenparameter erfasst werden. |
