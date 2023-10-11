---
title: Eine Virtual Report Suite auf bestimmte Daten beschränken
description: Erfahren Sie, wie Sie den Datumsbereich einer Virtual Report Suite so einschränken, dass er sich nur auf zugeordnete Daten konzentriert.
exl-id: 421d101d-8c64-47f7-b5a2-da039889f663
feature: CDA
source-git-commit: 266cf18050d60f08f7e170c56453d1e1d805cb7b
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 35%

---

# Eine Virtual Report Suite auf bestimmte Daten beschränken

Wenn wir das Zusammenfügen von Daten einschalten, beginnt dieses Zusammenfügen an einem bestimmten Datum. Angenommen, dieses Datum ist der 1. Juni. Die Virtual Report Suite der geräteübergreifenden Analyse enthält nicht zugeordnete Daten aus dem Zeitraum vor dem 1. Juni. Möglicherweise möchten Sie Daten aus der Virtual Report Suite vor dem 1. Juni ausblenden, damit sich Ihre Analyse nach dem Stitching auf Datumsbereiche konzentrieren kann.

Sie können die Virtual Report Suite-Daten auf bestimmte Daten beschränken, indem Sie Folgendes ausführen:

## Schritt 1: Virtual Report Suite mit einem rollierenden täglichen Datumsbereich erstellen

Wenn Sie die Virtual Report Suite einrichten, fügen Sie unter &quot;Komponenten&quot;einen Datumsbereich mit festem Start und einem rollierenden täglichen Datumsbereich hinzu. Der feste Beginn sollte der Tag sein, an dem das Zusammenfügen begann.

![](assets/rolling-daily.png)

## Schritt 2: Segment „exclude-exclude“ erstellen

Erstellen Sie anschließend ein Treffersegment, das den Datumsbereich in einen Ausschluss-Container innerhalb eines anderen Ausschluss-Containers einfügt. Es handelt sich um einen &quot;Ausschluss&quot;.

Der Grund für den Ausschluss ist, dass Datumsbereiche den Datumsbereich des Berichts überschreiben sollen. Wenn Sie also nur den Bereich ab dem 1. Juni mit einbeziehen, wird der Datumsbereich des Berichts immer ab dem 1. Juni sein. Dies führt zu unerwünschten Ergebnissen. Wenn Sie &quot;Ausschließen&quot;auswählen, wird dieses Verhalten außer Kraft gesetzt und die Daten, aus denen Sie Daten beziehen können, werden auf den entsprechenden Datumsbereich beschränkt.

![](assets/exclude-exclude.png)

## Schritt 3: Dieses Segment auf Ihre geräteübergreifende Analytics Virtual Report Suite anwenden

![](assets/apply-segment.png)

## Schritt 4: Ergebnisse im Reporting ansehen

Beachten Sie, dass das Reporting jetzt am gewünschten Datum beginnt, dem Tag, an dem das Zusammenfügen zum ersten Mal implementiert wurde:

![](assets/report-limited-dates.png)
