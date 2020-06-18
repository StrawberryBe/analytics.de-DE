---
title: Datenerfassungs-Abfrageparameter
description: Listet alle in Bildanforderungen verwendeten Abfragezeichenfolgenparameter auf.
translation-type: tm+mt
source-git-commit: edf3ac3ebc99444b86bcd9239cef9ed84d797565
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 75%

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
| `bh` | Keine | Browser-Höhe (in Pixel). Used in the [Browser height](/help/components/dimensions/browser-height.md) dimension. |
| `bw` | Keine | Browser-Breite (in Pixel). Used in the [Browser width](/help/components/dimensions/browser-width.md) dimension. |
| `c` | Keine | Farbqualität (in Bit). Used in the [Color depth](/help/components/dimensions/color-depth.md) dimension. |
| `c.` | [`contextData`](../vars/page-vars/contextdata.md) | Zeigt den Start von Kontextdatenvariablen an. Enthält nie einen Wert. |
| `.c` | [`contextData`](../vars/page-vars/contextdata.md) | Zeigt das Ende der Kontextdatenvariablen an. Enthält nie einen Wert. |
| `c1` – `c75` | [`prop1` – `prop75`](../vars/page-vars/prop.md) | [Eigenschaften](/help/components/dimensions/prop.md)oder benutzerdefinierte Traffic-Variablen. |
| `cc` | [`currencyCode`](../vars/config-vars/currencycode.md) | Die im Treffer verwendete Währung. |
| `cdp` | [`cookieDomainPeriods`](../vars/config-vars/cookiedomainperiods.md) | Die Anzahl der Punkte in einer Domäne. Dient zum korrekten Speichern von Cookies. |
| `ce` | [`charSet`](../vars/config-vars/charset.md) | Die Zeichencodierung der Bildanforderung. |
| `cl` | [`cookieLifetime`](../vars/config-vars/cookielifetime.md) | Die Lebensdauer des Besucher-Cookies. |
| `ch` | [`channel`](../vars/page-vars/channel.md) | Used in the [Site sections](/help/components/dimensions/site-section.md) dimension. |
| `cp` | Keine | Used in the [Hit Type](/help/components/dimensions/hit-type.md) dimension. |
| `ct` | Keine | Used in the [Connection Type](/help/components/dimensions/connection-type.md) dimension. |
| `D` | [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) | Gibt an, was für dynamische Variablen verwendet werden soll. |
| `ev` | [`events`](../vars/page-vars/events/events-overview.md) | Abkürzung für die `events`-Abfragezeichenfolge. |
| `events` | [`events`](../vars/page-vars/events/events-overview.md) | Durch Komma getrennte Liste der Ereignisse auf der Seite. Wird von den meisten [Metriken](/help/components/metrics/overview.md)verwendet. |
| `g` | [`pageURL`](../vars/page-vars/pageurl.md) | Die aktuelle URL der Seite mit bis zu 255 Byte. Used in the [Page URL](/help/components/dimensions/page-url.md) dimension. |
| `-g` | [`pageURL`](../../components/dimensions/page-url.md) | URLs, die länger als 255 Byte sind, werden geteilt. Die ersten 255 Byte werden im `g`-Parameter und alle verbleibenden Byte im `-g`-Parameter angezeigt. |
| `gn` | [`pageName`](../vars/page-vars/pagename.md) | Abkürzung für die `pageName`-Abfragezeichenfolge. |
| `gt` | [`pageType`](../vars/page-vars/pagetype.md) | Abkürzung für die `pageType`-Abfragezeichenfolge. |
| `h1` – `h5` | [`hier1` – `hier5`](../vars/page-vars/hier.md) | Hierarchiedimensionen. |
| `hp` | Keine | Wird nicht mehr länger verwendet. Legte in früheren Versionen von Adobe Analytics fest, ob die aktuelle URL die Homepage des Browsers war. |
| `j` | Keine | Die im Browser installierte JavaScript-Version. |
| `k` | Keine | Used in the [Cookie support](/help/components/dimensions/cookie-support.md) dimension. |
| `l1` – `l3` | [`list1` – `list3`](../vars/page-vars/list.md) | Listenvariablen. |
| `mid` | Keine | Experience Cloud-Besucher-ID. |
| `ndh` | Keine | Markierung, die angibt, ob die Bildanforderung von AppMeasurement stammt. |
| `ns` | [`visitorNameSpace`](../vars/config-vars/visitornamespace.md) | Hilft festzustellen, wo Cookies gesetzt werden. |
| `oid` | [`s_objectID`](../vars/page-vars/s-objectid.md) | Objekt-Kennung für die letzte Seite. Wird in Activity Map verwendet. |
| `ot` | Keine | Objektname für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `p` | Keine | Wird nicht mehr länger verwendet. Liste der im Browser verwendeten Plug-ins. |
| `pageName` | [`pageName`](../vars/page-vars/pagename.md) | Used in the [Page](/help/components/dimensions/page.md) dimension. |
| `pageType` | [`pageType`](../vars/page-vars/pagetype.md) | Used in the [Pages not found](/help/components/dimensions/pages-not-found.md) dimension. |
| `pccr` | Keine | Nur für neue Besucher und immer auf `true` gesetzt. Hilft unendlichen Umleitungen vorzubeugen. |
| `pe` | [`linkType`](../vars/config-vars/linktype.md) | Bestimmt den Typ des benutzerspezifischen Links. Erforderlich für [benutzerspezifische Links](/help/components/dimensions/custom-link.md), [Downloadlinks](/help/components/dimensions/download-link.md)und [Ausstiegslinks](/help/components/dimensions/exit-link.md). |
| `pev1` | Keine | Die URL, unter der der benutzerdefinierte Link aufgetreten ist. |
| `pev2` | [`linkName`](../vars/config-vars/linkname.md) | Anzeigename des benutzerspezifischen Links. |
| `pev3` | Keine | Wird nicht mehr länger verwendet. Verfolgte Meilensteine in früheren Versionen der Videoberichte. |
| `pf` | Keine | Plattformmarkierung; nur zur Verwendung durch Adobe. Nicht ändern. |
| `pid` | Keine | Seiten-Kennung für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pidt` | Keine | Seiten-Kennungstyp für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pl` | [`products`](../vars/page-vars/products.md) | Abkürzung für die `products`-Abfragezeichenfolge. |
| `products` | [`products`](../vars/page-vars/products.md) | Variable „products“ (Produktvariable). Wird in den [Produkt](/help/components/dimensions/product.md) - und [Kategorie](/help/components/dimensions/category.md) -Dimensionen verwendet. |
| `purchaseID` | [`purchaseID`](../vars/page-vars/purchaseid.md) | Dient zum Deduplizieren von Käufen. |
| `r` | [`referrer`](../vars/page-vars/referrer.md) | Verweisende URL des Treffers. Wird in Datenverkehrsquellen-Dimensionen wie [Werber](/help/components/dimensions/referrer.md) und [Verweisende Domäne verwendet](/help/components/dimensions/referring-domain.md) |
| `s` | Keine | Bildschirmauflösung in `width x height`. Used in the [Monitor resolutions](/help/components/dimensions/monitor-resolution.md) dimension. |
| `server` | [`server`](../vars/page-vars/server.md) | [Dimension „Server“.](/help/components/dimensions/server.md) |
| `sv` | [`server`](../vars/page-vars/server.md) | Abkürzung für die `server`-Abfragezeichenfolge. |
| `state` | [`state`](../vars/page-vars/state.md) | Dimension „Status“. |
| `t` | Keine | Generiertes Datum/Uhrzeit des Treffers. Verwendet das Format `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` ist Datum/Uhrzeit in JavaScript. Monat `0` ist der Januar, Monat `11` der Dezember.<br>- `w` ist der Wochentag. `0` ist Sonntag und `6` Samstag.<br>- `o` ist der negative GMT-Versatz in Minuten. Zum Beispiel ist `420` GMT-7. |
| `ts` | [`timestamp`](../vars/page-vars/timestamp.md) | Der benutzerdefinierte Zeitstempel, der mit dem Treffer festgelegt wird. Wird normalerweise für das Offline-Tracking verwendet. |
| `v` | Keine | Used in the [Java enabled](/help/components/dimensions/java-enabled.md) dimension. |
| `v0` | [`campaign`](../vars/page-vars/campaign.md) | [Dimension „Trackingcode“.](/help/components/dimensions/tracking-code.md) |
| `v1` – `v250` | [`evar1` – `eVar250`](../vars/page-vars/evar.md) | [eVars](/help/components/dimensions/evar.md)oder benutzerdefinierte Konvertierungsdimensionen. |
| `vid` | [`visitorID`](../vars/config-vars/visitorid.md) | Besucher-ID-Variable. |
| `vmk` | `vmk` | Wird nicht mehr länger verwendet. Migrationsschlüssel für Besucher, mit dem Implementierungen von Drittanbieter-Cookies zu Erstanbieter-Cookies migriert werden konnten. |
| `vvp` | `variableProvider` | Wird in Data Connectors verwendet. |
| `xact` | [`transactionID`](../vars/page-vars/transactionid.md) | Wird mit Data Sources verwendet, um Online- und Offlinedaten miteinander zu verbinden. |
| `zip` | [`zip`](../vars/page-vars/zip.md) | Used in the [Zip code](/help/components/dimensions/zip-code.md) dimension. |
