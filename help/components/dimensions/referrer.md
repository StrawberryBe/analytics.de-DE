---
title: Referrer
description: Die URL, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Referrer

Die Dimension &quot;Werber&quot;zeigt an, auf welchen URLs sich die Besucher befanden, wenn sie zum Erreichen Ihrer Site durchklickt wurden. Diese Dimension ist nützlich, um zu verstehen, welche bestimmten URLs den meisten Traffic zu Ihrer Site bringen. Ein Link muss auf der externen URL vorhanden sein, und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne URLs enthalten oder die Anzeige externer URLs verhindern.

## Diese Dimension mit Daten füllen

Diese Dimension erfordert die Konfiguration auf der Analytics-Oberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. beim Starten der Adobe Experience Platform), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `r` für die Zeichenfolge in Bildanforderungen einschließen.
* Auf der Analytics-Oberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md)Ihrer Report Suite konfigurieren. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne URLs enthalten oder die Anzeige externer URLs verhindern.

## Dimensionselemente

Dimensionselemente enthalten URLs, die Besucher zu Ihrer Site durchklicken. Wenn ein Treffer keine Werber-Daten enthält, gruppiert er sich unter dem Dimensionselement `"Typed/Bookmarked"`. Dieses Dimensionselement bedeutet, dass kein Werber vorhanden ist, z. B. wenn der Besucher die Browseradresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.
