---
description: Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.
keywords: Dynamic Tag Management;global variables;server variable;evar;props;dynamic variable prefix;dynamic variable
solution: Experience Cloud,Analytics,Dynamic Tag Management
title: Globale Variablen
uuid: d759320a-96ee-4073-b5fd-5257b7033003
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Globale Variablen

Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.

Diese Variablen werden bei allen Seitenladeregel-Beacons ausgelöst. Den gleichen Effekt können Sie durch Verwendung einer [Seitenladeregel](/help/implement/c-implement-with-dtm/c-rules/t-rules-page-conditions.md) erzielen, die so eingestellt ist, dass sie auf jeder Seite auslöst. Diese Variablen werden möglicherweise nicht in [Direktaufruf](/help/implement/c-implement-with-dtm/c-rules/t-rules-direct-conditions.md)- und [ereignisbasierten](/help/implement/c-implement-with-dtm/c-rules/t-rules-event-conditions.md) Regeln auslösen.

## Globale Variablen – Feldbeschreibungen {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png) **[!UICONTROL Tool bearbeiten]** &gt; **[!UICONTROL Globale Variablen]**

| Element | Beschreibung |
|--- |--- |
| Server | Diese vordefinierte Variable füllt die Server-Dimension in Adobe Analytics aus. Siehe [Seitenvariablen](/help/implement/js-implementation/c-variables/page-variables.md) |
| eVars | Die [eVar-Variablen](/help/implement/js-implementation/c-variables/page-variables.md) dienen zum Erstellen benutzerdefinierter Konversionsberichte. |
| Props | [Prop-Variablen](/help/implement/js-implementation/c-variables/page-variables.md) werden zum Erstellen benutzerdefinierter Traffic-Berichte verwendet. |
| Dynamisches Variablenpräfix | Ein spezielles Präfix am Anfang des Werts. Das Standard-Präfix ist „D=“. Siehe [Dynamische Variablen](/help/implement/js-implementation/c-variables/dynvars-overview.md) |
