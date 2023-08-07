---
description: Übersicht der Daten, die Adobe Analytics erfasst, und sonstige Hinweise zum Datenschutz.
keywords: Datenschutz
title: Datenschutzübersicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: ee0bf5beeac3c9780eb0c8420845114f7e840aec
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 12%

---

# Datenschutzübersicht

Besucher können mehr darüber erfahren, wie Adobe die im [Adobe-Datenschutzzentrum](https://www.adobe.com/de/privacy.html) erfassten Informationen im Allgemeinen verwendet. Es ist Sache Ihres Unternehmens, ob Sie offenlegen möchten, wie Sie die Adobe-Produkte und -Dienste verwenden. Denn nur Ihre Organisation hat die Kontrolle darüber, wie die Adobe-Dienste implementiert werden. Ihr Unternehmen ist für die Einhaltung Ihrer eigenen Datenschutzrichtlinien, Ihrer Servicevereinbarung mit Adobe und aller geltenden Gesetze verantwortlich.

Adobe empfiehlt dringend die Einhaltung der folgenden übergreifenden Konzepte:

* **Vermeiden Sie das Sammeln von persönlich identifizierbaren Informationen in Adobe Analytics.** Mit benutzerspezifischen Variablen können Sie praktisch alles erfassen, auf das Sie zugreifen können. Beachten Sie jedoch auch die Datenschutzrichtlinien Ihres Unternehmens und die geltenden Gesetze.
* **Bieten Sie Besuchern leicht auffindbare und leicht verständliche Informationen über Opt-out-Informationen.** Erlauben Sie ihnen, alles zu deaktivieren, was nicht unbedingt erforderlich ist. Die meisten Länder der europäischen Union erachten Analyse-Cookies nicht als unbedingt erforderlich.

## Aufschlüsselung der Datenerfassung

Adobe Analytics erfasst entweder automatisch die folgenden Datentypen oder kann diese möglicherweise erfassen:

| Datentyp | Details | Beispielvariablen mit diesen Daten |
| --- | --- | --- |
| Seitennamen oder URLs von Webseiten auf Ihrer Site | Immer erfasst. Für jeden Treffer ist eine URL oder ein Seitenname erforderlich. | [Seite](../components/dimensions/page.md), [Seiten-URL](../components/dimensions/page-url.md) |
| Zeitbasierte Daten | Immer erfasst. Für die Datenerfassung ist ein Zeitstempel erforderlich und zeitbasierte Daten werden vom Zeitstempel abgeleitet. | [Besuchszeit pro Seite](../components/dimensions/time-spent-on-page.md), [Stunde des Tages](../components/dimensions/hour-of-day.md), [Vormittag/Nachmittag](../components/dimensions/am-pm.md), [Wochentag/Wochenende](../components/dimensions/weekday-weekend.md), [Wochentag](../components/dimensions/day-of-week.md), [Monat des Jahres](../components/dimensions/month-of-year.md) |
| Daten von Webseiten auf anderen Sites | Adobe kann keine Daten auf nicht verbundenen Sites erfassen, auf denen Sie den Quellcode der Website nicht ändern können. AppMeasurement erfasst automatisch die verweisende URL, wenn ein Besucher auf Ihre Website gelangt. Sie können Ihre Implementierung so anpassen, dass Daten in Abfragezeichenfolgen erfasst werden, nachdem sie auf Ihre Site gelangt sind. | [Referrer](../components/dimensions/referrer.md), [Verweisende Domäne](../components/dimensions/referring-domain.md) |
| Anonymisierte Besucher-IDs | AppMeasurement generiert automatisch eine Besucher-ID und referenziert sie für jeden Browser, der Ihre Site besucht. Diese ID wird in einem Cookie gespeichert. Wenn für eine bestimmte Implementierung keine Cookies verfügbar sind, verwendet Adobe Analytics eine Ausweichmethode zur Besucheridentifizierung mit IP-Adresse und Benutzeragenten-Zeichenfolge. Siehe [Adobe Analytics- und Browsercookies](cookies/cookies.md) für weitere Informationen. | [Unique Visitors](../components/metrics/unique-visitors.md) |
| Identifizierbare Besucher-IDs | Adobe erfasst nicht automatisch benutzerdefinierte Besucher-IDs. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| Externe Suchbegriffe | AppMeasurement versucht, diese Daten automatisch anhand der verweisenden URL zu erfassen. Viele moderne Suchmaschinen enthalten diese Informationen jedoch nicht mehr. | [Suchbegriff](../components/dimensions/search-keyword.md) |
| Interne Suchbegriffe | Adobe erfasst nicht automatisch interne Suchdaten. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. Dies ist eine gängige Praxis für Unternehmen, die Adobe Analytics verwenden. | [eVar](../components/dimensions/evar.md) |
| Computer- und Browserspezifikationen | AppMeasurement sammelt automatisch Hinweise zu wenig entropy-Browsern wie Browser-Typ und Betriebssystemtyp und ob es sich bei dem Gerät um ein Desktop- oder Mobilgerät handelt. Es ist eine Konfiguration erforderlich, um Hinweise zur hohen Entropie zu sammeln, z. B. die spezifische Version/Build des Browsers, das Gerätemodell oder die Betriebssystemversion. Siehe [Übersicht über Client-Hinweise](client-hints.md) für weitere Informationen. | [Browser](../components/dimensions/browser.md), [Betriebssystem](../components/dimensions/operating-systems.md), [Mobilgerätedimensionen](../components/dimensions/mobile-dimensions.md), [Bildschirmauflösung](../components/dimensions/monitor-resolution.md) |
| Geolocation-Informationen | Adobe bietet die Möglichkeit, die Erfassung von Geolocation-Daten für jede Website oder App zu aktivieren oder zu deaktivieren (auf Report Suite-Ebene). Viele Implementierungstypen, einschließlich AppMeasurement, erfassen diese Daten automatisch. | [Städte](../components/dimensions/cities.md), [Regionen](../components/dimensions/regions.md), [Länder](../components/dimensions/countries.md) |
| IP-Adresse | Adobe bietet die Möglichkeit, beim Speichern dieser Daten das letzte Oktett zu verdecken oder die IP-Adresse des Besuchers vollständig zu verschleiern. EMEA-Kunden haben in der Regel eine vollständig verschleierte IP-Adresse. IP-Adresse ist nicht als Dimension in Adobe Analytics verfügbar. Sie ist nur in den Rohdaten enthalten ([Datenfeeds](../export/analytics-data-feed/data-feed-overview.md)). | Keine |
| Formulardaten auf Ihrer Site | Alle Implementierungstypen müssen konfiguriert werden, um diese Daten zu erfassen. Sie können diese Daten in benutzerdefinierte Variablen einfügen. | [eVar](../components/dimensions/evar.md) |
| Anzeigen oder Links, auf die auf Ihrer Site geklickt wurde | Wird bei Verwendung von AppMeasurement automatisch erfasst. Zusätzliche Informationen, wie der Speicherort von Klicks, sind bei aktiviertem Activity Map verfügbar. | [Activity Map](../analyze/activity-map/activity-map.md), [Exitlink](../components/dimensions/exit-link.md), [Downloadlink](../components/dimensions/download-link.md) |
| Auf Ihrer Site gekaufte Produkte | Alle Implementierungstypen müssen konfiguriert werden, um diese Daten zu erfassen. Adobe bietet mehrere Standardvariablen zum Speichern dieser Informationen. | [Produkt](../components/dimensions/product.md), [Bestellungen](../components/metrics/orders.md), [Umsatz](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Siehe Navigationsmenü unter [Übersicht über Dimensionen](../components/dimensions/overview.md) und [Übersicht über Metriken](../components/metrics/overview.md) für weitere Variablen, unter denen Adobe möglicherweise Daten erfassen kann.
