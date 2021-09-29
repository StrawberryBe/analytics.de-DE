---
title: Eindeutige Geräte
description: Die Anzahl der eindeutigen Geräte.
exl-id: fa5c860f-bea7-4d03-9632-fa6e025647bf
source-git-commit: db88bd439c036e97cca641f31f4fc3101a368636
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 5%

---

# Eindeutige Geräte

Die Metrik &quot;Eindeutige Geräte&quot;ist eine [geräteübergreifende Analyse](../cda/overview.md) -Metrik, die die Anzahl eindeutiger nicht identifizierter Geräte und eindeutiger virtueller Geräte zählt. Nicht identifizierte Geräte sind Geräte, die anonyme Treffer generiert haben. Eindeutige virtuelle Geräte sind unterschiedliche Personen, die pro Gerät identifiziert werden.

## Berechnung dieser Metrik

Summieren Sie für jedes Gerät alle eindeutigen Personen, die mit ihm verknüpft sind (einschließlich anonymer , wenn das Gerät nicht zuordenbare Treffer enthält).

Beachten Sie, dass diese Metrik in Nicht-CDA-Report Suites nicht mit [Unique Visitors](unique-visitors.md) übereinstimmt. Beispielsweise wird ein Gerät von drei verschiedenen Konten gemeinsam genutzt. Wenn alle 3 Konten Ihre Site in einem Berichtsfenster besuchen, zeigt der resultierende Bericht 3 Unique Devices in der geräteübergreifenden Analyse an. Dieselben Daten außerhalb der geräteübergreifenden Analyse zeigen 1 Unique Visitor.

## Beispiel

1. Bob gelangt über eine Werbeanzeige zu Ihrer Site, ist jedoch nicht angemeldet.
1. Bob möchte einen Kauf tätigen, aber es würde lieber auf dem Familiencomputer tun, weil er bereits dort angemeldet ist. Auf dem Familiencomputer tätigt er einen Kauf.
1. Am nächsten Tag überprüft er seine Bestellung auf seinem Telefon und authentifiziert sich dort.
1. Bob&#39;s Frau Alice durchsucht Ihre Website, während sie sich bei ihrem Konto auf dem Familiencomputer angemeldet hat.
1. Bob&#39;s Bruder Charles durchsucht auch Ihre Website, während er sich in seinem Konto auf dem Familiencomputer angemeldet.

![Anzahl eindeutiger Geräte](/help/components/metrics/assets/Unique_Devices_Count.png)

Wenn Sie diese Daten in einer Virtual Report Suite der geräteübergreifenden Analyse vor [Replay](/help/components/cda/replay.md) anzeigen, werden möglicherweise nicht authentifizierte Treffer zugeordnet:

* **5 eindeutige Geräte**: 1 für nicht authentifizierte Bob + 2 für Bob + 1 für Alice + 1 für Charles
* **4  [Personen](people.md)**: 1  [Nicht identifizierte Personen](unidentified-people.md) + 3  [Identifizierte Personen](identified-people.md).
