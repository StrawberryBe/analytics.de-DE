---
title: Analytics-Variablenzuordnung in Adobe Experience Edge Network
description: Erfahren Sie, welche XDM-Felder in Edge automatisch Analytics-Variablen zugeordnet werden
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
source-git-commit: 4fedc1d27a03d4376103e4648e1e66cbd62346af
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 97%

---

# Analytics-Variablenzuordnung in Adobe Experience Edge Network

In der folgenden Tabelle finden Sie die Variablen, die Adobe Experience Platform Edge Network automatisch Adobe Analytics zuordnet. Wenn Sie diese XDM-Feldpfade verwenden, ist keine zusätzliche Konfiguration erforderlich, um Daten an Adobe Analytics zu senden.

| XDM-Feldpfad | Analytics-Dimension und Beschreibung |
| --- | --- |
| `application.isClose` | Ermöglicht die Definition der Mobile-Metrik [Abstürze](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html?lang=de#metrics). |
| `application.isInstall` | Hilft bei der Bestimmung, wann die Mobile-Metrik [Erste Starts](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics) erhöht werden soll. |
| `application.isLaunch` | Hilft bei der Bestimmung, wann die Mobile-Metrik [Erste Starts](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics) erhöht werden soll. |
| `application.closeType` | Bestimmt, ob ein Schließen-Ereignis ein Absturz ist oder nicht. Gültige Werte sind `close` (eine Lebenszyklussitzung endet und ein Pausenereignis wurde für die vorherige Sitzung empfangen) und `unknown` (eine Lebenszyklussitzung endet ohne Pausenereignis). Hilft beim Festlegen der Metrik [Abstürze](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isInstall` | Die Mobile-Metrik [Installs](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isLaunch` | Die Mobile-Metrik [Starts](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.name` | Ermöglicht die Definition der Mobile-Dimension [App-ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html?lang=de#dimensions). |
| `application.isUpgrade` | Die Mobile-Metrik [Upgrades](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.version` | Ermöglicht die Definition der Mobile-Dimension [App-ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.sessionLength` | Die Mobile-Metrik [Länge der vorherigen Sitzung](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `commerce.checkouts.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Checkouts](../../components/metrics/checkouts.md) an. |
| `commerce.checkouts.value` | Inkrementiert die Metrik [Checkouts](../../components/metrics/checkouts.md) um den gewünschten Wert. |
| `commerce.order.currencyCode` | Definiert die Konfigurationsvariable [currencyCode](../vars/config-vars/currencycode.md). |
| `commerce.order.purchaseID` | Definiert die Seitenvariable [purchaseID](../vars/page-vars/purchaseid.md). |
| `commerce.productListAdds.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Cart Additions](../../components/metrics/cart-additions.md) an. |
| `commerce.productListAdds.value` | Erhöht die Metrik [Warenkorbhinzufügungen](../../components/metrics/cart-additions.md). |
| `commerce.productListOpens.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkörbe](../../components/metrics/carts.md) an. |
| `commerce.productListOpens.value` | Erhöht die Metrik [Warenkörbe](../../components/metrics/carts.md). |
| `commerce.productListRemovals.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbentnahmen](../../components/metrics/cart-removals.md) an. |
| `commerce.productListRemovals.value` | Erhöht die Metrik [Warenkorbentnahmen](../../components/metrics/cart-removals.md). |
| `commerce.productListViews.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Warenkorbansichten](../../components/metrics/cart-views.md) an. |
| `commerce.productListViews.value` | Erhöht die Metrik [Warenkorbansichten](../../components/metrics/cart-views.md). |
| `commerce.productViews.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die Metrik [Produktansichten](../../components/metrics/product-views.md) an. |
| `commerce.productViews.value` | Erhöht die Metrik [Produktansichten](../../components/metrics/product-views.md). |
| `commerce.purchases.value` | Erhöht die Metrik [Bestellungen](../../components/metrics/orders.md). |
| `device.model` | Die Mobile-Dimension [Gerätename](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `device.colorDepth` | Ermöglicht die Definition der Dimension [Farbtiefe](../../components/dimensions/color-depth.md). |
| `device.screenHeight` | Ermöglicht die Definition der Dimension [Bildschirmauflösung.](../../components/dimensions/monitor-resolution.md) |
| `device.screenWidth` | Ermöglicht die Definition der Dimension [Bildschirmauflösung.](../../components/dimensions/monitor-resolution.md) |
| `device.type` | Der Mobilgerätetyp. |
| `environment.browserDetails.acceptLanguage` | Ermöglicht die Definition der Dimension [Sprache](../../components/dimensions/language.md). |
| `environment.browserDetails.cookiesEnabled` | Definiert die Dimension [Cookie-Unterstützung](../../components/dimensions/cookie-support.md). Gültige Werte sind `Y` (der Browser akzeptiert Cookies) und `N` (der Browser lehnt Cookies ab). |
| `environment.browserDetails.javaEnabled` | Definiert die Dimension [Java aktiviert](../../components/dimensions/java-enabled.md). Gültige Werte sind `Y` (Java ist aktiviert) und `N` (Java ist deaktiviert). |
| `environment.browserDetails.userAgent` | Wird als Fallback-Identifizierungsmethode für [Unique Visitor](../../components/metrics/unique-visitors.md) verwendet. Wird normalerweise unter Verwendung der HTTP-Anfrage-Kopfzeile `User-Agent` befüllt. Sie können dieses Feld einer eVar zuordnen, wenn Sie es in Berichten verwenden möchten. |
| `environment.browserDetails.viewportHeight` | Definiert die Dimension [Browser-Höhe](../../components/dimensions/browser-height.md). |
| `environment.browserDetails.viewportWidth` | Definiert die Dimension [Browser-Breite](../../components/dimensions/browser-width.md). |
| `environment.carrier` | Die Mobile-Dimension [Betreibername](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.connectionType` | Ermöglicht die Definition der Dimension [Verbindungstyp](../../components/dimensions/connection-type.md). |
| `environment.ipV4` | Wird als Fallback-Identifizierungsmethode für [Unique Visitor](../../components/metrics/unique-visitors.md) verwendet. Wird normalerweise unter Verwendung der HTTP-Kopfzeile `X-Forwarded-For` befüllt. |
| `environment.language` | Die Mobile-Dimension „Locale“. |
| `environment.operatingSystem` | Die Mobile-Dimension [Betriebssystem](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.operatingSystemVersion` | Hilft beim Festlegen der Dimension [Betriebssystemversion](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `_experience.analytics.customDimensions.`<br/>`eVars.eVar1` -<br/>`_experience.analytics.customDimensions.`<br/>`eVars.eVar250` | Legt die entsprechende [eVar](../../components/dimensions/evar.md)-Dimension fest. |
| `_experience.analytics.customDimensions.`<br/>`listProps.prop1.delimiter` -<br/>`_experience.analytics.customDimensions.`<br/>`listProps.prop75.delimiter` | Das Begrenzungszeichen, das für eine bestimmte [Listen-Prop](../vars/page-vars/prop.md#list-props) verwendet wird. |
| `_experience.analytics.customDimensions.`<br/>`listProps.prop1.values` -<br/>`_experience.analytics.customDimensions.`<br/>`listProps.prop75.values` | Ein Zeichenfolgen-Array, das die Werte der entsprechenden [Listen-Prop](../vars/page-vars/prop.md#list-props) enthält. |
| `_experience.analytics.customDimensions.`<br/>`lists.list1.list[].value` -<br/>`_experience.analytics.customDimensions.`<br/>`lists.list3.list[].value` | Verkettet alle `value` Zeichenfolgen in den jeweiligen `list[]` -Array zu seiner jeweiligen [Listenvariable](../vars/page-vars/list.md) mithilfe von Kommatrennzeichen. |
| `_experience.analytics.customDimensions.`<br/>`props.prop1` -<br/>`_experience.analytics.customDimensions.`<br/>`props.prop75` | Legt die Dimension der entsprechenden [Prop](../../components/dimensions/prop.md) fest. |
| `_experience.analytics.event1to100.`<br/>`event1.id` -<br/>`_experience.analytics.event901to1000.`<br/>`event1000.id` | Wendet die [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) auf die jeweilige Metrik [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md) an. |
| `_experience.analytics.event1to100.`<br/>`event1.value` -<br/>`_experience.analytics.event901to1000.`<br/>`event1000.value` | Erhöht die jeweilige Metrik [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md) um den gewünschten Betrag. |
| `identityMap.ECID[0].id` | Die [Adobe Experience Cloud Identity Service-ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). |
| `marketing.trackingCode` | Definiert die Dimension [Trackingcode](../../components/dimensions/tracking-code.md). |
| `media.mediaTimed.completes.value` | Die Media Analytics-Metrik [Inhaltsbeendigung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-complete). |
| `media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `media.mediaTimed.federated.value` | Die Media Analytics-Metrik [Verknüpfte Daten](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#federated-data). |
| `media.mediaTimed.firstQuartiles.value` | Die Media Analytics-Metrik [25 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#twenty-five-progress-marker). |
| `media.mediaTimed.mediaSegmentView.value` | Die Media Analytics-Metrik [Ansichten des Inhaltssegments](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-segment-views). |
| `media.mediaTimed.midpoints.value` | Die Media Analytics-Metrik [50 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#fifty-progress-marker). |
| `media.mediaTimed.pauseTime.value` | Die Media Analytics-Metrik [Pausierung - Gesamtdauer](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#total-pause-duration). |
| `media.mediaTimed.pauses.value` | Die Media Analytics-Metrik [Pausierung - Ereignisse](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#pause-events). |
| `media.mediaTimed.primaryAssetReference.`<br/>`@id` | Die Media Analytics-Dimension [Asset-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#asset-id). |
| `media.mediaTimed.primaryAssetReference.`<br/>`dc:title` | Die Media Analytics-Dimension [Videoname](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#video-name). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Creator[N].iptc4xmpExt:Name` | Die Media Analytics-Dimension [Urheber](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#originator). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Episode.iptc4xmpExt:Number` | Die Media Analytics-Dimension [Folge](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#episode). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Genre` | Die Media Analytics-Dimension [Genre](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#genre). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Rating[N].iptc4xmpExt:RatingValue` | Die Media Analytics-Dimension [Inhaltsbewertung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-rating). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Season.iptc4xmpExt:Number` | Die Media Analytics-Dimension [Staffel](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#season). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Identifier` | Die Media Analytics-Dimension [Inhalts-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-id). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Name` | Die Media Analytics-Dimension [Anzeigen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#show). |
| `media.mediaTimed.primaryAssetReference.`<br/>`showType` | Die Media Analytics-Dimension [Sendungstyp](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#show-type). |
| `media.mediaTimed.primaryAssetReference.`<br/>`xmpDM:duration` | Die Media Analytics-Dimension [Videolänge](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#video-length). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`@id` | Die Media Analytics-Dimension [Mediensitzungs-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-session-id). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastChannel` | Die Media Analytics-Dimension [Inhaltskanal](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-channel). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastContentType` | Die Media Analytics-Dimension [Content-Typ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-type). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastNetwork` | Die Media Analytics-Dimension [Netzwerk](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#network). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | Die Media Analytics-Dimension [Inhaltssegment](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-segment). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`playerName` | Die Media Analytics-Dimension [Inhalts-Player-Name](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-player-name). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`playerSDKVersion.version` | Die Media Analytics-Dimension [SDK-Version](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#sdk-version). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`sourceFeed` | Die Media Analytics-Dimension [Medien-Feed-Typ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-feed-type). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`streamFormat` | Die Media Analytics-Dimension [Stream-Format](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#stream-format). |
| `media.mediaTimed.progress10.value` | Die Media Analytics-Metrik [10 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#ten-progress-marker). |
| `media.mediaTimed.progress95.value` | Die Media Analytics-Metrik [95 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#ninety-five-progress-marker). |
| `media.mediaTimed.resumes.value` | Die Media Analytics-Metrik [Inhaltswiederaufnahmen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-resumes). |
| `media.mediaTimed.starts.value` | Die Media Analytics-Metrik [Medienstarts](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-starts). |
| `media.mediaTimed.thirdQuartiles.value` | Die Media Analytics-Metrik [75 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#seventy-five-progress-marker). |
| `media.mediaTimed.timePlayed.value` | Die Media Analytics-Metrik [Besuchszeit für Inhalt](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#content-time-spent). |
| `media.mediaTimed.totalTimePlayed.value` | Die Media Analytics-Metrik [Besuchszeit für Medien](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html?lang=de#media-time-spent). |
| `placeContext.geo.latitude` | Die Mobile-Dimension „Breitengrad“. |
| `placeContext.geo.longitude` | Die Mobile-Dimension „Längengrad“. |
| `placeContext.geo.postalCode` | Die Dimension [Postleitzahl](../../components/dimensions/zip-code.md). |
| `placeContext.geo.stateProvince` | Die Dimension [US-Bundesstaaten](../../components/dimensions/us-states.md). |
| `productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar1` -<br/>`productListItems[]._experience.analytics.`<br/>`customDimensions.eVars.eVar250` | Wendet die [Produktsyntax](../vars/page-vars/products.md) für das Merchandising auf eVars an. |
| `productListItems[]._experience.analytics.`<br/>`event1to100.event1.value` -<br/>`productListItems[]._experience.analytics.`<br/>`event901-1000.event1000.value` | Wendet die [Produktsyntax](../vars/page-vars/products.md) für das Merchandising auf Ereignisse an. |
| `productListItems[].lineItemId` | Die Dimension [Kategorie](../../components/dimensions/category.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `productListItems[].name` | Die Dimension [Produkt](../../components/dimensions/product.md). Siehe auch die Seitenvariable [products. ](../vars/page-vars/products.md) Wenn `productListItems[].SKU` und `productListItems[].name` beide Daten enthalten, enthält der Wert in `productListItems[].SKU` verwendet. |
| `productListItems[].priceTotal` | Hilft bei der Bestimmung der Metrik [Umsatz](../../components/metrics/revenue.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `productListItems[].quantity` | Hilft bei der Bestimmung der Metrik [Einheiten](../../components/metrics/units.md). Siehe auch die Seitenvariable [products](../vars/page-vars/products.md). |
| `productListItems[].SKU` | Die Dimension [Produkt](../../components/dimensions/product.md). Siehe auch die Seitenvariable [products. ](../vars/page-vars/products.md) Wenn `productListItems[].SKU` und `productListItems[].name` beide Daten enthalten, enthält der Wert in `productListItems[].SKU` verwendet. |
| `web.webInteraction.URL` | Die Implementierungsvariable [linkURL](../vars/config-vars/linkurl.md). |
| `web.webInteraction.name` | Die Dimension [Benutzerspezifischer Link](../../components/dimensions/custom-link.md), [Downloadlink](../../components/dimensions/download-link.md) oder [Exitlink](../../components/dimensions/exit-link.md), je nach dem Wert in `web.webInteraction.type` |
| `web.webInteraction.type` | Bestimmt den Typ des angeklickten Links. Gültige Werte sind `other` (benutzerspezifische Links), `download` (Downloadlinks) und `exit` (Exitlinks). |
| `web.webPageDetails.URL` | Die Dimension [Seiten-URL](../../components/dimensions/page-url.md). |
| `web.webPageDetails.errorPage` | Flag, das bei der Bestimmung der [Dimension](../../components/dimensions/pages-not-found.md) und [Metrik](../../components/metrics/pages-not-found.md) „Pages Not Found“ hilft. |
| `web.webPageDetails.name` | Die Dimension [Seite](../../components/dimensions/page.md). |
| `web.webPageDetails.server` | Die Dimension [Server](../../components/dimensions/server.md). |
| `web.webPageDetails.siteSection` | Die Dimension [Site-Bereich](../../components/dimensions/site-section.md). |
| `web.webReferrer.URL` | Die Dimension [Referrer](../../components/dimensions/referrer.md). |

{style=&quot;table-layout:auto&quot;}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Zuordnen anderer XDM-Felder zu Analytics-Variablen

Wenn Sie Dimensionen oder Metriken zu Adobe Analytics hinzufügen möchten, können Sie dies über [Kontextdatenvariablen](../vars/page-vars/contextdata.md) tun. Alle XDM-Feldelemente, die nicht automatisch zugeordnet werden, werden als Kontextdaten mit dem Präfix a.x an Adobe Analytics gesendet. Sie können diese Kontextdatenvariable dann unter Verwendung der [Verarbeitungsregeln](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=de) der gewünschten Analytics-Variablen zuordnen. Angenommen, Sie senden das folgende Ereignis:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "search":{
                "term":"Example search term"
            }
        }
    }
})
```

Das Web SDK sendet diese Daten als die Kontextdatenvariable `a.x._atag.search.term` an Adobe Analytics. Anschließend können Sie eine Verarbeitungsregel verwenden, um den Wert dieser Kontextdatenvariablen der gewünschten Analytics-Variablen zuzuweisen, z. B. einer eVar:

![Suchbegriff-Verarbeitungsregel](assets/examplerule.png)
