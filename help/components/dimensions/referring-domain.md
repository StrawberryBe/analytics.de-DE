---
title: Referrerdomäne
description: Die übergreifende Domäne, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 5%

---


# Referrerdomäne

Die Dimension &quot;Verweisende Domäne&quot;zeigt an, welche Domänen Besucher durchklicken, um zu Ihrer Site zu gelangen. Diese Dimension ist nützlich, um zu verstehen, welche Websites von Drittanbietern den meisten Traffic zu Ihrer Site bringen. Ein Link muss auf der externen Site vorhanden sein und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne Domänen enthalten oder die Anzeige externer Domänen verhindern.

Derselbe Bericht kann unterschiedliche Ergebnisse zwischen Analysis Workspace und Data warehouse anzeigen. Analysis Workspace meldet die Referrerdomäne für jede einzelne Seite, mit Ausnahme der Werte, die mit internen URL-Filtern übereinstimmen. Data warehouse meldet nur die erste verweisende Domäne des Besuchs und ignoriert interne URL-Filter.

## Diese Dimension mit Daten füllen

Diese Dimension erfordert die Konfiguration auf der Analytics-Oberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `r` für die Zeichenfolge in Bildanforderungen einschließen.
* Auf der Analytics-Oberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md)Ihrer Report Suite konfigurieren. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne Domänen enthalten oder die Anzeige externer Domänen verhindern.

Adobe behält die verweisende Domäne bei einem Besuch bei. Wenn ein Besucher während eines Besuchs einen Link in einer anderen Domäne verlässt und durchklickt, wird der neue Wert aktualisiert und bleibt für den Rest des Besuchs bestehen. Wenn Sie nur den ursprünglichen Wert anzeigen möchten, finden Sie weitere Informationen unter [Ursprüngliche verweisende Domäne](original-referring-domain.md).

## Dimensionen

Zu den Elementen der Dimension gehören Domänen, die Besucher durch Ihre Site durchklicken. Wenn ein Treffer keine Werber-Daten enthält (entweder festgelegt oder dauerhaft), gruppiert er sich unter dem Dimensionselement `"Typed/Bookmarked"`. Dieses Dimensionselement bedeutet, dass kein Werber vorhanden ist, z. B. wenn der Besucher die Browseradresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.

### Dimensionen, die `googleusercontent.com`

Benutzer können Dimensionselemente mit der Domäne anzeigen `googleusercontent.com`.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls sie offline genommen werden. Diese zwischengespeicherten Seiten stehen neben den meisten Suchergebnissen zur Verfügung, indem Sie auf den Link &quot;Zwischengespeichert&quot;klicken. Wenn ein Benutzer auf diesen Link klickt und die von Google zwischengespeicherten Inhalte Ansicht, ist dies das Dimensionselement `googleusercontent.com` .
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Dienst anzeigen, stammt sie von `googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
