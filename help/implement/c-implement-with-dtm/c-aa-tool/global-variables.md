---
description: Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.
keywords: Dynamisches Tag-Management; globale Variablen; Servervariable; evar; props; dynamisches Variablenpräfix; dynamische Variable
seo-description: Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.
seo-title: Globale Variablen
solution: Marketing Cloud, Analytics, dynamisches Tag-Management
title: Globale Variablen
uuid: d 759320 a -96 ee -4073-b 5 fd -5257 b 7033003
translation-type: tm+mt
source-git-commit: 3489f00bd7dddefda0420fc361056416f6f10d3f

---


# Globale Variablen

Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.

Diese Variablen werden durch alle Seitenladesignale ausgelöst. Den gleichen Effekt können Sie durch Verwendung einer [Seitenladeregel](../../../implement/c-implement-with-dtm/c-rules/t-rules-page-conditions.md#task_69B41CB230EE4530A755D91233F73706) erzielen, die so eingestellt ist, dass sie auf jeder Seite auslöst. These variables might not fire in [Direct-Call](../../../implement/c-implement-with-dtm/c-rules/t-rules-direct-conditions.md#task_85EB8F01775A402BA53B8298F0AADA09) and [Event-Based](../../../implement/c-implement-with-dtm/c-rules/t-rules-event-conditions.md#task_A122DE72110F4579A91F9D96D92D39FC) rules.

## Globale Variablen – Feldbeschreibungen {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png)**[!UICONTROL Tool bearbeiten]** &gt; **[!UICONTROL Globale Variablen]**

| Element | Beschreibung |
|--- |--- |
| Server | Die vordefinierte Variable füllt die Dimension Server in Adobe Analytics. See [Page Variables](/help/implement/js-implementation/c-variables/page-variables.md) |
| eVars | [Evar-Variablen](/help/implement/js-implementation/c-variables/page-variables.md) werden zum Erstellen benutzerspezifischer Konversionsberichte verwendet. |
| Props | [Eigenschaftsvariablen](/help/implement/js-implementation/c-variables/page-variables.md) werden zum Erstellen benutzerspezifischer Traffic-Berichte verwendet. |
| Dynamisches Variablenpräfix | Ein spezielles Präfix am Anfang des Werts. Das Standard-Präfix ist „D=“. Siehe [Dynamische Variablen](/help/implement/js-implementation/c-variables/dynvars-overview.md) |
