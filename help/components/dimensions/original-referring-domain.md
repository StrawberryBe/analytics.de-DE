---
title: Ursprüngliche verweisende Domäne
description: Die erste verweisende Domäne, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
translation-type: tm+mt
source-git-commit: 7c722e361978a3d7517e95c23442b703e7e25270
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---


# Ursprüngliche verweisende Domäne

Die Dimension &quot;Ursprünglich verweisende Domäne&quot;meldet die erste verweisende Domäne, über die ein Besucher zum Erreichen Ihrer Site geklickt hat. Sobald er festgelegt wurde, enthält er denselben Wert für die gesamte Lebensdauer dieser Besucher-ID. Diese Dimension ist nützlich, um zu verstehen, welche Drittanbieter-Sites ursprünglich den Traffic zu Ihrer Site fördern.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne Domänen enthalten oder die Anzeige externer Domänen verhindern.

## Diese Dimension mit Daten füllen

Diese Dimension muss sowohl auf der Analytics-Oberfläche als auch in Ihrer Implementierung konfiguriert werden.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `r` für die Zeichenfolge in Bildanforderungen einschließen.
* Auf der Analytics-Oberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md)Ihrer Report Suite konfigurieren. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne Domänen enthalten oder die Anzeige externer Domänen verhindern.

Die Adobe behält die ursprünglich verweisende Domäne während der Lebensdauer eines Besuchers bei. Wenn ein Besucher zu irgendeinem Zeitpunkt einen Link in einer anderen Domäne verlässt und durchklickt, wird der neue Wert nicht aufgezeichnet. Weitere Informationen zu neuen Werten finden Sie unter [Verweisende Domäne](referring-domain.md).

## Dimensionen

Zu den Elementen der Dimension gehören Domänen, die Besucher durch Ihre Site durchklicken. Wenn ein Treffer keine Werber-Daten enthält (entweder festgelegt oder dauerhaft), gruppiert er sich unter dem Dimensionselement `"None"`. Dieses Dimensionselement bedeutet, dass kein Werber vorhanden ist, z. B. wenn der Besucher die Browseradresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.

## Verweisende Domäne mit ursprünglich verweisender Domäne vergleichen

Die verweisende Domäne kann sich zwischen den Besuchen ändern. So gelangt beispielsweise ein Besucher über einen Zeitraum von einer Woche zu Ihrer Site `google.com`und gelangt dann bis zu Ihrer Site `twitter.com`. Schließlich tätigen sie einen Kauf auf Ihrer Site. Wenn Sie Referrerdomäne als Dimension mit Last Touch-Zuordnung verwenden, wird der Kauf `twitter.com` gutgeschrieben. Wenn Sie die ursprüngliche verweisende Domäne als Dimension verwenden, `google.com` wird der Kauf unabhängig vom Zuordnungsmodell gutgeschrieben.

Die ursprüngliche verweisende Domäne ändert sich nie während der gesamten Lebensdauer einer angegebenen Besucher-ID.
