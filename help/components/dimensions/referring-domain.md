---
title: Referrerdomäne
description: Die übergreifende Domäne, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 1%

---


# Referrerdomäne

Die Dimension &quot;Verweisende Domäne&quot;zeigt an, welche Domänen Besucher durchklicken, um zu Ihrer Site zu gelangen. Diese Dimension ist nützlich, um zu verstehen, welche Websites von Drittanbietern den meisten Traffic zu Ihrer Site bringen. Ein Link muss auf der externen Site vorhanden sein und ein Besucher muss darauf klicken, damit der Dimensionswert angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne Domänen enthalten oder die Anzeige externer Domänen verhindern.

## Diese Dimension mit Daten füllen

Diese Dimension erfordert die Konfiguration auf der Analytics-Oberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. beim Starten der Adobe Experience Platform), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `r` für die Zeichenfolge in Bildanforderungen einschließen.
* Auf der Analytics-Oberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md)Ihrer Report Suite konfigurieren. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne Domänen enthalten oder die Anzeige externer Domänen verhindern.

Adobe behält die verweisende Domäne bei einem Besuch bei. Wenn ein Besucher während eines Besuchs einen Link in einer anderen Domäne verlässt und durchklickt, wird der neue Wert aktualisiert und bleibt für den Rest des Besuchs bestehen. Wenn Sie nur den ursprünglichen Wert anzeigen möchten, finden Sie weitere Informationen unter [Ursprüngliche verweisende Domäne](original-referring-domain.md).

## Dimensionswerte

Dimensionswerte umfassen Domänen, die Besucher zu Ihrer Site durchklicken. Wenn ein Treffer keine Werber-Daten enthält (entweder festgelegt oder dauerhaft), wird er unter dem Dimensionswert gruppiert `"Typed/Bookmarked"`. Dieser Dimensionswert bedeutet, dass kein Werber vorhanden ist, z. B. wenn der Besucher die Browseradresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.
