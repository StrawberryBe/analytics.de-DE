---
title: VRS auf bestimmte Daten beschränken
description: Verstehen Sie, wie Sie einen VRS-Datumsbereich so beschränken, dass er sich nur auf zusammengefügte Daten konzentriert.
exl-id: 421d101d-8c64-47f7-b5a2-da039889f663
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '256'
ht-degree: 100%

---

# VRS auf bestimmte Daten beschränken

Wenn wir das Zusammenfügen von Daten einschalten, beginnt dieses Zusammenfügen an einem bestimmten Datum. Angenommen, dieses Datum ist der 1. Juni. Die CDA-VRS enthält Daten von vor dem 1. Juni, die noch nicht zusammengefügt wurden. Eventuell möchten Sie Daten in der VRS vor dem 1. Juni ausblenden, damit sich Ihre Analyse auf Datumsbereiche nach dem Beginn des Zusammenfügens konzentrieren kann.

Sie können die VRS-Daten wie folgt auf bestimmte Datumsbereiche beschränken:

## Schritt 1: Erstellen einer VRS mit einem rollierenden täglichen Datumsbereich

Wenn Sie die VRS einrichten, fügen Sie unter „Komponenten“ einen Datumsbereich mit festem Beginn und einem täglich rollierenden Datumsbereich hinzu. Der feste Beginn sollte der Tag sein, an dem das Zusammenfügen begann.

![](assets/rolling-daily.png)

## Schritt 2: Segment „exclude-exclude“ erstellen

Erstellen Sie anschließend ein Treffersegment, das den Datumsbereich in einen Ausschluss-Container innerhalb eines anderen Ausschluss-Containers einfügt. Es handelt sich um ein „Ausschließen des Ausschließens“.

Der Grund für den Ausschluss ist, dass Datumsbereiche den Datumsbereich des Berichts außer Kraft setzen sollen. Wenn Sie also nur den Bereich ab dem 1. Juni mit einbeziehen, wird der Datumsbereich des Berichts immer ab dem 1. Juni sein. Dies führt zu unerwünschten Ergebnissen. Wenn Sie „exclude exclude“ auswählen, wird dieses Verhalten außer Kraft gesetzt und die Daten, aus denen Sie Informationen ziehen können, werden auf den entsprechenden Datumsbereich beschränkt.

![](assets/exclude-exclude.png)

## Schritt 3: Dieses Segment auf Ihre CDA VRS anwenden

![](assets/apply-segment.png)

## Schritt 4: Ergebnisse im Reporting ansehen

Beachten Sie, dass das Reporting jetzt am gewünschten Datum beginnt, dem Tag, an dem das Zusammenfügen zum ersten Mal implementiert wurde:

![](assets/report-limited-dates.png)
