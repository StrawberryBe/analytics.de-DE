---
title: Referrer
description: Die URL, auf der sich ein Besucher befand, bevor er zu Ihrer Site durchklickte.
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 97%

---


# Werber

Die Dimension „Referrer“ gibt an, auf welchen URLs sich die Besucher befanden, als sie sich zu Ihrer Site durchklickten. Diese Dimension ist nützlich, um zu verstehen, welche spezifischen URLs den meisten Traffic zu Ihrer Site leiten. Auf der externen URL muss ein Link vorhanden sein, und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne URLs enthalten sein oder die Anzeige externer URLs verhindert werden.

Derselbe Bericht kann zwischen Analysis Workspace und Data Warehouse unterschiedliche Ergebnisse anzeigen. Analysis Workspace meldet den Referrer für jede einzelne Seite, ausgenommen Werte, die mit internen URL-Filtern übereinstimmen. Data Warehouse meldet nur den ersten Referrer des Besuchs und ignoriert interne URL-Filter.

## Füllen dieser Dimension mit Daten

Diese Dimension erfordert die Konfiguration auf der Analytics-Benutzeroberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Sie können die Variablenüberschreibungen [`referrer`](/help/implement/vars/page-vars/referrer.md) verwenden, um sie manuell festzulegen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `r` bei allen Bildanforderungen einbeziehen.
* Auf der Analytics-Benutzeroberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne URLs enthalten sein oder die Anzeige externer URLs verhindert werden.

## Dimensionselemente

Zu den Dimensionselementen gehören die URLs, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten enthält, wird er unter dem Dimensionselement `"Typed/Bookmarked"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat. Das Dimensionselement `"Typed/Bookmarked"` wird auch bei Umleitungen angezeigt, die nicht für Analytics geeignet sind. Weitere Informationen finden Sie unter [Umleitungen und Aliase](/help/technotes/redirects.md) im Technotes-Benutzerhandbuch.

### Dimensionselemente, die `googleusercontent.com` enthalten

Benutzer können Dimensionselemente mit der Domäne `googleusercontent.com` anzeigen.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls diese offline geschaltet werden. Diese zwischengespeicherten Seiten sind neben den meisten Suchergebnissen verfügbar, indem Sie auf den Link „Zwischengespeichert“ klicken. Wenn ein Nutzer auf diesen Link klickt und den von Google zwischengespeicherten Inhalt anzeigt, ist `webcache.googleusercontent.com` ein typisches Dimensionselement.
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Dienst anzeigen, stammt sie von `translate.googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
