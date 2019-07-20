---
description: Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben.
seo-description: Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben.
seo-title: Kontextdatenvariable in eine evar kopieren
solution: Analytics
subtopic: Verarbeitungsregeln
title: Kontextdatenvariable in eine evar kopieren
topic: Admin Tools
uuid: 1 beaec 4 c -71 e 9-49 ce-b 154-78408 cc 532 a 3
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kontextdatenvariable in eine evar kopieren

Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben.

Kontextdatenvariablen werden in AppMeasurement im folgenden Format spezifiziert:

```
 s.contextData['search_term']
```

Die [!UICONTROL Kontextvariablenliste] enthält alle Variablen, die in den vorherigen 30 Tagen an die Report Suite gesendet wurden. If you know the context data variable name but have not sent it into the current report suite, you can add a value by typing the variable name and clicking **[!UICONTROL Add variable name context data]**:

![](assets/add-context-variable.png)

Die folgende Regeldefinition füllt eine eVar bei jedem Hit aus, der eine spezifische Kontextdatenvariable enthält:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn „Suchbegriff“-Kontextdaten eingestellt sind |
| Aktion | Wert von eVar3 auf „Suchbegriff“ überschreiben |

Beispiel:

![](assets/set-context-data.png)

Weitere Informationen finden Sie unter [Kontextdatenvariablen](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=context_data_variables) in der Implementierungshilfe.
