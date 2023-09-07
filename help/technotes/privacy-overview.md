---
description: Übersicht der Daten, die Adobe Analytics erfasst, und sonstige Hinweise zum Datenschutz.
keywords: Datenschutz
title: Datenschutzübersicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: 04f8602ccfa7fd2d1d2f3c56f477aeee3739c563
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 3%

---

# Datenschutzübersicht

Adobe möchte Ihr Unternehmen in die Lage versetzen, die geltenden Datenschutzgesetze und -vorschriften einzuhalten. Siehe [Datenschutz in Adobe Experience Cloud](https://www.adobe.com/de/privacy/experience-cloud.html) für weitere Informationen. In Bezug auf Adobe Analytics fungiert Adobe als &quot;Datenverarbeiter&quot;und Sie sind der &quot;Datenverantwortliche&quot;(oder gemäß den geltenden Datenschutz- und Datenschutzgesetzen gleichwertig). Es liegt an Ihrer Organisation, anzugeben, wie Sie ausschließlich Adobe und Dienstleistungen verwenden, da Ihre Organisation steuert, wie Adobe implementiert werden. Ihr Unternehmen ist für die Einhaltung Ihrer eigenen Datenschutzrichtlinien, Ihrer Servicevereinbarung mit Adobe und aller geltenden Gesetze verantwortlich.

Adobe empfiehlt dringend die Einhaltung der folgenden übergreifenden Konzepte:

* **Wenn Sie personenbezogene Daten erfassen, stellen Sie sicher, dass Sie die Datenschutzgesetze und -vorschriften einhalten.** Mit benutzerspezifischen Variablen können Sie praktisch alles erfassen, auf das Sie zugreifen können. Beachten Sie jedoch auch die Datenschutzrichtlinien Ihres Unternehmens und die geltenden Gesetze.
* **Stellen Sie Ihren Kunden leicht auffindbare und leicht verständliche Datenschutzinformationen für Ihr Unternehmen bereit.** Hilfreiche Informationen umfassen Abmelde-Links, die Verwendung der Browser-Daten und die Verwendung bzw. die Planung von Adobe-Diensten.
* **Achten Sie auf lokale und internationale Gesetze, die für Sie gelten.** Wenn Ihr Unternehmen auf globaler Ebene tätig ist, können einige internationale Gesetze gelten.

## Aufschlüsselung der Datenerfassung

Adobe bietet mehrere Datenerfassungsbibliotheken, die den Versand von Daten an Adobe unterstützen. Zu den wichtigen Beispielen gehören:

* **AppMeasurement**: Eine Bibliothek, die dazu bestimmt ist, Daten direkt an Adobe Analytics zu senden.
* **Web SDK**: Eine Bibliothek, die zum Senden von Daten an das Adobe Experience Platform Edge-Netzwerk konzipiert ist und diese Daten dann an Adobe Analytics weiterleitet.
* **Tags**: Eine webbasierte Benutzeroberfläche, mit der Sie Ihre Implementierung konfigurieren können, ohne Zugriff auf den Quellcode einer Website oder App über die ursprüngliche Tag-Implementierung hinaus benötigen zu müssen. Erweiterungen sind sowohl für AppMeasurement als auch für das Web SDK verfügbar.

Adobe Analytics kann die folgenden Datentypen erfassen:

| Datentyp | Details | Beispielvariablen mit diesen Daten |
| --- | --- | --- |
| Seitennamen oder URLs von Webseiten auf Ihrer Site | Wird immer erfasst, damit Adobe Analytics funktioniert. Für jeden Treffer ist eine URL oder ein Seitenname erforderlich. | [Seite](../components/dimensions/page.md), [Seiten-URL](../components/dimensions/page-url.md) |
| Zeitbasierte Daten | Wird immer erfasst, damit Adobe Analytics funktioniert. Für die Datenerfassung ist ein Zeitstempel erforderlich und zeitbasierte Daten werden vom Zeitstempel abgeleitet. | [Besuchszeit pro Seite](../components/dimensions/time-spent-on-page.md), [Stunde des Tages](../components/dimensions/hour-of-day.md), [Vormittag/Nachmittag](../components/dimensions/am-pm.md), [Wochentag/Wochenende](../components/dimensions/weekday-weekend.md), [Wochentag](../components/dimensions/day-of-week.md), [Monat des Jahres](../components/dimensions/month-of-year.md) |
| Daten von Webseiten auf anderen Sites | Adobe kann keine Daten auf nicht verbundenen Sites erfassen, auf denen Sie den Quellcode der Website oder App nicht ändern können. Datenerfassungsbibliotheken erfassen standardmäßig die verweisende URL, wenn ein Besucher auf Ihre Website gelangt. Sie können Ihre Implementierung so anpassen, dass Daten innerhalb von Abfragezeichenfolgen erfasst werden, nachdem Website- oder App-Besucher eintreffen. | [Referrer](../components/dimensions/referrer.md), [Verweisende Domäne](../components/dimensions/referring-domain.md) |
| Anonymisierte Besucher-IDs | Datenerfassungsbibliotheken generieren und referenzieren eine Besucher-ID für jeden Browser, der Ihre Site besucht. Diese ID wird in einem Cookie gespeichert. Wenn eine Datenerfassungsbibliothek keine Cookies aus irgendeinem Grund setzen kann, verwendet die Bibliothek eine Ausweichmethode zur Besucheridentifizierung anhand der IP-Adresse und der Benutzeragenten-Zeichenfolge. Siehe [Adobe Analytics- und Browsercookies](cookies/cookies.md) für weitere Informationen. | [Unique Visitors](../components/metrics/unique-visitors.md) |
| Identifizierbare Besucher-IDs | Adobe erfasst nicht automatisch benutzerdefinierte Besucher-IDs. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| Externe Suchbegriffe | Externe Suchdaten enthalten Suchbegriffe, die von Suchmaschinen stammen. Datenerfassungsbibliotheken suchen nach diesen Daten basierend auf der verweisenden URL. Viele moderne Suchmaschinen enthalten diese Informationen jedoch nicht mehr. | [Suchbegriff](../components/dimensions/search-keyword.md) |
| Interne Suchbegriffe | Interne Suchdaten enthalten Suchbegriffe, die aus den Suchfunktionen Ihrer Website oder App stammen. Adobe erfasst nicht automatisch interne Suchdaten. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. Diese Vorgehensweise wird häufig bei Unternehmen angewandt, die Adobe Analytics verwenden. | [eVar](../components/dimensions/evar.md) |
| Computer- und Browserspezifikationen | AppMeasurement sammelt automatisch Hinweise zu wenig entropy-Browsern wie Browser-Typ und Betriebssystemtyp und ob es sich bei dem Gerät um ein Desktop- oder Mobilgerät handelt. Eine benutzerdefinierte Konfiguration ist erforderlich, um Hinweise zur hohen Entropie zu sammeln, z. B. die spezifische Version/Build des Browsers, das Gerätemodell oder die Betriebssystemversion. Siehe [Übersicht über Client-Hinweise](client-hints.md) für weitere Informationen. | [Browser](../components/dimensions/browser.md), [Betriebssystem](../components/dimensions/operating-systems.md), [Mobilgerätedimensionen](../components/dimensions/mobile-dimensions.md), [Bildschirmauflösung](../components/dimensions/monitor-resolution.md) |
| Geolocation-Informationen | Adobe bietet die Möglichkeit, die Erfassung von Geolocation-Daten für jede Website oder App zu aktivieren oder zu deaktivieren (auf Report Suite-Ebene). Die Erfassung von Geolocation-Daten ist standardmäßig aktiviert. Datenerfassungsbibliotheken beinhalten die Geolocation, wenn sie aktiviert ist. | [Städte](../components/dimensions/cities.md), [Regionen](../components/dimensions/regions.md), [Länder](../components/dimensions/countries.md) |
| IP-Adresse | Adobe bietet die Möglichkeit, beim Speichern dieser Daten das letzte Oktett zu verschleiern oder die IP-Adresse des Besuchers vollständig zu verschleiern. EMEA-Kunden haben in der Regel die Einstellung der IP-Adresse standardmäßig vollständig verschleiert. Unabhängig von der Verschleierungseinstellung ist die IP-Adresse nicht als Dimension in Adobe Analytics verfügbar. Sie ist nur in [Datenfeeds](../export/analytics-data-feed/data-feed-overview.md). | Keine |
| Formulardaten auf Ihrer Site | Alle Implementierungstypen müssen konfiguriert werden, um diese Daten zu erfassen. Sie können diese Daten in benutzerdefinierte Variablen einfügen. | [eVar](../components/dimensions/evar.md) |
| Klicken Sie auf Anzeigen oder Links auf Ihrer Site | Wird standardmäßig bei Verwendung einer Datenerfassungsbibliothek erfasst. Zusätzliche Informationen, wie der Ort der Klicks, sind verfügbar, wenn Sie Activity Map aktivieren. | [Activity Map](../analyze/activity-map/activity-map.md), [Exitlink](../components/dimensions/exit-link.md), [Downloadlink](../components/dimensions/download-link.md) |
| Auf Ihrer Site gekaufte Produkte | Alle Implementierungstypen müssen konfiguriert werden, um diese Daten zu erfassen. Adobe bietet mehrere Standardvariablen, um diese Informationen zu sammeln. | [Produkt](../components/dimensions/product.md), [Bestellungen](../components/metrics/orders.md), [Umsatz](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Siehe Navigationsmenü unter [Übersicht über Dimensionen](../components/dimensions/overview.md) und [Übersicht über Metriken](../components/metrics/overview.md) für weitere Variablen, unter denen Adobe möglicherweise Daten erfassen kann.

## Datenverarbeitungsstandorte

Adobe verwaltet drei Datenverarbeitungsorte für Adobe Analytics. Diese Sites empfangen Rohdaten und verarbeiten sie in einer Report Suite, die für Datenspeicherung und Berichtsabruf optimiert ist. Diese Datenverarbeitungsspeicherorte befinden sich in **Oregon**, **London**, und **Singapur**. Siehe [Sicherheitsübersicht für Adobe Analytics](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf) für weitere Informationen.
