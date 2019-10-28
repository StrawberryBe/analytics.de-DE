---
description: Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.
keywords: Dynamic Tag Management;globale Variablen;Servervariable;eVar;props;dynamisches Variablenpräfix;dynamische Variable
seo-description: Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.
seo-title: Globale Variablen
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: Globale Variablen
uuid: d759320a-96ee-4073-b5fd-5257b7033003
translation-type: ht
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Globale Variablen

Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.

Diese Variablen werden durch alle Seitenladesignale ausgelöst. Den gleichen Effekt können Sie durch Verwendung einer [Seitenladeregel](../../../implement/c-implement-with-dtm/c-rules/t-rules-page-conditions.md#task_69B41CB230EE4530A755D91233F73706) erzielen, die so eingestellt ist, dass sie auf jeder Seite auslöst. Diese Variablen werden möglicherweise nicht in [Direktaufruf](../../../implement/c-implement-with-dtm/c-rules/t-rules-direct-conditions.md#task_85EB8F01775A402BA53B8298F0AADA09)- und [ereignisbasierten](../../../implement/c-implement-with-dtm/c-rules/t-rules-event-conditions.md#task_A122DE72110F4579A91F9D96D92D39FC) Regeln auslösen.

## Globale Variablen – Feldbeschreibungen {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png) **[!UICONTROL Tool bearbeiten]** &gt; **[!UICONTROL Globale Variablen]**

| Element | Beschreibung |
|--- |--- |
| Server | Diese vordefinierte Variable füllt die Server-Dimension in Adobe Analytics aus. Siehe [Seitenvariablen](/help/implement/js-implementation/c-variables/page-variables.md) |
| eVars | Die [eVar-Variablen](/help/implement/js-implementation/c-variables/page-variables.md) dienen zum Erstellen benutzerdefinierter Konversionsberichte. |
| Props | [Prop-Variablen](/help/implement/js-implementation/c-variables/page-variables.md) werden zum Erstellen benutzerdefinierter Traffic-Berichte verwendet. |
| Dynamisches Variablenpräfix | Ein spezielles Präfix am Anfang des Werts. Das Standard-Präfix ist „D=“. Siehe [Dynamische Variablen](/help/implement/js-implementation/c-variables/dynvars-overview.md) |
