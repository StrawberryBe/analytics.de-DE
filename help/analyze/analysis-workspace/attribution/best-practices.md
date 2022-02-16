---
title: Best Practices für die Attribution
description: Welche Best Practices bestehen für die Wahl eines Attributionsmodells?
feature: Attribution
exl-id: 92c6039c-f950-4746-8b34-ba18be258c08
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 100%

---

# Best Practices für die Attribution

Welches Attributionsmodells für Ihr Unternehmen am besten geeignet ist, hängt von einer Reihe von Überlegungen ab. Dieser Artikel zeigt eine Methodik sowie einige allgemeine Best Practices auf.

## Schritt 1: Explorative Analyse

>[!NOTE]
>Diese Analyse muss der Entscheidung für ein bestimmtes Attributionsmodell vorangehen.

In dieser vorbereitenden Phase geht es darum, ein Verständnis des Kundenverhaltens zu gewinnen und Konversionsmetriken zu bestimmen. Basierend auf der Konversionsmetrik erleichtern Tools wie [Daten-Feeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=de) (für Rohdaten) oder Analysis Workspace Ihr Verständnis von

* Wie viele Kunden haben jeweils Kontakt mit den einzelnen Marketing-Kanälen, bevor es zu ihrer Konversion kommt?
* Der Anteil/die Verteilung dieser Verhaltensweisen.

Wenn beispielsweise 50 % der Kunden vor ihrer Konversion über drei Kanäle mit Ihnen in Kontakt kommen, besteht dann eine Interaktion zwischen diesen drei Kanälen?
Sie können dann eine Analyse des oberen und des unteren Ende des Trichters durchführen, um Ihr Verständnis zu erweitern.

### Analyse des oberen Ende des Trichters

Bei der Analyse des oberen Ende des Trichters werden diejenigen Kanäle untersucht, die zur Förderung der Marken- oder Produkwahrnehmung dienen. So zielen etwa TV-Werbespots in der Regel auf die Markenwahrnehmung ab. Hierfür empfiehlt sich das [Attributionsmodell des Zeitverfalls](/help/analyze/analysis-workspace/attribution/models.md), da Ihr TV-Werbespot im Zeitverlauf aus dem Gedächtnis Ihrer Zielgruppe verschwinden wird.

### Analyse des unteren Ende des Trichters

Dieser Analyse liegt die Annahme zugrunde, dass Ihre Zielgruppe Ihre Marke bereits kennt und dass Sie versuchen, diese anhand bestimmter Methoden zur Konversion zu bringen. Dies geschieht über E-Mail- und Push-Benachrichtigungen oder etwa auch über Facebook-Anzeigen.

## Schritt 2: Regelbasierte Attribution

Dieser Schritt dient der Validierung Ihrer Hypothesen.

**Beispiel 1**

Angenommen, Ihre Hypothese lautet: „Mein für den Erstkontakt verwendeter Kanal hat größeren Einfluss auf die Konversion als mein für den Letztkontakt verwendeter“. In diesem Fall würden Sie das [Attributionsmodell Umgekehrt J-förmig](/help/analyze/analysis-workspace/attribution/models.md) anwenden, um diese Hypothese zu testen. Dieses Modell schreibt dem ersten Kontaktpunkt (bzw. „Touchpoint“) eine Gewichtung von 60 % zu.

**Beispiel 2**

Ihre Hypothese könnte lauten: „In unserer Branche (z. B. der Reisebranche) liegt das Attributionsfenster nicht bei 30, sondern bei 60 oder 90 Tagen, da Kunden vor dem Produktkauf intensive Recherchen vornehmen“. In diesem Fall würden Sie das [Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=de#lookback-windows) entsprechend auf 90 Tage anpassen.

## Schritt 3: Algorithmische Attribution verwenden

Die Validierung einer großen Anzahl möglicher Hypothesen und Kombinationen ist mit einem enormen Aufwand verbunden. Diese komplexe Aufgabe können Sie mittels [algorithmischer Attribution](/help/analyze/analysis-workspace/attribution/algorithmic.md) jedoch auch von integrierten Algorithmen erledigen lassen. Sofern Sie bereits das Attributionsmodell ermittelt haben, das ihre Fragen allesamt beantwortet und perfekt zu Ihren Anforderungen passt, ist dieser Schritt logischerweise nicht vonnöten.

## Weiter Überlegungen

* Möglicherweise sollten Sie ergänzend zu Analysis Workspace einen Datenwissenschaftler hinzuziehen.
* Sie können sich auf Rohdaten verlassen, wie in Daten-Feeds von Adobe.
* Erwägen Sie beispielsweise die Verwendung von [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de), wenn Sie Ihre Impressionsdaten berücksichtigen möchten.
