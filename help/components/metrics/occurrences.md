---
title: Vorfälle
description: Die Anzahl der Treffer, die eine Variable festgelegt oder beibehalten wurde.
translation-type: tm+mt
source-git-commit: 422e99d9ea70f0192443d7ebc3631c6bf99e7591
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# Vorfälle

Die Metrik &quot;Vorfälle&quot;zeigt die Anzahl der Treffer an, bei denen eine bestimmte Dimension festgelegt oder beibehalten wurde. Wenn Sie eine Dimension in Workspace auf eine leere Arbeitsfläche ziehen, wendet Adobe diese Metrik automatisch auf das Projekt an.

## Berechnung dieser Metrik

Schließen Sie von allen Treffern in einer Report Suite Treffer ein, bei denen ein Dimensionselement definiert oder beibehalten wird. Einige Dimensionen, wie z. B. [eVars](../dimensions/evar.md), bleiben über den Treffer hinaus erhalten, für den sie festgelegt wurden. Metriken wie [Seitenwerte](page-views.md) und [Vorfälle](occurrences.md) zählen sowohl Anfangswerte als auch beibehaltene Ansichten.

## Vergleichen mit ähnlichen Metriken

* **Vorfälle oder[Instanzen](instances.md)**: Vorfälle zählen Treffer, bei denen ein Dimensionselement festgelegt oder beibehalten wurde. Instanzen enthalten keine Treffer, bei denen ein Dimensionselement beibehalten wird.
* **Vorfälle im Vergleich zu[Seiten-Ansichten](page-views.md)**: Zu den Vorfällen gehören alle Treffertypen, einschließlich Verfolgungsaufrufe ([`t()`](/help/implement/vars/functions/t-method.md)) und Linkverfolgungsaufrufe ([`tl()`](/help/implement/vars/functions/tl-method.md)) der Ansicht. Die Metrik &quot;Ansichten&quot;umfasst nur Verfolgungsaufrufe der Ansicht und schließt Linkverfolgungsaufrufe aus.
