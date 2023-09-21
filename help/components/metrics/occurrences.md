---
title: Vorfälle
description: Die Anzahl der Treffer, für die eine Variable festgelegt oder beibehalten wurde.
feature: Metrics
exl-id: 8428e813-0fb4-4620-884e-1aa92fe33209
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 64%

---

# Vorfälle

Die &quot;Vorfälle&quot; [Metrik](overview.md) zeigt die Anzahl der Treffer an, bei denen eine bestimmte Dimension festgelegt oder beibehalten wurde. Wenn Sie eine Dimension in Workspace auf eine leere Arbeitsfläche ziehen, wendet Adobe diese Metrik automatisch auf das Projekt an.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite die Treffer ein, bei denen ein Dimensionselement definiert oder beibehalten wird. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus bestehen, für den sie festgelegt wurden. Diese Metrik zählt sowohl anfängliche als auch persistente Werte.

## Vergleich mit ähnlichen Metriken

* **Vorfälle oder [Instanzen](instances.md)**: Vorfälle zählen Treffer, bei denen ein Dimensionselement festgelegt oder beibehalten wurde. Instanzen enthalten keine Treffer, bei denen ein Dimensionselement beibehalten wird.
* **Vorfälle vs. [Seitenansichten](page-views.md)**: Zu den Vorfällen gehören alle Treffertypen, einschließlich Seitenansicht-Tracking-Aufrufe ([`t()`](/help/implement/vars/functions/t-method.md)), Linktracking-Aufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) und Daten aus der Zusammenfassung [Datenquellen](/help/import/data-sources/overview.md). Die Metrik &quot;Seitenansichten&quot;umfasst nur Seitenansichts-Tracking-Aufrufe, ausgenommen Linktracking-Aufrufe und Zusammenfassungsdatenquellen.
