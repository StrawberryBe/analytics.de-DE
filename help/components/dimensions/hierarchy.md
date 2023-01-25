---
title: Hierarchie
description: Eine benutzerdefinierte Dimension, die Sie in Berichten verwenden können.
feature: Dimensions
exl-id: f9bd3ae1-3578-44c5-a540-ea93feac5bef
source-git-commit: 42ff5018411dae64039ed6f12ec2b8ed12aceff4
workflow-type: ht
source-wordcount: '163'
ht-degree: 100%

---

# Hierarchie

>[!IMPORTANT]
>
>Diese Dimension wurde eingestellt und ist keine verfügbare Dimension mehr in Analysis Workspace. Adobe empfiehlt stattdessen die Verwendung von [eVars](evar.md) und Klassifizierungen.

Hierarchien sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den von ihnen festgelegten Treffer hinaus bestehen. Es sind bis zu 5 Hierarchien verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Füllen von Hierarchien mit Daten

Jede Hierarchie erfasst Daten aus der [`h1` - `h5` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. Beispielsweise erfasst der Abfragezeichenfolgenparameter `h1` Daten für Hierarchie 1, während der Abfragezeichenfolgenparameter `h4` Daten für Hierarchie 4 erfasst.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `hier1` – `hier5`. Die Implementierungsrichtlinien finden Sie [hier](/help/implement/vars/page-vars/hier.md) im Benutzerhandbuch zu Implementierungen.

## Dimensionselemente

Da Hierarchien benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihre Organisation, welche Dimensionselemente für jede Hierarchie gelten. Stellen Sie sicher, dass Sie den Zweck jeder Hierarchie und die typischen Dimensionselemente in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.
