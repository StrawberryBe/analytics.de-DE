---
title: Datenerfassungs-Abfrageparameter
description: Listet alle in Bildanforderungen verwendeten Abfragezeichenfolgenparameter auf.
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440

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
| `bh` | Keine | Browser-Höhe (in Pixel). Wird in der Dimension „Browser-Höhe“ verwendet. |
| `bw` | Keine | Browser-Breite (in Pixel). Wird in der Dimension „Browserbreit“ verwendet. |
| `c` | Keine | Farbqualität (in Bit). Wird in der Dimension „Farbtiefe“ verwendet. |
| `c.` | `contextData` | Zeigt den Start von Kontextdatenvariablen an. Enthält nie einen Wert. |
| `.c` | `contextData` | Zeigt das Ende der Kontextdatenvariablen an. Enthält nie einen Wert. |
| `c1` – `c75` | `prop1` – `prop75` | Benutzerdefinierte Traffic-Variablen. |
| `cc` | `currencyCode` | Die im Treffer verwendete Währung. |
| `cdp` | `cookieDomainPeriods` | Die Anzahl der Punkte in einer Domäne. Dient zum korrekten Speichern von Cookies. |
| `ce` | `charSet` | Die Zeichencodierung der Bildanforderung. |
| `cl` | `cookieLifetime` | Die Lebensdauer des Besucher-Cookies. |
| `ch` | `channel` | Wird in der Dimension „Website-Bereiche“ verwendet. |
| `cp` | Keine | Wird in der Dimension „Treffertyp“ verwendet. |
| `ct` | Keine | Wird in der Dimension „Verbindungstyp“ verwendet. |
| `D` | `dynamicVariablePrefix` | Gibt an, was für dynamische Variablen verwendet werden soll. |
| `ev` | `events` | Abkürzung für die `events`-Abfragezeichenfolge. |
| `events` | `events` | Durch Komma getrennte Liste der Ereignisse auf der Seite. |
| `g` | `pageURL` | Die aktuelle URL der Seite, bis zu 255 Byte. |
| `-g` | `pageURL` | URLs, die länger als 255 Byte sind, werden geteilt. Die ersten 255 Byte werden im `g`-Parameter und alle verbleibenden Byte im `-g`-Parameter angezeigt. |
| `gn` | `pageName` | Abkürzung für die `pageName`-Abfragezeichenfolge. |
| `gt` | `pageType` | Abkürzung für die `pageType`-Abfragezeichenfolge. |
| `h1` – `h5` | `hier1` – `hier5` | Hierarchievariablen. |
| `hp` | Keine | Wird nicht mehr länger verwendet. Legte in früheren Versionen von Adobe Analytics fest, ob die aktuelle URL die Homepage des Browsers war. |
| `j` | Keine | Die im Browser installierte JavaScript-Version. |
| `k` | Keine | Wird in der Dimension „Cookie-Unterstützung“ verwendet. |
| `l1` – `l3` | `list1` – `list3` | Listenvariablen. |
| `mid` | Keine | Experience Cloud-Besucher-ID. |
| `ndh` | Keine | Markierung, die angibt, ob die Bildanforderung von AppMeasurement stammt. |
| `ns` | `visitorNameSpace` | Hilft festzustellen, wo Cookies gesetzt werden. |
| `oid` | `objectID` | Objekt-Kennung für die letzte Seite. Wird in Activity Map verwendet. |
| `ot` | Keine | Objektname für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `p` | Keine | Wird nicht mehr länger verwendet. Liste der im Browser verwendeten Plug-ins. |
| `pageName` | `pageName` | Wird in der Dimension „Seite“ verwendet. |
| `pageType` | `pageType` | Wird in der Dimension „Seiten nicht gefunden“ verwendet. |
| `pccr` | Keine | Nur für neue Besucher und immer auf `true` gesetzt. Verhindert endlose Redirects. |
| `pe` | `linkType` | Bestimmt den Typ des benutzerspezifischen Links. |
| `pev1` | Keine | Die URL, unter der der benutzerdefinierte Link aufgetreten ist. |
| `pev2` | Keine | Anzeigename des benutzerspezifischen Links. |
| `pev3` | Keine | Wird nicht mehr länger verwendet. Verfolgte Meilensteine in früheren Versionen der Videoberichte. |
| `pf` | Keine | Plattformmarkierung; nur zur Verwendung durch Adobe. Nicht ändern. |
| `pid` | Keine | Seiten-Kennung für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pidt` | Keine | Seiten-Kennungstyp für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pl` | `products` | Abkürzung für die `products`-Abfragezeichenfolge. |
| `products` | `products` | Variable „products“ (Produktvariable). |
| `purchaseID` | `purchaseID` | Dient zum Deduplizieren von Käufen. |
| `r` | `referrer` | Verweisende URL des Treffers. |
| `s` | Keine | Wird in der Dimension „Bildschirmauflösungen“ verwendet. Bildschirmauflösung in `width x height`. |
| `server` | `server` | Dimension „Server“. |
| `sv` | `server` | Abkürzung für die `server`-Abfragezeichenfolge. |
| `state` | `state` | Dimension „Status“. |
| `t` | Keine | Generiertes Datum/Uhrzeit des Treffers. Verwendet das Format `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` ist Datum/Uhrzeit in JavaScript. Monat `0` ist der Januar, Monat `11` der Dezember.<br>- `w` ist der Wochentag. `0` ist Sonntag und `6` Samstag.<br>- `o` ist der negative GMT-Versatz in Minuten. Zum Beispiel ist `420` GMT-7. |
| `ts` | `timestamp` | Der benutzerdefinierte Zeitstempel, der mit dem Treffer festgelegt wird. Wird normalerweise für das Offline-Tracking verwendet. |
| `v` | Keine | Wird in der Dimension „Java aktiviert“ verwendet. |
| `v0` | `campaign` | Dimension „Trackingcode“. |
| `v1` – `v250` | `evar1` – `eVar250` | Benutzerdefinierte Konversionsdimensionen. |
| `vid` | `visitorID` | Besucher-ID-Variable. |
| `vmk` | `vmk` | Wird nicht mehr länger verwendet. Hat bei der Migration von Drittanbieter-Cookies zu Erstanbieter-Cookies geholfen. |
| `vvp` | `variableProvider` | Wird in Data Connectors verwendet. |
| `xact` | `transactionID` | Wird mit Data Sources verwendet, um Daten miteinander zu verknüpfen. |
| `zip` | `zip` | Wird in der Dimension „Postleitzahl“ verwendet. |
