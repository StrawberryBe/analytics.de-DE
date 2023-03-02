---
title: Best Practices für die Attribution
description: Welche Best Practices bestehen für die Wahl eines Attributionsmodells?
feature: Attribution
exl-id: 92c6039c-f950-4746-8b34-ba18be258c08
source-git-commit: ce7f953b8f7f1f7d0616074454e4401937fcc0c7
workflow-type: ht
source-wordcount: '422'
ht-degree: 100%

---

# Best Practices für die Attribution

Welches Attributionsmodells für Ihr Unternehmen am besten geeignet ist, hängt von einer Reihe von Überlegungen ab. Dieser Artikel zeigt eine Methodik sowie einige allgemeine Best Practices auf.

## Schritt 1: Explorative Analyse

>[!NOTE]
>Diese Analyse muss der Entscheidung für ein bestimmtes Attributionsmodell vorangehen.

In dieser vorbereitenden Phase geht es darum, ein Verständnis des Kundenverhaltens zu gewinnen und Konversionsmetriken zu bestimmen. Basierend auf der Konversionsmetrik erleichtern Tools wie [Daten-Feeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=de) (für Rohdaten) oder Analysis Workspace Ihr Verständnis von

* Anzahl der Kundinnen und Kunden, die vor der Konvertierung verschiedene Marketing-Kanäle nutzten
* Der Anteil/die Verteilung dieser Verhaltensweisen

Wenn beispielsweise 50 % der Kunden vor ihrer Konversion über drei Kanäle mit Ihnen in Kontakt kommen, besteht dann eine Interaktion zwischen diesen drei Kanälen?
Sie können dann eine Analyse des oberen und des unteren Ende des Trichters durchführen, um Ihr Verständnis zu erweitern.

### Analyse des oberen Ende des Trichters

Bei der Analyse des oberen Ende des Trichters werden diejenigen Kanäle untersucht, die zur Förderung der Marken- oder Produktwahrnehmung dienen. So zielen etwa TV-Werbespots in der Regel auf die Markenwahrnehmung ab. Hierfür empfiehlt sich das [Attributionsmodell des Zeitverfalls](/help/analyze/analysis-workspace/attribution/models.md), da Ihr TV-Werbespot im Zeitverlauf aus dem Gedächtnis Ihrer Zielgruppe verschwinden wird.

### Analyse des unteren Ende des Trichters

Bei der Analyse des unteren Trichters geht man davon aus, dass die Menschen bereits von Ihrer Marke wissen und Sie möchten, dass sie konvertieren. Verwenden Sie E-Mail- oder Push-Benachrichtigungen oder Facebook-Anzeigen.

## Schritt 2: Regelbasierte Attribution

Dieser Schritt dient der Validierung Ihrer Hypothesen.

**Beispiel 1**

Angenommen, Ihre Hypothese lautet: „Mein für den Erstkontakt verwendeter Kanal hat größeren Einfluss auf die Konversion als mein für den Letztkontakt verwendeter“. 

In diesem Fall würden Sie das [Attributionsmodell „Umgekehrt J-förmig“](/help/analyze/analysis-workspace/attribution/models.md) anwenden, um diese Hypothese zu testen. Dieses Modell schreibt dem ersten Kontaktpunkt (bzw. „Touchpoint“) eine Gewichtung von 60 % zu.

**Beispiel 2**

Angenommen, Ihre Hypothese lautet: „In unserer Branche (z. B. der Reisebranche) beträgt das Attributionsfenster 60 oder 90 Tage, nicht 30 Tage, da Kundinnen und Kunden vor dem Kauf eines Produkts sehr viel recherchieren.“

In diesem Fall würden Sie Ihr [Lookback-Fenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=de#lookback-windows) auf 90 Tage ändern.

## Schritt 3: Algorithmische Attribution verwenden

Wenn Sie noch kein Attributionsmodell haben, das alle Ihre Fragen zufriedenstellend beantwortet, können Sie die [algorithmische Attribution](/help/analyze/analysis-workspace/attribution/algorithmic.md) verwenden. Da es sehr schwierig ist, eine große Anzahl möglicher Hypothesen und Kombinationen zu validieren, werden bei der algorithmischen Attribution integrierte Algorithmen verwendet, um auf die einzelnen Dimensionen Punkte zu verteilen.

## Weiter Überlegungen

* Möglicherweise sollten Sie ergänzend zu Analysis Workspace einen Datenwissenschaftler hinzuziehen.
* Sie können sich auf Rohdaten verlassen, wie in Daten-Feeds von Adobe.
* Erwägen Sie beispielsweise die Verwendung von [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de), wenn Sie Ihre Impressionsdaten berücksichtigen möchten.
