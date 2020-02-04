---
title: Datenerfassungs-Abfrageparameter
description: Listet alle in Bildanforderungen verwendeten Abfragezeichenfolgenparameter auf.
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440

---


# Datenerfassungs-Abfrageparameter

In der folgenden Tabelle sind alle Abfragezeichenfolgenparameter aufgeführt, die Adobe in Bildanforderungen verwendet. Diese Informationen können beim Debugging mit [Paketanalysatoren](packet-monitor.md), beim [Hartkodieren von Bildanforderungen](../other/hardcoded.md)oder bei der Verwendung [dynamischer Variablen](../vars/page-vars/dynamic-variables.md)verwendet werden.

| Parameter | Analytics-Implementierungsvariable | Beschreibung |
| --- | --- | --- |
| `aamlh` | Keine | Standorthinweis für Audience Manager. Wird in Experience Cloud Shared Profile-Integration verwendet. |
| `aamb` | Keine | Audience Manager-Blob. Wird in Experience Cloud Shared Profile-Integration verwendet. |
| `aid` | Keine | Analytics-Besucher-ID. |
| `AQB` | Keine | Gibt den Anfang einer Abfragezeichenfolge für eine Bildanforderung an. |
| `AQE` | Keine | Gibt das Ende einer Bildanforderung an, d. h. die Anforderung wurde nicht abgeschnitten. |
| `bh` | Keine | Browserhöhe (in Pixel). Wird in der Dimension &quot;Browserhöhe&quot;verwendet. |
| `bw` | Keine | Browserbreite (in Pixel). Wird in der Dimension &quot;Browserbreite&quot;verwendet. |
| `c` | Keine | Farbqualität (in Bit). Wird in der Dimension &quot;Farbtiefe&quot;verwendet. |
| `c.` | `contextData` | Gibt den Start von Kontextdatenvariablen an. Enthält nie einen Wert. |
| `.c` | `contextData` | Gibt das Ende der Kontextdatenvariablen an. Enthält nie einen Wert. |
| `c1` - `c75` | `prop1` - `prop75` | Benutzerdefinierte Traffic-Variablen. |
| `cc` | `currencyCode` | Der Währungstyp, der im Treffer verwendet wird. |
| `cdp` | `cookieDomainPeriods` | Die Anzahl der Punkte in einer Domäne. Dient zum korrekten Speichern von Cookies. |
| `ce` | `charSet` | Die Zeichencodierung der Bildanforderung. |
| `cl` | `cookieLifetime` | Die Lebensdauer des Besucher-Cookies. |
| `ch` | `channel` | Wird in der Dimension &quot;Sitebereiche&quot;verwendet. |
| `cp` | Keine | Wird in der Dimension &quot;Treffertyp&quot;verwendet. |
| `ct` | Keine | Wird in der Dimension Verbindungstyp verwendet. |
| `D` | `dynamicVariablePrefix` | Gibt an, was für dynamische Variablen verwendet werden soll. |
| `ev` | `events` | Kurzbeschreibung für die `events` Abfragezeichenfolge. |
| `events` | `events` | Kommagetrennte Liste der Ereignisse auf der Seite. |
| `g` | `pageURL` | Die aktuelle URL der Seite, bis zu 255 Bytes. |
| `-g` | `pageURL` | URLs, die länger als 255 Byte sind, werden geteilt. Die ersten 255 Byte werden im `g` Parameter angezeigt und alle verbleibenden Bytes werden im `-g` Parameter angezeigt. |
| `gn` | `pageName` | Kurzbeschreibung für die `pageName` Abfragezeichenfolge. |
| `gt` | `pageType` | Kurzbeschreibung für die `pageType` Abfragezeichenfolge. |
| `h1` - `h5` | `hier1` - `hier5` | Hierarchievariablen. |
| `hp` | Keine | Wird nicht mehr länger verwendet. In früheren Versionen von Adobe Analytics wurde festgestellt, ob die aktuelle URL die Homepage des Browsers war. |
| `j` | Keine | Die im Browser installierte JavaScript-Version. |
| `k` | Keine | Wird in der Dimension Cookie-Unterstützung verwendet. |
| `l1` - `l3` | `list1` - `list3` | Listenvariablen. |
| `mid` | Keine | Experience Cloud-Besucher-ID. |
| `ndh` | Keine | Flag, das angibt, ob die Bildanforderung von AppMeasurement stammt. |
| `ns` | `visitorNameSpace` | Hilft bei der Bestimmung der Cookies. |
| `oid` | `objectID` | Objekt-ID für die letzte Seite. Wird in Activity Map verwendet. |
| `ot` | Keine | Objektname für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `p` | Keine | Wird nicht mehr länger verwendet. Liste der im Browser verwendeten Plug-ins. |
| `pageName` | `pageName` | Wird in der Dimension &quot;Seite&quot;verwendet. |
| `pageType` | `pageType` | Wird in der Dimension &quot;Seiten nicht gefunden&quot;verwendet. |
| `pccr` | Keine | Nur für neue Besucher eingestellt und immer auf `true`. Verhindert unendliche Umleitungen. |
| `pe` | `linkType` | Bestimmt den Typ des benutzerspezifischen Links. |
| `pev1` | Keine | Die URL, auf der der benutzerspezifische Link erfolgte. |
| `pev2` | Keine | Anzeigename des benutzerspezifischen Links. |
| `pev3` | Keine | Wird nicht mehr länger verwendet. Verfolgte Meilensteine in früheren Versionen der Videoberichte. |
| `pf` | Keine | Plattformflagge; nur zur Verwendung durch Adobe. Nicht ändern. |
| `pid` | Keine | Seiten-ID für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pidt` | Keine | Seiten-ID-Typ für die letzte Seite. Wird in früheren Versionen von Activity Map verwendet. |
| `pl` | `products` | Kurzbeschreibung für die `products` Abfragezeichenfolge. |
| `products` | `products` | Produktvariable. |
| `purchaseID` | `purchaseID` | Dient zum Deduplizieren von Käufen. |
| `r` | `referrer` | Verweisende URL des Treffers. |
| `s` | Keine | Wird in der Dimension &quot;Bildschirmauflösungen&quot;verwendet. Bildschirmauflösung in `width x height`. |
| `server` | `server` | Serverdimension. |
| `sv` | `server` | Kurzbeschreibung für die `server` Abfragezeichenfolge. |
| `state` | `state` | Statusdimension. |
| `t` | Keine | Generiertes Datum/Uhrzeit des Treffers. Verwendet das Format `dd/mm/yyyy hh:mm:ss w o`.<br>- `dd/mm/yyyy hh:mm:ss` ist Datum/Uhrzeit in JavaScript. Der Monat `0` ist der Januar, der Monat `11` der Dezember.<br>- `w` der Wochentag ist. `0` Sonntag, während Samstag `6` ist.<br>- `o` der negative GMT-Offset in Minuten. Zum Beispiel `420` ist GMT-7. |
| `ts` | `timestamp` | Der benutzerdefinierte Zeitstempel, der mit dem Treffer festgelegt wird. Wird normalerweise für die Offline-Verfolgung verwendet. |
| `v` | Keine | Wird in der Dimension &quot;Java aktiviert&quot;verwendet. |
| `v0` | `campaign` | Dimension &quot;Rückverfolgungscode&quot;. |
| `v1` - `v250` | `evar1` - `eVar250` | Benutzerdefinierte Konvertierungsdimensionen. |
| `vid` | `visitorID` | Besucher-ID-Variable. |
| `vmk` | `vmk` | Wird nicht mehr länger verwendet. Hilft bei der Migration von Drittanbieter-Cookies zu Erstanbieter-Cookies. |
| `vvp` | `variableProvider` | Wird in Data Connectors verwendet. |
| `xact` | `transactionID` | Wird mit Data Sources verwendet, um Daten miteinander zu verknüpfen. |
| `zip` | `zip` | Wird in der Dimension &quot;Postleitzahl&quot;verwendet. |
