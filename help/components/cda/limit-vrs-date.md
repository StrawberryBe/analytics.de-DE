---
title: VRS auf bestimmte Daten beschränken
description: Verstehen Sie, wie Sie einen VRS-Datumsbereich so beschränken, dass er sich nur auf geheftete Daten konzentriert.
translation-type: tm+mt
source-git-commit: 954927359420cfdb3d0e908758fc36464e15fee5
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# VRS auf bestimmte Daten beschränken

Wenn wir das Sticken einschalten, die Nähen Beginn an einem bestimmten Datum. Nehmen wir an, das Datum ist der 1. Juni. Die CDA-VRS enthält noch vor dem 1. Juni noch nicht zugewiesene Daten. Eventuell möchten Sie Daten in der VRS vor dem 1. Juni ausblenden, damit sich Ihre Analyse nach dem Beginn des Stichs auf Datumsbereiche konzentrieren kann.

Sie können die VRS-Daten wie folgt auf bestimmte Daten beschränken:

## Schritt 1: Erstellen einer VRS mit einem rollierenden täglichen Datumsbereich

Wenn Sie die VRS einrichten, fügen Sie unter &quot;Komponenten&quot;einen Datumsbereich mit festem Beginn und einem rollierenden Datumsbereich hinzu. Der feste Beginn sollte der Tag sein, an dem das Nähen begann.

![](assets/rolling-daily.png)

## Schritt 2: Segment &quot;exclude-exclude&quot;erstellen

Erstellen Sie anschließend ein Treffersegment, das den Datumsbereich in einen Ausschlussabschnitt eines anderen Containers einfügt. Es handelt sich um ein &quot;Ausschließen&quot;.

Der Grund für den Ausschluss ist, dass Datumsbereiche den Datumsbereich des Berichts außer Kraft setzen sollen. Wenn Sie also nur den 1. Juni miteinbeziehen, wird der Datumsbereich des Berichts immer vom 1. Juni vorgestellt. Dies führt zu unerwünschten Ergebnissen. Wenn Sie &quot;Ausschließen&quot;auswählen, wird dieses Verhalten außer Kraft gesetzt und die Daten, die Sie daraus ziehen können, werden auf den entsprechenden Datumsbereich beschränkt.

![](assets/exclude-exclude.png)

## Schritt 3: Dieses Segment auf Ihre CDA VRS anwenden

![](assets/apply-segment.png)

## Schritt 4: Ergebnisse im Berichte

Beachten Sie, dass Berichte nun am gewünschten Datum, d. h. am Tag der ersten Implementierung der Stich-Funktion, Beginn sind:

![](assets/report-limited-dates.png)