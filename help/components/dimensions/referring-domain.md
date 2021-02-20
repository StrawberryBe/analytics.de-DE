---
title: Referrer-Domäne
description: Die übergeordnete Domäne, auf der sich ein Besucher befand, bevor er zu Ihrer Site klickte.
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 100%

---


# Referrer-Domäne

Die Dimension „Referrer-Domäne“ gibt an, von welchen Domänen Besucher klicken, um zu Ihrer Site zu gelangen. Diese Dimension ist nützlich, um zu verstehen, welche Websites von Drittanbietern den meisten Traffic zu Ihrer Site leiten. Auf der externen Site muss ein Link vorhanden sein und ein Besucher muss darauf klicken, damit das Dimensionselement angezeigt wird.

>[!IMPORTANT]
>
>Sie müssen die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren, um diese Dimension verwenden zu können. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

Derselbe Bericht kann zwischen Analysis Workspace und Data Warehouse unterschiedliche Ergebnisse anzeigen. Analysis Workspace meldet die Referrer-Domäne für jede einzelne Seite, ausgenommen Werte, die mit internen URL-Filtern übereinstimmen. Data Warehouse meldet nur die erste Referrer-Domäne des Besuchs und ignoriert interne URL-Filter.

## Füllen dieser Dimension mit Daten

Diese Dimension erfordert die Konfiguration auf der Analytics-Benutzeroberfläche und Daten in Bildanforderungen.

* Innerhalb Ihrer Implementierung ruft diese Dimension Daten aus der [`r` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten mithilfe der JavaScript-Variablen `document.referrer` im Browser. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `r` bei allen Bildanforderungen einbeziehen.
* Auf der Analytics-Benutzeroberfläche müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md) Ihrer Report Suite konfigurieren. Wenn die internen URL-Filter nicht konfiguriert werden, können entweder interne Domänen enthalten sein oder die Anzeige externer Domänen verhindert werden.

Adobe behält die Referrer-Domäne für einen Besuch bei. Wenn ein Besucher innerhalb eines einzelnen Besuchs Ihre Site verlässt und auf einer anderen Domäne erneut auf einen Link zu Ihnen klickt, wird der neue Wert aktualisiert und bleibt für den Rest des Besuchs erhalten. Wenn Sie nur den ursprünglichen Wert anzeigen möchten, finden Sie weitere Informationen unter [Ursprüngliche Referrer-Domäne](original-referring-domain.md).

## Dimensionselemente

Zu den Dimensionselementen gehören die Domänen, durch die Besucher zu Ihrer Site klicken. Wenn ein Treffer keine Referrer-Daten (entweder gesetzt oder beibehalten) enthält, wird er unter dem Dimensionselement `"Typed/Bookmarked"` gruppiert. Dieses Dimensionselement bedeutet, dass kein Referrer-Wert vorhanden ist, z. B. wenn der Besucher die Browser-Adresse manuell in die Adressleiste eingegeben oder auf ein Lesezeichen geklickt hat. Das Dimensionselement `"Typed/Bookmarked"` wird auch bei Umleitungen angezeigt, die nicht für Analytics geeignet sind. Weitere Informationen finden Sie unter [Umleitungen und Aliase](/help/technotes/redirects.md) im Technotes-Benutzerhandbuch.

### Dimensionselemente, die `googleusercontent.com` enthalten

Benutzer können Dimensionselemente mit der Domäne `googleusercontent.com` anzeigen.

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Kopien von Seiten, falls diese offline geschaltet werden. Diese zwischengespeicherten Seiten sind neben den meisten Suchergebnissen verfügbar, indem Sie auf den Link „Zwischengespeichert“ klicken. Wenn ein Nutzer auf diesen Link klickt und den von Google zwischengespeicherten Inhalt anzeigt, ist `googleusercontent.com` das Dimensionselement.
* **Übersetzte Seiten**: Google bietet einen robusten und bequemen Übersetzungsdienst. Wenn Sie eine Site mit diesem Dienst anzeigen, stammt sie von `googleusercontent.com`. Dieses Dimensionselement wird angezeigt, wenn der Benutzer auf einen Link klickt, um zum ursprünglichen Inhalt zurückzukehren.
