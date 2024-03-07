---
description: Übersicht der Daten, die Adobe Analytics erfasst, und sonstige Hinweise zum Datenschutz.
keywords: Datenschutz
title: Datenschutzübersicht
feature: Privacy
exl-id: 71c83106-a047-47d7-9a70-4a24595e3d0a
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 3%

---

# Datenschutzübersicht

Adobe möchte Ihr Unternehmen in die Lage versetzen, die geltenden Gesetze und Vorschriften einzuhalten. Siehe [Datenschutz in Adobe Experience Cloud](https://www.adobe.com/de/privacy/experience-cloud.html){target=_blank} für weitere Informationen. Zwischen Adobe Analytics und Ihrem Unternehmen fungiert Adobe als &quot;Datenverarbeiter&quot;und Sie sind der &quot;Datenverantwortliche&quot;(oder entsprechend den geltenden Datenschutz- und Datenschutzgesetzen). Es liegt an Ihrer Organisation, anzugeben, wie Sie ausschließlich Adobe und Dienstleistungen verwenden, da Ihre Organisation steuert, wie Adobe implementiert werden. Bei der Verwendung von Adobe Analytics ist Ihr Unternehmen für die Einhaltung Ihrer eigenen Datenschutzrichtlinien, Ihrer Servicevereinbarung mit Adobe und aller geltenden Gesetze verantwortlich.

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
| Seitennamen oder URLs von Webseiten auf Ihrer Site | Diese Daten sind erforderlich, damit Adobe Analytics funktioniert. Für jeden Treffer ist eine URL oder ein Seitenname erforderlich. | [Seite](../components/dimensions/page.md), [Seiten-URL](../components/dimensions/page-url.md) |
| Zeitbasierte Daten | Diese Daten sind erforderlich, damit Adobe Analytics funktioniert. Für die Datenerfassung ist ein Zeitstempel erforderlich und zeitbasierte Daten werden vom Zeitstempel abgeleitet. | [Besuchszeit pro Seite](../components/dimensions/time-spent-on-page.md), [Stunde des Tages](../components/dimensions/hour-of-day.md), [Vormittag/Nachmittag](../components/dimensions/am-pm.md), [Wochentag/Wochenende](../components/dimensions/weekday-weekend.md), [Wochentag](../components/dimensions/day-of-week.md), [Monat des Jahres](../components/dimensions/month-of-year.md) |
| Referrer-Daten | Datenerfassungsbibliotheken erfassen standardmäßig die verweisende URL, wenn ein Besucher auf Ihre Website gelangt. Sie können Ihre Implementierung anpassen, um Daten in der Abfragezeichenfolge eines Referrers zu erfassen. Diese Vorgehensweise wird häufig bei Kampagnen und der Verfolgung der Anzeigenleistung angewandt. | [Referrer](../components/dimensions/referrer.md), [Verweisende Domäne](../components/dimensions/referring-domain.md) |
| Anonymisierte Besucher-IDs | Datenerfassungsbibliotheken generieren und referenzieren eine Besucher-ID für jeden Browser, der Ihre Site besucht. Diese ID wird in einem Cookie gespeichert. Wenn eine Datenerfassungsbibliothek keine Cookie-ID festlegen kann, verwendet die Bibliothek eine Ausweichmethode zur anonymen Besucheridentifizierung. Bei dieser Methode werden zugehörige Treffer mit demselben Besuch verknüpft, indem die IP-Adresse des Besuchers und die Benutzeragenten-Zeichenfolge verwendet werden. Wenn für Ihr Unternehmen die IP-Verschleierung aktiviert ist, wird diese Einstellung berücksichtigt. Siehe [Adobe Analytics- und Browsercookies](cookies/cookies.md) für weitere Informationen. | [Unique Visitors](../components/metrics/unique-visitors.md) |
| Identifizierbare Besucher-IDs | Adobe erfasst nicht automatisch benutzerdefinierte Besucher-IDs. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. | [`visitorID`](../implement/vars/config-vars/visitorid.md) |
| Externe Suchbegriffe | Externe Suchdaten enthalten Suchbegriffe, die von Suchmaschinen stammen. Datenerfassungsbibliotheken suchen nach diesen Daten basierend auf der verweisenden URL. Viele moderne Suchmaschinen enthalten diese Informationen jedoch nicht mehr. | [Suchbegriff](../components/dimensions/search-keyword.md) |
| Interne Suchbegriffe | Interne Suchdaten enthalten Suchbegriffe, die aus den Suchfunktionen Ihrer Website oder App stammen. Adobe erfasst nicht automatisch interne Suchdaten. Sie können Ihre Implementierung jedoch anpassen, um diese Daten zu erfassen. Diese Vorgehensweise wird häufig bei Unternehmen angewandt, die Adobe Analytics verwenden. | [eVar](../components/dimensions/evar.md) |
| Computer- und Browserspezifikationen | Datenerfassungsbibliotheken erfassen automatisch Browser-Hinweise mit geringer Entropie, z. B. den Browsertyp und den Betriebssystemtyp, und ob es sich bei dem Gerät um ein Desktop- oder ein Mobilgerät handelt. Eine benutzerdefinierte Konfiguration ist erforderlich, um Hinweise zur hohen Entropie zu sammeln, z. B. die spezifische Version/Build des Browsers, das Gerätemodell oder die Betriebssystemversion. Siehe [Übersicht über Client-Hinweise](client-hints.md) für weitere Informationen. | [Browser](../components/dimensions/browser.md), [Betriebssystem](../components/dimensions/operating-systems.md), [Mobilgerätedimensionen](../components/dimensions/mobile-dimensions.md), [Bildschirmauflösung](../components/dimensions/monitor-resolution.md) |
| Geolocation-Informationen | Adobe bietet die Möglichkeit, eine detaillierte geografische Position zu verhindern, indem das letzte Oktett einer IP-Adresse auf 0 gesetzt wird. Dadurch werden Geo-Informationen weniger präzise und können in [Report Suite-Einstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/general-acct-settings-admin.html?lang=de). | [Städte](../components/dimensions/cities.md), [Regionen](../components/dimensions/regions.md), [Länder](../components/dimensions/countries.md) |
| IP-Adresse | Adobe bietet die Möglichkeit, die IP-Adresse des Besuchers beim Speichern dieser Daten zu verschleiern (Hash) oder vollständig zu entfernen. EMEA-Kunden haben in der Regel die Einstellung der IP-Adresse standardmäßig verschleiert. Unabhängig von der Verschleierungseinstellung ist die IP-Adresse nicht als Dimension in Analysis Workspace verfügbar. Sie ist nur in [Datenfeeds](../export/analytics-data-feed/data-feed-overview.md). Siehe [Allgemeine Kontoeinstellungen](../admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md) im Admin-Handbuch finden Sie Details zu den verfügbaren Verschleierungseinstellungen. | Keine |
| Formulardaten auf Ihrer Site | Alle Implementierungstypen müssen konfiguriert werden, um diese Daten zu erfassen. Sie können diese Daten in benutzerdefinierte Variablen einfügen. | [eVar](../components/dimensions/evar.md) |
| Klicken Sie auf Anzeigen oder Links auf Ihrer Site | Wird erfasst, wenn [`trackExternalLinks`](../implement/vars/config-vars/trackexternallinks.md) oder [`trackDownloadLinks`](../implement/vars/config-vars/trackdownloadlinks.md) aktiviert ist. Zusätzliche Informationen, wie der Ort der Klicks, sind verfügbar, wenn Sie Activity Map aktivieren. | [Activity Map](../analyze/activity-map/activity-map.md), [Exitlink](../components/dimensions/exit-link.md), [Downloadlink](../components/dimensions/download-link.md) |
| Auf Ihrer Site gekaufte Produkte | Alle Implementierungstypen müssen konfiguriert werden, um diese Daten zu erfassen. Adobe bietet mehrere Standardvariablen, um diese Informationen zu sammeln. | [Produkt](../components/dimensions/product.md), [Bestellungen](../components/metrics/orders.md), [Umsatz](../components/metrics/revenue.md) |

{style="table-layout:auto"}

Siehe Navigationsmenü unter [Übersicht über Dimensionen](../components/dimensions/overview.md) und [Übersicht über Metriken](../components/metrics/overview.md) für weitere Variablen, unter denen Adobe möglicherweise Daten erfassen kann.

## Datenverarbeitungsstandorte

Adobe verwaltet drei Datenverarbeitungsorte für Adobe Analytics. Diese Sites empfangen Rohdaten und verarbeiten sie in einer Report Suite, die für Datenspeicherung und Berichtsabruf optimiert ist. Diese Datenverarbeitungsstandorte befinden sich derzeit in den USA (Oregon), Großbritannien (London) und Singapur. Siehe [Sicherheitsübersicht für Adobe Analytics](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adb-analytics-security-wp.pdf){target=_blank} für weitere Informationen.
