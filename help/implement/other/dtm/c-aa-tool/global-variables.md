---
description: Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.
keywords: Dynamic Tag Management;global variables;server variable;evar;props;dynamic variable prefix;dynamic variable
solution: Experience Cloud,Analytics
title: Globale Variablen
uuid: d759320a-96ee-4073-b5fd-5257b7033003
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 100%

---


# Globale Variablen

Beschreibung der Felder und Informationen über Variablen bei Verwendung des Dynamic Tag Managements zur Bereitstellung von Adobe Analytics.

Diese Variablen werden bei allen Seitenladeregel-Beacons ausgelöst. Den gleichen Effekt können Sie durch Verwendung einer  [Seitenladeregel](/help/implement/other/dtm/c-rules/t-rules-page-conditions.md) erzielen, die so eingestellt ist, dass sie auf jeder Seite auslöst. Diese Variablen werden möglicherweise nicht in [Direktaufruf](/help/implement/other/dtm/c-rules/t-rules-direct-conditions.md)- und [ereignisbasierten](/help/implement/other/dtm/c-rules/t-rules-event-conditions.md) Regeln auslösen.

## Globale Variablen – Feldbeschreibungen {#section_2917F62FCC8D43F982B2612A702DEF81}

**[!UICONTROL *`Property`*]** > ![](assets/settings_gear.png)**[!UICONTROL  Tool bearbeiten ]** > **[!UICONTROL  Globale Variablen ]**

| Element | Beschreibung |
|--- |--- |
| Server | Diese vordefinierte Variable füllt die Server-Dimension in Adobe Analytics aus. Siehe [Server](../../../vars/page-vars/server.md). |
| eVars | Die [eVar-Variablen](../../../vars/page-vars/evar.md) dienen zum Erstellen benutzerdefinierter Konversionsberichte. |
| Props | [Prop-Variablen](../../../vars/page-vars/prop.md) werden zum Erstellen benutzerdefinierter Traffic-Berichte verwendet. |
| Dynamisches Variablenpräfix | Ein spezielles Präfix am Anfang des Werts. Das Standard-Präfix ist „D=“. Siehe [Dynamische Variablen](../../../vars/page-vars/dynamic-variables.md). |
