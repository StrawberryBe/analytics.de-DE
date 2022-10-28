---
title: Hierarchie
description: Eine benutzerdefinierte Dimension, die Sie in Berichten verwenden können.
feature: Dimensions
source-git-commit: f435453f655caef89460de42ebecf489b021dc47
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 22%

---

# Hierarchie

>[!IMPORTANT]
>
>Diese Dimension wurde eingestellt und ist keine verfügbare Dimension in Analysis Workspace. Adobe empfiehlt stattdessen die Verwendung von [eVars](evar.md) und Klassifizierungen.

Hierarchien sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den von ihnen festgelegten Treffer hinaus bestehen. Es sind bis zu 5 Hierarchien verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Füllen von Hierarchien mit Daten

Jede Hierarchie erfasst Daten aus der [`h1` - `h5` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. Beispiel: die `h1` Abfragezeichenfolgenparameter erfasst Daten für Hierarchie 1, während der `h4` Abfragezeichenfolgenparameter erfasst Daten für Hierarchie 4.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `hier1` – `hier5`. Siehe [hier](/help/implement/vars/page-vars/hier.md) im Benutzerhandbuch zu Implementierungen für Implementierungsrichtlinien.

## Dimensionselemente

Da Hierarchien benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihr Unternehmen, welche Dimensionselemente für jede Hierarchie gelten. Vergewissern Sie sich, dass Sie den Zweck jeder Hierarchie und die typischen Dimensionselemente in einer [Lösungsdesigndokument](/help/implement/prepare/solution-design.md).
