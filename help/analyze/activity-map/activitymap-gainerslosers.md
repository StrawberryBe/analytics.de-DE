---
description: Mit Überlagerungen verfügen Sie über zahlreiche Möglichkeiten zur Konfiguration der Datenvisualisierung, sodass Sie die Beliebtheit der Links auf einer Seite einfach feststellen und verstehen können.
title: Anpassbare Überlagerungen
uuid: c1e56480-c1df-4a81-8a2a-42ea1362175c
feature: Activity Map
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 99%

---


# Anpassbare Überlagerungen

Mit Überlagerungen verfügen Sie über zahlreiche Möglichkeiten zur Konfiguration der Datenvisualisierung, sodass Sie die Beliebtheit der Links auf einer Seite einfach feststellen und verstehen können.

Überlagerungen ermöglichen Ihnen, Klickdaten direkt auf der Seite zu visualisieren. Dadurch unterscheidet sich ein visuelles Analysewerkzeug wie Activity Map von anderen hauptsächlich tabellarischen und grafischen Werkzeugen wie „Reports &amp; Analytics“.

Activity Map bietet drei Überlagerungstypen:

* Verlaufsüberlagerung (Heatmap)
* Blasenüberlagerung
* Überlagerung für Gewinner und Verlierer

Außerdem können Sie [Überlagerungsrendering für dynamischen Inhalt](/help/analyze/activity-map/activitymap-link-tracking/activitymap-stl-track-custom-elements.md) konfigurieren.

Um Änderungen an Überlagerungen vorzunehmen, öffnen Sie das [Einstellungsbedienfeld für Überlagerungen](/help/analyze/activity-map/activitymap-overlay-settings.md) und bearbeiten Sie die verfügbaren Optionen.

Wenn Sie den Mauszeiger über eine Überlagerung bewegen, werden die [Details](/help/analyze/activity-map/activitymap-overlay-details.md) dazu angezeigt.

## Verlaufsüberlagerung (Heatmap) {#section_06AF13DE05A1454D960176CD0DA921A6}

Die Farbintensität einer Verlaufsüberlagerung hängt von der Beliebtheit des Links ab. Diese Intensität kann für die 30 beliebtesten Links vereinheitlicht werden oder eine Funktion des absoluten Metrikwerts sein.

Diese Metriken werden überlagert als eine Art „Heatmap“ auf den Links der Seite angezeigt, um wesentliche Fragen wie die Folgenden zu beantworten:

* Welchen Wert hat eine einzelne Seite?
* Welchen Wert hat ein bestimmtes Element auf einer Seite?
* Welche digitale Stelle auf einer Seite ist am wertvollsten?

![](assets/gradient.png)

## Blasenüberlagerung {#section_A657AB3F64CB47F881BBFFD72B37D9D4}

Bei Blasenüberlagerungen wird der Inhalt der Überlagerung (Metrik, Prozentsatz oder Rang) in einer kleinen Beschriftungsblase angezeigt.

Blasenüberlagerungen werden angezeigt, wenn Sie diese Überlagerung in „Überlagerungstyp“ in der Symbolleiste auswählen. Blasenüberlagerungen werden für alle Links, die der Auswahl in den [Einstellungen für Activity Map](/help/analyze/activity-map/activitymap-overlay-settings.md) (Top 30, Top 50, alle...) entsprechen, angezeigt. Verlaufsüberlagerungen werden angezeigt, wenn diese Option nicht ausgewählt ist.

![](assets/bubble_overlay.png)

>[!NOTE]
>
>Blasenüberlagerungen für Untermenüs werden nur angezeigt, wenn Sie das Untermenü einblenden:
>
>![](assets/bubbles_submenu.png)>

## Überlagerungen für Gewinner und Verlierer {#section_EE80278E20C14824869BF5A27A4634C8}

**[!UICONTROL Überlagerungen für Gewinner und Verlierer]** sind nur im Livemodus verfügbar. Sie zeigen die Änderungen der Linkaktivität in Echtzeit, indem sie die Metriken des aktuellen Zeitraums mit den Metriken des letzten Zeitraums vergleichen. Sie stellen eine visuell ansprechende Möglichkeit dar, Trends in Echtzeit anzuzeigen.

Diese Echtzeitüberlagerung stuft Klicks auf Basis der Änderungen des Metrikwerts zwischen dem vorherigen und dem aktuellen Zeitraum ein.

![](assets/gainers_losers.png)

