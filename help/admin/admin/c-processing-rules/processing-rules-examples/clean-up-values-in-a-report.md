---
description: Sie können Werte auf gängige Fehlschreibungen prüfen und eine Korrektur vornehmen, damit sie in Berichten richtig angezeigt werden.
seo-description: Sie können Werte auf gängige Fehlschreibungen prüfen und eine Korrektur vornehmen, damit sie in Berichten richtig angezeigt werden.
seo-title: Bereinigen von Werten in einem Bericht
solution: Analytics
subtopic: Verarbeitungsregeln
title: Bereinigen von Werten in einem Bericht
topic: Admin Tools
uuid: fcd 72 afc -3 a 3 c -47 a 9-a 5 e 4-5389 dba 7 d 83
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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

