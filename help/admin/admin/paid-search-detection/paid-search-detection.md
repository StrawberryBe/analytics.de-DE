---
description: 'Die Erkennung von Paid Search unterscheidet gebührenpflichtige von kostenlosen Suchvorgängen in Suchmaschinen- und Such-Keyword-Berichten. '
title: 'Erkennung von Paid Search '
feature: Admin Tools
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
source-git-commit: 2c0aef13bdb88b0a7aa9f100c72c21f66a14c8dd
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 71%

---

# Erkennung von Paid Search 

[!UICONTROL Die Erkennung von Paid Search unterscheidet gebührenpflichtige von kostenlosen Suchvorgängen in Suchmaschinen- und Such-Keyword-Berichten. ] Sie können die Suchmaschinen angeben, in denen Sie kostenpflichtige Werbung verwenden, und eine in der URL von einem Besuch bei einer kostenpflichtigen Werbung gefundene Zeichenfolge eingeben.

## Konfigurationsoptionen {#section_0C2CFA0AF77B47098BE37CB024665D0D}

In der folgenden Tabelle werden die Felder und Optionen beschrieben, die Sie zur [Konfiguration der Erkennung von Paid Search](/help/admin/admin/paid-search-detection/t-paid-search-detection.md) verwenden.

| Option | Beschreibung |
| --- | --- |
| [!UICONTROL Suchmaschine] | Wählen Sie eine Suchmaschine aus der Dropdown-Liste. Sie geben die Suchmaschine an, wenn Sie unterschiedliche Parameter für die Abfragezeichenfolge in unterschiedlichen Suchmaschinen verwenden. Normalerweise wird der Wert `Any` ausreichend ist. |
| [!UICONTROL Abfragezeichenfolge] | Gibt eine Zeichenfolge für eine Übereinstimmung zwischen Groß- und Kleinschreibung und einem beliebigen Teil des Abfragezeichenfolgenparameters an, der nach dem &quot;?&quot;Teil der URL ist. <br>**Hinweis**: [!UICONTROL Erkennung gebührenpflichtiger Suchvorgänge] zwischen Groß- und Kleinschreibung unterschieden wird. Beispielsweise stimmt eine Regel, die &quot;PID&quot;als Abfragezeichenfolgenparameter angibt, nicht mit &quot;pid&quot;überein. Wenn das Unternehmen Groß- und Kleinschreibung verwendet, geben Sie die exakten Werte als separate Regeln ein, damit alle gewünschten Abfragezeichenfolgenparameter erfasst werden. |
