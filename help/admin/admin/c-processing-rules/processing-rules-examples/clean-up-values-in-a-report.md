---
description: Sie können Werte auf gängige Fehlschreibungen prüfen und eine Korrektur vornehmen, damit sie in Berichten richtig angezeigt werden.
subtopic: Processing rules
title: Bereinigen von Werten in einem Bericht
feature: Admin Tools
uuid: fcd72afc-3a3c-47a9-a5e4-53389dba7d83
exl-id: 109005a3-2ea4-4b61-a733-d1019218ec56
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 100%

---

# Bereinigen von Werten in einem Bericht

Sie können Werte auf gängige Fehlschreibungen prüfen und eine Korrektur vornehmen, damit sie in Berichten richtig angezeigt werden.

Um nicht versehentlich gültige Werte zu verändern, verwenden Sie hierbei die restriktivste Option für Übereinstimmungen. Sie können einen Bericht zu einer Variablen ausführen („prop1“ im Beispiel unten) und eine Suche nach den zu ersetzenden Begriffen vornehmen, damit es keine ungewollten Übereinstimmungen gibt. Beim Vergleich von Zeichenfolgen wird die Groß- und Kleinschreibung ignoriert.

| Regelsatz | Wert |
|---|---|
| Bedingung | Falls „prop1“ mit dem Begriff „Shopping“ beginnt |
| Aktion | Wert von „prop1“ auf benutzerdefinierten Wert „Shopping“ überschreiben |

Beispiel:

![](assets/clean-up-values-in-report.png)
