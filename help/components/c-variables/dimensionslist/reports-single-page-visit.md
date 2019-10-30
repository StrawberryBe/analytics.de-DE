---
description: Dieser Bericht ist nicht mit der Metrik „Einzelseitenbesuche“ in den Ad Hoc Analysis zu verwechseln. Der Bericht „Einzelseitenbesuche“ zeigt die Seiten, die ein Besucher Ihrer Website besucht und wieder verlässt, ohne das Anzeigen weiterer Seiten zu veranlassen.
seo-description: Dieser Bericht ist nicht mit der Metrik „Einzelseitenbesuche“ in den Ad Hoc Analysis zu verwechseln. Der Bericht „Einzelseitenbesuche“ zeigt die Seiten, die ein Besucher Ihrer Website besucht und wieder verlässt, ohne das Anzeigen weiterer Seiten zu veranlassen.
seo-title: Einzelseitenbesuch
solution: Analytics
title: Einzelseitenbesuch
topic: Berichte
uuid: 5ca52be8-c7f5-464a-8a06-55e8271760b4
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Einzelseitenbesuch

Dieser Bericht ist nicht mit der Metrik „Einzelseitenbesuche“ in den Ad Hoc Analysis zu verwechseln. Der Bericht „Einzelseitenbesuche“ zeigt die Seiten, die ein Besucher Ihrer Website besucht und wieder verlässt, ohne das Anzeigen weiterer Seiten zu veranlassen.

Der Bericht wird meist im Zusammenhang mit dem [!UICONTROL Seitenbericht] verwendet, kann jedoch in allen Traffic-Variablen angezeigt werden, wenn die [!UICONTROL Pfadsetzung] aktiviert ist. Mit diesem Bericht können Sie ermitteln, welche Entrypages die Besucher am wenigsten dazu anregen, Ihre Website weiter zu erkunden. Oder Sie stellen fest, wie viele Besuche nur auf einzelnen Seiten stattfinden. Anhand dieser Informationen können Sie die Inhalte optimieren und die Ausstiege auf diesen Seiten reduzieren.

## Berichteigenschaften {#section_2D30F939FE0648EF983DD7C1BAB1181B}

* Denselben Bericht erhalten Sie, wenn Sie einen [!UICONTROL Seitenbericht] ausführen und dazu die Metrik [!UICONTROL Einzelzugriff] verwenden.

* Ein Besuch, der nur einen individuellen Wert enthält, nicht eine einzelne Bildanforderung, gilt als Einzelseitenbesuch.

   * Im Kontext eines [Seitenberichts](../../../components/c-variables/dimensionslist/reports-pages.md#concept_0219136EA25745B58434D0C7E751D7D5) kann nur eine individuelle Seite bei einem Besuch aufgerufen werden.
   * Im Kontext eines Berichts[zu ](../../../components/c-variables/dimensionslist/reports-site-sections.md#concept_39E550D7A9E34C9580E81F5F9E12BDDD)Sitebereichen wird ein einzelner eindeutiger Sitebereich während des Besuchs ausgelöst.
   * Im Kontext einer [Traffic-Variablen](/help/admin/admin/c-traffic-variables/traffic-var.md)füllt ein Besuch diesen Bericht, wenn ein einzelner eindeutiger Wert ausgelöst wird.

* Einzelseitenbesuche können aus vielen Bildanforderungen bestehen, solange die Variable im Kontext des Berichts einen einzigen individuellen Wert enthält. Sobald ein zweiter individueller Wert eingeht, wird der Besuch nicht mehr als Einzelseitenbesuch angesehen.
* Dies wird als eine Art Pfadsetzungsbericht betrachtet. Für die [!UICONTROL Seitenvariable] ist die Pfadsetzung standardmäßig aktiviert. Auch jede Traffic-Variable verfügt über diese Fähigkeit. Ob die Pfadsetzung für weitere Traffic-Variablen aktiviert wird, hängt von Ihrem Vertrag ab. Nähere Informationen erhalten Sie vom Kundenbetreuer Ihrer Organisation.
* In diesem Bericht können bestimmte Zeileneinträge mit einem Suchfilter ermittelt werden.
* Der Bericht kann sowohl als [Trendformate](/help/components/c-variables/dimensionslist/reports-types.md) und [Rangformate](/help/components/c-variables/dimensionslist/reports-types.md) .

* In dem Bericht sind keine Aufschlüsselungen verfügbar.
* [!UICONTROL Besuche] sind die einzige im Bericht verfügbare Metrik.

