---
title: Referrer
description: Die URL, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 49%

---


# Referrer

Die Dimension „Referrer“ gibt an, auf welchen URLs sich die Besucher befanden, als sie sich zu Ihrer Site durchklickten. Diese Dimension ist nützlich, um zu verstehen, welche spezifischen URLs den meisten Traffic zu Ihrer Site leiten. Ein Link muss auf der externen URL vorhanden sein, und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne URLs enthalten sein oder die Anzeige externer URLs verhindert werden.

Derselbe Bericht kann unterschiedliche Ergebnisse zwischen Analysis Workspace und Data Warehouse anzeigen. Analysis Workspace meldet den Werber für jede einzelne Seite, wobei Werte ausgeschlossen werden, die mit internen URL-Filtern übereinstimmen. Data Warehouse meldet nur den ersten Werber des Besuchs und ignoriert interne URL-Filter.

## Füllen dieser Dimension mit Daten

Diese Dimension erfordert die Konfiguration auf der Analytics-Benutzeroberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `r` bei allen Bildanforderungen einbeziehen.
* Auf der Analytics-Benutzeroberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne URLs enthalten sein oder die Anzeige externer URLs verhindert werden.

## Dimensionen

Zu den Elementen der Dimension gehören URLs, die Besucher durchklicken, um zu Ihrer Site zu gelangen. If a hit does not have any referrer data, it groups under the dimension item `"Typed/Bookmarked"`. Dieses Dimensionselement bedeutet, dass kein Werber vorhanden ist, z. B. wenn der Besucher die Browseradresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat. Das `"Typed/Bookmarked"` Dimensionselement wird auch bei Umleitungen angezeigt, die nicht für Analytics geeignet sind. Siehe [Weiterleitungen und Aliase](/help/technotes/redirects.md) im Technotes-Benutzerhandbuch.

### Dimensionen, die `googleusercontent.com`

Benutzer können Dimensionselemente mit der Domäne anzeigen `googleusercontent.com`.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls sie offline genommen werden. Diese zwischengespeicherten Seiten stehen neben den meisten Suchergebnissen zur Verfügung, indem Sie auf den Link &quot;Zwischengespeichert&quot;klicken. Wenn ein Benutzer auf diesen Link klickt und den von Google zwischengespeicherten Inhalt Ansicht, `webcache.googleusercontent.com` ist dies ein typisches Dimensionselement.
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Dienst anzeigen, stammt sie von `translate.googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
