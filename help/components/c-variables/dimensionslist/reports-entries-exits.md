---
description: Der Bericht zu Entrypages zeigt nach Prozentsatz und Gesamtanzahl der Besuche an, welche Seiten auf Ihrer Site bei neuen Besuchen zuerst aufgerufen werden.
title: Ein- und Ausstiege
topic: Reports
uuid: 756de55b-136b-427b-a80c-f822260131b1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Ein- und Ausstiege

>[!NOTE]
>Bei Treffern, die mehrere Werte in der Produktvariable aufweisen, gelten Einstiege und Ausstiege für alle Produktwerte in einem Treffer, und nicht mehr nur für den ersten.

Der Bericht zu Entrypages zeigt nach Prozentsatz und Gesamtanzahl der Besuche an, welche Seiten auf Ihrer Site bei neuen Besuchen zuerst aufgerufen werden.

Die Ansicht erfasst:

* **Entrypages** (oder Abschnitte): Zeigt nach Prozentsatz und nach Gesamtanzahl der Besuche an, welche Seiten auf Ihrer Site bei einem neuen Besuch zuerst aufgerufen werden. Anhand dieses Berichts können Sie erkennen, welche Ihrer Webseiten die häufigsten Einstiegspunkte sind, und können dann die primären Einstiegspunkte Ihrer Site optimieren, um den Einstiegs-Traffic auf Ihre wichtigsten Mitteilungen zu lenken.

   Eine nützliche Verwendungsmöglichkeit für die Seitenansichten-Metrik: Führen Sie einen **[!UICONTROL Pfade]** > **[!UICONTROL Seiten]** > **[!UICONTROL Einstiegsseiten]**-Bericht aus, sortieren Sie nach dieser Metrik, und sehen Sie, welche Entrypages zu den meisten Seitenansichten führen.

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

[!DNL Page A] > [!DNL Page B] > [!DNL Page C]

Wenn Seite B und Seite C in einem Segment verwendet werden, dann wird nur die Seite A in einem [!UICONTROL Entrypages-Bericht] gemeldet, da die Seite A die Entrypage ist.
