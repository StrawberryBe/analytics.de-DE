---
title: Datenerfassungs-Abfrageparameter
description: Listet alle in Bildanforderungen verwendeten Abfragezeichenfolgenparameter auf.
exl-id: 2eb2ade7-a3db-4b00-8a70-2632d1c0aaaf
source-git-commit: 7025d132da9d281da6d57973a195a5e86a39bf18
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 94%

---

# Datenerfassungs-Abfrageparameter

In der folgenden Tabelle sind alle Abfragezeichenfolgenparameter aufgeführt, die Adobe in Bildanforderungen verwendet. Diese Informationen können beim Debugging mit [Paket-Analyzern](packet-monitor.md), beim [festen Programmieren von Bildanforderungen](../other/hardcoded.md) oder bei der Verwendung [dynamischer Variablen](../vars/page-vars/dynamic-variables.md) genutzt werden.

| Parameter | Analytics-Implementierungsvariable | Beschreibung |
| --- | --- | --- |
| `aamlh` | Keine | Audience Manager-Standorthinweis. Wird in der Experience Cloud Shared Profile-Integration verwendet. |
| `aamb` | Keine | Audience Manager-Blob. Wird in der Experience Cloud Shared Profile-Integration verwendet. |
| `aid` | Keine | Analytics-Besucher-ID. |
| `AQB` | Keine | Zeigt den Anfang einer Abfragezeichenfolge für Bildanforderungen an. |
| `AQE` | Keine | Zeigt das Ende einer Bildanforderung an (d. h., dass die Anforderung nicht abgeschnitten wurde). |
| `bh` | Keine | Browser-Höhe (in Pixel). Wird in der Dimension [Browser-Höhe](/help/components/dimensions/browser-height.md) verwendet. |
| `bw` | Keine | Browser-Breite (in Pixel). Wird in der Dimension [Browser-Breite](/help/components/dimensions/browser-width.md) verwendet. |
| `c` | Keine | Farbqualität (in Bit). Wird in der Dimension [Farbtiefe](/help/components/dimensions/color-depth.md) verwendet. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | Zeigt den Start von Kontextdatenvariablen an. Enthält nie einen Wert. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | Zeigt das Ende der Kontextdatenvariablen an. Enthält nie einen Wert. |
| `c1` – `c75` | [`prop1` – `prop75`](../vars/page-vars/prop.md) | [Props](/help/components/dimensions/prop.md) oder benutzerspezifische Traffic-Variablen. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | Die im Treffer verwendete Währung. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | Die Anzahl der Punkte in einer Domäne. Dient zum korrekten Speichern von Cookies. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | Die Zeichencodierung der Bildanforderung. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | Die Lebensdauer des Besucher-Cookies. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Wird in der Dimension [Website-Bereiche](/help/components/dimensions/site-section.md) verwendet. |
| `cp` | Keine | Wird in der Dimension [Treffertyp](/help/components/dimensions/hit-type.md) verwendet. |
| `ct` | Keine | Wird in der Dimension [Verbindungstyp](/help/components/dimensions/connection-type.md) verwendet. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | Gibt an, was für dynamische Variablen verwendet werden soll. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | Abkürzung für die `events`-Abfragezeichenfolge. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | Durch Komma getrennte Liste der Ereignisse auf der Seite. Wird von den meisten [Metriken](/help/components/metrics/overview.md) verwendet. |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | Die aktuelle URL der Seite mit bis zu 255 Byte. Wird in der Dimension [Seiten-URL](/help/components/dimensions/page-url.md) verwendet. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | URLs, die länger als 255 Byte sind, werden geteilt. Die ersten 255 Byte werden im `g`-Parameter und alle verbleibenden Byte im `-g`-Parameter angezeigt. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | Abkürzung für die `pageName`-Abfragezeichenfolge. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | Abkürzung für die `pageType`-Abfragezeichenfolge. |
| `h1` – `h5` | [`hier1` – `hier5`](../vars/page-vars/hier.md) | Hierarchiedimensionen. |
| `hp` | Keine | Wird nicht mehr verwendet. Legte in früheren Versionen von Adobe Analytics fest, ob die aktuelle URL die Homepage des Browsers war. |
| `j` | Keine | Die im Browser installierte JavaScript-Version. |
| `k` | Keine | Wird in der Dimension [Cookie-Unterstützung](/help/components/dimensions/cookie-support.md) verwendet. |
| `l1` – `l3` | [`list1` – `list3`](../vars/page-vars/list.md) | Listenvariablen. |
| `lrt` | Keine | Die &quot;letzte Anforderungszeitangabe&quot;, d. h. die Roundtrip-Zeit für die letzte Anforderung, in Millisekunden. Sie wird nur gesendet, wenn mehr als eine Anforderung von einer Seite gesendet wird oder wenn es sich bei der Seite um eine Einzelseitenanwendung handelt (SPA). |
| `mid` | Keine | Experience Cloud-Besucher-ID. |
| `ndh` | Keine | Markierung, die angibt, ob die Bildanforderung von AppMeasurement stammt. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | Hilft festzustellen, wo Cookies gesetzt werden. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | Objekt-Kennung für die letzte Seite. Wird in Activity Map verwendet. |
| `ot` | Keine | Objektname für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `p` | Keine | Wird nicht mehr verwendet. Liste der im Browser verwendeten Plug-ins. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Wird in der Dimension [Seite](/help/components/dimensions/page.md) verwendet. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Wird in der Dimension [Seiten nicht gefunden](/help/components/dimensions/pages-not-found.md) verwendet. |
| `pccr` | Keine | Nur für neue Besucher und immer auf `true` gesetzt. Hilft, endlose Umleitungen zu verhindern. |
| `pe` | [`tl()`](../vars/functions/tl-method.md) | Bestimmt den Typ des benutzerspezifischen Links. Für [benutzerspezifische Links](/help/components/dimensions/custom-link.md), [Downloadlinks](/help/components/dimensions/download-link.md) und [Exitlinks](/help/components/dimensions/exit-link.md) erforderlich. |
| `pev1` | Keine | Die URL, unter der der benutzerdefinierte Link aufgetreten ist. |
| `pev2` | [`tl()`](../vars/functions/tl-method.md) | Anzeigename des benutzerspezifischen Links. |
| `pev3` | Keine | Wird nicht mehr verwendet. Verfolgte Meilensteine in früheren Versionen der Videoberichte. |
| `pf` | Keine | Plattformmarkierung; nur zur Verwendung durch Adobe. Nicht ändern. |
| `pid` | Keine | Seiten-Kennung für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pidt` | Keine | Seiten-Kennungstyp für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pl` | [`products`](../vars/page-vars/products.md) | Abkürzung für die `products`-Abfragezeichenfolge. |
| `products` | [`products`](../vars/page-vars/products.md) | Variable „products“ (Produktvariable). Wird in den Dimensionen [Produkt](/help/components/dimensions/product.md) und [Kategorie](/help/components/dimensions/category.md) verwendet. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | Dient zum Deduplizieren von Käufen. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | Referrer-URL des Treffers. Wird in Traffic-Quellendimensionen wie [Referrer](/help/components/dimensions/referrer.md) und [Referrer-Domäne](/help/components/dimensions/referring-domain.md) verwendet. |
| `s` | Keine | Bildschirmauflösung in `width x height`. Wird in der Dimension [Bildschirmauflösungen](/help/components/dimensions/monitor-resolution.md) verwendet. |
| `server` | [`server`](../vars/page-vars/server.md) | Dimension [Server](/help/components/dimensions/server.md). |
| `sv` | [`server`](../vars/page-vars/server.md) | Abkürzung für die `server`-Abfragezeichenfolge. |
| `state` | [`state`](../vars/page-vars/state.md) | Dimension „Status“. |
| `t` | Keine | Generiertes Datum/Uhrzeit des Treffers. Verwendet das Format `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` ist Datum/Uhrzeit in JavaScript. Monat `0` ist der Januar, Monat `11` der Dezember.<br>- `w` ist der Wochentag. `0` ist Sonntag und `6` Samstag.<br>- `o` ist der negative GMT-Versatz in Minuten. Zum Beispiel ist `420` GMT-7. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | Der benutzerdefinierte Zeitstempel, der mit dem Treffer festgelegt wird. Wird normalerweise für das Offline-Tracking verwendet. |
| `v` | Keine | Wird in der Dimension [Java aktiviert](/help/components/dimensions/java-enabled.md) verwendet. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | Dimension [Trackingcode](/help/components/dimensions/tracking-code.md). |
| `v1` – `v250` | [`evar1` – `eVar250`](../vars/page-vars/evar.md) | [eVars](/help/components/dimensions/evar.md) oder benutzerspezifische Konversionsdimensionen. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | Besucher-ID-Variable. |
| `vmk` | `vmk` | Wird nicht mehr verwendet. Migrationsschlüssel für Besucher, mit dem Implementierungen von Drittanbieter-Cookies zu Erstanbieter-Cookies migriert wurden. |
| `vvp` | `variableProvider` | Wird in Data Connectors verwendet. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | Wird mit Data Sources verwendet, um Online- und Offline-Daten miteinander zu verbinden. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Wird in der Dimension [Postleitzahl](/help/components/dimensions/zip-code.md) verwendet. |
