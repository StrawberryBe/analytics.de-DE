---
description: Der Bericht zu Entrypages zeigt nach Prozentsatz und Gesamtanzahl der Besuche an, welche Seiten auf Ihrer Site bei neuen Besuchen zuerst aufgerufen werden.
seo-description: Der Bericht zu Entrypages zeigt nach Prozentsatz und Gesamtanzahl der Besuche an, welche Seiten auf Ihrer Site bei neuen Besuchen zuerst aufgerufen werden.
seo-title: Ein- und Ausstiege
solution: Analytics
title: Ein- und Ausstiege
topic: 'Berichte    '
uuid: 756 de 55 b -136 b -427 b-a 80 c-f 822260131 b 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Ein- und Ausstiege

>[!NOTE]
>Bei Treffern mit mehreren Werten in der Variablen "products" gelten" Einträge" und "Ausstiege" für alle Produktwerte in einem Treffer, nicht nur für die erste.

Der Bericht zu Entrypages zeigt nach Prozentsatz und Gesamtanzahl der Besuche an, welche Seiten auf Ihrer Site bei neuen Besuchen zuerst aufgerufen werden.

Die Ansicht erfasst:

* **Entrypages** (oder Abschnitte): Zeigt nach Prozentsatz und nach Gesamtanzahl der Besuche an, welche Seiten auf Ihrer Site bei einem neuen Besuch zuerst aufgerufen werden. Anhand dieses Berichts können Sie erkennen, welche Ihrer Webseiten die häufigsten Einstiegspunkte sind, und können dann die primären Einstiegspunkte Ihrer Site optimieren, um den Einstiegs-Traffic auf Ihre wichtigsten Mitteilungen zu lenken.

   A useful way to use the Page View metric is to run a **[!UICONTROL Paths]** &gt; **[!UICONTROL Pages]** &gt; **[!UICONTROL Pages Entry]** report, sort by it, and see which entry pages drive the most page views.

* **Ursprüngliche Entrypages**: Zeigt die erste angezeigte Seite eines ersten Besuchs auf Ihrer Site. Benutzer werden nur einmal gezählt, es sei denn, der Benutzer löscht seine Cookies oder wird nicht durch Cookies verfolgt.
* **Einzelseitenbesuche**: Zeigt Seiten, die am häufigsten sowohl Einstiegs- als auch Exitpages für Besucher waren.
* **Exitpages**: Zeigt nach Prozentsatz und Gesamtanzahl der Besuche an, welche die letzten Seiten waren, die die Besucher vor dem Verlassen der Site aufgerufen haben. Exitpages werden pro Besuch aufgeschlüsselt, d. h., sie werden für alle Hits für einen Besuch beibehalten.

**Metriken zu einem Entrypages-Bericht**

* **Einstiege**: Dasselbe wie Instanzen oder Vorfälle, wie häufig die angegebene Seite bei einem Besuch als Entrypage aufgerufen wird.
* **Besuche**: Bei wie vielen Besuchen diese Seite die Entrypage war; diese Metrik sollte mit der Anzahl der Einstiege identisch sein.
* **Ausstiege**: Wie häufig ein Ausstieg aufgetreten ist, bei dem die Entrypage angegeben war. Um zu erfahren, wie häufig die Entrypage ebenfalls die Exitpage war, verwenden Sie statt der Metrik „Ausstiege“ die Bounces-Metrik.

**Segmentierung in einem Entrypages-Bericht**

Wenn Sie einen [!UICONTROL Entrypages-Bericht] ausführen, werden ausschließlich die Entrypages in dem Bericht gemeldet, selbst wenn Sie ein Segment auf eine NichtEntrypage anwenden.

Nehmen Sie z. B. folgende Besuchssequenz an:

[!DNL Page A] &gt; [!DNL Page B] &gt; [!DNL Page C]

Wenn Seite B und Seite C in einem Segment verwendet werden, dann wird nur die Seite A in einem [!UICONTROL Entrypages-Bericht] gemeldet, da die Seite A die Entrypage ist.
