---
title: Ursprüngliche Referrer-Domain
description: Die erste Referrer-Domäne, auf der sich ein Besucher befand, bevor er zu Ihrer Site klickte.
feature: Dimensions
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '408'
ht-degree: 100%

---

# Ursprüngliche Referrer-Domain

Die Dimension „Ursprüngliche Referrer-Domäne“ gibt die erste Referrer-Domäne an, von welcher ein Besucher klickte, um zu Ihrer Site zu gelangen. Sobald sie festgelegt wurde, enthält sie denselben Wert für die gesamte Lebensdauer dieser Besucher-ID. Diese Dimension ist nützlich, um zu verstehen, welche Drittanbieter-Sites den Traffic ursprünglich zu Ihrer Site leiten.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

## Füllen dieser Dimension mit Daten

Diese Dimension muss sowohl in der Analytics-Oberfläche als auch in Ihrer Implementierung konfiguriert werden.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `r` bei allen Bildanforderungen einbeziehen.
* Auf der Analytics-Benutzeroberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

Adobe behält die ursprüngliche Referrer-Domäne für die gesamte Lebensdauer eines Besuchers bei. Wenn ein Besucher zu irgendeinem Zeitpunkt einen Link auf einer anderen Domain durchklickt, wird der neue Wert nicht erfasst. Informationen zum Anzeigen der neuen Werte finden Sie unter [Referrer-Domäne](referring-domain.md).

## Dimensionselemente

Zu den Dimensionselementen gehören die Domänen, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten (entweder gesetzt oder beibehalten) enthält, wird er unter dem Dimensionselement `"None"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.

## Referrer-Domäne im Vergleich zur ursprünglichen Referrer-Domäne

Die Referrer-Domäne kann sich zwischen Besuchen ändern. So gelangt beispielsweise ein Besucher über `google.com` zu Ihrer Seite und dann eine Woche später über `twitter.com`. Eventuell tätigt er einen Kauf auf Ihrer Site. Wenn Sie Referrer-Domäne als Dimension mit Letztkontakt-Attribution verwenden, wird der Kauf `twitter.com` gutgeschrieben. Wenn Sie die ursprüngliche Referrer-Domäne als Dimension verwenden, wird der Kauf unabhängig vom Attributionsmodell `google.com` gutgeschrieben.

Die ursprüngliche Referrer-Domäne ändert sich während der gesamten Lebensdauer einer bestimmten Besucher-ID nie.
