---
description: Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.
seo-description: Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.
seo-title: Ereignis mit einer Kontextdatenvariable festlegen
solution: Analytics
subtopic: Verarbeitungsregeln
title: Ereignis mit einer Kontextdatenvariable festlegen
topic: Admin Tools
uuid: 4a6018eb-03e2-4ec8-874b-e48bf716e103
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Ereignis mit einer Kontextdatenvariable festlegen

Verarbeitungsregeln können Ereignisse auf der Grundlage von Kontextdatenvariablen auslösen.

Kontextdatenvariablen werden in AppMeasurement im folgenden Format spezifiziert:

```
 s.contextData['search_term']
```

Die [!UICONTROL Kontextvariablenliste] enthält alle Variablen, die in den vorherigen 30 Tagen an die Report Suite gesendet wurden. If you know the context data variable name but have not sent it into the current report suite, you can add a value by typing the variable name and clicking **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

Die folgende Regeldefinition erweitert die Regel "Kontextdatenvariable [kopieren"auf eine eVar](../../../../admin/admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md#concept_43AA4980A2D847D6A3BEC50BCC0780E7) -Regel, um auch bei jedem Treffer, der eine spezifische Kontextdatenvariable enthält, ein Ereignis festzulegen:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn „Suchbegriff“-Kontextdaten eingestellt sind |
| Aktion | Ereignis „Suchvorgänge“ setzen |

Beispiel:

![](assets/processing_rule_set_event.png)

Weitere Informationen finden Sie unter [Kontextdatenvariablen](https://marketing.adobe.com/resources/help/en_US/sc/implement/context_data_variables.html) in der Implementierungshilfe.
