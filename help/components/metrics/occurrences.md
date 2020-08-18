---
title: Vorfälle
description: Die Anzahl der Treffer, für die eine Variable festgelegt oder beibehalten wurde.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 67%

---


# Vorfälle

Die Metrik „Vorfälle“ zeigt die Anzahl der Treffer an, bei denen eine bestimmte Dimension festgelegt oder beibehalten wurde. Wenn Sie eine Dimension in Workspace auf eine leere Arbeitsfläche ziehen, wendet Adobe diese Metrik automatisch auf das Projekt an.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite Treffer ein, bei denen ein Dimensionselement definiert oder beibehalten wird. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus bestehen, für den sie festgelegt wurden. Diese Metrik zählt sowohl anfängliche als auch beständige Werte.

## Vergleich mit ähnlichen Metriken

* **Vorfälle oder[Instanzen](instances.md)**: Vorfälle zählen Treffer, bei denen ein Dimensionselement festgelegt oder beibehalten wurde. Instanzen enthalten keine Treffer, bei denen ein Dimensionselement beibehalten wird.
* **Vorfälle im Vergleich zu[Seitenansichten](page-views.md)**: Zu den Vorfällen gehören alle Treffertypen, einschließlich Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) und Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)). Die Metrik „Seitenansichten“ umfasst nur Seitenansicht-Tracking-Aufrufe und schließt Linktracking-Aufrufe aus.
