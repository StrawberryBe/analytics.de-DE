---
description: Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.
subtopic: Processing rules
title: Festlegen eines Ereignisses mit einer Kontextdatenvariablen
topic: Admin tools
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Festlegen eines Ereignisses mit einer Kontextdatenvariablen

Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.

Kontextdatenvariablen werden in AppMeasurement im folgenden Format spezifiziert:

```
 s.contextData['search_term']
```

Die [!UICONTROL Kontextvariablenliste] enthält alle Variablen, die in den letzten 30 Tagen an die Report Suite gesendet wurden. Wenn Sie den Namen der Kontextdatenvariablen kennen, diese aber nicht an die aktuelle Report Suite gesendet haben, können Sie einen Wert hinzufügen, indem Sie den Variablennamen eingeben und auf **[!UICONTROL Kontextdaten für Variablennamen hinzufügen]** klicken:

![](assets/add-context-variable.png)

Die folgende Regeldefinition erweitert die Regel [Kontextdatenvariable in eine eVar kopieren](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md), um bei jedem Hit, der eine bestimmte Kontextdatenvariable enthält, auch ein Ereignis zu setzen:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn „Suchbegriff“-Kontextdaten eingestellt sind |
| Aktion | Ereignis „Suchvorgänge“ setzen |

Beispiel:

![](assets/processing_rule_set_event.png)

Weitere Informationen finden Sie unter [Kontextdatenvariablen](https://marketing.adobe.com/resources/help/de_DE/sc/implement/context_data_variables.html) in der Implementierungshilfe.
