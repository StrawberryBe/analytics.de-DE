---
description: Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.
subtopic: Processing rules
title: Festlegen eines Ereignisses mit einer Kontextdatenvariablen
topic: Admin tools
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
translation-type: tm+mt
source-git-commit: 327fdfd6a6d6bfe1c7bae9825fc8812b5ac7d095

---


# Festlegen eines Ereignisses mit einer Kontextdatenvariablen

Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.

Kontextdatenvariablen werden in AppMeasurement im folgenden Format spezifiziert:

```
 s.contextData['search_term']
```

The [!UICONTROL Context Variables] list contains all variables that were sent to the report suite in the previous 30 days. If you know the context data variable name but have not sent it into the current report suite, you can add a value by typing the variable name and clicking **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

Die folgende Regeldefinition erweitert die Regel [Kontextdatenvariable in eine eVar kopieren](/help/admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md), um bei jedem Hit, der eine bestimmte Kontextdatenvariable enthält, auch ein Ereignis zu setzen:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn „Suchbegriff“-Kontextdaten eingestellt sind |
| Aktion | Ereignis „Suchvorgänge“ setzen |

Beispiel:

![](assets/processing_rule_set_event.png)

Weitere Informationen finden Sie unter [Kontextdatenvariablen](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/contextdata.html) in der Implementierungshilfe.
