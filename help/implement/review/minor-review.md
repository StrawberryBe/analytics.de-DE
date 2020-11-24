---
title: Überprüfung der geringen Implementierung (nach jeder Website-Version)
description: Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Implementierung fehlerfrei und im Einklang mit Ihren KPIs ausgeführt wird.
translation-type: tm+mt
source-git-commit: 82064e267729b6995402bd122c6f71b3d38967a3
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Überprüfung der geringen Implementierung (nach jeder Website-Version)

Warum sollten Sie Ihre Implementierung nach jeder Website-Version überprüfen? Da Sie sicherstellen müssen, dass Ihre Codeaktualisierungen keine unbeabsichtigten Auswirkungen hatten, sollten Sie alle Probleme mit der Datenqualität beheben, solange diese noch gering sind. Wenn Sie diese Überprüfung nach jeder Website-Veröffentlichung immer wieder durchführen, werden Sie feststellen, dass Ihre [wichtigsten Reviews](/help/implement/review/major-review.md) (alle 6 Monate) viel einfacher sind. Sie werden auch verhindern, dass kleine Themen zu Big-Data-Problemen werden, die das Vertrauen der Interessenträger untergraben könnten.

## 1. Wie hat sich die Veröffentlichung auf die Daten für diesen Abschnitt der Site ausgewirkt?

Führen Sie gründliche Komponententests durch: Überprüfen Sie alle Code- und Variablen, die dem gerade aktualisierten Abschnitt der Site entsprechen, um sicherzustellen, dass die neue Verfolgung wunschgemäß funktioniert.

## 2. Dokumentation aktualisieren

Aktualisieren Sie Ihr Business Requirement Dokument (BRD) und Ihre Lösungsdesignreferenz (SDR) mit allen Variablen, die Sie hinzugefügt/geändert haben, um den Start aufzunehmen.

Verfügen Sie nicht über eine Dokumentation Ihrer Implementierung? Exportieren Sie eine Liste von Variablen und erstellen Sie Ihre BRD oder SDR mit [dieser Vorlage](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=en#implementation).

## 3. Beginn mit Ihren 5 KPIs

Die Kenntnis der fünf wichtigsten Leistungsindikatoren (KPIs) hilft Ihnen bei der Ermittlung der zugehörigen Metriken und Dimensionen, die Sie untersuchen müssen. Wenn Sie Ihre KPIs in den letzten 6 Monaten nicht aktualisiert haben oder wenn Ihr Unternehmen noch keine KPIs erstellt hat, befolgen Sie [diese Anweisungen](/help/implement/review/define-kpis.md).

## 4. Funktionieren alle KPI-Metriken und -Variablen nach der Veröffentlichung noch gut?

Codeaktualisierungen können unbeabsichtigte Auswirkungen haben. Sie möchten sicherstellen, dass alle Metriken und Dimensionen, die mit [Ihren Top-5-KPIs](/help/implement/review/define-kpis.md) verknüpft sind, weiterhin korrekt funktionieren. Gehen Sie folgendermaßen vor:

* **Erstellen Sie Dashboards** , um die Trendansicht der Ansichten dieser kritischen Metriken und Variablen zu sehen (Sie können auch intelligente Warnhinweise für jede Metrik einrichten) und diese für einen oder zwei Tage nach der Veröffentlichung überwachen, um sicherzustellen, dass die erwarteten Daten eingehen und die Daten korrekt sind. Suchen Sie nach Wendepunkten. Seien Sie bereit, alle kritischen Probleme sofort zu beheben. Wenn Sie Unstimmigkeiten feststellen, die nicht korrekt aussehen, sollten Sie sich Ihre Datenschicht, Tag-Manager-Regeln und Verarbeitungsregeln ansehen, um herauszufinden, warum.
* **Führen Sie das Analytics Health Dashboard** erneut aus, um breite Trends Ihrer KPI-Metriken und -Variablen zu überwachen.
Weitere Informationen dazu, wie Sie sicherstellen können, dass Ihre Metriken und Variablen ordnungsgemäß funktionieren, finden Sie in diesen Tipps von Adobe Analytics Champion Sarah Owen.

## 5. Gibt es Lücken in Ihrer Datenqualität?

Beurteilung der Situation und Erstellung eines Plans zur Behebung der Daten. Nehmen Sie dann die erforderlichen Änderungen vor, aktualisieren Sie Ihre Dokumentation und informieren Sie Ihre Stakeholder über die vorgenommenen Änderungen.

Sehen Sie sich dieses Video von Adobe Analytics Champion Sarah Owen über die natürlichen Zeiten an, in denen Sie Rezensionen Ihrer Implementierung in Ihren Zeitplan einpassen können:

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
