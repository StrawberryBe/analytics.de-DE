---
title: Seiten nicht gefunden
description: Die Anzahl der Treffer, die einen Fehler enthalten.
exl-id: 71e138b5-69bb-41b0-852c-ca4af22be1f3
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '109'
ht-degree: 100%

---

# Seiten nicht gefunden

*Auf dieser Hilfeseite wird beschrieben, wie „Seiten nicht gefunden“ als Metrik funktioniert. Weitere Informationen finden Sie unter der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).*

Die Metrik „Seiten nicht gefunden“ zeigt die Anzahl der Treffer an, bei denen die Seite einen Fehler enthielt. Diese Metrik ist nützlich, wenn Sie sehen möchten, welche Seiten oder URLs Fehlermeldungen enthalten haben (z. B. 404), sodass Sie die Fehlerursache ermitteln und beheben können.

## Berechnung dieser Metrik

Diese Metrik zählt alle Treffer, bei denen die [`pageType`](/help/implement/vars/page-vars/pagetype.md)-Variable dem Wert von `"errorPage"` entspricht. Dies ist das Metrik-Äquivalent der Dimension [Seiten nicht gefunden](../dimensions/pages-not-found.md).
