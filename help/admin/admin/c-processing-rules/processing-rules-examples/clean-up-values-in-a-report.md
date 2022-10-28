---
description: Sie können Werte auf gängige Fehlschreibungen prüfen und eine Korrektur vornehmen, damit sie in Berichten richtig angezeigt werden.
subtopic: Processing rules
title: Bereinigen von Werten in einem Bericht
feature: Admin Tools
uuid: fcd72afc-3a3c-47a9-a5e4-53389dba7d83
exl-id: 109005a3-2ea4-4b61-a733-d1019218ec56
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 84%

---

# Bereinigen von Werten in einem Bericht

Sie können Werte auf gängige Fehlschreibungen prüfen und eine Korrektur vornehmen, damit sie in Berichten richtig angezeigt werden.

Um sicherzustellen, dass Sie nicht versehentlich mit anderen Werten übereinstimmen, verwenden Sie die restriktivste verfügbare Übereinstimmungsoption. Sie können einen Bericht zu einer Variablen ausführen („prop1“ im Beispiel unten) und eine Suche nach den zu ersetzenden Begriffen vornehmen, damit es keine ungewollten Übereinstimmungen gibt. Beim Vergleich von Zeichenfolgen wird die Groß- und Kleinschreibung ignoriert.

| Regelsatz | Wert |
|---|---|
| Bedingung | Falls „prop1“ mit dem Begriff „Shopping“ beginnt |
| Aktion | Wert von „prop1“ auf benutzerdefinierten Wert „Shopping“ überschreiben |

Beispiel:

![](assets/clean-up-values-in-report.png)
