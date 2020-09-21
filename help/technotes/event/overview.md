---
title: Analyse der von Ereignissen betroffenen Daten
description: Verstehen Sie, wie die von einem Ereignis betroffenen Daten zur Datenqualität insgesamt beitragen.
translation-type: ht
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: ht
source-wordcount: '390'
ht-degree: 100%

---


# Analyse der von Ereignissen betroffenen Daten

Manchmal kann ein Ereignis die Datenqualität in Ihrem Unternehmen beeinträchtigen. Beispiele hierfür sind:

* Ein Bot, der Ausreißerdaten sendet, beispielsweise Umsätze in Millionenhöhe,
* Ihr Unternehmen hat eine Aktualisierung Ihrer Website veröffentlicht, die sich negativ auf Ihre Analytics-Implementierung auswirkt,
* Andere Aspekte, die die Datenqualität oder -vollständigkeit beeinträchtigen.

Wenn auf Ihrer Site Probleme mit der Datenqualität aufgetreten sind, möchten Sie diese möglicherweise von der Berichterstellung ausschließen, um geschäftliche Entscheidungen zu vermeiden. Verwenden Sie diese Abschnitte, um die Auswirkungen des Ereignisses auf Ihre Daten zu beurteilen und festzulegen, wie Sie vorgehen möchten.

## Ursache eines Ereignisses bestimmen

Wenn Sie sich nicht sicher sind, warum Sie Datenspitzen oder Datenrückgänge sehen, lesen Sie [Fehlerbehebung bei Datenspitzen/Datenrückgängen](spikes-drops.md).

## Daten mithilfe der Segmentierung analysieren und ausschließen

Adobe Analytics Angebots bietet eine einfache und stabile Möglichkeit, sich auf Daten zu konzentrieren oder diese auszuschließen. Sie können Datumsbereichsdimensionen innerhalb von Segmenten verwenden, um diese bestimmten Daten herauszufiltern oder sich darauf zu konzentrieren. Weitere Informationen finden Sie unter [Ausschließen spezifischer Daten in der Analyse](segments.md).

## Ereignis mit vorherigen Datumsbereichen vergleichen

Wenn Sie mehr darüber erfahren möchten, wie stark sich ein Ereignis im Laufe der Zeit auf Ihre Daten auswirkt, können Sie den Datumsvergleich in Analysis Workspace verwenden. Woche für Woche oder Monat für Monat vergleichen, um zu sehen, wie sie sich im Vergleich zu früheren Bereichen verhalten. Sie können diesen Vergleich dann verwenden, um festzustellen, wie stark ein Ereignis Trends beeinflusst. Weitere Informationen finden Sie unter [Daten, die von einem Ereignis beeinflusst wurden, mit vorherigen Datumsbereichen vergleichen](compare-dates.md).

## Daten mithilfe berechneter Metriken ableiten

Sobald Sie Segmente erstellt und den Datumsvergleich verwendet haben, können Sie beide Konzepte kombinieren, um Trend-Daten mithilfe berechneter Metriken zu korrigieren. Schließen Sie die Segmente in eine berechnete Metrik ein und multiplizieren Sie dann die betroffenen Tage mit dem beim Datumsvergleich gefundenen Versatz. Weitere Informationen finden Sie unter [Ableiten von Daten, die von Ereignissen betroffen sind](calcmetrics.md).

## Auswirkungen an Benutzer in Ihrer Organisation kommunizieren

Sobald Sie mit der geplanten Handhabung eines Ereignisses vertraut sind, können Sie mit den Benutzern in Ihrem Unternehmen [kommunizieren](communicate.md). Adobe bietet in Analytics mehrere Stellen an, an denen Sie Text platzieren können, um den Benutzern mitzuteilen, was passiert ist und welche Komponenten sie verwenden können.

## Video

Dieses Video führt Sie durch die oben genannten Schritte.

>[!VIDEO](https://video.tv.adobe.com/v/33316?quality=12&captions=ger)

* **0:27**: Daten mithilfe der Segmentierung ausschließen
* **2:55**: Ereignis mit vorherigen Bereichen vergleichen
* **8:42**: Daten mithilfe berechneter Metriken ableiten
* **11:46**: Auswirkungen an Benutzer kommunizieren
