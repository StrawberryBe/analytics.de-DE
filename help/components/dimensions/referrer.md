---
title: Referrer
description: Die URL, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 5%

---


# Referrer

Die Dimension &quot;Werber&quot;zeigt an, auf welchen URLs sich die Besucher befanden, wenn sie zum Erreichen Ihrer Site durchklickt wurden. Diese Dimension ist nützlich, um zu verstehen, welche bestimmten URLs den meisten Traffic zu Ihrer Site bringen. Ein Link muss auf der externen URL vorhanden sein, und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne URLs enthalten oder die Anzeige externer URLs verhindern.

Derselbe Bericht kann unterschiedliche Ergebnisse zwischen Analysis Workspace und Data warehouse anzeigen. Analysis Workspace meldet den Werber für jede einzelne Seite, wobei Werte ausgeschlossen werden, die mit internen URL-Filtern übereinstimmen. Data warehouse meldet nur den ersten Werber des Besuchs und ignoriert interne URL-Filter.

## Diese Dimension mit Daten füllen

Diese Dimension erfordert die Konfiguration auf der Analytics-Oberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `r` für die Zeichenfolge in Bildanforderungen einschließen.
* Auf der Analytics-Oberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md)Ihrer Report Suite konfigurieren. Wenn interne URL-Filter nicht konfiguriert werden, können sie entweder interne URLs enthalten oder die Anzeige externer URLs verhindern.

## Dimensionen

Zu den Elementen der Dimension gehören URLs, die Besucher durchklicken, um zu Ihrer Site zu gelangen. Wenn ein Treffer keine Werber-Daten enthält, gruppiert er sich unter dem Dimensionselement `"Typed/Bookmarked"`. Dieses Dimensionselement bedeutet, dass kein Werber vorhanden ist, z. B. wenn der Besucher die Browseradresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat.

### Dimensionen, die `googleusercontent.com`

Benutzer können Dimensionselemente mit der Domäne anzeigen `googleusercontent.com`.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls sie offline genommen werden. Diese zwischengespeicherten Seiten stehen neben den meisten Suchergebnissen zur Verfügung, indem Sie auf den Link &quot;Zwischengespeichert&quot;klicken. Wenn ein Benutzer auf diesen Link klickt und den von Google zwischengespeicherten Inhalt Ansicht, `webcache.googleusercontent.com` ist dies ein typisches Dimensionselement.
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Dienst anzeigen, stammt sie von `translate.googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
