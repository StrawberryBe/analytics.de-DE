---
title: Best Practices für die Attribution
description: Welche Best Practices bestehen für die Wahl eines Attributionsmodells?
feature: Attribution
exl-id: 92c6039c-f950-4746-8b34-ba18be258c08
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 59%

---

# Best Practices für die Attribution

Welches Attributionsmodells für Ihr Unternehmen am besten geeignet ist, hängt von einer Reihe von Überlegungen ab. Dieser Artikel zeigt eine Methodik sowie einige allgemeine Best Practices auf.

## Schritt 1: Explorative Analyse

>[!NOTE]
>Diese Analyse muss der Entscheidung für ein bestimmtes Attributionsmodell vorangehen.

In dieser vorbereitenden Phase geht es darum, ein Verständnis des Kundenverhaltens zu gewinnen und Konversionsmetriken zu bestimmen. Basierend auf der Konversionsmetrik erleichtern Tools wie [Daten-Feeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=de) (für Rohdaten) oder Analysis Workspace Ihr Verständnis von

* Anzahl der Kunden, die verschiedene Marketing-Kanäle vor der Konvertierung
* Der Anteil/die Verteilung dieser Verhaltensweisen

Wenn beispielsweise 50 % der Kunden vor ihrer Konversion über drei Kanäle mit Ihnen in Kontakt kommen, besteht dann eine Interaktion zwischen diesen drei Kanälen?
Sie können dann eine Analyse des oberen und des unteren Ende des Trichters durchführen, um Ihr Verständnis zu erweitern.

### Analyse des oberen Ende des Trichters

Die Analyse-Kanäle der oberen Trichter werden verwendet, um Marken- oder Produktbewusstsein zu schaffen. So zielen etwa TV-Werbespots in der Regel auf die Markenwahrnehmung ab. Hierfür empfiehlt sich das [Attributionsmodell des Zeitverfalls](/help/analyze/analysis-workspace/attribution/models.md), da Ihr TV-Werbespot im Zeitverlauf aus dem Gedächtnis Ihrer Zielgruppe verschwinden wird.

### Analyse des unteren Ende des Trichters

Bei der Analyse der unteren Trichter wird davon ausgegangen, dass die Benutzer bereits über Ihre Marke Bescheid wissen und Sie möchten, dass sie konvertieren. Verwenden Sie E-Mail-, Push-Benachrichtigungen oder Facebook-Anzeigen.

## Schritt 2: Regelbasierte Attribution

Dieser Schritt dient der Validierung Ihrer Hypothesen.

**Beispiel 1**

Angenommen, Ihre Hypothese lautet: &quot;Mein Erstkontakt-Kanal hat mehr Auswirkungen auf die Konversion als mein Letztkontakt-Kanal.&quot;

In diesem Fall würden Sie dann die [&quot;Umgekehrtes J-förmiges&quot;Attributionsmodell](/help/analyze/analysis-workspace/attribution/models.md) um diese Hypothese zu testen. Dieses Modell schreibt dem ersten Kontaktpunkt (bzw. „Touchpoint“) eine Gewichtung von 60 % zu.

**Beispiel 2**

Angenommen, Ihre Hypothese lautet: &quot;In unserer Branche (wie der Reisebranche) beträgt das Attributionsfenster 60 oder 90 Tage, nicht 30 Tage, da Kunden vor dem Kauf eines Produkts viel recherchieren.&quot;

In diesem Fall würden Sie Ihre [Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=de#lookback-windows) auf 90 Tage.

## Schritt 3: Algorithmische Attribution verwenden

Wenn Sie noch kein Attributionsmodell haben, das zufriedenstellende Antworten auf all Ihre Fragen bietet, können Sie [algorithmische Attribution](/help/analyze/analysis-workspace/attribution/algorithmic.md). Da es sehr schwierig ist, eine große Anzahl möglicher Hypothesen und Kombinationen zu validieren, verwendet die algorithmische Attribution integrierte Algorithmen, um die Gewichtung über Dimensionselemente hinweg zuzuordnen.

## Weiter Überlegungen

* Möglicherweise sollten Sie ergänzend zu Analysis Workspace einen Datenwissenschaftler hinzuziehen.
* Sie können sich auf Rohdaten verlassen, wie in Daten-Feeds von Adobe.
* Erwägen Sie beispielsweise die Verwendung von [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de), wenn Sie Ihre Impressionsdaten berücksichtigen möchten.
