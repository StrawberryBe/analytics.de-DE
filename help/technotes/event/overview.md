---
title: Analyse der von Ereignissen betroffenen Daten
description: Verstehen Sie, wie die von einem Ereignis betroffenen Daten zur Datenqualität insgesamt beitragen.
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 3%

---


# Analyse der von Ereignissen betroffenen Daten

Manchmal kann ein Ereignis die Datenqualität in Ihrem Unternehmen beeinträchtigen. Zu den Beispielen gehören:

* Ein Bot sendet Auslieferungsdaten, z. B. Millionen Dollar Umsatz
* Ihr Unternehmen hat eine Aktualisierung Ihrer Website veröffentlicht, die Ihre Analytics-Implementierung negativ beeinflusst hat
* Andere Aspekte, die sich auf die Datenqualität oder -vollständigkeit auswirken

Wenn auf Ihrer Site ein Datenqualitätsproblem aufgetreten ist, sollten Sie es möglicherweise vom Berichte ausschließen, um Geschäftsentscheidungen darüber zu vermeiden. Verwenden Sie diese Abschnitte, um die Auswirkungen des Ereignisses auf Ihre Daten zu messen und festzulegen, wie Sie fortfahren möchten.

## Bestimmen der Ursache eines Ereignisses

Wenn Sie sich nicht sicher sind, warum die Daten eine Spitze oder einen Rückgang aufweisen, lesen Sie [Fehlerbehebung bei Spitzen/Datenverlust](spikes-drops.md).

## Daten mithilfe der Segmentierung analysieren und ausschließen

Adobe Analytics Angebots bietet eine einfache und stabile Möglichkeit, Daten mithilfe der Segmentierung zu fokussieren oder auszuschließen. Sie können Datumsbereichsdimensionen in Segmenten verwenden, um diese Daten zu filtern oder sich auf diese Daten zu konzentrieren. See [Exclude specific dates in analysis](segments.md).

## Vergleichen eines Ereignisses mit vorherigen Datumsbereichen

Wenn Sie mehr über die Auswirkungen eines Ereignisses auf Ihre Daten im Zeitverlauf erfahren möchten, können Sie den Datumsvergleich in Analysis Workspace verwenden. Mit dieser Funktion können Sie Daten von Tag zu Tag, Woche oder Monat miteinander vergleichen, um einen Vergleich mit vorherigen Bereichen anzustellen. Mit diesem Vergleich können Sie dann bestimmen, wie stark ein Ereignis Trends beeinflusst. Siehe [Datumsvergleiche, die von einem Ereignis beeinflusst wurden, mit vorherigen Datumsbereichen](compare-dates.md).

## Daten mithilfe berechneter Metriken ableiten

Nachdem Sie Segmente erstellt und den Datumsvergleich verwendet haben, können Sie beide Konzepte kombinieren, um Trenddaten mithilfe von berechneten Metriken zu korrigieren. Schließen Sie die Segmente in eine berechnete Metrik ein und multiplizieren Sie dann die betroffenen Tage mit dem beim Datumsvergleich gefundenen Offset. See [Derive data impacted by events](calcmetrics.md).

## Auswirkungen auf Benutzer in Ihrer Organisation kommunizieren

Sobald Sie mit der geplanten Handhabung eines Ereignisses vertraut sind, können Sie mit den Benutzern in Ihrem Unternehmen [kommunizieren](communicate.md). Adobe-Angebote finden Sie an mehreren Stellen in Analytics, an denen Sie Text platzieren können, um den Benutzern mitzuteilen, was passiert ist und welche Komponenten sie verwenden können.

## Video

Dieses Video führt Sie durch die oben genannten Schritte.

>[!VIDEO](https://video.tv.adobe.com/v/33316?quality=12)

* **0:27**: Daten mithilfe der Segmentierung ausschließen
* **2:55**: Ereignis mit vorherigen Bereichen vergleichen
* **8:42**: Daten mithilfe berechneter Metriken ableiten
* **11:46**: Auswirkungen an Benutzer kommunizieren
