---
description: Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.
seo-description: Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.
seo-title: Festlegen eines Ereignisses mit einer Kontextdatenvariablen
solution: Analytics
subtopic: Verarbeitungsregeln
title: Festlegen eines Ereignisses mit einer Kontextdatenvariablen
topic: Admin Tools
uuid: 4 a 6018 eb -03 e 2-4 ec 8-874 b-e 48 bf 716 e 103
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Festlegen eines Ereignisses mit einer Kontextdatenvariablen

Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.

Kontextdatenvariablen werden in AppMeasurement im folgenden Format spezifiziert:

```
 s.contextData['search_term']
```

Die [!UICONTROL Kontextvariablenliste] enthält alle Variablen, die in den vorherigen 30 Tagen an die Report Suite gesendet wurden. If you know the context data variable name but have not sent it into the current report suite, you can add a value by typing the variable name and clicking **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

The following rule definition expands on the [Copy a Context Data Variable to an eVar](../../../../admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md#concept_43AA4980A2D847D6A3BEC50BCC0780E7) rule to also set an event on every hit that contains a specific context data variable:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn „Suchbegriff“-Kontextdaten eingestellt sind |
| Aktion | Ereignis „Suchvorgänge“ setzen |

Beispiel:

![](assets/processing_rule_set_event.png)

Weitere Informationen finden Sie unter [Kontextdatenvariablen](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=context_data_variables) in der Implementierungshilfe.
